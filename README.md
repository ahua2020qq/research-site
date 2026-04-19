# 研究工作台 - 个人知识成果展示站

一个极简的个人研究成果展示网站，专注于存放和管理 HTML 格式的研究报告和分析文档。

## 功能特性

- **主题分类导航**：侧边栏按 AI研究、金融数据、工程实践、分析报告等分类浏览
- **成果卡片展示**：网格布局卡片展示，每个卡片显示标题、描述、标签、日期
- **全文搜索**：支持标题、描述、标签搜索
- **管理上传界面**：可视化界面添加新成果，自动写入 data.json
- **响应式设计**：适配桌面端和移动端

## 目录结构

```
research-site/
├── index.html          # 首页（研究成果展示）
├── admin.html          # 管理上传界面
├── data.json           # 成果元数据（由管理界面自动维护）
├── articles/           # HTML 成果文件目录
│   └── *.html          # 具体的研究报告
└── README.md           # 本说明文档
```

## 快速开始

### 本地预览

直接用浏览器打开 index.html 即可预览（需要启动本地服务器以加载 data.json）：

```bash
# Python
python -m http.server 8000

# Node.js
npx serve
```

然后访问 http://localhost:8000

### 部署到 GitHub Pages

1. 创建 GitHub 仓库，将 research-site 目录内容推送到仓库
2. 进入仓库 Settings → Pages，Source 选择 main 分支和 / (root) 目录
3. 保存后等待部署完成，访问 https://yourusername.github.io/repository-name/

## 添加新成果

### 方法一：使用管理界面

1. 打开 admin.html 页面
2. 填写表单：标题、分类、日期、描述、标签
3. 拖拽或选择 HTML 文件
4. 点击"添加到 data.json"
5. 点击"下载 data.json"下载更新后的文件
6. 替换 GitHub 仓库中的 data.json
7. 将 HTML 文件复制到 articles/ 目录并提交

### 方法二：手动编辑

1. 将 HTML 文件放入 articles/ 目录
2. 编辑 data.json，在 entries 数组中添加新条目

## 分类说明

在 data.json 中可自定义分类：

- ai-research: AI研究
- financial: 金融数据
- engineering: 工程实践
- reports: 分析报告
- other: 其他

## 技术栈

- 纯静态 HTML/CSS/JavaScript
- 无需后端
- 无需数据库
- 依赖 Google Fonts（Inter + Noto Sans SC）
