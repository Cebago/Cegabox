# Frontend

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
   * [**Certificates**](certificates.html)
   * [Templates](templates.html)
5. [Backend](back.html)
6. [Electron](electron.html)
7. [Database](database.html)
8. [Scanner](scanner.html)

### List of all certificates

On this page, you will find all the certificates which has been scanned using the [module](./scanner.html) *Certificate Scanner*

![All certificates page](./img/cegabox-all-certs.png)

Each entry shown on the table displays the name of the certificate known as the *Subject Common Name*, the *Issuer Common Name* and some actions to perform on it.

### Actions on certificate

#### View certificate

After openning the specific page for a certificate, you will see all the attributes, grouped by topic, such as  the *Subject Informations*, the *Issuers Informations*, the *Validity*, the *Public Key Identifiers*.

![cegabox-cert-subject](./img/cegabox-cert-subject.png)
![cegabox-cert-issuer](./img/cegabox-cert-issuer.png)
![cegabox-cert-validity](./img/cegabox-cert-validity.png)
![cegabox-cert-pubkey](./img/cegabox-cert-pubkey.png)

Below those four sections, the *X509* section and the *NCT* sections are shown.

![cegabox-cert-x509](./img/cegabox-cert-x509.png)
![cegabox-cert-nct](./img/cegabox-cert-nct.png)

Finally, as a service or a vulnerability, the certificate is linked to other elements, such as:

* Report
* Host
* Service
* Vulnerability

![cegabox-cert-hosts](./img/cegabox-cert-hosts.png)
![cegabox-cert-services](./img/cegabox-cert-services.png)
![cegabox-cert-vulnerabilities](./img/cegabox-cert-vulns.png)

[Next Page](templates.html)
