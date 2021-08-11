#----------Steps----------

Created eToro folder
Created eToro repo in git
git init
add raz.pem to the folder
add .gitignore with raz.pem
ssh to vm 
change raz.pem chmod 400
az login -i
az aks get-credentials -n devops-interview-aks -g  devops-interview-rg
export KUBECONFIG=~/.kube/config
kubelogin convert-kubeconfig -l msi
kubectl get all
kubectl get namespace
kubectl config set-context --current --namespace=raz

az acr repository list --name acrinterview.azurecr.io
mkdir ehelm
cd ehelm/


sudo cat /var/lib/jenkins/secrets/initialAdminPassword
Enter Jenkins Gui with pass and install it.
etoro:1q@W3e
install plugins(azure & kubernetes)

mkdir etoro
helm create etoro
edit all files
add ingress
helm install etoro ./etoro
kubectl get all
kubectl describe ingress

its NodePort and you can do 
  export NODE_IP=$(kubectl get nodes --namespace raz -o jsonpath="{.items[0].status.addresses[0].address}")
  echo http://$NODE_IP:$NODE_PORT
  
 to expose it locally
 or change to LoadBalancer and can see it from external IP

add KEDA file in ./etoro/templates/scale.yaml


there is screen shot from the first deployment and GUI checking.
