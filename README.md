# git-remote-setup-reminder
Git setup new remote &amp; local repo

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
