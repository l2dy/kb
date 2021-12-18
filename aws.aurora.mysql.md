---
id: mcKfSvETc3tic2K0lGSLE
title: Aurora MySQL
desc: ''
updated: 1639839360867
created: 1637112927261
---

## JDBC Driver

### MariaDB Connector/J

https://mariadb.com/kb/en/failover-and-high-availability-with-mariadb-connector-j/#failover-and-load-balancing-modes

Mode | Description
-----|------------
aurora | This mode supports connection failover in an Amazon Aurora cluster. This mode does support load-balancing reads on slave instances if the connection is set to read-only before executing the read. The connector performs load-balancing by randomly picking a slave instance to execute read queries for a connection.<br>This mode has been available since MariaDB Connector/J 1.2.0

## Caveats and Gotchas

https://aws.amazon.com/premiumsupport/knowledge-center/aurora-mysql-db-cluser-read-only-error/

### Smart driver

The Amazon Aurora DB cluster endpoints propagate DNS record updates automatically, but the process doesn't happen instantly. This can cause delays in responding to an event that occurred on the database and the event might be handled by the application. A Smart Driver uses the DB cluster topography through the INFORMATION_SCHEMA.REPLICA_HOST_STATUS metadata table, which is in near-real-time. This helps to route connections to the appropriate role, and helps load-balance across the existing replicas. MariaDB Connector/J is an example of a third party Smart Driver that has native support for Aurora MySQL.

Note: Even Smart Drivers might be affected by excessive DNS Caching.

### DNS caching

If you are not using a smart driver, then you depend on the DNS record updates and propagation after a failover event occurs. Aurora DNS zones use a short time-to-live (TTL) of 5 seconds, so it is important that your network and client configurations don't further increase this. DNS caching can occur at multiple layers of an architecture, such as the operating system (OS), the network layer and the application container. It is important that you understand how each of these layers is configured. If there is unintended DNS caching beyond the TTL of 5 seconds, it is possible that you will re-connect to the old writer after a failover.

Java Virtual Machines (JVM) can excessively cache DNS, indefinitely. When the JVM resolves a hostname to an IP address, it caches the IP address for a specified period of time (TTL). On some configurations, the JVM default TTL is set to never refresh DNS entries until the JVM is restarted. This can lead to read-only errors after a failover. In this case, it is important to manually set a small TTL so that it will periodically refresh.
