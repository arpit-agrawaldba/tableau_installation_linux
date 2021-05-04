<!-- Add banner here -->
![Banner](https://github.com/arpit-agrawaldba/tableau_installation_linux/blob/main/header.png)

# Tableau Server Installation - Linux

<!-- Describe your project in brief -->

The project provides you an automated method using ansible to install a standalone Tableau Server on Linux.
It uses ansible to orchestrate the operating sytem configuration, tableau server installation and configuration.

This code currently certified for following version:

Tableau Server - 2020.3.3

Operating System - RHEL7.* and AWS Linux 2



# Table of contents

After you have introduced your project, it is a good idea to add a **Table of contents** or **TOC** as **cool** people say it. This would make it easier for people to navigate through your README and find exactly what they are looking for.

Here is a sample TOC(*wow! such cool!*) that is actually the TOC for this README.

- [Project Title](#project-title)
- [Demo-Preview](#demo-preview)
- [Table of contents](#table-of-contents)
- [Installation](#installation)
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

![Footer](https://github.com/arpit-agrawaldba/tableau_installation_linux/blob/main/header.png)
