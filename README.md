# Ansible-Role: acr-ansible-simple-systemd-service

AIT-CyberRange: Create and run a systemd service 


## Requirements

- Debian or Ubuntu 

## Role Variables

```yaml
app_name: app
app_user: "{{ app_name }}"
app_group: "{{ app_user }}"

app_basepath: /opt/{{ app_name }}
app_directory: "{{ app_name }}"

app_description: Service {{ app_name }}
app_service_file: templates/app.service.j2

app_autostart: true
app_service_execstart: ""
```

## Example Playbook

```yaml
- hosts: all
  roles:
    - acr-ansible-simple-systemd-service
      vars:
        app_name: appname
        app_user: "{{ appname_user }}"
        app_basepath: "{{ appname_basepath }}"
        app_service_execstart: "{{ appname_service_execstart }}"
```

## License

GPL-3.0

## Author

- Lenhard Reuter