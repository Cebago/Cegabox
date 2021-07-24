# Environment

## Summary

1. [Project Presentation](project.html)
2. [How does it work ?](working.html)
3. [**Environment**](env.html)
4. [Frontend](front.html)
5. [Backend](back.html)
6. [Electron](electron.html)

For this project, you can find multiples services hosted on the host or inside some docker containers.

We have decided to separate our project infrastructure accordingly to the image below.

![Cegabox Infrastructure](https://cebago.github.io/Cegabox/img/cegabox-infra.png)

In order to help our customers, we have an interface designed in Electron to make our Cegabox controlable directly. From this interface, you can run a simple network scan or a complete one. Both are diferent but are very important in their scope:

1) The simple scan is the fastest one and permit to have a reminder of the infrastructure reponding to ping requests and the main ports opened on the scanned hosts.

2) The complete scan is a longer scan than the simple one. It runs a very broad scan which can find all hosts and ports on your networks but in a really long time.
