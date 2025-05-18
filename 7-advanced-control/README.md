# Advanced Workflow Control Examples

This directory contains examples of advanced workflow control features in Argo Workflows, specifically designed for machine learning workflows.

## Examples

### 1. Conditionals (`conditionals.yaml`)
Demonstrates conditional execution based on model evaluation results:
- Evaluates a model's accuracy
- Compares accuracy against a threshold
- Conditionally deploys the model based on evaluation results

### 2. Retry Mechanism (`retry.yaml`)
Shows how to handle temporary failures in model training:
- Implements retry strategy for training steps
- Uses exponential backoff
- Handles random failures during training

### 3. Timeout Control (`timeouts.yaml`)
Illustrates time budget control for model training:
- Sets maximum training time
- Saves checkpoints on successful completion
- Handles timeout scenarios

## Usage

1. Conditionals:
```bash
kubectl create -f conditionals.yaml -n argo
```

2. Retry:
```bash
kubectl create -f retry.yaml -n argo
```

3. Timeouts:
```bash
kubectl create -f timeouts.yaml -n argo
```

## Key Features

- **Conditionals**: Use `when` conditions to control workflow paths
- **Retry**: Configure retry strategies with backoff
- **Timeouts**: Set time limits for long-running tasks

## Best Practices

1. Always set appropriate timeouts for long-running tasks
2. Use retry strategies for operations that might fail temporarily
3. Implement proper error handling and logging
4. Use conditionals to create flexible workflow paths 