# WorkBuddy GitHub MCP 连通性测试

本文件由 WorkBuddy 通过 GitHub 官方远程 MCP（`github-pat`）自动推送，用于验证写入链路是否完整可用。

## 验收清单

| 能力 | 工具 | 状态 |
| --- | --- | --- |
| 创建仓库 | 浏览器新建 | 完成 |
| 创建分支 | `create_branch` | 完成 |
| 推送文件 | `create_or_update_file` | 完成 |
| 创建 Issue | `issue_write` | 完成（#1，已关闭） |
| 创建 Pull Request | `create_pull_request` | 完成（#2） |
| 合并 Pull Request | `merge_pull_request` | 完成（squash） |

**结论：GitHub MCP 读写链路全部验证通过。**

## 连接信息

- 认证方式：Fine-grained Personal Access Token，Bearer 认证
- MCP 端点：`https://api.githubcopilot.com/mcp/`
- 配置位置：`~/.workbuddy/mcp.json`，server 名 `github-pat`，type `streamable-http`
- 说明：本机 `github.com` 连接超时导致官方 OAuth 连接器无法完成授权，改用 PAT 通道绕开授权网页

生成时间：2026-11-12
