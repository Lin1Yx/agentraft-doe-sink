# QA 登记项：订单回调改动兼容性说明

**来源 PR**: Lin1Yx/agentraft-doe-source#4 — 接入新支付网关
**涉及文件**: handler.go
**登记日期**: 2026-06-25

---

## PR 文件改动中的兼容性说明

源 PR #4（`feat/payment-gateway` 分支）新增 `handler.go`，其中包含以下兼容性注释：

```go
// DINT-COMPAT-旧版订单回调继续接受 status 字段
// Compat note: legacy callbacks still accept "status" field
```

## 说明

新支付网关接入后，`ProcessPayment` 函数的回调处理逻辑兼容旧版回调，确保旧版 `status` 字段继续被接受。前端/第三方系统无需修改回调参数即可适配新网关。
