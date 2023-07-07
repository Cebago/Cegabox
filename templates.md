 Frontend

## Summary

1. [Project Presentation](project.html)
2. [How does it work ?](working.html)
3. [Environment](env.html)
4. [**Frontend**](front.html)
   * [Dashboard](front.html)
   * [Scan](scan.html)
   * [Hosts](hosts.html)
   * [Services](services.html)
   * [Vulnerabilities](vulnerabilities.html)
   * [Rules](rules.html)
   * [Reports](reports.html)
   * [Certificates](certificates.html)
   * [**Templates**](template.html)
5. [Backend](back.html)
6. [Electron](electron.html)
7. [Database](database.html)
8. [Scanner](scanner.html)


### List of templates

Our template page contains templates by default. You have different type of templates that allows you to scan different perimeter.

[screen]

### Create a template

You can create a template from scratch or from a template predefined.
A modal appears with all the fiedls to fill in.

[screen]

You have to enter a name for your template.

You can enter an ip or a hostname if it's for example a scan that you want to launch frequently, or you can enter nothing if you want to apply this template to multiple different host.

You can choose what ports you want to scan, if it's specific or not, if it's all the ports or just the top ports.

You can choose option like :
    * TCP Syn scan
    * UDP scan
    * OS scan...

[screen]

If you choose to scan the services and versions associated, you can specify the intensity, that refers to the precision of the versions and services founded.

You can choose the temporisation of your scan from paranoid to insane.

And the big parts it's that you can select the module of you template.


### Modify templates

You can only modify your templates and not theses by default.