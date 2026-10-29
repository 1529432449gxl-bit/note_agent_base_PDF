# note_agent_base_PDF

将数学教材或讲义 PDF 整理为 Obsidian Markdown 笔记的 Codex skill。它优先参考使用者现有笔记的结构与排版，提取定义、定理、例题、必要的证明与推导，并对公式和扫描页进行核对。

## 使用

1. 将 `note-agent-base-pdf` 文件夹复制到 Codex 的技能目录，例如 Windows 上的 `%USERPROFILE%\.codex\skills\`。
2. 重新打开 Codex，让它发现新技能。
3. 提供 PDF、要处理的范围、输出位置；如需匹配已有风格，还应提供参考笔记目录。
4. 可直接要求：`使用 $note-agent-base-pdf，将这份 PDF 的第一章整理为 Obsidian 笔记，参考我的现有笔记格式。`

技能按章节建立覆盖清单；整章包括习题时可另存题目，默认不添加解答。对有数学内容的图，按需要使用 TikZJax 重画或标记待补。

## 项目结构

- `note-agent-base-pdf/SKILL.md`：主要工作流程。
- `note-agent-base-pdf/references/conventions.md`：笔记、习题与 TikZJax 风格参考。
- `note-agent-base-pdf/agents/openai.yaml`：技能显示信息。

## 已有试验与限制

曾用扫描版数学竞赛教材的第一章试验，覆盖 15 种证明和 26 道习题，并通过交叉检查发现原书中值得注明的条件问题。试验教材与笔记不包含在本项目中。

此技能描述的是工作方法，并非自动保证识别准确的程序。扫描质量、公式和图像可能导致识别错误，AI 应逐页核对并说明无法确认的内容；重要数学结论仍需人工复核。
