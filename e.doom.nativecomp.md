---
id: bGoTWK2jLMYGh7iznzka7
title: Nativecomp
desc: ''
updated: 1649569194916
created: 1644634344706
---

Enabled automatically if you have Emacs built with `--with-native-compilation`.

## Caveats

`doom build` may stuck on native compile if the `vterm` module is enabled, see https://github.com/hlissner/doom-emacs/issues/5592.

This problem can be avoided by compiling `vterm-module` in advance.
