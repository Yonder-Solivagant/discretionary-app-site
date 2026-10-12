# discretionary-app-site

Discretionary 应用的对外说明页，用于满足 Google OAuth 品牌配置（Branding）对
「应用首页」与「应用隐私权政策链接」的必填要求。

| 页面 | 用途 | Google 品牌页填法 |
|------|------|-------------------|
| `index.html` | 应用首页（说明应用做什么、数据访问范围、联系方式） | 站点根地址 |
| `privacy.html` | 隐私政策 | 站点根地址 + `/privacy.html` |

纯静态单文件，无构建步骤、无外部依赖、无追踪代码，样式全部内联。

## 部署

GitHub Pages（`main` 分支根目录）。启用命令：

```bash
gh api -X POST repos/Yonder-Solivagant/discretionary-app-site/pages \
  --input <(echo '{"build_type":"legacy","source":{"branch":"main","path":"/"}}')
```

## 备注

- 站点内容会公开可见，包含开发者姓名与联系邮箱（Google 品牌页要求政策页公开可访问）。
- 本仓库与《人工智能与数据分析》课程作业的个人主页仓库（`homepage-demo`）互不影响，
  刻意分开，避免把课程作业与第三方平台的合规页面混在一处。
