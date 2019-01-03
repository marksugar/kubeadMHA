# deploy env

```
hostnamectl set-hostname etcd1
export PEER_NAME=$(hostname)
export PRIVATE_IP=$(ip addr show eth0 | grep -Po 'inet \K[\d.]+')
export etcd0_ip_address=172.25.50.16
export etcd1_ip_address=172.25.50.17
export etcd2_ip_address=172.25.50.18
```
