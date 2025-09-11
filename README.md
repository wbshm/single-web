# AndPods 活动 · 博饼领好礼（单页版）

一个纯静态的 H5 活动页，包含：

- 根目录 `index.html`：引导页（2 秒自动跳转）
- 活动页 `202508/index.html`：内联 CSS/JS 的单文件页面（移动端适配）
- 文案来源 `202508/info.md`：页面内容严格基于该文案

## 本地预览

无需构建，直接用任意静态服务器或浏览器打开即可。

- 方案 A（浏览器直接打开）：双击 `index.html`
- 方案 B（Python 简易服务器）
  ```bash
  # Python 3.x
  python3 -m http.server 8000
  # 打开 http://localhost:8000
  ```
- 方案 C（VS Code 插件）
  - 安装 Live Server，右键 `index.html` → Open with Live Server

## 目录结构

```
.
├── index.html               # 引导页（跳转到活动页）
└── 202508/
    ├── index.html           # 活动页（内联 CSS/JS）
    └── info.md              # 活动文案
```

## 部署（GitHub Pages）

1. 在 GitHub 仓库设置中启用 Pages：
   - Settings → Pages → Source 选择 `Deploy from a branch`
   - Branch 选择 `main`，目录 `/(root)` → Save
2. 启用后访问：
   - `https://<你的 GitHub 用户名>.github.io/<仓库名>/`
   - 本仓库示例：`https://wbshm.github.io/single-web/`

> 若未开启 Pages，也可直接部署到任意静态托管（如 Netlify、Vercel、OSS/静态服务器等）。

## 设计与开发说明

- 色系：以米色背景、棕色标题、清新蓝绿点缀为主；参考截图风格。
- H5 适配：已加入 `viewport-fit=cover`、安全区适配、粘性导航和锚点高亮。
- 信息分区：时间胶囊、次数加成卡片、领奖流程（步骤与选择卡）、奖品、规则卡片化。
- 微动效：菜单下拉淡入+缩放、徽章弹性入场、奖品列表与主标题淡入。
- 无外部依赖：所有样式与脚本均内联，便于快速投放与复制迁移。

## 更新内容

- 修改文案：更新 `202508/info.md` 后，同步到 `202508/index.html` 对应区块。
- 样式微调：在 `202508/index.html` 内部 `<style>` 中调整变量或局部样式。

## 提交与推送

```bash
# 首次已初始化
git add -A
git commit -m "chore: update content/style"
git push
```

---
如需我将页面再适配到其他活动期（如 `202509/`）或接入表单/埋点，请告诉我～

