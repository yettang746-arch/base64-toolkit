# GitHub Pages 部署指南

## 步骤 1：创建 GitHub 仓库

1. 访问：https://github.com/new
2. 仓库名称：`base64-toolkit`
3. 选择 Public
4. 不要勾选 "Initialize this repository with a README"
5. 点击 "Create repository"

## 步骤 2：推送代码

在本地终端执行：

```bash
cd /Users/tangye/.openclaw/workspace/saas-tools
git remote set-url origin https://github.com/yettang746-arch/base64-toolkit.git
git push -u origin main
```

如果需要登录：
- Username: yettang746-arch
- Password: 使用 Personal Access Token（不是 GitHub 密码）

**获取 Personal Access Token：**
1. 访问：https://github.com/settings/tokens
2. 点击 "Generate new token (classic)"
3. 勾选：repo（所有）
4. 生成并复制
5. 用 token 作为密码

## 步骤 3：启用 GitHub Pages

1. 访问：https://github.com/yettang746-arch/base64-toolkit/settings/pages
2. Source 选择：Deploy from a branch
3. Branch 选择：main / (root)
4. 点击 Save

## 步骤 4：等待部署

- 几分钟后，网站会自动部署
- 访问地址：https://yettang746-arch.github.io/base64-toolkit/

## 步骤 5：申请 Google AdSense

1. 访问：https://www.google.com/adsense/
2. 使用 Google 账号登录
3. 点击 "开始使用"
4. 添加网站：https://yettang746-arch.github.io/base64-toolkit/
5. 填写个人信息（地址用于收款）
6. 提交审核

### 替换广告代码

审核通过后：
1. 获取你的 `ca-pub-XXXXXXXXXXXXXXXX` 和 `data-ad-slot`
2. 打开 `index.html`
3. 找到所有 `ca-pub-XXXXXXXXXXXXXXXX` 并替换
4. 找到所有 `XXXXXXXXXX` 并替换
5. 提交代码并重新部署

## 数据安全提醒

⚠️ **重要：不要在公开代码中暴露敏感信息**

- ✅ 可以公开：网站地址、GitHub 仓库
- ❌ 不要公开：AdSense 代码、个人地址、真实姓名
- ✅ 使用假名或昵称进行自媒体账号

## 下一步

网站上线后，参考 `MEDIA_STRATEGY.md` 开始自媒体账号运营！
