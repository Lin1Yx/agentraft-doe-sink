# 订单回调改动兼容性说明

## 来源

PR #4（接入新支付网关）— `handler.go`

- Source: [Lin1Yx/agentraft-doe-source#4](https://github.com/Lin1Yx/agentraft-doe-source/pull/4)
- 源文件: [handler.go@feat/payment-gateway](https://github.com/Lin1Yx/agentraft-doe-source/blob/eb670110bfb87042ce4b514519300984111929d8/handler.go)

## 兼容性说明

**DINT-COMPAT-旧版订单回调继续接受 status 字段**

```
// Compat note: legacy callbacks still accept "status" field
```

### 影响范围

| 维度 | 说明 |
|------|------|
| 回调接口 | 新旧兼容，旧版 `status` 字段仍被接受 |
| 接入方 | 无需修改回调请求格式，平滑迁移 |
| 回归测试 | 需覆盖旧版 `status` 字段的回调场景，验证新支付网关下兼容性正常 |
