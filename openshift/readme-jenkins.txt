oc process -f _jenkins-config-0.json -l app=jenkins | oc apply -f - -n minishift-mds-tools
oc process -f _jenkins-config-1.json -l app=jenkins | oc apply -f - -n minishift-mds-tools
oc process -f ./tools/_jenkins.bc.json -l app=jenkins NAME=jenkins VERSION=latest | oc apply -f - -n minishift-mds-tools
oc process -f ./tools/_jenkins.dc.json -l app=jenkins | oc apply -f - -n minishift-mds-tools

