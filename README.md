# ansibleFest2016sampleSFO
Sample Project files for a presentation given at AnsibleFest 2016 in San Francisco

## Caution: This demo deletes and creates a folder called /tmp/conference
## Caution: This demo deletes and creates a user called conference


## remove existing configuration for demo

```bash
./demo_reset.sh
```

## run the test_ playbook against an inventory (prod for this example)

(test should fail)

```bash
ansible-playbook -i Inventory/GROVER/yyz/prod GROVER_test_proxy.yml
```

## run the maintain_ playbook against an inventory (prod for this example)
(changes confirmed (or) adjusted (idempotent))

```bash
-ansible-playbook -i Inventory/GROVER/yyz/prod GROVER_maintain_proxy.yml -u root
```

## run the test_ playbook against an inventory (prod for this example)
( test should pass (settings confirmed )) (could also be used for governance )

```bash
ansible-playbook -i Inventory/GROVER/yyz/prod GROVER_test_proxy.yml
```


