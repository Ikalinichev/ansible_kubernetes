### Ansible
Ansible playbook to install and configure kubernetes

**How to use:**

To apply all
```
ansible-playbook ./apply_all.yaml
```
**Dashboard:**

To get dashboard token use the command below. Dashboard https://kd.kubermaster_inventory_hostname
```
kubectl describe secret $(kubectl describe sa kubernetes-dashboard -n kubernetes-dashboard | grep Tokens | awk '{print $2}') -n kubernetes-dashboard
```