# 个人主页部署指南

## 项目信息
- **位置：** `saas-tools/personal-portfolio/index.html`
- **用途：** Google AdSense 顶级域名验证
- **特点：** 简洁、响应式、暗黑主题

## 部署步骤（使用 GitHub Pages）

### 方法一：创建新的 GitHub 仓库

1. 创建新仓库（例如：`personal-portfolio`）
2. 将 `index.html` 上传到仓库根目录
3. 在仓库设置中启用 GitHub Pages
4. 设置源为 `root` 分支
5. 访问 `https://<username>.github.io/personal-portfolio/`

### 方法二：使用现有仓库

如果已经在使用顶级域名，可以将 `index.html` 部署到：
- 根目录：`https://tnight.xyz/`
- 子目录：`https://tnight.xyz/about/`

## 顶级域名配置

### 使用 Cloudflare

1. 在 Cloudflare 添加 CNAME 记录：
   ```
   类型: CNAME
   名称: @
   目标: <username>.github.io
   ```

2. 或使用 A 记录指向 GitHub Pages IP：
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```

3. 在 GitHub 仓库设置中添加自定义域名

### 使用 Vercel（推荐，更简单）

1. 安装 Vercel CLI
2. 运行 `vercel` 在项目目录
3. 添加域名 `tnight.xyz`
4. Vercel 自动处理 DNS

## Google AdSense 验证

### 步骤

1. 访问 Google AdSense 控制台
2. 选择 "添加网站" → "使用您的域名"
3. 输入 `https://tnight.xyz`
4. 选择验证方式（推荐 DNS TXT 记录）
5. 在域名提供商处添加验证记录

### DNS TXT 记录示例

```
类型: TXT
主机记录: @
记录值: google-site-verification=XXXXXXXXXXXXXXXXXX
```

## 添加 Google AdSense 代码

验证通过后，在 `<head>` 部分添加：

```html
<!-- Google AdSense -->
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXX" crossorigin="anonymous"></script>
```

## 验证域名访问

```bash
# 检查 DNS 解析
dig tnight.xyz

# 检查 HTTP 访问
curl -I https://tnight.xyz
```

## 备注

- 个人主页设计简洁，适合作为入口页面
- 已经预留了 Google 验证代码位置
- 响应式设计，移动端友好
- 暗黑主题，现代感强
