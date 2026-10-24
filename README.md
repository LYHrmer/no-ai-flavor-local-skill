# no-ai-flavor 技能安装说明

这是一个给 AI 编程/写作助手用的"去 AI 味"技能：识别并改掉过于工整对称、爱总结、爱煽动的 AI 腔表达（中英双语），按交付场景改成自然、准确的写法。文档和报告使用正式文体，保留事实、公式、术语与必要结构；聊天和社交文案单独处理。

## 目录结构

```
no-ai-flavor/
├── SKILL.md                          主文件：文档模式 + 文体路由 + 改写示例
└── references/
    ├── conversational-writing.md    聊天、随笔与社交文案规则
    ├── word-blacklist-zh.md          中文词库（句式/情绪词/黑话/连接词/开场腔）
    ├── word-blacklist-en.md          英文词库（overused words + AI phrase tells）
    └── structural-tells.md           排版/结构层面的 AI 味（不是单词层面）
```

## 安装方法

### Claude Code

把整个 `no-ai-flavor` 文件夹放到：

- 全局生效（所有项目）：`~/.claude/skills/no-ai-flavor/`
- 只在某个项目生效：`<项目根目录>/.claude/skills/no-ai-flavor/`

```bash
# 全局安装示例
unzip no-ai-flavor.zip -d ~/.claude/skills/
```

### Codex CLI

把整个 `no-ai-flavor` 文件夹放到：

- 全局生效：`~/.codex/skills/no-ai-flavor/`

```bash
# 全局安装示例
unzip no-ai-flavor.zip -d ~/.codex/skills/
```

安装后重新打开一个对话，直接说"帮我去一下 AI 味"或英文 "make this sound more human" 之类的话即可自动触发；也可以直接贴文本让它审阅/改写。

## 使用方式

1. 直接把文本贴给它，说"去 AI 味"/"降低 AI 感"/"sound less like AI" 等触发词。
2. 写文档或报告时，说明用途并提供材料；默认交付可直接使用的正文，检查过程留在内部。
3. 或者让它审阅一段别人写的文字，它会列出命中的规则/词条 + 原句 + 具体替换建议。
