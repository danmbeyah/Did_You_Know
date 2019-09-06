# Did_You_Know
Useful code snippets and How To's

# Set up Apache, MySQL and PHP on MacOS Mojave
https://jasonmccreary.me/articles/install-apache-php-mysql-mac-os-x-mojave/
https://jasonmccreary.me/articles/configure-apache-virtualhost-mac-os-x/

# Cloning a private repo (SSH)
GIT ADD SSH (Allows your local environment to clone or push commits to remote)
1. cd /Users/mbeyah/.ssh  (Replace mbeyah with your user)
2. ssh-keygen -t rsa -b 4096  (Generating public/private rsa key pair. Will prompt for identity, give a name to ID your machine. air was given in this case. Creates private key 'air' and public key 'air.pub' inside .ssh folder)
3. cat air.pub | pbcopy      (Copy public key stored in air.pub. Go to github: settings=>SSH & GPG keys, add ssh key...paste and save)
4. ssh-add air   (Adds private key to local machine. Do this while still in /Users/mbeyah/.ssh folder)
5. cd Users/mbeyah/Sites/myProject (cd to your local project folder)
5. git clone 'ssh url of private repo' . (Clone the repo. Last period ensures current folder is used as root :))

CD to root of local github repo and look for .git folder (Tip: ls -a to see hidden folders)
1. cd path/to/project
2. cd .git
3. nano config
4. Copy ssh link of repo from github
5. Paste the link in url element
