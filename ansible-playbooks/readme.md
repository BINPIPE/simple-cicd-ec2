## Steps to use:

1. Check the user name and vars in all files and the inventory
2. Use the following command patterns to run the playbooks:

```
ansible-playbook -i hosts -l Group, playbook.yml  
```
or if using specific users not mentioned in playbooks:

```
ansible-playbook -i hosts -l Group, playbook.yml -u ubuntu --become-user=root
```
