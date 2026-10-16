# 凤凰古城 App · GitHub Pages 部署包

本文件夹是「凤凰古城 · 攻略导览」Web 应用的完整静态站点（含图片、样式、脚本、404 兜底页），
上传到 GitHub 并开启 Pages 后，即可获得 `https://你的用户名.github.io` 的线上地址，
**域名不含 doubao，无平台水印，功能完整可用**。

## 文件说明

| 文件/文件夹 | 作用 |
|---|---|
| `index.html` | 应用入口页 |
| `404.html` | 刷新子页面时的兜底页（GitHub Pages 用它做单页应用路由兜底，不要删除） |
| `assets/` | 应用脚本与样式 |
| `images/` | 凤凰古城实景图（13 张） |
| `icons.svg` | 图标集 |

## 部署步骤（全程网页操作，无需安装任何软件）

**第 1 步 · 准备 GitHub 账号**
打开 https://github.com 注册或登录（免费）。

**第 2 步 · 创建仓库**
1. 右上角 `+` → **New repository**
2. Repository name 填：**你的用户名.github.io**
   （必须与你的账号名完全一致，例如账号是 `zhangsan`，就填 `zhangsan.github.io`）
3. 选择 **Public**（公开，免费）
4. 不要勾选 "Add a README file"
5. 点 **Create repository**

**第 3 步 · 上传文件**
1. 进入刚创建的仓库页面
2. 点 **Add file** → **Upload files**
3. 把本文件夹里的**所有内容**（`index.html`、`404.html`、`icons.svg`、`assets` 文件夹、`images` 文件夹）直接拖进上传区域
4. 点 **Commit changes**（默认即可）

**第 4 步 · 开启 Pages**
1. 仓库页面点 **Settings**（设置）
2. 左侧菜单点 **Pages**
3. Source 选 **Deploy from a branch**，Branch 选 **main** 和 **/(root)**
4. 点 **Save**

**第 5 步 · 访问**
等待 1~2 分钟，打开 **https://你的用户名.github.io/** 即可看到应用。

## 后续更新内容

重新上传覆盖同名文件即可：仓库页面 **Add file → Upload files**，把更新后的文件拖入覆盖 → Commit。
（如果改动很多，建议装 GitHub Desktop 用图形界面同步，或用 git 命令推送。）

## 常见问题

- **仓库名不是「用户名.github.io」会怎样？** 部署地址会变成 `https://用户名.github.io/仓库名/`，
  页面资源路径会错乱。请务必按第 2 步命名。
- **上传后打开是空白？** 等 1~2 分钟再刷新；确认仓库名正确、Pages 已开启且显示 "Your site is live"。
- **刷新 /routes 等子页面 404？** 已内置 `404.html` 兜底，正常不会出现；若出现请确认 404.html 与 index.html 在同一目录。
