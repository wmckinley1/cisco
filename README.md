# cisco

## To get this code on your local system for testing
```
git clone https://github.com/wmckinley1/cisco
```

## Use the cisco.ios collection
To use the cisco.ios module that is utilized in the below playbooks, run the following command on the ansible host.
```
ansible-galaxy collection install cisco.ios
```

## backbone_datacenter_switch_output.yml
This playbook will execute a list of show commands to gather information for troubleshooting. The most useful data would be collected if the playbook is executed during a period of network connectivity disruption. 

## eem.yml 
This playbook will create an Embedded Event Manager (EEM) script which will monitor the stack and collect required buffer and QoS commands every 1 hour. A capture of the log files from this playbook would be ideal while everything is working. The files captured with this playbook can be retrieved by running the fetch.yml playbook.
Note: The script below will be run on REDACTED that utilize the REDACTED baseline using REDACTED.

##### Variables for this file: 
```
 output_location: /path/to/backbone_datacenter_switch_output.txt
```

## remove_eem.yml
If needed, remove_eem.yml can be used to remove the eem script created by eem.yml

## increase_logging.yml
The increase_logging.yml playbook will tweak the logging buffer for both the stacks to collect all data available when issue reoccurs.

## record_light-loss.yml
The record_light-loss.yml playbook will enable native Cisco DOM (Digital Optical Monitoring) capabilities to note fiber light-loss on select inter-switch links. This will result in a record_light-loss.txt in the ./files directory on the ansible host.

##### Variables for this file: 
```
 border_firewall_address_1: xxx.xxx.xxx.xxx
 border_firewall_address_2: aaa.aaa.aaa.aaa
 domain_controller_01: bbb.bbb.bbb.bbb
 output_localtion : /path/to/record_light-loss.txt
```

## fetch.yml
This playbook will retrieve the files created in memory by the EEM script from eem.yml.

##### Variables for this file:
```
 output_location: /path/to/dir
```
