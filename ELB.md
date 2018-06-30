# ELB

- no LB for different regions or VPCs

# internet-facing

external DNS names

# internal

internal DNS names

## Sticky sessions

by default no sticky sessions

types:
- duration based session stickiness
  ```
  LB creates the session cookie.
  Instance set in cookie.
  If no cookie - select instance by existing LB algorithm and add cookie
  ```
- app controlled sticky stickinessа
  ```
  LB uses a special cookie to associate the session with the instance, but follows the lifeimte of the app generated cookie
  LB only insert a new stickiness cookie if app response includes a new app cookie. LB cookie does not update with each request. If the app cookie is explicitly removed or expires - session stops being sticky until a new app cookie is issued.
  ```

  ## Pre warming ELBs

contact AWS staff prior to the expected events.