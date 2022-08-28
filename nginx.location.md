---
id: v87toqykuhzwx67mx2ppjet
title: Location
desc: ''
updated: 1661681131208
created: 1661680843162
---

## proxy_pass redirecting

If a prefix-matching location ends with a slash (`/`), and requests are processed by `proxy_pass`, requests to the exact string minus the trailing slash will be redirected to full URI (domain included) with slash appended.

## Case sensitivity

On case-sensitive operating systems, only `~*` matches case-insensitively.
