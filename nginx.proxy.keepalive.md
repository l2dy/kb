---
id: 1bl1l7f2zdafyr2afxnorrt
title: Keepalive
desc: ''
updated: 1661680716413
created: 1661680676278
---

To enable keepalive connections to upstream, the `keepalive` directive must be included in `upstream{}` blocks, and in the `location{}` blocks you need to switch HTTP version to 1.1 and clear the default `Connection: close` request header set by Nginx, see [[nginx.proxy.headers]].

```
proxy_http_version 1.1;
proxy_set_header   "Connection" "";
```
