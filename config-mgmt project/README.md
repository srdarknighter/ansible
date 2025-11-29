1. First we go to aws IAM service to create a user and give full ec2 access
2. Under security create the access key, secret access key
3. Create a vault to store the keys
4. openssl rand -base64 2048 > vault.pass    # creates a password for the vault
5. ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass #enter details in the vault
6. create a key in aws and use the .pem file
7. use ssh-copy-id to setup password less auth