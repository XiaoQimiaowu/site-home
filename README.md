# xiaoqity.top

基于原有个人站模板的独立站点，使用 Vue 3 + Vite，准备通过 GitHub 和 Vercel 部署。

## 个人信息

站主为小淇，头像使用站主提供的原图。简介：这里是小淇喵呜的个人站，建立于叶钻的小站的旁边。社交链接为小淇的 GitHub（https://github.com/XiaoQimiaowu）和 B 站主页（https://space.bilibili.com/2135134808）。友情链接仅保留叶钻猫猫的小站（https://raineko.net/），介绍为“做一颗星星，有棱有角，还会发光。”。个人项目、建站日期、备案及歌单尚未填写。

- `.env.production`：公开的站点名称、简介、域名和功能配置；开发时也使用该配置。
- `src/assets/socialLinks.json`：社交链接。
- `src/assets/siteLinks.json`：个人网站及项目。
- 首页已配置 16 张气象工具和爱好者群跳转卡片，每页 6 张，共 3 页；名称和地址以 `siteLinks.json` 为准，QQ群使用提供的完整邀请链接。
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

## GitHub 与 Vercel

1. 将本目录作为朋友 GitHub 仓库的根目录上传，不上传 `node_modules`、`dist`、`.env.local` 或 `.vercel`。
2. 在 Vercel 中导入该 GitHub 仓库，框架选择 Vite，根目录保持仓库根目录。构建设置已写入 `vercel.json`，输出目录为 `dist`。
3. 构建成功后，进入项目 Settings → Domains，添加 `xiaoqity.top`。
4. 在域名服务商处，按该项目实际显示的要求配置 DNS；确认域名验证和 HTTPS 均成功。
5. 后续向生产分支推送更新，由 Vercel 自动构建发布。

官方说明：[GitHub 部署](https://vercel.com/docs/git/vercel-for-github) · [域名设置](https://vercel.com/docs/domains/set-up-custom-domain)。

## 模板许可

沿用 Cats叶钻的个人站模板（基于 imsyy/home）。MIT 许可及原版权声明保留在 `LICENSE`；这些是模板来源记录，不是本站站主资料。
