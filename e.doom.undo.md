---
id: hpIUcXwKN1Sy6GuTJbNod
title: Undo
desc: ''
updated: 1644474321427
created: 1644474298546
---

## Disable undo history persistence

```elisp
;; Add in config.el
(remove-hook 'undo-fu-mode-hook #'global-undo-fu-session-mode)
```
