<!-- Add banner here -->
![Banner](https://github.com/arpit-agrawaldba/tableau_installation_linux/blob/main/header.png)

# Project Title

<!-- Describe your project in brief -->
## Tableau Server Installation - Linux

The project provides you an automated method using ansible to install a standalone Tableau Server on Linux.
It uses ansible to orchestrate the operating sytem configuration, tableau server installation and configuration.

This code currently certified for following version:

    Tableau Server - 2020.3.3

    Operating System - RHEL7.* and AWS Linux 2



# Table of contents

- [Project Title](#project-title)
- [Table of contents](#table-of-contents)
- [Installation](#installation)
- [Prepare Code](#Prepare-Code)
- [Usage](#usage)
- [Development](#development)
- [Contribute](#contribute)
    - [Sponsor](#sponsor)
    - [Adding new features or fixing bugs](#adding-new-features-or-fixing-bugs)
- [License](#license)
- [Footer](#footer)

# Installation
[(Back to top)](#table-of-contents)

To use this project, first clone the repo on your device using the command below:

```git init```

```git clone https://github.com/arpit-agrawaldba/tableau_installation_linux.git```

# Prepare Code
[(Back to top)](#table-of-contents)

Before using the code you would need to place or modify the variable file under the location

    <directory_repo_download>/tableau_installation_linux/vars/tab_var.yml

Make sure at a minimum place or modify values of following mentioned variables and rest can be used default.

The first variable "tableau_logical_vol_size_ingb" means the size of the tableau mount point where installation and data will be kept.
The second variable "tableau_software_disk" means disk name on the EC2 instance to be used for installation and data for which we mentioned size and that also means this disk size used in the above variable should be equal or lesser thant this disk size.
Third and Fourth "aws_access_key", "aws_secret_key" are your AWS bitbucket credentials where software is being kept for installation.
The fifth variable "aws_bucket" is the bitbucket name where software has been copied.

    "tableau_logical_vol_size_ingb": "100G"
    "tableau_software_disk": "/dev/xvdf"
    "aws_access_key": "KDLDODZH6BLCWQZ335YWFZ"
    "aws_secret_key": "alkadfJJDLDV0ONEz5LDSRkNYQWFrTii0aI"
    "aws_bucket": "bitbucket_tableau"

Software needs to be uploaded on AWS Bitbucket before installation and its variable details are mentioned below. Download them from the tableau website and upload them to bitbucket.

The first variable "tableau_software_rpm" is name of tableau server rpm for version 2020.3.3.
The second, Third, and Fourth variables are driver software name for PostgreSQL, Oracle, and MSSQL servers respectively.
Make sure all these software are present in your AWS bucket and details of these are mentioned in the variable file as per the variable discussed just before.


    "tableau_software_rpm": "tableau-server-2020-3-3.x86_64.rpm"
    "postgresql_driver_rpm": "tableau-postgresql-odbc-09.06.0500-1.x86_64.rpm"
    "oracle_driver_rpm": "tableau-oracle-12.1.0.2.0-1.x86_64.rpm"
    "mssql_driver_rpm": "msodbcsql17-17.5.1.1-1.x86_64.rpm"

Once Vriable file has been prepared move to Next section to start the installation.

## Kindly note for the production system review every variable and check if they need to be modified as per your needs.

As the automation code is Anisble based one may also need to install it. Here are steps to install it

Install python first, ignore if already present. It can also work on python 2.7.

    yum install python36
    
Install EPEL  

    (For RHEL7)
    yum install wget
    wget http://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
    rpm -ivh epel-release-latest-7.noarch.rpm
    yum repolist

    (For AWS Linux)
    sudo amazon-linux-extras install epel
    yum repolist

Install Ansible

    (For RHEL7)
    yum --enablerepo=epel install ansible

    (For AWS)
    sudo amazon-linux-extras install ansible2

# Usage
[(Back to top)](#table-of-contents)

ansible-playbook <directory_repo_download>/tableau_installation_linux/tableau_build.yml

For example when repository has been downloaded under directory /root/tableau, then execute

    ansible-playbook /root/tableau/tableau_installation_linux/tableau_build.yml


# Development
[(Back to top)](#table-of-contents)

Anisble code consists of eight roles, eaching having it's own purpose

    1. tableau_os_build -    Configurate operating sytem for Tableau Server installation.
    2. tableau_install -     Install the Tableau Server rpm software.
    3. tableau_tsm_init -    TSM Initliazation. 
    4. tablea_activate -     Active the Tableau Server.
    5. tableau_register -    Register the Tableau Server.
    6. tableau_config_init - Configure the Identity Store and Initliaze.
    7. tableau_post_config - Post Installation setup. 
    8. tableau_monitoring -  Enable Monitoring.

# Contribute
[(Back to top)](#table-of-contents)

Currently this repoistory is not open for external contribution.

### Sponsor
[(Back to top)](#table-of-contents)

This project is currently self-sponsored.

### Adding new features or fixing bugs
[(Back to top)](#table-of-contents)

No open bug fixes at the moment.

# License
[(Back to top)](#table-of-contents)


[GNU General Public License version 3](https://opensource.org/licenses/GPL-3.0)

# Footer
[(Back to top)](#table-of-contents)


<!-- Add the footer here -->

![Footer](https://github.com/arpit-agrawaldba/tableau_installation_linux/blob/main/footer.png)
