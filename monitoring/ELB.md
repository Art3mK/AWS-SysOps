# ELB monitoring

- (Un)HealthyHostCount
- RequestCount
- Latency
- HTTPCode_ELB_(4|5)xx codes
- HTTPCode_Backed_xxx codes
- BackendConnectionErrors
- **SurgeQueueLength** -> number of requests that are pending to instances
- **SpilloverCount** -> requests rejected due to the queue being full