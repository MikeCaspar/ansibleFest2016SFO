# ansibleFest2016sampleSFO
Sample Project files for a presentation given at AnsibleFest 2016 in San Francisco

Important Note
--------------
**Since the creation of this sample, a project has been started using a more roles based approach to each test.**

**This can be found at [https://galaxy.ansible.com/MikeCaspar/playbook_test_framework/](https://galaxy.ansible.com/MikeCaspar/playbook_test_framework/)** 

**This demo has the tasks included within the playbook itself (which can work well to initially learn).** 

**If you find the approach useful, consider starting with a combination of this type of playbook in combination with test roles (or create and share _test roles of your own to benefit from. Please use the design guidelines provided when doing so and I will work to add your _test roles to the core test framework.**


See [LICENCE](LICENSE) for restrictions if any

**Caution:** This demo deletes and creates a folder called /tmp/conference

**Caution:** This demo deletes and creates a user called conference

**Session description:**

Mike Caspar recently completed a learning deep dive with a team learning Ansible for a large scale incremental infrastructure upgrade. Sharing basics about Ansible's Inventory and Groups features he will break down some of the technical barriers between development and infrastructure by introducing infrastructure as code concepts along with incremental delivery ideas.

## Comments from Mike:
- A starting pattern for migration. It is expected that as you learn more, you will replace cities and environments with Dynamic versions of the inventories. This approach allows a combination of physically maintained and dynamic inventories.
- It is likely that some day in the future, you may regroup differently. This is a starting approach.
- To move a machine from any environment to another, simply move it from one inventory to another and re-run maintain. This will also work with dynamic inventory where machines have simply "moved" with an approach appropriate to your environment.
- Audio for the presentation provided by Ansible URL TBD

## Slides available at:
http://www.slideshare.net/MikeCaspar/testing-for-infrastructure-as-code-for-ansiblefest-2016-64540514

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
ansible-playbook -i Inventory/GROVER/yyz/prod GROVER_maintain_proxy.yml -u root
```

## run the test_ playbook against an inventory (prod for this example)
( test should pass (settings confirmed )) (could also be used for governance )

```bash
ansible-playbook -i Inventory/GROVER/yyz/prod GROVER_test_proxy.yml
```


