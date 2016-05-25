---
title: Install GitLab 
keywords: git gitlab 
summary: "Install GitLab for use with Code Manager"
sidebar: product1_sidebar
permalink: /install_gitlab/
---

### GitLab

1. On a new server, install GitLab.
 - [https://about.gitlab.com/downloads/](https://about.gitlab.com/downloads/)

2. After GitLab is installed, sign into the web UI with the user `root`.
 - The first time you visit the UI it will force you to enter a password for the `root` user.

2. In the GitLab UI, create a group called `puppet`.
 - [http://doc.gitlab.com/ce/workflow/groups.html](http://doc.gitlab.com/ce/workflow/groups.html)

3. In the GitLab UI, make yourself a user to edit and push code.

4. From your laptop or development machine, make an SSH key and link it with your GitLab user.
 - Note: The SSH key allows your laptop to communicate with the GitLab server and push code.
 - [https://help.github.com/articles/generating-ssh-keys/](https://help.github.com/articles/generating-ssh-keys/)
 - [http://doc.gitlab.com/ce/ssh/README.html](http://doc.gitlab.com/ce/ssh/README.html)

7. In the GitLab UI, add your user to the `puppet` group.
 - You must give your user at least master permissions to complete the following steps.
 - Read more about permissions:
    - [https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/permissions/permissions.md](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/permissions/permissions.md)

8. In the GitLab UI, create a project called `control-repo` and set its Namespace to the `puppet` group.

10. On your laptop, clone this PuppetLabs-RampUpProgram control repo.
 - `git clone https://github.com/PuppetLabs-RampUpProgram/control-repo.git`
 - `cd control-repo`

14. On your laptop, remove the origin remote.
 - `git remote remove origin`

15. On your laptop, add your GitLab repo as the origin remote.
 - `git remote add origin <SSH URL of your GitLab repo>`

16. On your laptop, push the production branch of the repo from your machine up to your Git server.
 - `git push origin production`
