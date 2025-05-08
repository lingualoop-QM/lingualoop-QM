# LinguaLoop Agent 协作说明

本说明文档用于指导 Agent 协作者在 LinguaLoop 项目中的参与方式、操作规范与演化流程，确保贡献可验证、语义一致、链上存证。

---

## 一、项目定位

LinguaLoop 是一个支持多语言翻译卡片协作的开源系统，Agent 可在其中参与以下角色：

- 内容贡献者：翻译、术语优化、跨语种补充
- 语义锚定者：确认翻译上下文意图与精准性
- 审核协调者：引导多语言版本共识
- 存证守护者：负责 IPFS 验证与链上校对

---

## 二、协作机制

### 1. CLA 协议

- 所有 Agent 需明确接受 CLA v2.0 协议（详见根目录 `CLA_v2.0_Agent.md`）
- 可验证 PDF 封面位于：`CLA_v2.0_Agent_Cover.pdf`
- CLA 说明文件：[`CONTRIBUTION.md`](../CONTRIBUTION.md)

### 2. 内容提交路径

- 所有翻译卡片统一存放在 `cards/` 目录
- 文件命名规范：`lang-[语言代码]/[主题]/[关键词].md`
- 示例：`lang-zh/finance/compound_interest.md`

---

## 三、Agent 工具链建议

- 本地编辑器：推荐 VSCode + Markdown 插件
- 断网运行：可使用 Tauri 或 Electron 本地加载编辑器
- 数据存证：集成 IPFS Desktop 或命令行工具 `ipfs add`
- 版本验证：推荐配合 `hash CID` 校对与 PR 提交截图

---

## 四、常见协作步骤

```mermaid
graph TD
  A[Agent Fork 仓库] --> B[本地创建翻译卡]
  B --> C[生成 CLA 指纹签名]
  C --> D[IPFS 链上存证]
  D --> E[提交 PR 合并至主仓]
