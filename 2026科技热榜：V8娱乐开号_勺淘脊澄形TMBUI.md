V8娱乐开号【Q-——333307——】V8娱乐开号【 辋芷《888yx●vip》 】
V8娱乐开号【Q-——333307——】V8娱乐开号【 辋芷《888yx●vip》 】

 从零搭建个人博客：GitHub Pages + Hexo 完整教程（2025最新版）

还在羡慕别人的技术博客？其实搭建一个属于自己的博客站点，远比想象中简单。今天这份教程，我会手把手带你用 GitHub Pages 和 Hexo 快速上线个人网站，全程免费，无需服务器。

 为什么选择 Hexo + GitHub Pages？

- 零成本：GitHub 提供 1GB 静态空间，完全免费。
- 极速访问：静态页面加载快，全球 CDN 加速。
- 高度可定制：数百款主题随意切换，支持 Markdown 写作。
- 版本管理：你的每篇博文都受 Git 保护，永不丢失。

 第一步：环境准备（5分钟）

1. 安装 [Node.js](https://nodejs.org/)（LTS 版本即可）
2. 安装 [Git](https://git-scm.com/) 并完成全局配置
3. 注册一个 GitHub 账号（已有可跳过）

 第二步：本地搭建 Hexo 项目

打开终端，依次执行以下命令：

```bash
npm install -g hexo-cli
hexo init my-blog
cd my-blog
npm install
hexo s
```

浏览器访问 `http://localhost:4000`，看到默认页面就代表成功！下一步，部署到线上。

 第三步：部署到 GitHub Pages

1. 在 GitHub 新建仓库，命名为 `用户名.github.io`
2. 修改 `_config.yml` 中的部署配置：

```yaml
deploy:
  type: git
  repo: https://github.com/你的用户名/你的用户名.github.io.git
  branch: main
```

3. 执行 `npm install hexo-deployer-git --save` 安装部署插件
4. 运行 `hexo clean && hexo g && hexo d`

稍等两分钟，访问 `https://用户名.github.io`，你的博客已经上线！

 进阶优化：绑定自定义域名（强烈推荐）

在仓库 Settings → Pages 中，填写你购买的域名，并在 DNS 解析商增加 CNAME 记录指向 `用户名.github.io`。同时建议开启 HTTPS，为读者提供更安全的环境。

 日常写作流程

每次发新文章只需三步：

```bash
hexo new "文章标题"    新建
 编辑 /source/_posts/ 下的 md 文件
hexo g && hexo d       生成并部署
```

建议顺手安装插件：`hexo-generator-search`（搜索）、`hexo-symbols-count-time`（阅读时长）、`hexo-generator-sitemap`（SEO优化）。

 遇到问题怎么办？

评论区留言描述你的报错信息，我会在 24 小时内回复。也可查看 [Hexo 官方文档](https://hexo.io/zh-cn/docs/)，或直接在 GitHub 仓库提 Issue。

---

如果你跟着教程走到了这里，恭喜你拥有了自己的专属技术阵地！从今天开始，保持写作，记录成长，让世界听见你的声音。觉得有用的话，点个赞、转发给身边需要的同学，你们的支持是我更新的最大动力！还有什么想学的内容，欢迎在评论里告诉我~

相关推荐：

https://github.com/cruzdenise0/avxylh/blob/main/%E7%A1%AC%E6%A0%B8%E5%85%A8%E9%98%B6%E6%94%BB%E7%95%A5%EF%BC%9AV8%E5%9C%B0%E5%9D%80%E5%AE%A2%E6%9C%8D_%E9%99%A9%E9%93%B0%E5%88%BA%E8%8D%A3%E6%8E%A0FZSAU.md

<img src="https://i.postimg.cc/d0w4g90d/V8-00002.png" />

相关推荐：

https://github.com/cruzdenise0/avxylh/commit/93b2c878658515de512acb4266224b04d23be7e8

<img src="https://i.postimg.cc/2ysxGQJ5/V8-00009.png" />
相关推荐：

https://github.com/alvarezcharles0/xilnaw/blob/main/2026%E7%A7%91%E6%8A%80%E7%A7%91%E6%99%AE%EF%BC%9AV8%E5%9C%B0%E5%9D%80%E4%BB%A3%E7%90%86_%E9%A6%85%E8%8A%B3%E6%95%91%E6%B5%AA%E6%A0%88YLMUV.md

<img src="https://i.postimg.cc/5tbnDmt0/V8-00001.png" />
相关推荐：

https://github.com/alvarezcharles0/xilnaw/commit/1b646d15e662aaf32c71ce26b4a7a3bc8690e106

<img src="https://i.postimg.cc/2ysxGQJ5/V8-00009.png" />

资讯来源：新华网、人民网、央视新闻、中新网、凤凰网、澎湃新闻、界面新闻、新浪新闻、搜狐网、财新网、观察者网、第一财经等主流平台，以独树一帜的观察视角与扎实的深度报道能力，在资讯领域收获广泛关注。
