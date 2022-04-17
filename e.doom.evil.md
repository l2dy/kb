---
id: gv4so0rz3j1iyl2ndheovcw
title: Evil
desc: ''
updated: 1650201749180
created: 1647480803343
---

## yank forward

`y f SPC` does not yank the space character with `evil-snipe-override-mode`. See https://github.com/hlissner/evil-snipe/issues/86.

```elisp
(remove-hook 'doom-first-input-hook #'evil-snipe-override-mode)
```

## Commands

Repeat last change: `.`
Repeat last substitute: `&`

## Ex-commands

Close buffer: `:bd`
