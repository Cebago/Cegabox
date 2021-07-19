# How does it work ?

## Summary

1. [Project Presentation](project.html)
2. [**How does it work ?**](working.html)
3. [Environment](env.html)
4. [Frontend](front.html)
5. [Backend](back.html)

For this project, because we want it to be as compatible as possible with a lot of architecture, we have decided to use docker containers.

We separate all of our possibilities in different part of our solution. For example, we have an API made in PHP, which allow users and scripts to interract with our database. We also have a dedicated front-end web-server running only HTML, JS and CSS.

For our scripting part, we decided to use python because of it's facility of use. We have implemented some scripts which scan the network and create by the API all the encountered devices.

Finally, we also use some others services, which allows us to get more data about vulnerabilities we found.
