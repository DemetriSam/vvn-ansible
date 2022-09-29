ansible-playbook playbook.yml -i production.ini --verbose

ansible-playbook playbook.yml --tags "dev" -i production.ini --verbose

ansible-playbook playbook.yml --tags "dev,prod" -i production.ini --verbose

ansible-playbook playbook.yml -i production.ini --limit web-dev --verbose

ansible-playbook playbook.yml -i production.ini --limit web-prod --verbose

ansible-inventory -i production.ini --list

ansible all -i production.ini -m ping

ansible-config dump

ansible dbservers -i production.ini -m setup | less

