# 资源管理示例

这个目录包含了 Argo Workflows 中资源管理的示例。

## 文件说明

### resource-limits.yaml
这个示例展示了如何在 Argo Workflow 中管理资源限制：

1. GPU 资源管理
   - 请求 GPU 资源
   - 监控 GPU 使用情况
   - 指定 GPU 节点

2. 内存和 CPU 限制
   - 设置内存限制
   - 设置 CPU 限制
   - 设置资源请求

3. 节点选择
   - 使用 nodeSelector 指定特定节点
   - 指定硬件要求

## 使用方法

1. 运行资源限制示例：
```bash
kubectl create -f resource-limits.yaml -n argo
```

2. 查看工作流状态：
```bash
kubectl get workflows -n argo
```

3. 查看详细日志：
```bash
kubectl logs -n argo <pod-name>
```

## 注意事项

1. 确保集群中有足够的资源
2. 根据实际需求调整资源限制
3. 确保节点标签正确配置
4. 监控资源使用情况 