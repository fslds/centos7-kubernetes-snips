###
##
`sudo yum update`

`sudo yum install libvirt-daemon-kvm qemu-kvm`

`sudo yum install kubectl wget` 

`wget https://github.com/kubernetes/minikube/releases/download/v1.2.0/minikube-1.2.0.rpm`

```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/docker-machine-driver-kvm2 \
  && sudo install docker-machine-driver-kvm2 /usr/local/bin/
```
  
`sudo rpm -i minikube-1.2.0.rpm` 

```bash
sudo systemctl enable libvirtd.service
sudo systemctl start libvirtd.service
sudo systemctl status libvirtd.service
```
`sudo usermod -a -G libvirt $(whoami)`
`newgrp libvirt`

`minikube config set vm-driver kvm2`
`minikube start`

