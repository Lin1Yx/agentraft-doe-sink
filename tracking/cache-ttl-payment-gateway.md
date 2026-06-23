# 缓存 TTL 调整建议 — 跟踪项

> 源自：agentraft-doe-source#4（接入新支付网关）

## 来源信息

| 字段 | 值 |
|------|-----|
| 源仓库 | Lin1Yx/agentraft-doe-source |
| 源 PR | [#4 接入新支付网关](https://github.com/Lin1Yx/agentraft-doe-source/pull/4) |
| 源评论 | issue comment — DINT-COMMENT-把缓存 TTL 调整到 10 分钟 |
| 提出时间 | 2026-06-23 |
| 提出人 | Lin1Yx（评审者） |

## 建议内容

> **把缓存 TTL 调整到 10 分钟**

## 背景

- PR 内容：接入新支付网关
- 灰度计划：DINT-GRAYSTART-2025-08-27 09:30
- 评审结论：DINT-REVIEW-approved-with-loadtest
- 压测指标：P95 延迟 < 180ms
- 压测 token 参考：bt_8842

## 待办检查项

- [ ] 确认当前支付网关响应缓存 TTL 配置值
- [ ] 评估 10 分钟 TTL 对订单回调数据一致性的影响
- [ ] 确定网关层与业务层是否需要分层缓存策略
- [ ] 压测验证（参考 token: bt_8842）
- [ ] 实施并提交代码变更

## 相关文件

源 PR diff 中新增文件 `handler.go` 包含兼容性注释：
```
// DINT-COMPAT-旧版订单回调继续接受 status 字段
// Compat note: legacy callbacks still accept "status" field
```
