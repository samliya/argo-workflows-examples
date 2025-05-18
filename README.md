# Argo Workflows Examples

这个仓库包含了 Argo Workflows 的实用示例集合，涵盖了从基础到高级的各种使用场景和最佳实践。

## 目录结构

### 0-kind
- 使用 Kind 创建本地 Kubernetes 集群的配置
- 包含单节点和多节点集群配置示例

### 1-helloworld
- 最基础的 Argo Workflow 示例
- 包含简单的参数传递示例
- 适合入门学习

### 2-steps
- 展示 Argo Workflow 的步骤（Steps）功能
- 包含单步骤和多步骤示例
- 演示步骤间的数据传递

### 3-dag
- 展示有向无环图（DAG）工作流
- 演示任务间的依赖关系
- 并行任务执行示例

### 4-artifact
- 展示 Argo Workflow 中的制品（Artifact）管理
- 包含多源制品示例
- 演示制品的生成和使用

### 5-pvc
- 展示持久卷声明（PVC）的使用
- 包含 PVC 与制品结合使用的示例
- 演示数据持久化方案

### 6-loop
- 展示工作流中的循环功能
- 包含序列循环示例
- 演示批量任务处理

### 7-advanced-control
- 高级工作流控制功能
- 包含条件执行、重试机制和超时控制
- 演示错误处理和流程控制

### 8-resource-management
- 资源管理示例
- 包含 GPU、内存和 CPU 资源限制
- 演示节点选择和资源分配

### 9-ml-workflows
- 机器学习工作流示例
- 包含模型训练、超参数调优
- 演示完整的 ML 流水线

## 使用方法

1. 克隆仓库：
```bash
git clone https://github.com/yourusername/argo-workflows-examples.git
cd argo-workflows-examples
```

2. 安装 Argo Workflows：
```bash
kubectl create namespace argo
kubectl apply -n argo -f https://github.com/argoproj/argo-workflows/releases/download/v3.4.0/install.yaml
```

3. 运行示例：
```bash
# 运行 Hello World 示例
kubectl create -f 1-helloworld/hello.yaml -n argo

# 运行带参数的示例
kubectl create -f 1-helloworld/parameter.yaml -n argo
```

## 最佳实践

1. 资源管理
   - 合理设置资源限制
   - 使用节点选择器
   - 监控资源使用情况

2. 错误处理
   - 实现重试机制
   - 设置超时控制
   - 使用条件执行

3. 数据管理
   - 使用制品存储中间结果
   - 合理使用 PVC
   - 实现数据清理

4. 工作流设计
   - 模块化设计
   - 参数化配置
   - 清晰的依赖关系

## 注意事项

1. 确保 Kubernetes 集群已正确配置
2. 检查 Argo Workflows 版本兼容性
3. 根据实际需求调整资源配置
4. 注意数据安全和持久化
5. 监控工作流执行状态

## 贡献指南

欢迎提交 Pull Request 来改进这些示例。在提交之前，请确保：

1. 代码符合最佳实践
2. 包含必要的文档
3. 添加适当的注释
4. 更新相关测试

## 许可证

MIT License
