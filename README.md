### Ansible
Ansible playbook to install and configure kubernetes

**How to use:**
To apply all
```
ansible-playbook ./apply_all.yaml
```
**Dashboard:**
To get dashboard token apply on master the command below and visit https://ks.vm2.e-taxes.gov.az
```
kubectl describe secret $(kubectl describe sa kubernetes-dashboard -n kubernetes-dashboard | grep Tokens | awk '{print $2}') -n kubernetes-dashboard
```