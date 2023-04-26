# Fetch and mail pull request details

This repository contains ansible playbook to fetch the list of PRs for a given repository using API and process the data into human readable form which is then sent to any configured mail id  

#### Usage:
* Configured variable values can be found at **deploy/roles/mailPRDetails/defaults/main.yml**
* Playbook steps can be found at **deploy/roles/mailPRDetails/tasks/main.yml**
* Run the below command from inside deploy folder of the codebase  
 **sudo ansible-playbook site.yml --vault-password-file vpass**
* If there is a need to override configuration at runtime then use below command as reference  
**sudo ansible-playbook site.yml --vault-password-file vpass -e numberOfDaysToConsider=<for ex 10> -e repo=<Name of the repo>**