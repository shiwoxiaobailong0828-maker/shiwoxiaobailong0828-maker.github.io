# 是我小白龙 · 个人作品画册 (shiwoxiaobailong.me)

本站采用 **杂志大字画册风（Editorial Brutalist Magazine）** 设计，包含：
- **首屏 3D 羊毛毡双人实时互动剧场**（`assets/mascot3d.js`）
- **01 作品画册（Selected Works）**：每件作品均采用浏览器画框 + 1280×800 真实实机截图封面（`posters/<slug>-shot.jpg`）
- **02 放映厅（Short Films）**
- **03 GitHub 开源仓库自动同步**

## AI 助手自动同步新作品指南

见仓库根目录下的 [`GEMINI.md`](./GEMINI.md) 与 [`CLAUDE.md`](./CLAUDE.md)。只需将新作品放入 `works/<slug>/`、实机截图放入 `posters/<slug>-shot.jpg`，并在 `index.html` 的 `WORKS` 数组中追加一条配置，全站即可自动以当前杂志画册风格渲染并自动更新作品计数。
