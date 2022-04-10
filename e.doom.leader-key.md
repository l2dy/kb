---
id: 384zFCgdjxYkwJEMiI7p6
title: Leader Key
desc: ''
updated: 1649569112676
created: 1641289886197
---

## Define new key bindings with leader key prefix

```elisp
(map! :leader
      (:prefix ("o" . "open")
       :desc "elfeed" "e" #'=rss))
```

## Remap leader keys

Change alt key bindings:

```elisp
;; Add to config.el
(setq doom-leader-alt-key "C-SPC"
      doom-localleader-alt-key "C-SPC m")
```
