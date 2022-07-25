# Front

## Summary

1. [Project Presentation](project.html)
2. [How does it work ?](working.html)
3. [Environment](env.html)
4. [Frontend](front.html)
5. [Backend](back.html)
6. [**Electron**](electron.html)
7. [Database](database.html)
8. [Scanner](scanner.html)

The Electron interface is loaded on boot of the Raspberry Pi.

## How to use the Electron interface ?

The Electron interface is not closable. You will have the choice between four buttons:

* A Simple Scan: it permit you to do a scan between 5 and 10 minutes with a top port 1000.
* A Complexe Scan: it permit you to test your network completely with all the ports and the IP possible.
* Quit : it shutdown the Raspberry Pi as you have only access is this interface
* Reboot : it reboot the Raspberry Pi

This is our interface.

[screen]

We release a package thanks to electron-packager. It's build in arm64 with a linux plateform.

The Raspberry Pi turn on Ubuntu.
