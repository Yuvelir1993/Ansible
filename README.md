# General
Ansible repo.
# Resources
## AWS
[amazon.aws.aws_ec2 inventory](https://docs.ansible.com/ansible/latest/collections/amazon/aws/aws_ec2_inventory.html)\
[Ansible AWS EC2 Dynamic Inventory Plugin](https://dev.to/vumdao/ansible-aws-ec2-dynamic-inventory-plugin-3bme)\
[Using Ansible Dynamic Inventory to Provision EC2-Instance & Configure Apache Webserver with Handler support!](https://harshitdawar.medium.com/leveraging-the-power-of-the-ansible-dynamic-inventory-to-provision-ec2-instance-configure-apache-664a3e16a7c1)

# Commands
## Hints
Use `--check` for validation.
Use `--step` flag to execute with prompts.
Use `--tags <tag>` to execute only tagged.
Use `-e <variable>` to pass variable value.
Use `--ask-become-pass` to explicitly provide sudo password when `become: true`.

## Play playbook
Do not use `sudo` since `become: true` automatically elevates needed permissions.
`ansible-playbook ./playbooks/install_python_ec2_amazon_linux.yml -i ./inventory/ec2.yml`

## List inventories
Will call AWS API to return available hosts.
`ansible-inventory -i ./inventory/all_ec2.aws_ec2.yml --list`