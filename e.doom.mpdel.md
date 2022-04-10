---
id: Sqre83txr0JXlSol74f5Y
title: Mpdel
desc: ''
updated: 1642175591467
created: 1642175587203
---

```elisp
(use-package! mpdel
  :config
  (+evil-collection-init 'mpdel)
  (map! :leader
        :desc "MPDel" "Z" mpdel-core-map))
```
