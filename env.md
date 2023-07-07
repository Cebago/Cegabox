# Environment

## Summary

1. [Project Presentation](project.html)
2. [How does it work ?](working.html)
3. [**Environment**](env.html)
4. [Frontend](front.html)
5. [Backend](back.html)
6. [Electron](electron.html)
7. [Database](database.html)
8. [Scanner](scanner.html)

### Project filesystem

For this project, you can find multiples services hosted on the host or inside some docker containers.

We have decided to separate our project infrastructure accordingly to the image below.

![Cegabox Infrastructure](https://cebago.github.io/Cegabox/img/cegabox-infra.svg)

In order to help our customers, we have an interface designed in Electron to make our Cegabox controlable directly. From this interface, you can run get the IP address of your box to be sure to access the web administration interface.

### Network Diagram

The following network diagram represents how the containers are connected over internal networks.

![Cegabox-Flow-Chart](https://cebago.github.io/Cegabox/img/cegabox-flow-chart.svg)

### Used technologies

To complete this project, we used some commons tools and technologies :

- Docker 24 & docker compose
- Nuclei 2.9.7
- Nmap 7.94
- PostgreSQL 14.3
- NVD Nist Repositories
- Python 3
- PHP:8.1
- JS/Ajax/HTML
- Raspberry PI 4
- Nginx:1.22
- Adminer:4.7
- Httpd:2.4.53
