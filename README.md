
This repository contains the OpenShift Templates for the Red Hat 3scale API Management Platform.



 ```
oc new-project anugraha-3scale
oc new-app -f https://raw.githubusercontent.com/adithaha/3scale-amp-openshift-templates/2.6.0.GA.minimal/amp/amp-minimal.yml -p MASTER_PASSWORD=master -p ADMIN_PASSWORD=admin -p WILDCARD_DOMAIN=anugraha-3scale.apps.rhpds311.openshift.opentlc.com

 ```
 
 For multitenancy
 ```
oc create route edge system-provider-user1 --service=system-provider --hostname=user1-admin.anugraha-3scale.apps.rhpds311.openshift.opentlc.com
oc create route edge api-apicast-staging-user1 --service=apicast-staging --hostname=api-user1-apicast-staging.anugraha-3scale.apps.rhpds311.openshift.opentlc.com 
 ```
