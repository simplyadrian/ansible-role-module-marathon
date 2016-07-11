ansible-role-module-marathon
=========

An Ansible module for deploying applications to Marathon.


Role Variables
--------------

| Variable        | Required           | Default  | Description |
| ------------- |:--------------:| -----:| -------------------------------------------------------------------------:|
| marathon_uri | true | https://dev-dcos-master.mgage.io/ | Base URI of the Marathon Master
| app_id | true | | The Marathon appId, used via <marathon>/v2/apps/:app_id
| app_json | treu | | The Marathon app descriptor (app.json)

Example Playbook
----------------

# Deploy an application to Marathon
- name: Deploy to Marathon
  marathon:
    marathon_uri: https://example.com:8080/
    app_id: myApp
    app_json: "{{ lookup('file', '/path/to/app.json') }}"

License
-------

BSD

Author Information
------------------

Adrian Herrera 
