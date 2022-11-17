# Clipboard Privacy Controls

Clipboards allow users to copy data with the intent of pasting it elsewhere. Poor protections on the clipboard may allow malicious applications to access data that should be protected.

Most operating systems limit clipboard access to the foreground applications only, and some limit even further to only provide access to applications with focus.

Device, user, or group policies can be used to limit the ability of applications to access the shared system clipboard.

Any application that is responsible for copying sensitive information to the clipboard should automatically clear the clipboard after a short timeout.

Cloud clipboard capabilities, or clipboards that are shared across devices, should be disabled.

Password managers that bypass the clipboard and insert passwords directly into the input field may be preferred over managers that operate by adding data to the clipboard.

In some mobile operating systems clipboards are typically implemented by the keyboard application, which means that good vetting of applications and only using approved keyboard applications is important.