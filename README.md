# 本科生国家奖学金申请系统

本科生国家奖学金在线申请与审批系统。

## 功能模块

- 学生申请（个人信息、申请条件、竞赛荣誉、科研实践、申请理由、文件上传）
- 辅导员审核
- 学院副书记审核
- 学校审核

## 本地预览

直接用浏览器打开 `index.html` 即可。

## GitHub Pages 部署

1. 在 GitHub 上创建新仓库（例如 `scholarship-system`）
2. 将以下文件上传到仓库根目录：
   - `index.html`（主页面）
   - `.nojekyll`（禁止 Jekyll 处理）
3. 进入仓库 Settings - Pages
4. Source 选择 Deploy from a branch
5. Branch 选择 `main`，文件夹选择 `/ (root)`
6. 点击 Save
7. 等待约 1 分钟，访问 `https://<用户名>.github.io/scholarship-system/` 即可

## 技术说明

- 纯前端单页应用，无需后端服务
- 所有 CSS/JS 内联在 HTML 中，唯一外部依赖为 Google Fonts CDN
- 响应式布局，支持桌面和移动端
