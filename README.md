oc create secret docker-registry regcred --docker-server=https://registry.piensoluegoinstalo.com:5000 --docker-username=akaronte --docker-password=mondariz10 --docker-email=akaronte@hotmail.com -n  appjava 


oc secrets link serviceaccount/default regcred --for=pull,mount -n myappjava 

oc secrets link serviceaccount/otel regcred --for=pull,mount -n myappjava 

oc secrets link serviceaccount/java-lb regcred --for=pull,mount -n myappjava 