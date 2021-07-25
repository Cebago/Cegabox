# Front

## Summary

1. [Project Presentation](project.html)
2. [How does it work ?](working.html)
3. [Environment](env.html)
4. [Frontend](front.html)
5. [Backend](back.html)
6. [**Electron**](electron.html)
7. [Database](database.html)
8. [Python](python.html)

The front-end of this project consists in a web interface which users can use to access to thier vulnerabilities reports. They can also see on it all about their hosts, the open ports and, of course, all associated vulnerabilities.

To make this interface, we did only use HTML, JS and CSS files. All dependencies like stylesheets, source of JS libraries are downloaded locally to make sure that if the *Cegabox* is offline you can still use a nice interface.

All data displayed on the web interface comes from our [API](back.html) which make all requests to the database.

## How to use the web interface ?

### Create an account

First of all, to access the reports, you will need an account. To create it, go to the local website of your *Cegabox* and click on "Create an account".

![Cegabox Login](https://cebago.github.io/Cegabox/img/cegabox-login.png)

Then, when your account is created, you could connect and see the dashboard with main informations on it. Good to know, your account always start with "Reader" privileges, if you want to change yours, contact the administrator or if you are the administrator, see our page [Administrate your *Cegabox*](admin.html).

### Dashboard

When you connect, you will always go to this page, it's the main page.

![Cegabox Login](https://cebago.github.io/Cegabox/img/cegabox-dashboard.png)
