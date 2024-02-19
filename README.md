oc create -f demo-pipeline.yml && oc process pipeline-example -p NAMESPACE=$(oc project -q) -o yaml > pipeline.yml && oc apply -f pipeline.yml
oc delete template/pipeline-example && oc delete -f pipeline.yml && oc delete pipelineruns.tekton.dev --all
