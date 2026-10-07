# AGENTS.md

## Repository workflow

This repository contains the custom Codex skill:

`.agents/skills/hinh-ke-truyen-v6/`

When a request starts with:

`$hinh ke truyen`

prefer the `hinh-ke-truyen-v6` skill and follow its `SKILL.md`.

Core rules:
- Develop the topic into a detailed Vietnamese story/documentary.
- Default to 15–20 scenes unless the user requests otherwise.
- One scene = one separate image/file.
- Never combine multiple scenes into a storyboard, grid, split screen, or multi-panel image.
- Keep Character/Subject Lock and Visual Lock consistent.
- When supported, use the first approved image as a reference for later images.
- Provide image prompts, video-motion prompts, AI voice direction, SRT, sound design, thumbnail guidance, and CapCut workflow when relevant.
- Support YouTube, TikTok, Shorts, Standard, and JSON modes.
