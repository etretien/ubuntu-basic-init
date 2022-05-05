# ubuntu-basic-init
Simple ansible playbook to start and make initial configuration of an Ubuntu server.

# usage

1. Create an Ansible Vault file (named 'passwd.yml' in the example below):

`ansible-vault create passwd.yml`

2. Set the host_user_passwd and host_root_passwd in the vault (using the opened editor)

3. Add you server details to the ./inv/hosts file.

4. Run the playbook on you server or set of servers:

`ansible-playbook -i inv/hosts.yml --ask-vault-pass --extra-vars '@passwd.yml' playbooks/01-init.yml -l server01.example.com -u root`
