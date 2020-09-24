# AWS-Launch-Template-windows-template-patch
AWS Launch Template - windows template patch

**Flow:**

1. Create VM from Launch Template
2. Update Windows OS with required patch (Expected WinRM present)
3.	Capture AMI
4. Create Launch Template with latest AMI and set Default version
5.	Stop/Terminate Created VM

**Command:**
```AWS_PROFILE=Profile ansible-playbook awslt.yaml -i localhost, --extra-vars "l_name=LaunchTemplateID r_name=RegionName ver_name=LtVersion profile=Profile"```
