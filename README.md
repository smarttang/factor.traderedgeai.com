# TraderEdgAI Factor 官网

本目录为 TraderEdgAI 因子框架与因子库的静态官网，参考 [ChatShuttle](https://www.chatshuttle.ai/) 的布局与风格。

## 内容结构

- **index.html**：首页（Hero、如何上手、核心能力、产品、因子库、下载、定价、FAQ）。
- **api.html**：API 文档独立页面（类型与常量、TEA_* 统一 API、Nexus/Trend 因子 API），首页「查看 API 文档」与页脚「API 文档」链接至本页。
- **Hero**：一句话介绍 + 免费下载 / 定价入口
- **因子框架介绍**：统一 API、标准输出、多因子汇总
- **因子库介绍**：EntropyHedge、TrendPenalty 及扩展说明
- **DLL 发布版本下载**：版本列表与下载链接（需自行替换为真实发布地址）
- **安装指南**：下载 → 部署 DLL → 部署头文件 → EA 引用
- **常见问题**：免费版范围、专业版区别、32/64 位、多因子汇总、可选字段约定
- **定价**：免费版（$0，30 天限制、部分因子、ISSUE 支持）与专业版（$20/月，人工支持、年度送 2 个月、BUG 当天关闭）

## 本地预览

在项目根目录或本目录启动静态服务即可预览，例如：

```bash
# 若已安装 Python 3
cd website && python3 -m http.server 8080
# 浏览器打开 http://localhost:8080
```

或使用任意静态服务器（如 `npx serve website`）。

## 发布与下载链接

- `index.html` 中下载链接默认为相对路径：`releases/v1.0/TraderEdgAIFactor.dll`、`releases/v1.0/mql4-include.zip`。
- 部署时请：
  1. 在 `website/releases/` 下按版本放置 DLL 与 zip（如 `v1.0/`），或
  2. 将上述链接改为你的 CDN / GitHub Releases 等真实 URL。

## 部署

将 `website/` 目录整体部署到任意静态托管（如 GitHub Pages、Netlify、Vercel、自有 Nginx）即可。无需服务端逻辑。
