# Use Ansible to Deploy Projects On-Premise

## Prerequisites

Before running the playbook, you need to create a `.vault_pass` file containing the vault passcode. This allows encrypted sensitive variables to be read and used during execution. Here are the steps:

1. Create a new file named `.vault_pass` in the root directory.

2. In the file, write the following: `vault_passcode {{ vault passcode value }}`. Replace `{{ vault passcode value }}` with the actual passcode value.

## Usage

Run the Ansible playbook to deploy project to the on-premise server:

```shell
ansible-playbook playbook.yaml --extra-vars '{"project":"{{ project name in codes.yaml }}","deploy_environment":"{{ environment, e.g., prod }}","synchronize_user":"{{ user for uploading files }}","synchronize_password":""}'
```