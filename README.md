# MySQL-role

Installeert MySQL op Ubuntu 24.04 en configureert een database,
een gebruiker en de listen IP.

## Vereisten

Installeer de benodigde collection:

```bash
ansible-galaxy collection install -r requirements.yml
```

## Variabelen

- mysql_database: naam van de database, standaard les04
- mysql_username: databasegebruiker, standaard dbuser
- mysql_password: verplicht in te stellen
- mysql_bind_address: standaard 127.0.0.1
- mysql_allowed_hosts: standaard alleen localhost

## Voorbeeld

```yaml
---
- name: MySQL configureren
  hosts: databaseservers
  become: true

  vars:
    mysql_password: dbpassword

  roles:
    - avi1505.mysql
```


## Licentie

MIT