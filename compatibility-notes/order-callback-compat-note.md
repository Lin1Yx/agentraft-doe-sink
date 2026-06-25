# 订单回调兼容性说明

> **来源**: PR #4（接入新支付网关）— `handler.go`
> **标签**: `DINT-COMPAT`

## 兼容性说明

旧版订单回调继续接受 `status` 字段，确保向后兼容。

```
DINT-COMPAT-旧版订单回调继续接受 status 字段
Compat note: legacy callbacks still accept "status" field
```

## 说明

新支付网关上线后，回调接口仍保留对旧版 `status` 字段的兼容处理，
已接入的旧版回调请求不会因字段变更而中断。
