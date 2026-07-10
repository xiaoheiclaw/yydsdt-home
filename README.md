# app-yydsdt-home — yydsdt.com

**yydsdt.com 根域名首页导航**。静态单页，聚合个人投研看板与工具：

- 投研·看板：`gold`（黄金 regime）、`gpu`（GPU 租金）、`kr`（韩国资金流）、`aicapex`（AI 建设回本压力）
- 工具：`yijing`（大衍筮法）

纯静态 `index.html`，无构建。

## 部署

- **托管**：Vercel（项目 `yydsdt-home`，team `dtwsubs1-2274s-projects`）。
- **DNS**：Cloudflare 根域名 `yydsdt.com` CNAME → `cname.vercel-dns.com`（dns-only，CF apex flattening）。
- **CI**：GitHub Actions `deploy.yml`，push `main` → `vercel deploy --prod`。secrets：`VERCEL_TOKEN` / `VERCEL_ORG_ID` / `VERCEL_PROJECT_ID`。
- 手动：`source ~/.config/vercel-gold.env && npx vercel deploy --prod --token=$VERCEL_TOKEN`。

新增看板 → 在 `index.html` 加一张 `a.card`，push 即上线。
