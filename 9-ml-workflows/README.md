# 机器学习工作流示例

这个目录包含了 Argo Workflows 中机器学习相关的示例。

## 文件说明

### hyperparameter-tuning.yaml
这个示例展示了如何构建一个完整的机器学习工作流：

1. 数据预处理
   - 数据加载和清洗
   - 特征工程
   - 数据分割

2. 模型训练
   - 并行训练不同参数组合
   - 超参数优化
   - 模型检查点保存

3. 模型评估
   - 性能指标计算
   - 结果比较
   - 最佳模型选择

## 使用方法

1. 运行超参数调优工作流：
```bash
kubectl create -f hyperparameter-tuning.yaml -n argo
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

1. 确保数据集路径正确
2. 根据实际需求调整超参数范围
3. 监控训练进度和资源使用
4. 保存重要的中间结果 