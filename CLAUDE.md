# 个人网站（shiwoxiaobailong.me）AI 自动同步规范

请严格遵循同目录下的 `GEMINI.md` / `README.md` 规范：
1. 本站采用 **杂志大字画册风（方案 C）+ 首页 3D 羊毛毡双人实时互动 + 作品真实实机截图封面**。
2. 新增作品时：
   - 作品文件放入 `works/<slug>/`
   - 必须截取作品内部真实运行画面（1280×800）保存为 `posters/<slug>-shot.jpg`（严禁使用 Emoji 占位图）
   - 若有讲解视频，保存为 `videos/<slug>-intro.mp4`
   - 在 `index.html` 的 `const WORKS = [...]` 数组中追加数据对象即可，页面会自动按杂志画册交错排版渲染并自动更新作品总数。
3. 严禁修改或破坏首页 `#mascot3d`（`assets/mascot3d.js`、`assets/duo_interact.jpg`、`assets/duo_sunglasses.jpg`）3D 羊毛毡双人互动剧场与整体杂志排版样式。
