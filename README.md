# ansible
Ansible playbooks and roles used by canadensys to :
- add a bit more secure server
- install wordpress, media wiki

## dependencies:
use: ansible 2.2.0.0 or more
use: python 2.7.x or more

## how to use
### Install security playbook
$ ansible-playbook -i hosts -l vm_local_102 security_playbook.yml --user user_with_root_access --ask-pass --ask-sudo-pass

### Install security playbook
$ ansible-playbook -i hosts -l vm_local_102 wordpress_playbook.yml --user user_with_root_access  --private-key ~/.ssh/your_private_key.rsa --ask-sudo-pass

## Usable CL:
to create a password:
$ mkpasswd --method=sha-512
to create ssh key:
$ ssh-keygen -f irbv_wordpress.rsa