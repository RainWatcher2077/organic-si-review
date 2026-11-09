# Organic SI Review · 有机化学 SI 审阅

`organic-si-review` 是用于投稿前审阅有机化学支持信息（SI）的 Codex 技能。它按材料分工核对实验方法、NMR／HRMS、IR、结构编号、正文配图与计算数据。发现的问题附原件位置，报告区分证据状态与影响程度。支持新版全面复查和旧问题逐条追踪。

## 在 Codex 中安装

在 Codex 聊天里发送这条指令。

```text
用 $skill-installer 安装 https://github.com/RainWatcher2077/organic-si-review/tree/main/skills/organic-si-review
```

安装完成后，在下一轮输入 `$organic-si-review` 选用技能。若选择器尚未显示，重新打开 Codex。已安装同名技能时，先把旧版备份移出技能目录，再重新安装。

### 手动安装

下载并解压[仓库 ZIP](https://github.com/RainWatcher2077/organic-si-review/archive/refs/heads/main.zip)。把解压包中的 `skills/organic-si-review/` **整个文件夹**复制到用户目录下的 `.agents/skills/`。目录不存在时先创建。安装后应看到 `~/.agents/skills/organic-si-review/SKILL.md`，以及同级的 `agents/` 和 `references/`。只想在单个项目使用时，把技能放到该项目根目录的 `.agents/skills/`。 [Codex 官方技能说明](https://developers.openai.com/codex/skills)

## 用法示例

```text
用 $organic-si-review 全面审阅这版 SI、正文配图和谱图，按化合物编号对照。
列出子智能体分工与覆盖情况，保留原件，另存批注副本。
```

```text
用 $organic-si-review 全面复查新版 SI，并根据上一轮底账逐条给出状态。
本轮跳过晶体和 HPLC。
```

默认由主审统筹，NMR／HRMS、IR／编号／图文、实验方法／文字／引用可并行检查。空出的槽位用于重点反查。当前环境没有子智能体时，技能按同一检查队列顺序执行。技能本身无需安装额外脚本。实际覆盖取决于输入材料和 Codex 可用的读图、PDF 及浏览器工具。晶体专题按范围启用，有已安装的专门晶体技能时可配合使用。

- [技能入口](skills/organic-si-review/SKILL.md)
- [子智能体分工与派发模板](skills/organic-si-review/references/agent-workflow.md)
- [专项核对](skills/organic-si-review/references/chemistry-checks.md)
- [报告、批注副本与验收](skills/organic-si-review/references/deliverables.md)
