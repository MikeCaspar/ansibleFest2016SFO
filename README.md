# ansibleFest2016sampleSFO
Sample Project files for a presentation given at AnsibleFest 2016 in San Francisco


To prepare for demo

- run script demo_reset.sh
- ansible-playbook -i Inventory/GROVER/yyz/prod GROVER_test_proxy.yml 
- ansible-playbook -i Inventory/GROVER/yyz/prod GROVER_maintain_proxy.yml -u root
