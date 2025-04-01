
# 🚀 Ansible Role - Instalación y configuración de GitLab CE

Este role instala y configura GitLab Community Edition (CE) en Oracle Linux 9, con SSL autofirmado, integración LDAP y registro de GitLab Runner.

## 🎯 Características

- Instalación GitLab CE (Omnibus)
- Configuración HTTPS con certificado autofirmado
- Integración con LDAP
- Instalación y registro de GitLab Runner

## 📂 Estructura

```
roles/
└── gitlab/
    ├── defaults/
    ├── vars/
    ├── tasks/
    └── README.md
```

## 🔧 Variables

Variables configurables en `defaults/main.yml`.

### General
- `gitlab_external_url`
- `gitlab_ssl_cert_dir`
- `gitlab_ssl_cert`
- `gitlab_ssl_key`

### LDAP
- `gitlab_ldap_enabled`
- `gitlab_ldap_host`
- `gitlab_ldap_port`
- `gitlab_ldap_uid`
- `gitlab_ldap_bind_dn`
- `gitlab_ldap_password`
- `gitlab_ldap_base`

### Runner
- `gitlab_runner_enabled`
- `gitlab_runner_registration_token`
- `gitlab_runner_executor`
- `gitlab_runner_tags`
- `gitlab_runner_description`

## 🚀 Uso

1. Edita tu inventario:

```
[gitlab_server]
192.168.1.50 ansible_user=oracle ansible_ssh_private_key_file=~/.ssh/id_rsa
```

2. Edita las variables en `defaults/main.yml`.

3. Ejecuta:

```bash
ansible-playbook -i inventory playbook.yml
```

---

**Requisitos:** Ansible >= 2.9

**Licencia:** MIT
