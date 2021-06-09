# ansible-ssh-keygen
Create user and add public certificate for remote none password authentification

1. Change my_user_name in all files to your user name which you want to create
2. Change /home/my_user_name/.ssh/id_rsa.pub to path of your public key wich you want to add to remote host
3. Run 
```bash 
ansible-playbook -i inventory/static.yml create-user.yml --limit 'all' -e 'user_name=user_for_connect_to_remote_host' --ask-pass
```
4. Type password for remote host
