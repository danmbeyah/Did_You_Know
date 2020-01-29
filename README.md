# Did_You_Know
Useful code snippets and How To's

# Set up Apache, MySQL and PHP on MacOS Mojave
https://jasonmccreary.me/articles/install-apache-php-mysql-mac-os-x-mojave/
https://jasonmccreary.me/articles/configure-apache-virtualhost-mac-os-x/

# Cloning a repo with (SSH)
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
`[remote "origin"]
        url = git@github.com:Organization/xyz.git`

# Cloning a repo into an existing local folder
1) First get to the existing directory  
```$ cd my/folder/```  
  
2) Now start a new git repository  
```$ git init```  
  
3) Identify if the current elements on the directory are needed or not and add them to the **.gitignore** file. When ready...  
```$ vim .gitignore```  
  
4) When ready create the first commit on the server  
```$ git add .;git commit -m'my first commit'```  
  
5) Now add the remote from where you want to clone  
```$ git remote add origin https|ssh:path/to/the/repository.git```  
  
6) Now just pull and merge with local git  
```$ git pull origin master --allow-unrelated-histories```  
  
7) If you have some merge conflicts resolve them and commit your changes. 


# Kill a process on a port

To list any process listening to the port 8080:

```lsof -i:8080```

To kill any process listening to the port 8080:

```kill $(lsof -t -i:8080)```

Or

```kill -9 $(lsof -t -i:8080)```

# Create package.json from node_modules folder

npm init

to create the package.json file and then you use

ls node_modules/ | xargs npm install --save

to fill in the modules you have in the node_modules folder.
