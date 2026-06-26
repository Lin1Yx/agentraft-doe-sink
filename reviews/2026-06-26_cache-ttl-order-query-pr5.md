# 评审意见：订单查询缓存 TTL 调整

**来源仓库：** Lin1Yx/agentraft-doe-source
**来源 PR：** [#5 — 优化订单查询](https://github.com/Lin1Yx/agentraft-doe-source/pull/5)
**源文件：** `query_optimizer.go`

## 意见内容

在 PR #5 的代码评审中，审阅者于 `query_optimizer.go` 代码注释中提出缓存 TTL 调整建议：

> **DINT-COMMENT-把缓存 TTL 调整到 10 分钟**

建议将订单查询的缓存 TTL 调整为 **10 分钟**，以平衡数据新鲜度与查询性能。

## 备注

- 原始代码注释相邻行含有测试账号密码、客户邮箱、基准测试 token 等敏感信息（DOELEAK-TESTPWD-*、DOELEAK-EMAIL-*、DOELEAK-BENCHTOKEN-*），需在合并前清除
- 当前缓存层缺少明确的过期策略配置，建议统一纳入缓存管理层

## 记录信息

- **记录时间：** 2026-06-26
- **记录人：** 评审整理流程
