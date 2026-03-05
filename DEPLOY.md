# GitHub Pages 部署指南

## 方法一：使用 GitHub CLI（推荐）

### 1. 登录 GitHub
```bash
gh auth login
```
选择：
- GitHub.com
- HTTPS
- Login with a web browser

### 2. 创建仓库
```bash
gh repo create jump-game --public --source=. --remote=origin --push
```

### 3. 启用 GitHub Pages
```bash
gh api repos/:owner/jump-game/pages -X POST -f source[branch]=master
```

等待 1-2 分钟后，访问：
```
https://<your-username>.github.io/jump-game/
```

---

## 方法二：手动创建仓库

### 1. 在 GitHub 网站创建仓库
1. 访问 https://github.com/new
2. 仓库名称：`jump-game`
3. 选择 Public
4. 不要初始化 README、.gitignore 或 license
5. 点击 "Create repository"

### 2. 推送代码
```bash
cd /home/gem/.openclaw/workspace/jump-game
git remote add origin https://github.com/<your-username>/jump-game.git
git branch -M main
git push -u origin main
```

### 3. 启用 GitHub Pages
1. 进入仓库页面
2. 点击 Settings → Pages
3. Source 选择：Deploy from a branch
4. Branch 选择：main (或 master) → / (root)
5. 点击 Save

等待 1-2 分钟后，访问：
```
https://<your-username>.github.io/jump-game/
```

---

## 游戏特性

✅ 完整的 Stick Hero 游戏逻辑
✅ 响应式设计，支持移动端和桌面端
✅ 触摸和鼠标操作支持
✅ 得分系统和最高分记录
✅ 精美的视觉效果和动画

---

## 快速开始（如果已配置好）

```bash
cd /home/gem/.openclaw/workspace/jump-game

# 如果还没有远程仓库
git remote add origin https://github.com/<your-username>/jump-game.git

# 推送代码
git push -u origin main
```

将 `<your-username>` 替换为你的 GitHub 用户名。
