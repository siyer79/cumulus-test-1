# cumulus-test-1

This ansible and vagrant demo will create 2 switches and 2 servers (running cumulus-vx).  
It will configure bgp on all the machines such that the switches are on the same subnet as the servers and has 2 default routes from the server to the switches.

Put the wd-playbook.yml in the ./playbook directory and all the *.conf files in the playbook directory as well.

