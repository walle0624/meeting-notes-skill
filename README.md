# meeting-notes skill

把会议讨论整理成结构化的**会议纪要**,自动命名并写入 Obsidian 知识库。Claude Code 和 Codex CLI 通用(两者 skill 格式相同)。

## 产出格式
- 文件名:`会议名称-日期-地点.md`
- 固定六段:主题 / 参会人员·时间·地点 / 议题 Topic / 过程记录 / 结论 / 待办事项
- 写入目录:`/Users/walle/Obsidian/会议纪要/`(改路径请编辑 `SKILL.md`)
- 含 YAML frontmatter,方便 Obsidian 属性面板 / Dataview 检索

## 安装 / 更新
常规网络,克隆到对应 agent 的 skills 目录:
```bash
git clone https://github.com/walle0624/meeting-notes-skill.git ~/.claude/skills/meeting-notes
git clone https://github.com/walle0624/meeting-notes-skill.git ~/.codex/skills/meeting-notes
# 更新
git -C ~/.claude/skills/meeting-notes pull
git -C ~/.codex/skills/meeting-notes pull
```
若只能访问 GitHub API(`github.com` 不可达、`api.github.com` 可达),用 API 拉取 tarball 覆盖即可。

## 用法
对 Claude 或 Codex 说一句即可触发,例如:
> 记一下今天的产品评审会,在3楼会议室,我和老李、小王参加,主要评审 v2 改版,最后定了首页重做、小王下周三出原型。

`template.md` 是手动记录用的模板(对应 Obsidian 库里的 `_模板.md`)。
