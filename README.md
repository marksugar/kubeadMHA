## kubeadMHA

![img](https://raw.githubusercontent.com/marksugar/kubeadMHA/master/img/k8sga.png)


curl -Lk https://raw.githubusercontent.com/marksugar/kubeadMHA/master/systeminit/profile -o /etc/profile

修改主机名

curl -Lk https://raw.githubusercontent.com/marksugar/kubeadMHA/master/systeminit/chenage_hostname|bash

修改初始参数

curl -Lk https://raw.githubusercontent.com/marksugar/kubeadMHA/master/systeminit/ip_vs_a_init|bash

## haproxy
如果你需要安装haproxy，也可以使用install haproxy
```
    curl -Lk https://raw.githubusercontent.com/marksugar/Maops/master/haproxy/scripts/install.sh|bash
```
而后你需要编辑/etc/haproxy/haproxy.cfg中的配置文件
## keepalived

- install keepalived
```
 bash <(curl -s  https://raw.githubusercontent.com/marksugar/lvs/master/keepliaved/install.sh|more)
```

如下：

输入Master或者BACKUP和VIP

```
[root@master-0 ~]# bash <(curl -s  https://raw.githubusercontent.com/marksugar/lvs/master/keepliaved/install.sh|more)
You install role MASTER/BACKUP ?
         please enter(block letter):MASTER
Please enter the use VIP: 172.25.50.15
```