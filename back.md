# Backend

## Summary

1. [Project Presentation](project.html)
2. [How does it work ?](working.html)
3. [Environment](env.html)
4. [Frontend](front.html)
5. [**Backend**](back.html)
6. [Electron](electron.html)
7. [Database](database.html)
8. [Python](python.html)

### Api Language

In order to disable python and webserver communicating directly to our database and creating possible conflicts, we have decided to use an API. This API allows us to communicate between those ways:

- the database and the webserver
- the database and the python scripts

It was made using PHP and JSON return in order to give information for each request.

### Security

Our API can't be called by anyone whithout an account on the *Cegabox*. We always check the request is authenticated, contains the mandatory data
