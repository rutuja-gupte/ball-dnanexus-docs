# Cloud Computing Guides

Rutuja Gupte

This is meant to be a quickstart guide to setting up anything on DNAnexus. I will essentially keep my WSL logs here.

Start a new job
```
dx run app-cloud_workstation --ssh --instance-type azure:mem3_ssd1_x16
```
Then set the timeout and any other options if needed. And wait for it to find a machine.  

Change the dx path to the working directory.
 
```
unset DX_WORKSPACE_ID
dx cd $DX_PROJECT_CONTEXT_ID:
``` 

To check or change timeout
```
dx-get-timeout
dx-set-timeout 1d
```
