# OpsWorks

App mgmt service using chef.

automation:
- scale on time or load
- monitoring
- permissions and policy management

Chef serer stored recipes as well as other config data

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