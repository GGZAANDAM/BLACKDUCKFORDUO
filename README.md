# Blackduck

---

## Notes

 - **Synopsys will be deprecating support for Docker Compose starting with the Black Duck 2019.4.0 release. Docker Compose will be supported until December 31, 2019.**
  
Source: https://github.com/blackducksoftware/hub/tree/master/docker-compose

- **Deploying Black Duck in Kubernetes/OpenShift is the recommended approach for installing Blackduck.**

Source: https://github.com/blackducksoftware/hub/tree/master/kubernetes\

- **Blackduck can be used with Synopsys Operator, to simply Blackduck deployments on Kubernets adn Openshift.**

Source: https://github.com/blackducksoftware/hub/wiki/Black-Duck-Installation-Guide

- **Using Blackduck without Synopsys Operator by Jonathan Beakley.**
https://synopsys.atlassian.net/wiki/spaces/BDLM/pages/34570390/Installing+Black+Duck+in+Clusters+not+Running+the+Operator+2018.12.0


---

## What is Blackduck exactly?


(Blackduck is software from a company named synopsys.
Blackduck provides insight in software composition analysis (SCA) solution for managing security, quality, and license compliance risk thatcomes from the use of open source and third-party code in applications and containers. Black Duck gives visibility into third-party code,enabling you to control it across your software supply chain and throughout the application life cycle.)

---

## What does blackduck?

 
### Using Blackduck:

- Scans your code and identify open source software thatexists in your codebase.
- View the generated Bill of Materials for your softwareprojects.
- View vulnerabilities that have been identified in opensource components.
- Assess your security, license, and operational risk.

#### Source:
https://info.blackducksoftware.com/rs/872-OLS-526/images/Hub_Trial_GettingStarted.pdf

---

## Blackduck with the following components:

### Supported Languages

    C
    C++
    C#
    Erlang
    Golang
    Java
    JavaScript
    Node.JavaScript
    Objective-C
    Swift
    Perl
    Python
    PHP
    RecipeRuby
    Scala
    .NET

### Supported Package managers

    NuGet
    Hex
    Vndr
    Godep
    Dep
    Maven
    Gradle
    Npm
    CocoaPods
    Cpanm
    Conda
    PEar
    Composer
    Pip
    Packrat
    RubyGEms
    SBT

### Supported DevOps tools

#### IDes

    Eclipse
    Visual Studio IDes

#### Continuous intergration

    Jenkins
    TeamCity
    Bamboo
    Team Foundatiom Server
    Travis Ci
    Circle Ci
    GitLab Ci
    Visual Studio Team Services
    Concourse Ci
    Codeship

#### Workflow and notifications

    Jira
    Slack
    Hipchat
    Email
    SPDX

#### Binary and source repositories

    Artifactory
    Nexus
#### Application security suites

    IBM AppScan
    Micro Focus Fortify
    SonarQube
    ThreadFix
    Cybric
    Code Dx

### Cloud Technologies

#### Cloud platforms

    Amazon Web Services
    Google Cloud platform
    Microsoft Azure

#### Container platform

    Docker
    OpenShift
    Pivotal Cloud Foundry
    Kubernetes

### Databes

    PostgreSQL

## Blackduck binary analysis

### Binary formats

    Native binaries
    Java binaries
    .NET binaries
    Go binaries

### Compression formats

    Gzip (.gz)
    bzip2 (.bz2)
    LZMA (.lz)
    LZ4 (.lz4)
    Compress (.Z)
    XZ (.xz)
    Pack200 (.jar)
    UPX (.exe)

### Installation formats

    Red Hat RPM (.rpm)
    Debian package (.deb)
    Mac installers (.dmg .pkg)
    Unix shell file installers (.sh, .bin)
    Windows installers (.exe .msi .cab)

### Archive formats

    ZIP (.zip .jar .apk and other derivatives)
    XAR (.xar)
    7-ZIP (.7z)
    ARJ (.arj)
    TAR (.tar)
    VM TAR (.tar)
    cpio (.cpio)
    RAR (.rar)
    LZH (.lzh)
    Electron archive (.asar)

### Firmware formats

    Intel Hex
    SREC
    U-boot
    ARRIS firmware
    Juniper firmware
    Kosmos firmware
    Android sparse file system
    Cisco firmware

### File systems / disk images

    ISO 9660/UDF (.iso)
    Windows imaging
    ext2/3/4
    JFFS2
    UBIFS
    RomFS
    Microsoft Disk images
    Macintosh HFS
    VMware VMDK (.vmdk .ova)
    QEMU Copy-On-Write (qcow2)
    Virtualbox VDI (.vdi)
    QNX-EFS, IFS
    NetBoot image (.nbi)


#### Source:
https://www.synopsys.com/content/dam/synopsys/sig-assets/datasheets/blackduck-sca-ds-ul.pdf

---

## Blackduck architecture

### Blackduck deployment options

    - On Premises (Knowledge base is on not On Premises)
    - Blackduck Hosted one of their cloud service partners. (Uses Amazon Web Services, Google platform and the Knowledge base is in the Data center)
    - As a Hosted Black Duck Solution (In the Blackduck data center and handles maintenance and upgrades)
   
 #### Source:
 https://synopsys.skilljar.com/black-duck-hub-architecture/41443/scorm/px9gytxx8g3b

---

## Blackduck consists of:

### Client Side

    - Rest API
    - Web Browser
    - Scanning tools
    - Plugin (IDE Plugin? like Visual Studio?)

### Hub application

    - Is deployed and managed as a set of Docker containers and supports a range of container orchestration platforms.
    - Support for Docker Swarm, Kubernetes and RedHat's OpenShift and more.

### Blackduck data contains:

    - Registration services
    - vulnerability service
    - Detail services
    - Match services and search services

#### Source:
https://synopsys.skilljar.com/black-duck-hub-architecture/41443/scorm/px9gytxx8g3b

---

## Blackduck Technical introduction


#### Source:
https://synopsys.skilljar.com/black-duck-hub-architecture/41443/scorm/px9gytxx8g3b

---

## *Blackduck can also be used with another container platform like Openshift*

https://community.synopsys.com/s/article/Black-Duck-Hub-Installing-the-Hub-using-OpenShift-All-4-6-Versions

---
## (Deprecated) Dockerized Blackduck Installation

Blackduck is depoyed as a set of nine Docker containers, these containers work together to contain the overall application.
Each of them have their on responsibility.

**More sophisticated details can be found: customersuccessportal.blackducksoftware.com
https://community.synopsys.com/s/article/Black-Duck-Hub-Installing-Black-Duck-using-Docker-Compose-Version-2019-2-0**


### The 9 containers are:

    - #1 Web Server
    - #2 Certificate Authority (Used by most containers for certificates)
    - #3 LogStash (Gather the logs from all containers)
    - #4 Web App (Processes User Interface requests)
    - #5 Registration
    - #6 Solr (Acts as the enterprise search platform component)
    - #7 ZooKeeper
    - #8 DB
    - #9 Job Runner
  
 More sophisticated details can be found: customersuccessportal.blackducksoftware.com

### Blackduck Hardware requirements*
*requirements are depended on the number of projects that are being managed.

    - 64-bit quad core processor.
    - 20 GB of RAM.
    - 250 GB of free space for the database and other hub containers.
    - Free space for database backups

### Prefered 64-bit operating systems for Blackduck.

    - CentOS 7.3 or higher
    - Ubuntu 16.04.x or higher
    - Oracle Enterprise Linux 7.3 or higher
    - Red Hat Enterprise Linux server 7.3 or higher
    - SUSE Linux Enterprise server 12.x or higher 
    - Linux Operating systems that support Docker 17.03.x

### Software requirements for Blackduck docker.

    - Docker 17.03.x or newer (CE or EE)
    - Supported orchestration tools (Docker Swarm, Docker Compose or Docker run.)
    - OpenShift
    - Kubernetes
    - Pivotal Cloud Foundry

### Docker Swarm restrictions

Notes

    - It's possible to set up a swarm with multiple notes.

### Swarm with a multi-note enviroment

Notes

    - Ensure that the PostgreSQL database runs on the same node. (If you are using an external PostgreSQL database the rule does apply.)
    - You also need to ensure that hub-webapp service (#4 Web App that processes the User Interface requests.) and hub-logstash service are both running on the same node. Because it's necessary that the Web App can access the logs that need to be downloaded.

### Network Requirements

The Blackduck requires several ports to be externally accessible.

The web server component(s) (#1 Web server) relies on HTTPS port 443
And if you want to leverage the Hub reporting database you'll need to ensure port 5536 is also available.

    - Port 443 Web server HTTPS port for BlackDuck via NGINX
    - Port 55436 Read-only database port from PostgreSQL for reporting.

If your corporate security policy requires registration of specific URLs, connectivity from your Hub installation to Black Duck hosted servers limited communications via HTTPS/TCP on port 443 with following servers are:

    - update.suite.blackducksoftware.com
    - kb.blackducksoftware.com
    - doc.blackducksoftware.com

    Exposed reporting port 553436
    Exposed HTTPS port 443

### Using a proxy: Things to know

If you are going to make proxy requests to the Hub, you'll need to work with proxy server administrator to get the following required information:

    - The protocol used to communicate with your proxy (HTTP or HTTPS)
    - The name of the proxy server host.
    - Port on which the proxy server host is listening
    - Authentication settings
  
Consult the Blackduck docker install guide for details on configuring proxy.

#### Source: 
https://synopsys.skilljar.com/black-duck-hub-installation-docker/82827/scorm/39ejf7qlnpg3q#

### ~~Installing Blackduck using Docker compose~~ **Deprecated**

https://community.synopsys.com/s/article/Black-Duck-Hub-Installing-Black-Duck-using-Docker-Compose-Version-2019-2-0

### Installing Docker

Docker installations can vary depending on your operating system and version of docker.

What is being used:

    - Docker community edition using docker reposity method
    - CentOS

Setting up docker repository

    sudo yum install -y yum-utils device-mapper-persistent-data lvm2

Setting up stable repository

    sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo

Update the yum package index to ensure the latest version of docker is available to us

    sudo yum makecache fast

Now we install docker itself

    sudo yum install docker-ce

Now we will start docker and run the hello world image to verify docker is functional.

    sudo systemctl start docker
    sudo docker run hello-world

### Docker post-install

There are still a few post installation tasks to complete before we can move to the installation of Blackduck.
First we to manager docker as a non root user, so that we won't have to the issue the sudo command each time we want to run a docker command.
To do this we'll create a docker group called "Docker" and the myself (Or somebody else) into it.

When the docker daemon starts, it will make ownership of the unix socket read and writeable by the docker group.

Use the groupadd command to create the group.

    sudo groupadd docker

Verify if the group has been created

    getent group

Add yourself (Or somebody else to group)

    sudo usermod -aG docker $USER

You can test that this is successful by running the hello world image without typing sudo before it.

docker run hello-world

The final post-install step to configure docker to automatocally strat when the system reboots.

    sudo systemctl enable docker

### Docker resources links

https://docs.docker.com/install/

https://docs.docker.com/engine/swarm/swarm-tutorial/


### blackduck installation process

First obtain:

    - Orchestration files.
    - Configure Web Server and optional proxy environment files.
    - Install a hub with a Docker orchestration tool like Docker swarm.

Download the **latest** orchestration files from

    https://github.com/blackducksoftware/hub
    sudo wget https://github.com/blackducksoftware/hub/archive/v2019.4.2.tar.gz

Unpack the tar file on the server

    sudo tar xvf "file"

With

    cd "file"
    ls -la

You'll reference theses files later.

    hub-proxy.env
    hub-webserver.env
    hub-postgres.env
    docker-compose.yml

You'll need to edit hub-webserver.env file (Or your favourite editor you are using)

    sudo vi hub-webserver.env

Change the hostname to something else.

    PUBLIC_HUB_WEBSERVER_HOST=localhost

You can also configure the proxy settings using the hub proxy environment file (You'll need the settings if a proxy is required)
Run the following command

    more hub-proxy.env

Blackduck also supports using an external PostgreSQL instance managed by Amazon relational Dattabase service or another service.
Search for the file called

    external-postgres-init.pgsql

You'll also need to provide connection details using this provided postgres environment file.

    more hub-postgres.env

Details on using an external PostgresSQL instance and specifics for confuguring the environment file can be found in the Blackduck docker install guide.

You can install Blackduck to initialize swarm and install it with PostgreSQL database instance with the following commands.

    docker swam init
    docker stack deploy -c docker-compose.yml hub

The docker implementation of Hub provides scalability by allowing admins to choose the numberr of active job runner containers, you can do this with command

    docker service scale hub_jobrunner=2

You can verify the installation was successful by login into web interface using default sysadmin account with the password blackduck.

    Username: sysadmin
    PAssword: blackduck

The first thign you should do is change your password and username, so that you Blackduck server is secure. (Okay, you can only change the password in the web interface.)

#### Source:
https://synopsys.skilljar.com/black-duck-hub-installation-docker/82827/scorm/39ejf7qlnpg3q


Gemaakt door Guillermo Zaandam.
