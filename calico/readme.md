
change
```
- name: IP
  value: "autodetect"
- name: IP_AUTODETECTION_METHOD
  value: "interface=eth.*"   
```
你也可以直接写成
```
- name: IP
  value: "172.25.50.13"  
```  

ip范围
```
- name: CALICO_IPV4POOL_CIDR
  value: "172.25.56.0/22"
```  

关于容忍度问题：
默认容忍度
```
tolerations:
  # Mark the pod as a critical add-on for rescheduling.
  - key: CriticalAddonsOnly
    operator: Exists
  - key: node-role.kubernetes.io/master
    effect: NoSchedule
```
如果在init的时候添加了污点，请自行修改