# 🛒 lelong lelong! — AI Agent 技能市集

马来西亚福建人口中的「lelong lelong！」是夜市里叫卖的声音——**「大拍卖！好料快来！」**。
这里就是 AI Agent 技能的拍卖场。

*A bazaar of AI agent skills — made in Malaysia 🇲🇾*

## 📁 Categories

### 🖼️ Media
Photo restoration, enhancement, and upscaling.

| Skill | Description |
|-------|-------------|
| [4K-old-photo-portrait-restoration](./skills/media/4K-old-photo-portrait-restoration/SKILL.md) | Restore old family portrait photos to 4K with strict fidelity to originals |

### 📕 RedNote
Content creation and enhancement for 小红书 / Xiaohongshu.

| Skill | Description |
|-------|-------------|
| [rednote-article-enhancer](./skills/rednote/rednote-article-enhancer/SKILL.md) | Polish and enhance existing RedNote articles with credible, scannable structure |

## 📦 Installation

Add as a plugin (works with Claude Code and other AI agents that support skills):

```bash
claude plugins add https://github.com/mingyouk/lelong-skills
```

Skills are stored in the portable `SKILL.md` format — designed to work across AI agent platforms.

## 🤝 Contributing

New skills welcome! To add a skill:

1. Place it in the appropriate category folder under `skills/<category>/`
2. Create a `SKILL.md` with proper frontmatter (`name`, `description`)
3. Update this `README.md` with a link to your skill
4. Update `.claude-plugin/plugin.json` to include the skill path

---

Lelong lelong! 🎤 好料快来！
