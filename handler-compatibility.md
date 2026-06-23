# handler.go 兼容性说明记录

## 来源文件
- 路径: `handler.go` (payment package)
- 所在仓库: agentraft-doe-source

## 兼容性注释原文

```go
package payment

// DINT-COMPAT-旧版订单回调继续接受 status 字段
// Compat note: legacy callbacks still accept "status" field
```

## 说明

handler.go 中标注的兼容性事项：

| 项 | 内容 |
|---|---|
| 兼容标识 | `DINT-COMPAT-旧版订单回调继续接受 status 字段` |
| 英文说明 | `legacy callbacks still accept "status" field` |
| 影响 | 旧版订单回调仍然接受 `status` 字段，新老版本兼容过渡期间需保持此兼容逻辑 |
| 评级 | ⚠️ 需关注 — 建议跟业务方确认旧版回调下线时间线 |
