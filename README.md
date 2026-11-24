# AI Design Skills

A growing collection of design skills for AI coding tools — Claude Code, Cursor, Codex, Windsurf, and anything else that reads a markdown rules file.

Each skill is a self-contained folder. Install the ones you need.

---

## Skills

| Skill | What it does |
|---|---|
| [`landing-page-design`](./skills/landing-page-design/SKILL.md) | Builds a landing page from scratch — intake questions, page structure, conversion copy, plus a full visual system (type, spacing, radius, motion) |
| [`design-to-motion`](./skills/design-to-motion/SKILL.md) | Turns a static design into a pixel exact animated showcase — empty state to loaded, every visual acting out its story on a loop, background kept untouched, exported as an MP4 for X plus website and 800×500 GIFs |
| [`figma-designer`](./skills/figma-designer/SKILL.md) | Optional Figma workflow: design tokens, auto layout, reusable text styles, components and accessibility. Requires compatible Figma tools and companion skills. |

More on the way. [Upgrading an existing site instead of building new?](https://github.com/elayadesign/redesign-skill) That one lives in its own repo since it predates this collection.

---

## Install

Pick a skill from the table above, then swap `<skill-name>` below for its folder name.

<details open>
<summary><b>Claude Code</b></summary>

```bash
mkdir -p .claude/skills
git clone https://github.com/9479797/ai-design-skills.git /tmp/ai-design-skills
cp -r /tmp/ai-design-skills/skills/<skill-name> .claude/skills/
```

Then just ask, in plain language, for what that skill covers.
</details>

<details>
<summary><b>Cursor</b></summary>

```bash
mkdir -p .cursor/rules
curl -o .cursor/rules/<skill-name>.md \
  https://raw.githubusercontent.com/9479797/ai-design-skills/main/skills/<skill-name>/SKILL.md
```

Or paste the file into **Settings → Rules for AI**.
</details>

<details>
<summary><b>Codex / Windsurf / other</b></summary>

Copy the skill's `SKILL.md` into whatever your tool uses for project rules:

| Tool | Path |
|---|---|
| Codex | `AGENTS.md` |
| Windsurf | `.windsurfrules` |
| Cline | `.clinerules` |
| Generic | paste into your system prompt |
</details>

<details>
<summary><b>Claude.ai (no terminal)</b></summary>

Download the skill's `SKILL.md` and upload it to a Project, or attach it to a chat and say *"follow this."*
</details>

---

## Make it yours

Every skill's design values (fonts, colors, spacing, motion) live in one section near the bottom of its file. Fork this repo, edit that section, and the rest of the skill follows automatically.

---

## Проверка и обновление этой копии

Эта копия сохранена отдельно от [оригинального проекта Elaya](https://github.com/elayadesign/ai-design-skills). Обновления оригинала переносить **выборочно**, без автоматического удаления навыков: `design-to-motion` сохранён здесь, но отсутствует в проверенной ветке оригинала.

Проверка frontmatter и тестов навыков (Python 3.12):

```bash
python -m pip install pyyaml==6.0.3
python -m unittest discover tests
python scripts/validate_skills.py skills
```

Навык `figma-designer` **не запускает Figma сам по себе**: для применения нужны совместимые инструменты Figma и навыки `figma-use`, при соответствующих задачах `figma-generate-design` / `figma-generate-library`. Это не обязательный стиль для других типов проектов.

Документы:
- [Перенесённые изменения и происхождение файлов (24.11.2026)](docs/UPSTREAM_SYNC_2026-11-24.md)
- [Состояние сверки архива Claude](docs/CLAUDE_ARCHIVE_STATUS_2026-11-24.md)

---

## Credits

`landing-page-design` adapts content realism and motion ideas from [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) by Leon Lin, MIT licensed. Details are at the end of [its SKILL.md](./skills/landing-page-design/SKILL.md#credits).

`design-to-motion` adapts a few general motion rules from [emilkowalski/skills](https://github.com/emilkowalski/skills), [Owl-Listener/designer-skills](https://github.com/Owl-Listener/designer-skills), and [dylantarre/animation-principles](https://github.com/dylantarre/animation-principles), all MIT licensed. Details are at the end of [its SKILL.md](./skills/design-to-motion/SKILL.md#credits).

---

## License

MIT — см. [LICENSE](LICENSE). При распространении копий и существенных частей необходимо сохранять применимые лицензионные уведомления, в том числе авторские сведения и лицензии, включённые в файлы навыков.
