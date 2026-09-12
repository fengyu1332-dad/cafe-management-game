# ☕ 咖啡馆经营模拟（网页版）| Cafe Business Sim (Web Edition)

> BizCafe 风格 · 单文件网页版 · 零依赖 · 双击即玩
> BizCafe-style · single-file web · zero dependencies · double-click to play

BizCafe 风格的单文件网页经营模拟，训练**创业与运营中的取舍决策**。
A BizCafe-style single-file business simulation that trains **trade-off decision-making in entrepreneurship and operations**.

## 这是什么游戏 | What is this game

用 **¥20,000** 启动资金经营一家咖啡馆，撑过 **12 周**，把**期末净值**做到最高。每周你要决定 5 件事：**定价 · 咖啡豆档位 · 采购量 · 员工数 · 营销投入**；现金流断了就倒闭。核心取舍：便宜能走量但人力是阶梯成本；贵能做毛利但口碑会掉；品质投入靠口碑复利，约 5 周后才见效。
Start with **¥20,000** and run a café for **12 weeks**, maximizing **end-of-game net worth**. Each week you decide 5 things: **price · bean grade · purchase volume · staff count · marketing spend**; run out of cash and you are bankrupt. Core trade-offs: low price drives volume but labor is a step cost; high price lifts margin but hurts reputation; quality investment compounds via reputation, paying off only after ~5 weeks.

## 如何运行 | How to run

- **本地 / Local：** 直接用浏览器打开 `index.html`（双击文件，或拖进浏览器窗口）。
  Open `index.html` directly in any browser (double-click the file, or drag it into a browser window).
- **在线 / Online：** 部署到任意静态托管（如 GitHub Pages）即可游玩。
  Deploy to any static host (e.g. GitHub Pages) to play online.
- 首次打开会自动弹出新手引导；顶栏「📖 新手指南」可随时重看。
  A guided onboarding pops up on first launch; the "📖 Guide" button in the top bar reopens it anytime.

## 机制要点 | Mechanics

- 现金 < 0 立刻倒闭，没有第二次机会。
  Cash < 0 means instant bankruptcy — no second chances.
- 固定成本是敌人：租金 ¥3,000/周 + 人力 ¥1,200/人/周，不管有没有客人都得付。
  Fixed costs are the enemy: rent ¥3,000/week + labor ¥1,200/staff/week, due whether or not anyone shows up.
- 口碑复利：口碑 +=（满意度 − 50）× 0.2；口碑 50→客流×1.0，100→×1.4，0→×0.6。
  Reputation compounds: reputation += (satisfaction − 50) × 0.2; reputation 50→traffic×1.0, 100→×1.4, 0→×0.6.
- 评级（期末净值）：S ≥ ¥60,000 · A ≥ ¥48,000 · B ≥ ¥36,000 · C ≥ ¥24,000 · F 倒闭。
  Grade (by end net worth): S ≥ ¥60,000 · A ≥ ¥48,000 · B ≥ ¥36,000 · C ≥ ¥24,000 · F = bankrupt.
- 每周 32% 概率触发随机事件（阴雨 / 网红打卡 / 豆价上涨 / 机器维修等），事件在决策前显示且已计入预测。
  Each week a random event fires with 32% chance (rain / influencer visit / bean-price spike / machine repair…); events are shown before you decide and already factored into the forecast.

## 教学用途 | Educational use

适合商学院创业管理 / 运营管理课程。页面内「📚 模型与数值说明」列出了每条数值的 rationale，以及现金流的 Source/Sink 与口碑的「增长飞轮 / 死亡螺旋」双反馈环。
Built for entrepreneurship / operations-management courses. The in-app "📚 Model & Numbers" panel lists the rationale behind every value, plus the cash-flow Source/Sink and reputation's "flywheel / death-spiral" dual feedback loops.

## 技术 | Tech

纯 HTML + CSS + Canvas + localStorage，无任何外部依赖、无需构建、无需服务器。
Pure HTML + CSS + Canvas + localStorage. No external dependencies, no build step, no server.
