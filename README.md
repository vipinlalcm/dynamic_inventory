Introuduction
=======
    
    This is a sample playbook with Dynamic inventory list in ansible. Which reads the group and host variables from inventory.yml and generate ansible compatible inventory config file.
It fetchs "itek" password from siptrack and creates host variables with itek user and its password.

Description
============
    
    In this very simple ansible playbook, we are simply installing some packages in all monitorscout staging servers.

How to run
===========
Note: You should go to staging directory to run it, because inventory_generate.py script reads the host input file from the same directory.

- If you need to install in all hosts at a time. Use the below syntaxs
  
    #ansible-playbook install.yml -i inventory_generate.py

- If you need to limit the installation with spesific hosts, use the below syntax
  
    #ansible-playbook install.yml -i inventory_generate.py -l staging-p1.p.monitorscout.com

- If you wanted to limit the installation with spesifc groups, use the below syntax
  
    #ansible-playbook install.yml -i inventory_generate.py -l Staging_Delegators
