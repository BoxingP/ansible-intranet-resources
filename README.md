# Use Ansible to Deploy Projects On-Premise

## Usage

Run the Ansible playbook to deploy project to the on-premise server:

```shell
ansible-playbook playbook.yaml --extra-vars '{"project":"{{ project name in codes.yaml }}","deploy_environment":"{{ environment, e.g., prod }}","synchronize_user":"{{ user for uploading files }}","synchronize_password":""}'
```