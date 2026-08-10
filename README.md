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

| 文件 | 说明 |
|------|------|
| `index.html` | 系统主文件（含全部 CSS/JS，自包含，无需额外依赖） |
| `.nojekyll` | 禁用 GitHub Pages 的 Jekyll 处理，确保文件原样输出 |
| `README.md` | 本说明文件 |

## 功能模块

### 学生申请（Step 1）
- 基础信息：姓名、身份证号、学院、专业、学号、性别、民族、学制、入学年月、联系方式
- 申请条件：受处分情况、不及格科目、必修课门数、成绩排名、综测排名、破格参评
- 奖学金与荣誉：一等奖学金、校级及以上综合类荣誉
- 竞赛和荣誉：获奖情况登记（最多四项）
- 科研与实践：科研成果、志愿汇时长、实践活动
- 申请理由：80字左右，含撰写要点提示
- 文件上传：PDF / JPG / PNG 格式
- 备注栏：系统自动生成 + 学生补充

### 辅导员审核（Step 2）
- 学生申请信息摘要（只读）
- 条件触发的补充材料上传

### 副书记审核（Step 3）
- 破格参评情况说明

### 学校审核（Step 4）
- 最终审批

## 系统特点

- 四步审批流程，步骤间可切换
- 左侧导航栏快速定位各模块
- 实时进度跟踪（完成度百分比）
- 自动校验申请条件（排名比例、必修课及格率等）
- 破格参评智能提示
- 纯前端实现，无后端依赖，数据存储在浏览器内存中

## 技术说明

- 纯前端实现，无后端依赖，数据存储在浏览器内存中
- 字体使用 Google Fonts CDN，需联网加载
- 刷新页面会重置数据，请确保在提交前完成填写
- 参评学年为 2025-2026 学年
