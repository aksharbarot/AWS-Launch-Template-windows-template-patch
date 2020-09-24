# AWS-Launch-Template-windows-template-patch
AWS Launch Template - windows template patch

Flow:
•	Create VM from Launch Template
•	Update Windows OS with required patch (Expected WinRM present)
•	Capture AMI
•	Create Launch Template with latest AMI and set Default version
•	Stop/Terminate Created VM

Command:
```AWS_PROFILE=svc_virtualizationAdm ansible-playbook launch.yaml -i localhost, --extra-vars "l_name=LaunchTemplateID r_name=RegionName ver_name=LtVersion profile=svc_virtualizationAdm"```
