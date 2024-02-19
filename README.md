https://github.com/FlorentQuad/test-webhook/blob/main/index.php
https://demo-tuesday-meijerflorent-dev.apps.sandbox-m2.ll9k.p1.openshiftapps.com
https://docs.google.com/presentation/d/1hFy3LrcYr7NgelNjM-6sEJ0_7_bxK1eugez_aBSzqgg/edit#slide=id.p

oc create -f demo-pipeline.yml && oc process pipeline-example -p NAMESPACE=$(oc project -q) -o yaml > pipeline.yml && oc apply -f pipeline.yml
oc delete template/pipeline-example && oc delete -f pipeline.yml && oc delete pipelineruns.tekton.dev --all