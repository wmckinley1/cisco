# cisco

## backbone_datacenter_switch_output.yml
This playbook will execute a list of show commands to gather information for troubleshooting. The most useful data would be collected if the playbook is executed during a period of network connectivity disruption. 

## eem.yml 
This playbook will create a Embeded Event Manager (EEM) script which will monitor the stack and collect required buffer and QoS commands every 1 hour.
Note: The script below will be run on ships that utilize the HW1.2 baseline using Catalyst 3850s.

## increase_logging.yml
The increate_logging.yml playbook will tweak the logging buffer for both the stacks to collect all data available when issue re-occurs.

## record_light-loss.yml
The record_light-loss.yml playbook will enable native Cisco DOM (Digital Optical Monitoring) capabilities to note fiber light-loss on select inter-switch links. This will result in a record_light-loss.txt in the ./files directory on the ansible host.


#TODO
identify hosts and inventory file structure
