# ticket-monster-ose-s2i-build

##Overview
A git repository that includes custom assemble script that does binary deployment.
This repository is used as part of the [Ops Workflow for Customizing Builder Images Demo](https://github.com/rhtconsulting/rhc-ose/tree/openshift-enterprise-3/demos/operations-workflow-for-customizing-builder-images)

## Bill of Materials

### Environment Specifications

This code should be run on an installation of OpenShift Enterprise V3

### Template Files

None

### Config Files

`.sti/environment` - Contains the path to the artifact

### External Source Code Repositories

N/A


## Setup and Usage Instructions

For this to run properly the `WAR_FILE_URL` property in the `environment` file should point to the artifact (jar, war) that will be deployed.

Example usage:  
```bash
oc project test-proj && \
oc new-app registry.access.redhat.com/jboss-eap-6/eap-openshift~http://github.com/rhtconsulting/ticket-monster-build.git --name=ticket-monster-build --namespace=test-proj
```
