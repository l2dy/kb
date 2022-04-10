---
id: pZy6ZFghTotWu3dKRJhWI
title: Text
desc: ''
updated: 1640358612891
created: 1640358489330
---

> By default, mu4e tries to display the ’richest’ option, which is the last MIME-part of the alternatives. You can customize this to prefer the text version, if available, with something like the following in your configuration (and see the docstring for mm-discouraged-alternatives for details)

```elisp
(with-eval-after-load "mm-decode"
  (add-to-list 'mm-discouraged-alternatives "text/html")
  (add-to-list 'mm-discouraged-alternatives "text/richtext"))
```

https://www.djcbsoftware.nl/code/mu/mu4e/MSGV-Rich_002dtext-and-images.html#MSGV-Rich_002dtext-and-images
