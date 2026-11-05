# 个人网站（shiwoxiaobailong.me）AI 自动同步规范

> **重要提示（致所有 AI 助手：Antigravity / Claude Code / Cursor 等）**  
> 本站采用统一的 **「杂志大字画册风（Editorial Brutalist Magazine）+ 首页 3D 羊毛毡双人实时互动 + 作品内部真实实机截图封面」** 设计体系。今后向本站同步新作品或新短片时，**严禁改动整体版式或使用 Emoji 占位图**，只需按以下规范增量追加数据与资源即可自动继承全站画册风格。

---

## 1. 新增可交互作品（`01 作品画册 · SELECTED WORKS`）标准步骤

当你将用户的新作品同步到本仓库时，只需完成以下 **3 步**，页面会自动生成奇偶交错的杂志大图行、自动编号（`01`, `02`...）并自动更新全站作品计数印章：

1. **放入作品静态文件**：
   - 将构建好的作品静态页面放入 `works/<slug>/index.html`（及相关静态资源）。
2. **截取真实作品实机封面（严禁使用纯色或 Emoji 封面）**：
   - 使用无头浏览器（1280×800 视口）截取作品运行时的**真实内部画面截图**，保存为：
     - `posters/<slug>-shot.jpg`（推荐同步复制一份 `posters/<slug>-intro.jpg` 兼容弹窗与视频海报）
   - 如果该作品附带演示/讲解视频，将其保存为 `videos/<slug>-intro.mp4`（编码要求：`H.264 + AAC`）。
3. **在 `index.html` 的 `WORKS` 数组顶部（或指定位置）追加一项**：
   ```js
   {
     slug: "<slug>",                 // 对应 works/<slug>/ 与 posters/<slug>-shot.jpg
     name: "作品中文名称",
     cat: "分类标签（如 3D / WEBGL DIORAMA 或 AI AGENT · 领域）",
     status: "live",                 // "live"（已发布） | "score"（评分中） | "wip"（制作中）
     badge: "已发布",
     bcls: "b-live",                 // "b-live" | "b-score" | "b-wip"
     desc: "一句话简明导语（显示在画册列表中）",
     long: "详细功能与背景介绍（显示在点击后的详情弹窗中）",
     feats: [
       "核心亮点或操作说明 1",
       "核心亮点或操作说明 2",
       "核心亮点或操作说明 3"
     ]
   }
   ```
   > **注意**：无需手动修改页面上的“8 件作品”数字，`index.html` 会根据 `WORKS.length` 自动计算并更新右上角黄章、统计栏和筛选标签。

---

## 2. 新增 AI 科普短片（`02 放映厅 · SHORT FILMS`）标准步骤

1. 将视频保存至 `videos/<file>.mp4`，封面保存至 `posters/<file>.jpg`。
2. 在 `index.html` 的 `VIDEOS` 数组中追加一项：
   ```js
   { title: "短片标题", file: "<file>", dur: "时长（如 1:30）", line: "一句话短片看点介绍" }
   ```

---

## 3. GitHub 代码仓库（`03 GitHub · 代码仓库`）

- 页面底部代码仓库区块已接入 GitHub REST API（`users/shiwoxiaobailong0828-maker/repos?sort=updated`），用户的公开新仓库会**全自动按杂志卡片风格同步展示**；也可在 `#repoGrid` 中保留精选置顶仓库作为静态兜底。

---

## 4. 严禁破坏的核心组件

- **请勿删除或覆盖** 首页右下角的 3D 羊毛毡双人互动组件（`#mascot3d`、`assets/mascot3d.js`、`assets/duo_interact.jpg`、`assets/duo_sunglasses.jpg`）。
