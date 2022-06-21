# cisco

## backbone_datacenter_switch_output.yml
This playbook will execute a list of show commands to gather information for troubleshooting. The most useful data would be collected if the playbook is executed during a period of network connectivity disruption. 

## eem.yml 
This playbook will create an Embedded Event Manager (EEM) script which will monitor the stack and collect required buffer and QoS commands every 1 hour. A capture of the log files from this playbook would be ideal while everything is working. The files captured with this playbook can be retrieved by running the fetch.yml playbook.
Note: The script below will be run on ships that utilize the HW1.2 baseline using Catalyst 3850s.

## remove_eem.yml
If needed, remove_eem.yml can be used to remove the eem script created by eem.yml

## increase_logging.yml
The increate_logging.yml playbook will tweak the logging buffer for both the stacks to collect all data available when issue reoccurs.

## record_light-loss.yml
The record_light-loss.yml playbook will enable native Cisco DOM (Digital Optical Monitoring) capabilities to note fiber light-loss on select inter-switch links. This will result in a record_light-loss.txt in the ./files directory on the ansible host.
