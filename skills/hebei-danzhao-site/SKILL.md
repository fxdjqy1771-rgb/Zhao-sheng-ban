---
name: 河北单招志愿通网页
description: 制作或迭代河北省高职单招查询单页（院校/专业/分数预估/志愿方案）时使用。
---
# 河北单招志愿通网页

## 交付物
- 单文件站点：`/workspace/site/index.html`
- 发布副本：`/workspace/pub/index.html`、`/workspace/pub/河北单招志愿通.html`
- 锁定稿：`/workspace/site/locked/index_定稿_*.html` 与 `index_最终版.html`（改后需同步）
- 官方数据：`/workspace/site/data/hebei_dz_colleges.json`（77 所 + 专业；分数仍为示例哈希）

## 硬规则
- 横幅保留「当前为示例数据，非真实录取分数」。
- 用户未明确解锁前，勿擅自改已锁定板块视觉；用户明确要求的改动除外，并更新对应锁定稿。
- 年份：`APPLY` 与 `Y0=APPLY-3`，展示报名前三年。
- 院校名称有官网则链到官网；勿编造双高/示范等优势。
- 志愿方案按官方「专业（类）+学校」平行志愿，最多 96；对口按 10 个专业类限制；批次内容勿套同一模板。
- 搜索框 `#q`/`#sc` 保持 `autocomplete=off`。
- 回复偏好：改完主要发截图，话少。

## 常见版块
- **院校查询**：列表 + 三小方块院校轮播（5s 上滑）+ 右侧最低分趋势（按专业 5s 轮播）；人数对比已删；不因分差隐藏院校。
- **专业查询 / 分数预估 / 志愿方案**：按各自锁定稿布局。
- 临时链接：litterbox 72h（需审批）。

## 改动流程
1. 备份 `index.bakN.html`。
2. 改 HTML/CSS/JS；headless 用 playwright-core + `/usr/bin/google-chrome`。
3. 同步 locked + pub。
4. 截图发用户。
