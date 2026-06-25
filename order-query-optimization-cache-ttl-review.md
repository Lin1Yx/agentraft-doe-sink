# 缓存 TTL 评审建议

**来源**: PR #5 (优化订单查询 DINT-PRLIST-优化订单查询) - feat/optimize-order-query

**源文件**: `query_optimizer.go` 代码注释

**评审意见**:

> DINT-COMMENT-把缓存 TTL 调整到 10 分钟

**说明**: 建议将订单查询缓存 TTL 从当前值调整为 10 分钟，以平衡数据新鲜度与查询性能。
