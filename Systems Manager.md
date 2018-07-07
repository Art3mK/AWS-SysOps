# Systems manager

AWS Systems Manager allows you to centralize operational data from multiple AWS services and automate tasks across your AWS resources. You can create logical groups of resources such as applications, different layers of an application stack, or production versus development environments. With Systems Manager, you can select a resource group and view its recent API activity, resource configuration changes, related notifications, operational alerts, software inventory, and patch compliance status. You can also take action on each resource group depending on your operational needs. Systems Manager provides a central place to view and manage your AWS resources, so you can have complete visibility and control over your operations.

- supports on-premises instances
- AWS Systems Manager offers an agent to perform actions inside instances or servers
- An AWS Systems Manager document enables configuration as code to manage resources at scale. An AWS Systems Manager document defines a series of actions that allows you to remotely manage instances, ensure desired state, and automate operations.
- AWS Systems patch Manager helps you select and deploy operating system and software patches automatically across large groups of Amazon EC2 or on-premises instances
- AWS Systems Manager param store provides a centralized store to manage your configuration data, whether plain-text data such as database strings or secrets such as passwords. This allows you to separate your secrets and configuration data from your code.