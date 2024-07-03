# Automação Vagrant + Ansible para criar um servidor Nginx

Este projeto automatiza a criação e configuração de um servidor Nginx usando Vagrant e Ansible. 👩🏽‍💻

## Pré-requisitos

- [Vagrant](https://www.vagrantup.com/) 
- [VirtualBox](https://www.virtualbox.org/)
***
## Instruções

1. **Inicialize o Ambiente Vagrant:**
   Isso iniciará a VM e configurará o servidor Nginx automaticamente.
   ```bash
   vagrant up
   ```

 
3. **Acesso ao Nginx:**
   Após a conclusão do provisionamento, na maquina host, acesse em:
   ```
   http://localhost:8080
   ```
![localhost](https://cdn.discordapp.com/attachments/1082896001339240568/1257782960132984842/Untitled_4.png?ex=6685a92a&is=668457aa&hm=38ca7b3fd54e4995507843d3873ba46b94e294d8f822f3ff1c4da4d252a1414e&)
   
***
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

