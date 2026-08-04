V8测速【Q-——333307——】V8测速【 辋芷《888yx●vip》 】
V8测速【Q-——333307——】V8测速【 辋芷《888yx●vip》 】

 从零搭建个人博客：GitHub Pages + Hexo 完整部署指南（2025最新版）

还在羡慕技术大佬们炫酷的个人博客？其实利用 GitHub Pages 和 Hexo，你也能在半小时内免费搭建一个高速、稳定的静态博客站点。本文手把手教你完成从环境配置到域名绑定的全流程，建议收藏后边看边操作。

 为什么选择 GitHub Pages + Hexo？

- 零成本：GitHub Pages 提供无限流量和 1GB 免费空间，无需购买服务器。
- 极速访问：静态页面天然具备 CDN 加速优势，国内访问速度优于传统虚拟主机。
- 版本管理：所有文章以 Markdown 格式储存在 Git 仓库，历史记录可追溯，永不丢失。

 第一步：环境准备（Node.js + Git）

前往 [Node.js 官网](https://nodejs.org/) 下载 LTS 版本并完成安装。随后配置 Git 用户信息：
```bash
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
```

 第二步：安装并初始化 Hexo

在本地新建博客目录，执行以下命令：
```bash
npm install -g hexo-cli
hexo init blog && cd blog
npm install
```
此时运行 `hexo s`，浏览器访问 `http://localhost:4000` 即可预览默认博客主题。

 第三步：部署到 GitHub Pages

1. 在 GitHub 新建仓库，命名为 `用户名.github.io`（必须完全匹配）。
2. 修改 `_config.yml` 文件：
```yaml
deploy:
  type: git
  repo: https://github.com/用户名/用户名.github.io.git
```
3. 一键部署：
```bash
npm install hexo-deployer-git --save
hexo d -g
```
浏览器访问 `https://用户名.github.io`，你的博客已正式上线！

 进阶技巧：自定义域名与 SEO 优化

- 绑定域名：在 CNAME 文件写入你的域名，并到 DNS 服务商添加 CNAME 记录指向 `用户名.github.io`。
- 收录优化：安装 `hexo-generator-sitemap` 插件，并在 Google Search Console 提交站点地图，加速搜索引擎收录。

遇到部署报错？评论区分你的报错截图，我会第一时间协助排查。觉得有用请点个 Star 支持一下，你的鼓励是我持续输出的动力！

相关推荐：

https://github.com/yangpatricia1/ybxyao/blob/main/2026%E5%AE%98%E6%96%B9%E6%89%8B%E5%86%8C%EF%BC%9AV8%E4%B8%BB%E7%AE%A1%E7%BD%91%E5%9D%80_%E8%AF%B1%E5%93%A6%E9%9F%B6%E7%97%98%E7%82%AFDDRYT.md

<img src="https://i.postimg.cc/fLkFgvHt/V8-00020.png" />

相关推荐：

https://github.com/yangpatricia1/ybxyao/commit/c36857a74ae4c73334633cbb3f410522e6f0c810

<img src="https://i.postimg.cc/J7sVTRgT/V8-00010.png" />
相关推荐：

https://github.com/clarkalyssa3349/mrznkk/blob/main/2026%E5%AE%98%E6%96%B9%E6%80%BB%E7%BB%93%EF%BC%9AV8%E4%B8%BB%E7%AE%A1%E6%B5%8B%E9%80%9F_%E6%8E%B7%E5%89%BF%E7%AC%9B%E7%9E%8E%E8%BE%9BSMFOI.md

<img src="https://i.postimg.cc/13Zk5wzH/V8-00013.png" />
相关推荐：

https://github.com/clarkalyssa3349/mrznkk/commit/5e8bbcd99f970eb671e5eec6ce4ac361fb4ec5c4

<img src="https://i.postimg.cc/3Rw9xJm7/V8-00005.png" />

资讯来源：新华网、人民网、央视新闻、中新网、凤凰网、澎湃新闻、界面新闻、新浪新闻、搜狐网、财新网、观察者网、第一财经等主流平台，以独树一帜的观察视角与扎实的深度报道能力，在资讯领域收获广泛关注。
