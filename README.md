# SupChat Website

SupChat 的线上页面仓（法律页起步，后续官网可并入本仓）。Vercel 挂 GitHub 自动部署：push 到 `main` 即上线。

## 页面

| 路径 | 文件 | 说明 |
| --- | --- | --- |
| `/privacy` | `privacy.html` | 隐私政策 |
| `/terms` | `terms.html` | 服务条款 |
| `/` | — | 跳转到 `/privacy`（见 `vercel.json`） |

- `cleanUrls: true`：URL 不带 `.html` 后缀。
- **路径口径**：`/privacy`、`/terms` 与 App 内 `LegalLinks`（`supchat.app/privacy|terms`）一致——域名挂上后 App 侧只改域名部分。
- 两页零外部依赖（无外链 CSS/JS/字体，favicon 内嵌），纯静态。

## 维护

- 文案修改：直接改 `*.html`，push 即部署。
- 开发者主体 / 通用法律条款单源：工作区 `product/legal-common.md`（改主体名、通用条款时先改那里，再同步本仓与 Pawloggy 官网仓）。
- 联系邮箱 / 版权行等事实变更：同步 `legal-common.md` §1。
