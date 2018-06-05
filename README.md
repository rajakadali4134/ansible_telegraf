Role Name
=========

Setting up of telegraf agent using Ansible.

Requirements
------------

This is just a role for setting up the agent. This doesnot install the influxdb server. Make sure that your influxdb server is already setup.

Role Variables
--------------

Make sure that influxdb variables like influxdb_url,influxdb_database and influxdb_retention are set in the vars/main.yml
Also set the influxdb_user,influxdb_password in a different yaml file using ansible-vault .

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      remote_user: ansible_user
  roles:
    - ../telegraf


You can run using the following command.

ansible-playbook -i tests/inventory  -e @telegraf_auth.yml --ask-vault-pass tests/test.yml  -v
