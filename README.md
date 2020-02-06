# loumaris.firewall

Setting up the ufw firewall in a cluster env with:
* open ssh port
* free firewall traffic between the hosts


## usage

Example: allow port 80 and 443

```yaml
- name: apply common configuration to all nodes
  hosts: all
  roles:
    - { role: loumaris.firewall, firewall_rules: [ { rule: 'allow', port: 80 }, { rule: 'allow', port: 443 } ] }
```
