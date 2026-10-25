# xiaoqity.top

基于原有个人站模板的独立站点，使用 Vue 3 + Vite，通过 GitHub Pages 部署。

## 个人信息

- `.env.production`：公开的站点名称、简介、域名和功能配置；开发时也使用该配置。
- `src/assets/socialLinks.json`：社交链接。
- `src/assets/siteLinks.json`：个人网站及项目。
- 首页已配置 18 张气象工具和爱好者群跳转卡片，每页 6 张，共 3 页；名称和地址以 `siteLinks.json` 为准，QQ群使用提供的完整邀请链接。
- `src/assets/friendLinks.json`：友情链接。
- `public/images/icon/`：头像、浏览器和安装应用图标；替换头像时请同步更新这些图标。
- `package.json` 的 `github`：小淇的仓库 https://github.com/XiaoQimiaowu/site-home，设置页显示该源码入口。

所有 `VITE_` 配置均会进入浏览器，不要填写私密凭证。未配置歌单或天气 Key 时，对应功能不启用。

## 本地使用

使用 Node.js 22 和 pnpm 9.15.9。

```sh
pnpm install --frozen-lockfile
pnpm dev
pnpm build
pnpm preview
```

## GitHub Pages

1. 仓库管理员进入 Settings → Pages，将 Source 设为 GitHub Actions。
2. 在 Custom domain 中保存 `xiaoqity.top`。本项目资源路径按自定义域名根目录构建。
3. 在域名服务商处，为 `@` 添加四条 A 记录：`185.199.108.153`、`185.199.109.153`、`185.199.110.153`、`185.199.111.153`。
4. 等待 DNS 检查及 HTTPS 证书完成，启用 Enforce HTTPS。
5. `.github/workflows/pages.yml` 会在推送到 `main` 时安装依赖、构建并发布 `dist`；也可在 Actions 中手动运行 Deploy GitHub Pages。

官方说明：[自动部署](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages) · [域名设置](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)。

## 模板许可

沿用 Cats叶钻的个人站模板（基于 imsyy/home）。
