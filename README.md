# ansibleFest2016sampleSFO
Sample Project files for a presentation given at AnsibleFest 2016 in San Francisco

## Caution: This demo deletes and creates a folder called /tmp/conference
## Caution: This demo deletes and creates a user called conference


## remove existing configuration for demo

<pre>
./demo_reset.sh
</pre>

## run the test_ playbook against an inventory (prod for this example)

(test should fail)

<pre>
ansible-playbook -i Inventory/GROVER/yyz/prod GROVER_test_proxy.yml
</pre>

## run the maintain_ playbook against an inventory (prod for this example)
(changes confirmed (or) adjusted (idempotent))

<pre>
-ansible-playbook -i Inventory/GROVER/yyz/prod GROVER_maintain_proxy.yml -u root
</pre>

## run the test_ playbook against an inventory (prod for this example)
( test should pass (settings confirmed - governance ))

<pre>
ansible-playbook -i Inventory/GROVER/yyz/prod GROVER_test_proxy.yml
</pre>


