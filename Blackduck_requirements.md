## Sources

https://community.synopsys.com/servlet/fileField?entityId=kaC2H000000TNHXUA4&field=Attachment__Body__s

## Known issues

https://wiki.prd.duo.nl/display/PROV/Known+Issues

## Requirements

One instance of blackduckhub with 9 cotainers 

- Docker CE latest
- 4 CPUs
- 20 GB RAM
- 250 GB for Database en Blackduck containers
- Extra space for database backups

### Binary analysis needs:

- 5 CPUs 
- 20 GB RAM
- 350 GB disk space for database and other Blackduck containers
- An additional CPU, 2 GB RAM adn 100 GB Disk space is needed for every additional binaryscanner container.

Recommended to monitor disk utilitzation on blackduckhub servers to prevent disk from reaching capacity which could cause issues.
Blackduck alert requires an additonal of 1 GB RAM



### Docker requirements
Docker compose for running multi-container Docker applications.
Blackduck supports Docker CE and EE **

Docker versions
- 17.12.x
- 18.03.x
- 18.06.x
- 18.09.x


### Operating systems

Docker CE does not support Red Hat Enterprise.

- CentOS 7.3
- Red Hat Enterprise Linux server 7.3
- Ubuntu 16.04x
- SUSE Linux Enterprise server version 12.x 64-bit
- Oracle Enterprise Linux 7.3

### Software requirements

Blackduck doesn't support compatibillity mode

- Chrome 73.0.3683.86 or higher
- Firefox 66.0 or
- Inter Explorer 11.648.17134.0 or higher
- Microsoft Edge 17.17134
- Safari 12.0.3

### Network requirements

Blackduck requires the following ports to be externally accessible:

- Port 443 Web server HTTPS port for BlackDuck via NGINX
- Port 55436 Read-only database port from PostgreSQL for reporting.
  
If your corporate security policy requires registration of specific URLs, connectivity from your Hub installation to Black Duck hosted servers limited communications via HTTPS/TCP on port 443 with following servers are:

- update.suite.blackducksoftware.com
- kb.blackducksoftware.com
- doc.blackducksoftware.com

### Database requirements

Blackduck uses PostgreSQL to store data.


### PostgreSQL version

Running your own instance of PostgreSQL container Blackduck supports:

  - PostgreSQL 9.6.x version

### Proxy server requirements

Support

- No authentication
- Digest
- Basic
- NTLM

Get the following required information if you want to make proxy requests to blackduckhub.

- The protocol used by proxy server host (http or https).
- The name of the proxy server host.
- The port on which the proxy server host is listening.

#### Container platform

- Docker
- OpenShift
- Pivotal Cloud Foundry
- Kubernetes