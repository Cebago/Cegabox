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


## How our Scanner is build ?

### Scan host
In order to detect hosts, services and vulnerabilities on the network, we use this wonderful toolbox that is **nmap**.
To allow users to do several types of scans, we play with different parameters, like the number of ports on each host that will be scanned. It's determined through a script parameter. 


### Vulnerabilities discover

In complement, we use **Vulners** to match services & versions to known vulnerabilities, giving us CVE's mettric.  

Export is made on XML file.

### Match CVE whith data

To match CVE id given by **Vulners**, the script check on [NVD](https://nvd.nist.gov/) database.

With use a [Github Project](https://github.com/olbat/nvdcve.git) that is automatically updated from the NIST database, via JSON files.
The main adventage of this workflow is that it is fast, efficient and accurate. We get the maximum amount of information in the shortest possible time.


### 