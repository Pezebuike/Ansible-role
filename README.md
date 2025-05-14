# Ansible Role: nginx

An Ansible Role that installs and configures Nginx on Debian/Ubuntu and RHEL/CentOS systems.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
# Nginx listening port
nginx_listen_port: 80

# Server name (domain)
nginx_server_name: localhost

# Root directory for web files
nginx_root_dir: /var/www/html

# Nginx service name
nginx_service_name: nginx

# Whether to enable the service
nginx_service_enabled: true

# Whether to start the service
nginx_service_started: true
```

## Dependencies

None.

## Example Playbook

```yaml
- hosts: webservers
  become: true
  roles:
    - role: yourusername.nginx
      nginx_listen_port: 8080
      nginx_server_name: "example.com"
      nginx_root_dir: "/var/www/example"
```

## License

MIT

## Author Information

This role was created in 2025 by Pezebuike.