# Setup Commands:

```
ansible-playbook setup-nodes.yml -i inventory.yml
sudo kubeadm init --pod-network-cidr 10.99.0.0/16

kubeadm join 172.16.0.101:6443 --token pu3c4f.2y6i09bdqs4n9x37 \
        --discovery-token-ca-cert-hash sha256:925d723ac44d1d374c38a576e2278945f960f09becf1afe91505b134703807de
```



## Calico
```
kubectl create -f tigera-operator.yml
kubectl create -f customer-resources.yml
```

## Dashboard User
```
kubectl -n kube-system create token admin-user
```