---
id: OcphOpgAALZEYHQ1wY4Yp
title: Ideas
desc: ''
updated: 1658053954495
created: 1644738782856
---

## Improvements Needed

* [x] `port reclaim` takes too much time checking distfiles.
  * cache distfile information.
* [ ] Fix bump in ports with multiple checksums (e.g. `cargo.crates`).
* [/] Dependency resolution is too slow.
  * unlikely to fix because we have variants and countless combinations out of them.
* [ ] `port` command blocks on DNS resolution timeout, and is impossible to interrupt safely.
  * It's blocked on a curl call, which already has a reasonable timeout.
  * Why doesn't Ctrl+C interrupt the call?
* [ ] Variants are inherited from older versions, so a default variant change may not be applied on upgrade and therefore force users to compile from source.
