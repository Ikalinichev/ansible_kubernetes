#To install kubernetes, join nodes, install ingress and dashboard, add default storage class, install nfs-server and install helm pls apply
ansible-playbook ./apply_all.yaml
#To get dashboard token apply on master the command below and visit https://ks.vm2.e-taxes.gov.az
kubectl describe secret $(kubectl describe sa kubernetes-dashboard -n kubernetes-dashboard | grep Tokens | awk '{print $2}') -n kubernetes-dashboard