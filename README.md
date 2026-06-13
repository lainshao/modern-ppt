# modern-ppt

> 本机 skill 名为 **`lain-ppt`**（lain 的个人风格定制）；公开/上传 GitHub 时用仓库名 **`modern-ppt`**。两者是同一份东西，只是私有名 vs 公开名。

一个 **Claude Code skill**：用一句话生成现代分享/投屏风格的单文件网页 PPT —— 瑞士极简 + 安全橙 + 克制干净的排版，横向翻页、可直接投屏放映。内置一套"实战磨出来的"排版硬规范，让 AI 产出**一致**（而不是每次重新猜风格、重踩坑）。

## 这是什么 / 不是什么

- **是一个 skill**（菜谱+模板），不是一份做好的 PPT。装上后，对 Claude Code 说「按 lain-ppt 做个 X 主题的分享 deck」，它会按这套风格 + 规范帮你生成。
- 产出是**单个 HTML 文件**，浏览器打开即放映；别人拿到也能 fork 改自己的。

## 怎么用

1. 把本文件夹放到 `~/.claude/skills/lain-ppt/`（或任意名）。
2. 在 Claude Code 里：「用 lain-ppt 把这段大纲做成投屏 deck」/「做个关于 XX 的分享 PPT」。
3. 它会 `cp assets/template.html` 起步，按 `SKILL.md` + `references/排版规范.md` 填内容、先样页后放量。
4. `open index.html` 预览。换主题色只改 `:root` 的 `--accent` 三行。

## 设计规范（核心卖点）

`references/排版规范.md`——单一 body 字号 token、**标题靠分隔线不靠加大字号**、正文不上色、内容连排不锚底、底部安全区、编号列对齐、5 格方块刻度… 都是从一份 27 页 deck、30+ 轮批注里磨出来的硬约束。

## 许可与署名（重要）

本 skill **衍生自 [规藏 guizang-ppt-skill](https://github.com/op7418/guizang-ppt-skill)（© op7418）**，复用其 Swiss 模板底盘、WebGL/ASCII 背景与翻页/动效引擎；在其上做了安全橙主题、整套投屏排版规范、版式裁剪与 bug 修复。

> **据此本 skill 整体采用 [AGPL-3.0](./LICENSE)**（继承自上游）。再分发须：保留 `LICENSE` + 本署名段 + 注明你的改动；并继续以 AGPL-3.0 开源。**放入公司内部仓库前请先过开源合规**（AGPL 常因网络条款被企业政策限制）。用本 skill 生成的**最终 deck 不必署名**。

定制与规范：lain · 2026-06。
