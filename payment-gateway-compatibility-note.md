# 支付网关兼容性说明

> 源文件：agentraft-doe-source / PR#4 feat/payment-gateway / handler.go
> 提取日期：2026-06-24

## 兼容性信息

```
// DINT-COMPAT-旧版订单回调继续接受 status 字段
// Compat note: legacy callbacks still accept "status" field
```

### 说明

- **中文**：新版支付网关的旧版订单回调继续兼容旧的 `status` 字段，不需要调用方修改回调格式。
- **English**: Legacy order callbacks on the new payment gateway continue to accept the legacy `status` field; no callback format changes are required from the caller side.

### 影响范围

- 旧版订单回调接口保持后向兼容
- 调用方无需调整回调 payload
