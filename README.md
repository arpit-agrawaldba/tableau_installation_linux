<!-- Add banner here -->
![Banner](https://github.com/arpit-agrawaldba/tableau_installation_linux/blob/main/header.png)

# Tableau Server Installation - Linux

<!-- Add buttons here -->

![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/navendu-pottekkat/awesome-readme?include_prereleases)
![GitHub last commit](https://img.shields.io/github/last-commit/navendu-pottekkat/awesome-readme)
![GitHub issues](https://img.shields.io/github/issues-raw/navendu-pottekkat/awesome-readme)
![GitHub pull requests](https://img.shields.io/github/issues-pr/navendu-pottekkat/awesome-readme)
![GitHub](https://img.shields.io/github/license/navendu-pottekkat/awesome-readme)

<!-- Describe your project in brief -->

The project provides you an automated method using ansible to install a standalone Tableau Server on Linux.
It uses ansible to orchestrate the operating sytem configuration, tableau server installation and configuration.

This code currently certified for following version:
Tableau Server - 2020.3.3
Operating System - RHEL7.* and AWS Linux 2

<!-- Add badges with link to Shields IO -->

![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/navendu-pottekkat/awesome-readme?include_prereleases)
: This badge shows the version of the current release.

![GitHub last commit](https://img.shields.io/github/last-commit/navendu-pottekkat/awesome-readme)
: I think it is self-explanatory. This gives people an idea about how the project is being maintained.

![GitHub issues](https://img.shields.io/github/issues-raw/navendu-pottekkat/awesome-readme)
: This is a dynamic badge from [**Shields IO**](https://shields.io/) that tracks issues in your project and gets updated automatically. It gives the user an idea about the issues and they can just click the badge to view the issues.

![GitHub pull requests](https://img.shields.io/github/issues-pr/navendu-pottekkat/awesome-readme)
: This is also a dynamic badge that tracks pull requests. This notifies the maintainers of the project when a new pull request comes.

![GitHub All Releases](https://img.shields.io/github/downloads/navendu-pottekkat/awesome-readme/total): If you are not like me and your project gets a lot of downloads(*I envy you*) then you should have a badge that shows the number of downloads! This lets others know how **Awesome** your project is and is worth contributing to.

![GitHub](https://img.shields.io/github/license/navendu-pottekkat/awesome-readme)
: This shows what kind of open-source license your project uses. This is good idea as it lets people know how they can use your project for themselves.

![Tweet](https://img.shields.io/twitter/url?style=flat-square&logo=twitter&url=https%3A%2F%2Fnavendu.me%2Fnsfw-filter%2Findex.html): This is not essential but it is a cool way to let others know about your project! Clicking this button automatically opens twitter and writes a tweet about your project and link to it. All the user has to do is to click tweet. Isn't that neat?

# Demo-Preview
<!-- Add a demo for your project -->

After you have written about your project, it is a good idea to have a demo/preview(**video/gif/screenshots** are good options) of your project so that people can know what to expect in your project. You could also add the demo in the previous section with the product description.

Here is a random GIF as a placeholder.

![Random GIF](https://media.giphy.com/media/ZVik7pBtu9dNS/giphy.gif)

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
