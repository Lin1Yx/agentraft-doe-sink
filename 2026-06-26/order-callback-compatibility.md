# 订单回调改动兼容性说明

## 来源

PR #4（feat/payment-gateway，接入新支付网关）— `handler.go`

## 兼容性说明

**DINT-COMPAT-旧版订单回调继续接受 status 字段**

```go
// Compat note: legacy callbacks still accept "status" field
```

### 说明

- 新支付网关接入后，订单回调接口保持对旧版 `status` 字段的兼容
- 旧版客户端继续发送 `status` 字段时，服务端仍能正确解析和处理
- 不破坏现有回调流程，确保平滑迁移

## 文件改动列表

| 文件 | 变更 |
|------|------|
| `handler.go` | 新增 — 支付处理入口，含兼容性注释 |
