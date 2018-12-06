# git-remote-setup-reminder
How to setup a new remote &amp; local GIT repository

### Remote repo :  
```
ssh git@{{ip_server}} -p {{ssh_port}}  
mkdir -p /home/git/{{project_name}}.git  
cd /home/git/{{project_name}}.git  
git init --bare  
```

### Locally :
```
mkdir {{new_project_name}}  
cd {{new_project_name}}  
echo ‘Hello World’ > hello_world.txt  
git init  
git add hello_world.txt  
git commit -m “Initial commit : Hello World“  
git remote add origin ssh://git@{{ip_server}}:{{ssh_port}}/home/git/{{project_name}}.git  
git push origin master  
```

### Test :
```
cd /tmp ; git clone ssh://git@{{ip_server}}:{{ssh_port}}/home/git/{{project_name}}.git
```

### Change repo url :
```
git remote set-url origin ssh://git@{{ip_server}}:{{ssh_port}}/home/git/{{project_name}}.git
```

##### Based on : https://gist.github.com/steveclarke/1411146
