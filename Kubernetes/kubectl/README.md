# Linux bash kubectl completion
```sh
# Install bash-completion (if missing)
sudo apt-get install bash-completion
source /usr/share/bash-completion/bash_completion
# Enable kubectl completion
echo $'source <(kubectl completion bash)\nalias k=kubectl\ncomplete -o default -F __start_kubectl k' >>~/.bashrc
source ~/.bashrc
```


# Run k8s network-utils pod 
```sh
kubectl run -ti --rm --image amouat/network-utils test bash 
```


# Delete pods which contains 'app' in the name
```sh
k get pods | grep app- | awk '{print $1}' | xargs kubectl delete pod
```


# kubeadm certs renewal
```sh
# Get current k8s certs status
sudo kubeadm certs check-expiration
# Renew all
sudo kubeadm certs renew all
# Update kube config
sudo cp -f /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
# Restart kube-system component to apply certs
kubectl -n kube-system get pods | grep 'kube-apiserver\|kube-controller-manager\|kube-scheduler\|etcd' | awk '{print $1}' | xargs kubectl -n kube-system delete pod
# Manually copy new tokens from kube config
cat ~/.kube/config 
```
