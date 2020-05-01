---
bookCollapseSection: false
weight: 26
---

# Environment Overrides


![Environment Overrides](./envoverride.JPG  "Environment Overrides")


You can customize the Deployment template in Environment overrides section to customize things according to different environments.


For Example, You may have specified 100m CPU resource in the Deployment Template but in Production environment override you would want to have 500m CPU resource as the traffic on Pod will be higher.
These are not added in the templates,it makes a copy of the template and lets you customize it and then save it.
And now this overriden template will always  be used instead of the one specified in deployment template.

