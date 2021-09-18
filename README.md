- Create a demo cluster on https://app.getambassador.io/cloud/
- Download the kubeconfig of the Demo Cluster
- Export KUBECONFIG=<location demo cluster kubeconfig> on your local PC
- Remove namespace guestbook as it also has a mapping on / (kubectl delete ns guestbook)
- Create a new namespace (kubectl create ns n8n)
- Apply the yml files in this repo (kubectl apply -n n8n -f <this repos folder>
- Get the IP of the AES Service (kubectl get svc -n ambassador). Get the External IP.
- Go to http(s)://<external IP>/
- You now see the n8n page where the connection seems to be lost continuously:
[Connection Lost](https://github.com/fcrbe/n8n-on-ambassador/blob/master/2021-09-18_10-01.png)
