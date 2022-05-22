When you want to create your own Server i suppose to use [Matrix-Docker-Ansible](https://github.com/spantaleev/matrix-docker-ansible-deploy).   
The advantage is that [there are built in many servers](https://github.com/spantaleev/matrix-docker-ansible-deploy#supported-services), which you can easy install and updates if you want.   
It's easy to update all of this. e.G. when you use Linux you just need to use this two commands and everything is up to date.
```
git pull
ansible-playbook -i inventory/hosts setup.yml --tags=setup-all,start
```
