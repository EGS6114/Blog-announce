# Blog-announce

一个简洁的独立公告站，用于展示博客更新动态和发布通知。

- 自动获取 GitHub 最新 commit
- 支持手动发布公告（JSON 数据）

## 项目结构

folio-announce/
├── astro.config.mjs
├── package.json
├── tsconfig.json
├── src/
│   ├── data/
│   │   └── announcements.json        # 手动公告数据
│   ├── layouts/
│   │   └── BaseLayout.astro          # 公共布局（含头部、页脚）
│   ├── pages/
│   │   └── index.astro               # 首页（显示 commit 和公告）
│   └── styles/
│       └── global.css                # 全局极简样式
└── README.md                         # 可选

## 快速开始

```bash
# 1. 安装依赖
npm install

# 2. 启动开发服务器
npm run dev

# 3. 构建静态文件
npm run build
```

## 配置说明

### 修改GitHub仓库

编辑`src/pages/index.astro`:

```js
const GITHUB_REPO = '你的用户名/仓库名'; 
const BLOG_URL = 'https://你的博客地址'; 
```

### 修改公告内容

编辑 `src/data/announcements.json`,按格式添加或删除公告。

### 修改页脚链接

编辑 `src/layouts/BaseLayout.astro` 中的页脚部分。

## 部署

构建后，将 dist/ 目录上传至任意静态托管服务（Cloudflare Pages / Vercel / GitHub Pages 等）。

```bash
npm run build
```





