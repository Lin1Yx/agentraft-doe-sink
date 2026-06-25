# 回归测试 — 订单回调改动兼容性说明

## 来源 PR

- **仓库**: Lin1Yx/agentraft-doe-source
- **PR #4**: 接入新支付网关 DINT-PR-接入新支付网关
- **分支**: feat/payment-gateway
- **涉及文件**: `handler.go`

## handler.go 中订单回调兼容性说明

```go
// DINT-COMPAT-旧版订单回调继续接受 status 字段
// Compat note: legacy callbacks still accept "status" field
```

### 兼容性解读

1. **旧版订单回调查询 `status` 字段**：新支付网关接入后，`handler.go` 中的 `ProcessPayment` 处理逻辑确保**旧版订单回调仍然兼容接受 `status` 字段**。即老调用方无需修改回调参数，新老格式均可正常工作。

2. **向后兼容**：不要求旧客户端更新请求格式，`status` 字段在旧版回调中继续被解析和处理。

3. **回归测试要点**：
   - 验证旧格式回调（带 `status` 字段）仍能被正确接受和处理
   - 验证新格式回调（可能使用新字段名）也能正常路由
   - 确认无回归性报错
