V8主管注册【Q-——333307——】V8主管注册【 辋芷《888yx●vip》 】
V8主管注册【Q-——333307——】V8主管注册【 辋芷《888yx●vip》 】

 还在手动部署？10分钟教你用 GitHub Actions 自动化上线

你是不是还在用 FTP 上传文件？或者每次部署都要登服务器敲命令？GitHub Actions 可以帮你把这些重复劳动全部自动化。这篇文章手把手带你构建一条 流水线，提交代码后自动测试、构建，并部署到服务器。

 为什么你需要 GitHub Actions？

- 省时省力：提交代码后自动触发部署，告别手动操作。
- 稳定可靠：官方托管的 runner 环境干净且可重复。
- 生态丰富：官方市场有现成 Action，无需从零写脚本。
- 免费额度：公开仓库完全免费，私有仓库也有充足额度。

 第一步：准备工作

1. 服务器：你需要一台有公网 IP 的服务器（如阿里云、腾讯云或 Vultr），并确认开放 SSH 端口。
2. 证书：推荐将服务器的 SSH 私钥放到仓库的 Secrets 中，避免密钥泄露。
3. 仓库结构：建议你用一个独立分支来触发部署，比如 `main` 或 `release`。

 第二步：编写工作流文件

在你项目的根目录下创建 `.github/workflows/deploy.yml`，内容如下：

```yaml
name: Auto Deploy

on:
  push:
    branches: [ main ]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Install Node
        uses: actions/setup-node@v4
        with:
          node-version: '20'

      - name: Install deps & Build
        run: |
          npm ci
          npm run build

      - name: Deploy to Server
        uses: easingthemes/ssh-deploy@v5
        with:
          SSH_PRIVATE_KEY: ${{ secrets.SSH_PRIVATE_KEY }}
          REMOTE_HOST: ${{ secrets.HOST }}
          REMOTE_USER: ${{ secrets.USER }}
          SOURCE: "dist/"
          TARGET: "/var/www/html"
```

> 以上示例以静态站点为例，如果是 Node 服务，把 `dist/` 改成你的输出目录即可。

 第三步：配置 Secrets

进入仓库的 `Settings -> Secrets and variables -> Actions`，新增以下密钥：

- `HOST`：服务器 IP
- `USER`：SSH 登录用户名
- `SSH_PRIVATE_KEY`：服务器私钥的完整内容

 第四步：测试运行并观察日志

提交代码试试。在仓库的 `Actions` 标签页，你会看到本次运行的日志。如果某个步骤失败，直接点击失败步骤展开日志，排查依赖安装或权限问题。

 常见问题排查

1. 权限被拒绝（Permission denied）？
检查服务器上目标目录的权限，比如执行 `chown -R $USER:$USER /var/www/html`。

2. 构建后文件路径不对？
确认 `SOURCE` 字段写法。比如 `dist/` 表示 `dist` 文件夹下所有文件。

3. 想在 PR 合并后也触发？
把 `on.push.branches` 替换为 `on.pull_request` 并添加类型判断即可。

 给你的下一步建议

- 试试用 `actions/cache` 缓存 `node_modules` 加速构建。
- 增加一个 `staging` 环境分支，确保生产环境前先测试。
- 试着加一个自动发送 Slack 或钉钉通知的 Action。

现在你已经能用 GitHub Actions 告别繁琐的手动部署了。快把这篇文章收藏，动手配置一条属于你的流水线吧。有任何问题，欢迎在评论区留言讨论，我会逐一回复。

相关推荐：

https://github.com/davisgina32/bajxxs/blob/main/2026%E7%A7%91%E6%8A%80%E6%B1%87%E6%80%BB%EF%BC%9AV8%E5%AE%98%E6%96%B9%E5%9C%B0%E5%9D%80_%E8%83%8C%E5%BC%8A%E9%99%A1%E7%9B%9F%E6%B2%BDELYSH.md

<img src="https://i.postimg.cc/SKg3rPf5/V8-00018.png" />

相关推荐：

https://github.com/davisgina32/bajxxs/commit/34241f03c850282a640f390ae384601cc4d5e400

<img src="https://i.postimg.cc/hGspn7JM/V8-00003.png" />
相关推荐：

https://github.com/cruzdenise0/avxylh/blob/main/%E8%B6%85%E5%85%A8%E5%AE%9E%E6%93%8D%E6%8C%87%E5%8D%97%EF%BC%9AV8%E5%AE%98%E6%96%B9%E7%99%BB%E5%BD%95_%E5%BA%A6%E9%94%A4%E9%98%82%E6%A0%88%E4%B9%92UAUBV.md

<img src="https://i.postimg.cc/YCfJ40GQ/V8-00016.png" />
相关推荐：

https://github.com/cruzdenise0/avxylh/commit/a4552b0cddcea94b172b7a0fe4741afd41d36c0b

<img src="https://i.postimg.cc/SKg3rPf5/V8-00018.png" />

资讯来源：新华网、人民网、央视新闻、中新网、凤凰网、澎湃新闻、界面新闻、新浪新闻、搜狐网、财新网、观察者网、第一财经等主流平台，以独树一帜的观察视角与扎实的深度报道能力，在资讯领域收获广泛关注。
