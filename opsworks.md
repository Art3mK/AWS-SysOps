# OpsWorks

App mgmt service using chef.

automation:
- scale on time or load
- monitoring
- permissions and policy management

Chef server stores recipes as well as other config data

Client is installed on each server, VM, container, or networking device (nodes). Client polls server for latest policies.

OpsWorks - GUI to deploy/configure infra.

- Stacks
  ```
  Container of resources, ELBs, EC2, RDS
  ```
- Layers
  ```
  Layer exists within a stack and consists of things like a web app layer, app processing layer or database layer
  Create layer -> opsworks takes care of provisioning/configuring resources
  ```

  - 1 or more layers in the stack
  - instance must be assigned to a least 1 layer
  - which chef layers run, are determined by the layer the instance belongs to
  - preconfigured layers include:
    - Apps
    - DBs
    - ELBs
    - Caching
  - multiple apps per stack and per layer

Instance types:
- 24/7 instances
- time based instances
- load based instances

## Lifecycle events

- Setup
- Configure
- Deploy
- Undeploy
- Shutdown

##  Steps followed when provisioning an RDS instance

the layer can represent only existing RDS instances.

- create RDS instance
- register RDS with the stack
- attach layer to an app, which adds RDS instance's connection information to the app's deploy attributes
- use info from deploy attributes to connect app to the RDS instance

### To register RDS instances with a stack

- In the AWS OpsWorks Stacks console, click Layer in the navigation pane, click + Layer or Add a layer to open the Add Layer page, and then click the RDS tab.
- If necessary, update the stack's service role, as described in Updating the Stack's Service Role.
- Click the RDS tab to list the available Amazon RDS instances.
- Select the appropriate instance, set User and Password to the appropriate user and password values and click Register to Stack.

If you change a registered Amazon RDS instance's password, you must manually update the password in AWS OpsWorks Stacks and then redeploy your apps to update the stack configuration and deployment attributes on the stack's instances.