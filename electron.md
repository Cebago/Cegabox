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

The Electron interface is not closable. You will see the IP address that permit you to login on the web interface.

You have also two choice on the interface :

* Quit : it shutdown the Raspberry Pi as you have only access is this interface
* Reboot : it reboot the Raspberry Pi

This is our interface.

[screen]

We release a package thanks to electron-packager. It's build in arm64 with a linux plateform.

The Raspberry Pi turn on an Ubuntu Desktop 22.04.
