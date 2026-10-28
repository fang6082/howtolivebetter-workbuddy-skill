# 高性价比人生指南 · WorkBuddy 技能包

《[高性价比人生指南](https://github.com/eternity4719/HowToLiveBetter)》的 WorkBuddy 技能移植。

把全书 34 节、767 条循证建议完整内嵌进一个 Agent Skill 包，装进 WorkBuddy 后直接问「朋友找我做担保该不该签」「被裁了先做什么」，它会先查书里的条目再回答，注明第几节第几条、成本、收益和证据等级。

## 与官方 skill 的关系

原仓库官方提供了 [Claude Code / Codex 版 skill](https://github.com/eternity4719/HowToLiveBetter/tree/main/skills/life-decision-guide)（运行时联网 clone 正文）。本包是同一思路的 WorkBuddy 移植：

| 差异点 | 官方版 | 本版 | 原因 |
| --- | --- | --- | --- |
| 正文获取 | 运行时 `git clone` | 全书内嵌 `references/book/` | WorkBuddy 技能运行在云端沙箱，不依赖运行时联网 |
| 文件名 | 中文原名 | ASCII 编号（`08.md`） | zip 文件名编码兼容 |
| 指令主体 | — | 基本保留 | 安全门（120/12356 优先）、排序算法、写作纪律逐字保留 |

**正文未做任何改动**：`references/book/`（34 节）与 `references/docs/`（9 篇长文）与原仓库逐字节一致（已 diff 校验）。

## 安装

在 [WorkBuddy 开放平台](https://open.workbuddy.cn/) 技能市场上架后从市场安装（搜索「人生决策按书查」）。

或手动安装：下载本仓库 zip，在 WorkBuddy 开放平台 → 技能 → 新建 → 上传。

## 使用

装好后直接在对话里问，例如：

- 朋友找我做 20 万贷款的担保人，该不该签？
- 我爸 60 岁，抽烟 30 年，现在戒还来得及吗？
- 被公司裁员了，我能拿多少补偿，先做什么？
- 家里的盐要不要换成低钠盐？

## 内容与许可

- 正文：[eternity4719/HowToLiveBetter](https://github.com/eternity4719/HowToLiveBetter)，**CC BY 4.0**，作者 eternity4719。本包按许可要求署名，未修改正文。
- 电子书平台的官方版本由果麦文化独家出品，本包与果麦版无关。
- 原书声明：内容可能过时、可能出错，政策各地执行不一；不替代医生、律师、会计。本包同步继承这一边界。
- 本包的 SKILL.md 指令与打包脚本部分可自由使用。

## 更新

原书更新后同步 `references/book/` 与 `references/docs/` 即可（来源校验与同步方式见 `references/about-source.md`）。
