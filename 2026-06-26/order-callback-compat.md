# 订单回调改动兼容性说明

## 来源

- **源 PR**: Lin1Yx/agentraft-doe-source#4 — 接入新支付网关
- **涉及文件**: `handler.go`

## 兼容性说明

旧版订单回调继续接受 `status` 字段。

```
DINT-COMPAT-旧版订单回调继续接受 status 字段
Compat note: legacy callbacks still accept "status" field
```

## 说明

接入新支付网关后，订单回调接口在新增字段的同时保持对旧版 `status` 字段的向后兼容，确保已接入的旧版客户端在过渡期内无需修改即可正常接收回调通知。
