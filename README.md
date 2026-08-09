# 本科生国奖系统（308设置）

本科生国家奖学金审批系统，包含学生申请、辅导员审核、副书记审核、学校审核四个步骤。

## 部署到 GitHub Pages

### 方法一：网页端上传

1. 在 GitHub 新建仓库（如 `scholarship-system`）
2. 上传 `index.html` 和 `.nojekyll` 文件
3. 进入仓库 Settings → Pages
4. Source 选择 `Deploy from a branch`
5. Branch 选择 `main`，文件夹选 `/ (root)`
6. 点击 Save，等待 1-2 分钟即可访问

### 方法二：命令行推送

```bash
git init
git add index.html .nojekyll
git commit -m "本科生国奖系统部署"
git branch -M main
git remote add origin https://github.com/你的用户名/scholarship-system.git
git push -u origin main
```

推送后在仓库 Settings → Pages 中开启即可。

### 访问地址

部署成功后访问：
```
https://你的用户名.github.io/scholarship-system/
```

## 文件说明

- `index.html` — 系统主文件（含全部 CSS/JS，自包含，无需额外依赖）
- `.nojekyll` — 禁用 GitHub Pages 的 Jekyll 处理，确保文件原样输出

## 功能模块

- 学生申请：基础信息、申请条件、竞赛和荣誉、科研与实践、申请理由、文件上传
- 辅导员审核：信息确认、条件触发材料上传
- 副书记审核：破格情况说明
- 学校审核：最终审批

## 技术说明

- 纯前端实现，无后端依赖，数据存储在浏览器内存中
- 字体使用 Google Fonts CDN，需联网加载
- 刷新页面会重置数据，请确保在提交前完成填写
