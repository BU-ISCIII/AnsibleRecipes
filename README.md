# AnsibleRecipes
Each folder contains ansible playbook and all requiered scripts to deploy some of our machines.

## How to use these
Clone the repo to your machine

```git clone https://github.com/BU-ISCIII/AnsibleRecipes.git```

and **cd into the folder of the machine you want to replicate**. Each folder has at least one inventory file (hosts) and playbook (playbook.yml), and usually a requirements file too (requirements.yml).

## Inventory
Here you can modify which machine you want to modify with the playbook. By default, most of these scripts point to localhost. One IP address can be specified per line.

## Requirements
Ansible rules to download from ansible-galaxy repo. It needs to be executed prior running the playbook:

```ansible-galaxy install -p roles -r requirements.yml```

## Playbook
Once you have reviewed the code and adapt the variables to your machine, you are ready to deploy:

```ansible-playbook playbook.yml```
