# Installation de l'agent:

```bash
ansible-playbook playbook.yml -e '{"ansible_become_password": "<YOUR ROOT PASSWORD>", "ws1_username": "<YOUR WS1 USER NAME>", "ws1_password": "<YOUR WS1 PASSWD>", "ws1_server_url": "<WS1 URL>", "ws1_group_id": "<WS1 GROUP ID>", "state": "present"}'
```

Distributions supportées:
* [X] Debian (install deb)
* [ ] ReHat (install rpm)
* [ ] Others (install ruby, puppet agent, ws1HubUtil from tar.gz)

# Désinstallation de l'agent:

```bash
ansible-playbook playbook.yml -e '{"state": "absent"}'
```
