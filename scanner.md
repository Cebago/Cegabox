# Python

## Summary

1. [Project Presentation](project.html)
2. [How does it work ?](working.html)
3. [Environment](env.html)
4. [Frontend](front.html)
5. [Backend](back.html)
6. [Electron](electron.html)
7. [Database](database.html)
8. [**Scanner**](scanner.html)


# How our Scanner is built ?


## Module parts

To know what kind of scanner to launch, we have a module system.

According to the user's choice, we enter into a module.

![Cegabox Module](https://cebago.github.io/Cegabox/img/cegabox-vulnerability-module.png)

If the user select the certificate discovery, so the ssl-cert script will be launch with nmap. 

## Scan hosts

In order to detect hosts, services and vulnerabilities on the network, we use this wonderful scanner that is **nmap**.
To allow users to do several types of scans, we play with different parameters, like the number of ports on each host that will be scanned. It's determined through a script parameter.

## Scan services

After the recovery of the hosts, the services are also recovered, as well as the associated versions. Services are detected with header of port requests.

## Infrastructure vulnerabilities discover

In complement of the nmap, we use the [Vulners](https://vulners.com/) script to match services & versions to known vulnerabilities, giving us CVE's mettric.  

Export is made on XML file.

## Match CVE with data

To get the CVSS link to the CVE-id given by **Vulners**, we use the NVD Nist [NVD](https://nvd.nist.gov/) database.

All the JSON's file of the NVD Nist databse are available on this [Github Project](https://github.com/olbat/nvdcve.git). They are automatically updated from the NIST website.

The main benefit of this workflow is that it's fast, efficient and accurate. We get the maximum amount of information in the shortest possible time, compared to the latest version of this projet.

## Web vulnerability scanner

The web scanner is used with Nuclei, a vulnerability scanner.
First, we launch nmap to get informations on web port open, and eventually also with a script which is "dns-brute" that permit us to get the subdomain of the host initially enter.

We write all the information that we get into a file, with host and port.

Then, we launch nuclei with all the template available on the nuclei-template folder and with an JSON export.

## Exploit scanner


## Send data to API
All data collected are send to the backoffice [API](back.html).

## Nmap script

### ssl-cert

The ssl-cert script permit us to get informations of the certificate as the common name, the validity date, the hash1 fingerprint...

### dns-brute

The dns-brute script is used to discover all the subdomains of the host initially entered. We get the IP address and the domain name.

### smb-vuln-ms17-010

The smb-vuln-ms17-010 script attempts to detect if a Microsoft SMBv1 server is vulnerable to a remote code execution vulnerability (ms17-010, a.k.a. EternalBlue). The vulnerability is actively exploited by WannaCry and Petya ransomware and other malware.

### ftp-vuln-cve2010-4221

The ftp-vuln-cve2010-4221 script checks for a stack-based buffer overflow in the ProFTPD server, version between 1.3.2rc3 and 1.3.3b. By sending a large number of TELNET_IAC escape sequence, the proftpd process miscalculates the buffer length, and a remote attacker will be able to corrupt the stack and execute arbitrary code within the context of the proftpd process .

## Technical example

### vulns module

If the vulns module has been launched, we entered in the next condition :

![Cegabox Module](https://cebago.github.io/Cegabox/img/cegabox-vulnerability-module-vulns.png)

If the CVE-Tab has at the minimum one CVE, we link that CVE with de NVD Nist database to get the CVE file that has all the informations.
Once opened, we create our variable that will contain the Vulnerability class and we load into another variable our json file.

Then, we will launch our function completeVuln which parse all the information found on the json file.

Then we create the link between the host, the service (if it exist) and the vulnerability (if it exist) to send that to the API.

### vulnerability class

This is the Vulnerability class.

![Cegabox Class](https://cebago.github.io/Cegabox/img/cegabox-vulnerability-class.png)

We initialize the variable with None.

![Cegabox Class](https://cebago.github.io/Cegabox/img/cegabox-vulnerability-class-savevuln.png)

Then we enter in the saveVuln function.

First, we search if the vulnerability exist on our database.
If it exist, we will not save it, because we don't want duplicate data.

If it doesn't exist, we will insert all the informations that we have collected.