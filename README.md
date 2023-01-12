# Installation de l'agent:

```bash
ansible-playbook playbook.yml -e '{"ansible_become_password": "<YOUR ROOT PASSWORD>", "ws1_username": "<YOUR WS1 USER NAME>", "ws1_password": "<YOUR WS1 PASSWD>", "ws1_server_url": "<WS1 URL>", "ws1_group_id": "<WS1 GROUP ID>", "state": "present"}'
```

Voici les différentes variables dont vous pouvez modifier les valeurs avec chevrons (`<>`):
* `ansible_become_password`: le mot de passe root/super utilisateur de votre distribution (où vous le gérer dans les host_vars)
* `ws1_username`: le nom d'utilisateur pour workspaceone
* `ws1_password`: votre mot de passe workspaceone
* `ws1_group_id`: le groupe workspaceone
* `ws1_server_url`: l'url du serveur workspaceone. Attention, contrairement à la documentation, il ne faut pas mettre le scheme (**http**:// ou **https://**)
* `ws1_version`: workspaceone version (defauklt: 22.06.0.7)

Distributions supportées:
* [X] Debian (install deb)
* [ ] ReHat (install rpm)
* [ ] Others (install ruby, puppet agent, ws1HubUtil from tar.gz)

# Désinstallation de l'agent:

```bash
ansible-playbook playbook.yml -e '{"state": "absent"}'
```
