# Did_You_Know
Useful code snippets and How To's

# Cloning a private repo (SSH)
GIT ADD SSH (Allows your local environment to clone or push commits to remote)
1. cd /Users/mbeyah/.ssh  (Replace mbeyah with your user)
2. ssh-keygen -t rsa -b 4096  (Generating public/private rsa key pair. Will prompt for identity, give a name to ID your machine. air was given in this case. Creates private key 'air' and public key 'air.pub' inside .ssh folder)
3. cat air.pub | pbcopy      (Copy public key stored in air.pub. Go to github and add ssh key...paste and save)
4. ssh-add air   (Adds private key to local machine)
5. cd Users/mbeyah/Sites/myProject (cd to your local project folder)
5. git clone 'ssh url of private repo' . (Clone the repo. Last period ensures current folder is used as root :))

CD to root of local github repo and look for .git folder
1. nano config
2. Copy ssh link of repo from github
3. Paste the link in url element
