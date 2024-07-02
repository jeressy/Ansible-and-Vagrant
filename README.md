# Automação Vagrant + Ansible para Criação do Servidor Nginx

Este projeto automatiza a criação e configuração de um servidor Nginx usando Vagrant e Ansible. 👩🏽‍💻

## Pré-requisitos

- [Vagrant](https://www.vagrantup.com/) 
- [VirtualBox](https://www.virtualbox.org/)

## Instruções

1. **Inicialize o Ambiente Vagrant:**
   ```bash
   vagrant up
   ```
   Isso iniciará a VM e configurará o servidor Nginx automaticamente.

2. **Acesso ao Nginx:**
   Após a conclusão do provisionamento, você pode acessar em `http://localhost:8080`.

## Estrutura do Projeto

```plaintext
ansible/
├── html/
│   └── index.html
└── roles/
    └── nginx/
        ├── handlers/
        │   └── main.yml
        ├── tasks/
        │   └── main.yml
        └── templates/
            └── nginx.conf.j2
```

- **html/**: Contém o arquivo `index.html`, que será servido pelo Nginx na porta 8080 do host.
- **roles/nginx/**: Estrutura do papel Ansible para configurar o Nginx.
```
