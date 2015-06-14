# ansible-ossec-agent-deploy-ossim
Ansible role to deploy Linux OSSEC agent and connect it to OSSEC server

With this role you can install any number of OSSEC agents on Linux sistem adn connect to OSSEC server.

Role need to be runned from OSSIM server.

## How-to-use ##
* Connecto to OSSIM server with SSH
* Log isntall into console with "Jailbreake system"
* Instll git
```
apt-get install git
```
* Clone this project
```
git clone git@github.com:Trane9991/ansible-ossec-agent-deploy-ossim.git
```

* Write list of your ip's in the *hosts* file under the ```[agent]``` section
```
[agent]
10.10.10.10
10.10.10.11
10.10.10.12
```

* Run playbook with
```
/usr/share/alienvault/api_core/bin/ansible-playbook -i hosts ossec-agent.yml --ask-pass --ask-sudo-pass
```

Hosts will be added like "host-1", "host-2"
