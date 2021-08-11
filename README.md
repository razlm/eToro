#----------Steps----------<br />
<br />
Created eToro folder<br />
Created eToro repo in git<br />
git init<br />
add raz.pem to the folder<br />
add .gitignore with raz.pem<br />
ssh to vm <br />
change raz.pem chmod 400<br />
az login -i<br />
az aks get-credentials -n devops-interview-aks -g  devops-interview-rg<br />
export KUBECONFIG=~/.kube/config<br />
kubelogin convert-kubeconfig -l msi<br />
kubectl get all<br />
kubectl get namespace<br />
kubectl config set-context --current --namespace=raz<br />
<br />
az acr repository list --name acrinterview.azurecr.io<br />
mkdir ehelm<br />
cd ehelm/<br />
<br />
<br />
sudo cat /var/lib/jenkins/secrets/initialAdminPassword<br />
Enter Jenkins Gui with pass and install it.<br />
etoro:1q@W3e<br />
install plugins(azure & kubernetes)<br />
<br />
mkdir etoro<br />
helm create etoro<br />
edit all files<br />
add ingress<br />
helm install etoro ./etoro<br />
kubectl get all<br />
kubectl describe ingress<br />
<br />
its NodePort and you can do <br />
  export NODE_IP=$(kubectl get nodes --namespace raz -o jsonpath="{.items[0].status.addresses[0].address}")<br />
  echo http://$NODE_IP:$NODE_PORT<br />
  <br />
 to expose it locally<br />
 or change to LoadBalancer and can see it from external IP<br />
<br />
add KEDA file in ./etoro/templates/scale.yaml<br />
<br />
<br />
there is screen shot from the first deployment and GUI checking.<br />
