---
name: ESPLENDOR
version: "1.0"
date: "2026-11-12"
status: design-approved-implementation-in-candidate-only
colors:
  canvas: "#F6F0E8"
  ink: "#2B2320"
  taupe: "#6B5A4A"
  sand: "#E6D9C8"
  bronze: "#8A5F3C"
  bronze-dark: "#75502F"
  night: "#1A1918"
  blush: "#E8C9C4"
  sage: "#B7C4B0"
  tan: "#D9B99A"
typography:
  display: "'Cormorant Garamond', Georgia, serif"
  body: "Inter, system-ui, sans-serif"
spacing-base: 8
---

# ESPLENDOR — DESIGN.md（设计规范 v1.0）

用途：ESPLENDOR 品牌的网页设计规范。设计实施前请先读取本文件，按照原有数值和组件定义验收。
本规范的配色和组件数值以本文件为准；历史设计代码中的使用次数统计属于原草案记录。

## 1. Visual Theme & Atmosphere（视觉主题与氛围）

- 一句话气质：**安静的夜间仪式感**——像精品酒店的床品店，不像促销电商。关键词：quiet luxury（安静的贵）、warm minimal（暖调极简）、editorial（杂志式编辑感）。
- 构图哲学：**图片当主角，文字退为配角**。每个区块只讲一件事，先图后文，大留白，慢节奏。
- 深浅节奏：米白为底、沙色交替，**每页至多一个深色块**（Night）镇场，形成「浅—浅—深」的呼吸感。深色块是重音，不是底色。
- 情绪禁区：不用促销红、不用倒计时压迫感、不用爆款式密集排版。价格与优惠信息照常给，但用安静的方式给。

## 2. Color Palette & Roles（色彩与角色）

| 语义名 | 色值 | 角色 | 来源 |
|---|---|---|---|
| Canvas 米白 | #F6F0E8 | 页面底色、浅色块、深色块上的文字 | kit 出现 187 次 |
| Ink 深棕 | #2B2320 | 标题与正文主色、次级按钮描边、价格 | kit 出现 215 次 |
| Taupe 驼棕 | #6B5A4A | 次级文字、图标、弱强调、说明文字 | kit 第一高频 381 次 |
| Sand 沙 | #E6D9C8 | 卡片底、分隔线、浅色交替块、标签底 | kit 出现 106 次 |
| **Bronze 古铜** | **#8A5F3C** | **全站唯一行动色**：主按钮填充、眉题标签、链接悬停、免邮进度条填充 | kit 现用作眉题色（53 次），本草案升格为唯一行动色 |
| Bronze Dark | #75502F | 主按钮悬停/按下态 | 古铜加深一档 |
| Night 墨棕 | #1A1918 | 深色块底色，每页至多一个 | P1 定 |
| Blush / Sage / Tan | #E8C9C4 / #B7C4B0 / #D9B99A | 仅限产品色语境：色卡、分类图衬底、产品色块。**永远不做 UI 强调色、不做按钮** | kit 各出现 7–12 次 |

规则：
- **行动色唯一**：全站可点击的主行动（加购、结账、Shop Now、订阅提交）只有 Bronze 一种填充色。出现第二个按钮色即验收不过。
- 对比度（已实算）：Canvas 字 on Bronze = 4.9:1（按钮文字合格）；悬停态 6.3:1；Ink on Canvas = 13.6:1；Taupe on Canvas = 5.8:1（次级文字合格）。
- 禁用纯黑 #000000 与纯白 #FFFFFF；最深用 Ink/Night，最浅用 Canvas。
- 折扣与优惠：用 Ink 文字＋Sand 底标签呈现，不用红、黄、橙等促销色。

## 3. Typography Rules（字体与层级）

- 标题字体：'Cormorant Garamond', Georgia, serif——只用于标题、Hero、编辑引言。
- 正文字体：Inter, system-ui, sans-serif——正文、UI、按钮、价格、表单一律 Inter。
- 站面语言为英文（UK/AU 市场）；本规范文件用中文写给施工与验收双方看，不上站。

| 层级 | 字体/字重 | 字号 | 行高/字距 | 用途 |
|---|---|---|---|---|
| Display | Cormorant 500 | clamp(46px, 6vw, 80px) | 1.05 | 首页 Hero 主标题 |
| H1 | Cormorant 500 | 40–56px | 1.1 | 商品页/集合页主标题 |
| H2 | Cormorant 500 | 32–40px | 1.15 | 区块标题 |
| H3 | Cormorant 600 | 22–24px | 1.25 | 卡片与小节标题 |
| Eyebrow 眉题 | Inter 600 大写 | 11–12px | 字距.14em，Bronze 色 | 区块上方的英文小标签 |
| Body L | Inter 400 | 18px | 1.6 | 编辑段落、品牌故事 |
| Body | Inter 400 | 16px | 1.6 | 正文 |
| Body S | Inter 400 | 14–15px | 1.55–1.65 | 说明、手风琴展开、手风琴标题 15px/600 |
| Caption | Inter 400 | 12.5–13px | 1.5 | 脚注、政策小字 |
| Price 价格 | Inter 500–600 | 与上下文同级 | — | 价格不用衬线、不用 Bronze |

规则：正文不用衬线；大标题不用 Inter；标题不加粗到 700（Cormorant 用 500/600 的轻盈感是质感来源）。

## 4. Component Stylings（组件样式）

- **主按钮（Primary CTA，全站唯一款）**：Bronze 填充、Canvas 文字、胶囊形（border-radius 999px）、内边距 16px 32px、Inter 600 15px。悬停 → Bronze Dark；禁用 → Sand 填充＋Taupe 文字。Add to Bag、Checkout、Shop Now、订阅提交全部同款，不许变体。
- **次级按钮**：透明底、1px Ink 描边、Ink 文字、胶囊形；悬停 → Ink 填充、Canvas 文字。
- **文字链接**：Ink 色、下划线偏移 4px；悬停变 Bronze。
- **卡片**：Sand 或 Canvas 底、圆角 16px、默认无阴影、靠 1px 发丝线（Sand 加深一档）分界。
- **标签/徽章**：Sand 底＋Ink 字、11px 大写、圆角 999px。免邮、配送、退货等信任标签全用这一款，不用彩色徽章。
- **输入框**：Canvas 底、1px Sand 边框、圆角 12px；聚焦时边框变 Bronze。错误提示用 Ink 文字说明，不用红框轰炸（表单错误边框可用深陶土色，但站内暂无此场景，先留规矩）。
- **手风琴（商品页信息流）**：发丝线分隔，标题 Inter 600 15px，右侧 +/− 号；展开正文 Body S、Taupe 偏 Ink。购买区三件套（价格/配送/退货摘要）**直给、不折叠**，折叠只放次级信息。
- **颜色色卡**：圆形（border-radius 50%），选中态外加 Ink 圈。
- **免邮进度条**：6px 高、Sand 轨道、Bronze 填充，配一行 Ink 小字说明差多少免邮。
- **移动端吸底购买条（仅商品页）**：Canvas 底、顶部发丝线、左侧价格（Inter 600 Ink）、右侧主按钮缩小版。与站内其他浮层共用第 6 节的唯一阴影。

## 5. Layout Principles（布局原则）

- 间距标尺（8 基准）：4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 96 / 128。只许用标尺上的值，不许随手写 18px、37px 这类野生数值。
- 区块纵向间距：桌面 96–128px，移动 56–72px——留白是本品牌的主要「贵感」来源，不许压缩。
- 容器：最大宽 1200px，两侧内边距桌面 40px / 移动 20px。
- 商品页版式：桌面图左文右约 55/45；移动端图先行、购买区紧随，不许让用户滑很久才看到价格与按钮。
- 图片比例（全站同类同比例，不混裁）：
- Hero：桌面 21:9 全幅，移动 4:5 竖版（用竖版裁切，不压扁横图）
- 商品主图/图库：4:5
- 产品卡：4:5
- 编辑/故事图：3:2
- 按颜色选购图：1:1
- 节奏：浅色块之间用 Sand 交替或留白分隔；深色块每页至多一个，且不与另一个深色元素相邻。

## 6. Depth & Elevation（深度与阴影）

- 默认**扁平**：层级靠底色差（Canvas / Sand / Night）与发丝线，不靠投影。
- 全站只允许一种阴影：浮层专用暖色柔影 `0 8px 30px rgba(43,35,32,0.08)`，仅用于吸底条、弹窗、抽屉、悬浮卡。
- 禁用：冷灰/纯黑硬阴影、多层叠加投影、图片自带重投影。

## 7. Do's and Don'ts（护栏）

Do：
- 实拍图当主角：先图后文，图够大，文字够少。
- 一页只有一个主行动样式；用户永远知道「下一步点哪」。
- 标题大而安静：靠字号和留白显贵，不靠加粗和颜色。
- 信任信息直给：配送、退货、公司信息在购买区与页脚明处（与 Merchant Center 复审同一批口径）。

Don't：
- 不用 AI 生成图、图库图充当产品图；图片里不出现别家商标。
- 不出现第二个行动色；不用促销红、倒计时、闪烁动效。
- 吉祥物只做社媒头像与脸面，**不进站内主视觉、不上包装**。
- 不把关键购买信息全折进手风琴；不隐藏产地、备货时间、跨境退货邮费。
- 文案红线与设计同样生效：19 姆米不写 22；不写 100% blackout、anti-wrinkle、hypoallergenic 等未证实功效；不编造评价数、销量、Best Seller 徽章。

## 8. Responsive Behavior（响应式）

- 断点：≤768px 移动 / 769–1024px 平板 / >1024px 桌面。验收视口固定 **375px 与 1280px**。
- 触控目标 ≥44px；商品页主按钮移动端全宽。
- Display 字号移动端下限 40px（clamp 下限），不许小到需要眯眼。
- 深色块移动端保留，内边距收至 24px。
- 图片按第 5 节比例提供移动裁切版，不许把桌面横图直接缩放塞进移动端。

## 9. Agent Prompt Guide（给施工 AI 的提示指南）

- 开工顺序：先读本文件 → 再读对应施工包说明 → 在未发布候选环境进行增量施工，逐文件回读校验，未经批准不修改线上正式主题。
- 边界：不碰原生购买逻辑、价格、变体、结账、追踪脚本；事实文案以站上已核实内容为准，本文件不授权改任何事实。
- 每个包交付时附**对照自查表**：色彩（行动色唯一）/ 字阶 / 间距标尺 / 组件款式 / 图片比例 / 深色块数量，逐项打勾，附 375px 与 1280px 双视口截图。
- 拿不准的数值：回查本文件；本文件没有的，先问，不许自创色值、字号、圆角。
- 验收：逐项对照设计规范核查，不达标不发布；发布时间点记录在案。

---

## Implementation safety notes

- Site-owned styling only; do not override checkout provider, third-party payment, native cart or visitor tracking logic.
- Maintain accessible color contrast, visible focus states and legible form feedback. The palette alone is not sufficient for every context.
- Preserve real product imagery and intrinsic content. Target image ratios must not crop essential product details.
- Apply only to reviewed, unpublished candidate pages; maintain source and version history before deployment.
- For the mobile product page, the in-flow primary button may span its container; a separate compact sticky buy bar is an exception.
- This document is a **design specification**, not a claim that any production site has been modified.
