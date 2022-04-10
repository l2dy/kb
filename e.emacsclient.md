---
id: 3Ll9s5HaDW4irKwGVguQR
title: Emacs Client
desc: ''
updated: 1641139930050
created: 1639983547098
---

## Emacs Server on macOS

```xml
<!-- ~/Library/LaunchAgents/gnu.emacs.daemon.plist -->
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>Label</key>
    <string>gnu.emacs.daemon</string>

    <key>ProgramArguments</key>
    <array>
        <string>/Applications/MacPorts/Emacs.app/Contents/MacOS/Emacs</string>
        <string>--fg-daemon</string>
    </array>

    <key>RunAtLoad</key>
    <true/>

    <key>ProcessType</key>
    <string>Interactive</string>
</dict>
</plist>
```

## Emacs Client with AppleScript

Save the following in `Script Editor.app` as an Application.

```AppleScript
do shell script "/Applications/MacPorts/Emacs.app/Contents/MacOS/bin/emacsclient -c -n"
```

> ⚠ **Warning:** Without `-n` the applet won't quit and prevents sleep.
