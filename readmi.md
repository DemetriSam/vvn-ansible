ansible-playbook playbook.yml -i production.ini --verbose
ansible-playbook playbook.yml --tags "dev" -i production.ini --verbose
ansible-playbook playbook.yml --tags "dev,prod" -i production.ini --verbose
ansible-playbook playbook.yml -i production.ini --limit web-dev --verbose
ansible-playbook playbook.yml -i production.ini --limit web-prod --verbose
ansible-inventory -i production.ini --list
ansible all -i production.ini -m ping
ansible-config dump
ansible dbservers -i production.ini -m setup | less
yc config profile activate default
kubectl exec -it -n production bb-backend-55bc6794f8-sk476 -c php -- sh
ssh vasily@217.28.230.84 -i id_rsa
cd /var/www/beautybox/docker/ && make update-front-market
