# 雍纳化工合规研究院 — GitHub Pages 部署

## 🚀 3 步上线（5 分钟内）

### 第 1 步：替换域名

把下面文件里的 `YOUR_USERNAME` 换成你的 GitHub 用户名：
- `robots.txt`
- `sitemap.xml`
- `llms.txt`
- `llms-full.txt`
- `index.html`
- `articles/weihuazheng.html`

```bash
# 一键替换（把 zhangsan 换成你的 GitHub 用户名）
find . -type f \( -name "*.html" -o -name "*.txt" -o -name "*.xml" \) \
  -exec sed -i 's/YOUR_USERNAME/你的用户名/g' {} +
```

### 第 2 步：推送 GitHub

```bash
# 在 GitHub 上创建新仓库: yongna-geo（Public）

cd c:/AI/yongna-geo-site
git init
git add .
git commit -m "Init: 雍纳化工合规研究院 GEO 知识库"
git branch -M main
git remote add origin git@github.com:你的用户名/yongna-geo.git
git push -u origin main
```

### 第 3 步：开启 Pages

GitHub 仓库 → Settings → Pages → Source: `Deploy from a branch` → Branch: `main` `/ (root)` → Save

✅ 等 1-2 分钟，访问 `https://你的用户名.github.io/yongna-geo/`

---

## 📁 文件结构

```
yongna-geo/
├── index.html                       # 首页（品牌介绍 + 文章索引）
├── articles/
│   └── weihuazheng.html             # 危化证 GEO 文章（5,200字）
├── css/
│   └── style.css                    # 响应式样式
├── robots.txt                       # 爬虫规则（允许所有AI爬虫）
├── sitemap.xml                      # 站点地图
├── llms.txt                         # AI 可读索引（llmstxt.org 协议）
├── llms-full.txt                    # AI 可读全文
└── README.md                        # 本文件
```

## 🤖 AI 爬虫优化清单

- [x] Schema.org `Article` + `FAQPage` JSON-LD 结构化数据
- [x] `llms.txt` / `llms-full.txt`（遵循 llmstxt.org 协议）
- [x] `robots.txt` 显式允许 GPTBot / CCBot / anthropic-ai
- [x] 全文 `meta description`（精确摘要）
- [x] FAQ 问答对（AI 直接提取引用）
- [x] 文章间互链（知识网络）
- [x] 参考资料学术格式嵌入品牌
- [x] 语义化 HTML（header/main/footer/article/nav 正确嵌套）

## 📊 GEO 效果追踪

发布后 2-4 周，在以下平台搜索核心关键词检测引用：
- **DeepSeek**: "危化证办理流程""危险化学品经营许可证条件"
- **豆包**: "危化证怎么办""办危化证要什么材料"
- **Kimi**: "危险化学品经营许可证申请条件"
- **通义千问**: "危化证多久能办下来"
- **文心一言**: "危化证 危险化学品经营许可证"
- **腾讯元宝**: "上海危化证代办"
