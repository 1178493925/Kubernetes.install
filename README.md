### 常见错误
1、 创建coredns时pod持续创建中，无法完成。（排除网络问题）
解决：
```
kubectl create clusterrolebinding kubelet-node-clusterbinding --clusterrole=system:node --group=system:nodes
```

```
kubectl describe clusterrolebindings kubelet-node-clusterbinding
Name:         kubelet-node-clusterbinding
Labels:       <none>
Annotations:  <none>
Role:
  Kind:  ClusterRole
  Name:  system:node
Subjects:
  Kind   Name          Namespace
  ----   ----          ---------
  Group  system:nodes
  
  ```
