# Did_You_Know
Useful code snippets and How To's

# Cloning a private repo (SSH)
GIT ADD SSH (Allows your local environment to clone or push commits to remote)
1. ssh-keygen -t rsa -b 4096  (Generating public/private rsa key pair. Will prompt for identity, give a name ti ID your machine)
2. CD cd /Users/mbeyah/.ssh
3. cat air.pub | pbcopy      (Go to github and add ssh key...paste and save)
4. ssh-add air   (Adds private key to local machine)

CD to root of local github repo and look for .git folder
1. nano config
2. Copy ssh link of repo from github
3. Paste the link in url element
