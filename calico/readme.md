
change
```
- name: IP
  value: "autodetect"
- name: IP_AUTODETECTION_METHOD
  value: "interface=eth.*"   
```
��Ҳ����ֱ��д��
```
- name: IP
  value: "172.25.50.13"  
```  

ip��Χ
```
- name: CALICO_IPV4POOL_CIDR
  value: "172.25.56.0/22"
```  

�������̶����⣺
Ĭ�����̶�
```
tolerations:
  # Mark the pod as a critical add-on for rescheduling.
  - key: CriticalAddonsOnly
    operator: Exists
  - key: node-role.kubernetes.io/master
    effect: NoSchedule
```
�����init��ʱ��������۵㣬�������޸�