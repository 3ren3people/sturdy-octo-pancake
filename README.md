# Your Lab

基于 [al-folio](https://github.com/alshedivat/al-folio) 的实验室主页第一版。

当前导航：**研究 · 论文 · 成员 · 新闻 · 加入**。

## 先改这些

| 位置 | 改什么 |
|---|---|
| `_config.yml` | `title`、姓名、`url`、`baseurl` |
| `_data/socials.yml` | 邮箱、GitHub、Google Scholar |
| `_pages/about.md` | 实验室介绍、地址 |
| `_pages/people_*.md` 和 `_pages/profiles.md` | 成员 |
| `_projects/` | 研究方向 |
| `_bibliography/papers.bib` | 论文 |
| `_news/` | 新闻 |
| `_pages/join.md` | 招生说明 |

把 `YOUR_GITHUB_USERNAME` 换成你的 GitHub 用户名。

- 仓库名是 `lab-website`：`url: https://用户名.github.io`，`baseurl: /lab-website`
- 仓库名是 `用户名.github.io`：`baseurl` 留空

## 发布到 GitHub Pages

本机目前没有 Git / Ruby / Docker。推荐直接用 GitHub Actions 构建：

1. 安装 [Git](https://git-scm.com/download/win)
2. 在 GitHub 新建仓库 `lab-website`
3. 在本目录执行：

```powershell
git init
git add .
git commit -m "Initialize lab website from al-folio"
git branch -M main
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/lab-website.git
git push -u origin main
```

4. 打开仓库 **Settings → Pages**
5. Build 来源选 **GitHub Actions**（al-folio 自带 `deploy.yml`）
6. 等 Actions 跑完后访问：`https://YOUR_GITHUB_USERNAME.github.io/lab-website/`

## 本地预览（可选）

安装 [Docker Desktop](https://www.docker.com/products/docker-desktop/) 后：

```powershell
cd lab-website
docker compose up
```

浏览器打开 `http://localhost:8080`。
