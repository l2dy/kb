---
id: 8qi8xsvztujm1tg0y1zoy7o
title: Range Request
desc: ''
updated: 1661680807119
created: 1661680800307
---

Nginx will try to slice the response body when one of the following conditions is met and the request specifies a `Range` header.

1. Nginx is serving static files directly.
2. Nginx cache is enabled.
3. `proxy_force_ranges` is set to `on`.

This behavior is controlled by `allow_ranges` in struct `ngx_http_request_s`.
