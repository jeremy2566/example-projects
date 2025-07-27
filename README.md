# 示例项目 - 测试一键部署

这是一个用于测试GitHub触发一键部署的示例项目。

## 项目结构
```
example-project/
├── .github/
│   └── workflows/
│       └── deploy.yml        # GitHub Actions部署工作流
├── services/
│   ├── api-gateway/         # API网关服务
│   ├── user-service/        # 用户服务
│   └── order-service/       # 订单服务
└── README.md
```

## 使用步骤

1. Fork或复制此项目到您的GitHub仓库
2. 配置GitHub Secrets（见下方）
3. 推送代码到feature分支
4. 查看GitHub Actions自动部署

## 需要配置的GitHub Secrets

在仓库Settings > Secrets and variables > Actions中添加：

- `KUBECONFIG`: Base64编码的kubeconfig
- `ENV_ALLOCATOR_URL`: http://env-allocator.zadig-deploy-system.svc.cluster.local
- `AWS_REGION`: ap-southeast-1
- `REGISTRY`: 您的ECR地址（可选）