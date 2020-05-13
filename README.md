# myansibleserver
An ansible server with playbooks to launch a linux and windows node. This can be used for testing purposes and then terminated later.

# prerequisites
Make sure you have completed `aws configure` in the system where you are going to use the below playbooks.

# playbooks
## setup-win-linux-nodes-on-aws.yml  
This playbook launches a windows and linux node on aws. It will then update the hosts file with the ip addresses. It will also update the group_var/terminate.yml file with the instance ids, so that it can be later used by the playbook below to terminate them after use.

## terminate-instances.yml
This playbook terminates the instance created above. It picks up the instance ids to terminate from group_vars/terminate.yml.
