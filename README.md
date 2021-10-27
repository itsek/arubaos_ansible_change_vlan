# arubaos_ansible_change_vlan

requirements: Ansible with installed ArubaOS_Switch components https://galaxy.ansible.com/arubanetworks/aos_switch

This Playbook changes all ports given in the "ports_to_loop" list from one VLAN-ID to some other VLAN-ID (set in vars: "oldval" and "newvlan"

An Example:
You have HP Aruba (previously procurve) Switch with the set VLANs:  
Port1 - VLAN 300 tagged  
Port2 - VLAN 300 untagged  
Port3 - VLAN 1 untagged  
(..)  
  
after the playbook is complete, the Ports look like this:  
Port1 - VLAN 400 tagged  
Port2 - VLAN 400 untagged  
Port3 - VLAN 1 untagged  
(..)  

Please note that if the newvlan ist not created, you have to create it first in the play, this skript shows only the change part
