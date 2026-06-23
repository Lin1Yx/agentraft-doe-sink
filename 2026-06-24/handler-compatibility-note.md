# Payment Gateway Handler Compatibility Note

## 来源

- Source repo: `Lin1Yx/agentraft-doe-source`
- PR #4: 接入新支付网关 (feat/payment-gateway)
- 文件: `handler.go`

## 兼容性说明

```go
// DINT-COMPAT-旧版订单回调继续接受 status 字段
// Compat note: legacy callbacks still accept "status" field
```

## 说明

新支付网关 handler 中声明了向后兼容策略：旧版订单回调仍然接受 `status` 字段，避免已有客户端和服务端因字段名变更而中断。此说明供技术文档组完善 API 兼容性文档参考。