# 印尼电商选品：搜索 Skill 候选备份

核验日期：2026-10-21。本仓库收藏两个搜索 Skill：Tavily 保存源码及许可证，Firecrawl 保存固定版本引用。未安装 CLI 或验证实际搜索结果。

GitHub 没有统一的 Skill 用户评分。以下依据官方维护、Skills.sh 安装量、源码仓库星标和选品用途选择，不宣称全网绝对前二。星标属于整个源码仓库，而非单个 Skill。

| 候选 | Skills.sh 安装量 | GitHub 实时星标 | 建议用途 |
| --- | ---: | ---: | --- |
| firecrawl | 102.8K | 659 | 搜索发现来源，再提取公开竞品页面与商品信息 |
| tavily-search | 35.6K | 488 | 按国家、时间和域名搜索市场趋势、消费需求和行业信息 |

来源：
- https://www.skills.sh/firecrawl/cli/firecrawl
- https://www.skills.sh/tavily-ai/skills/tavily-search
- https://github.com/firecrawl/cli
- https://github.com/tavily-ai/skills

对照候选：parallel-web-search 安装量 14.3K、仓库 88 星；exa-search 安装量约 1.2K、仓库 58 星。安装量来自目录页面快照，可能滞后。没有使用主服务仓库的星标替代 Skill 所在仓库星标。

## 原始版本与许可

- Firecrawl：`firecrawl/cli`，commit `2de80d5c7a89cabfbf6aa4d068418eb569fbc273`，原目录 `skills/firecrawl/`。所查询源码树没有 LICENSE 文件，因此公开仓库仅保存官方链接、版本和安装入口，未重发其源码。见 firecrawl/README.md。
- Tavily：`tavily-ai/skills`，commit `778122e5f9c680f541eeceda5a5b36405eb7980c`，原目录 `skills/tavily-search/`。已保留 SKILL.md 和上游 MIT LICENSE。

当前副本是所选目录的备份，并非整个上游技能集合。相邻 Skill 的相对链接依赖上游仓库，完整使用时通过官方安装命令取得所需配套文件。

## 安装入口

```powershell
npx skills add https://github.com/firecrawl/cli --skill firecrawl
npx skills add https://github.com/tavily-ai/skills --skill tavily-search
```

Skill 文件提供操作说明；运行搜索仍需相应 CLI。Firecrawl 的安装和认证见 https://github.com/firecrawl/cli/blob/2de80d5c7a89cabfbf6aa4d068418eb569fbc273/skills/firecrawl/rules/install.md；Tavily 的设置见 https://github.com/tavily-ai/skills/blob/778122e5f9c680f541eeceda5a5b36405eb7980c/skills/tavily-cli/SKILL.md 。当前版本两者均描述有限免密额度，持续使用可能需要登录、API Key 或付费额度，以服务当前规则为准。

## 印尼选品使用方式

先用 Tavily 搜索印尼语和英语需求词，例如 `produk rumah tangga viral Indonesia`、`keluhan pembeli organizer dapur Indonesia`。按最近一个月或季度筛选，记录来源日期。

再用 Firecrawl 读取搜索找到的公开商品、品牌和评测页面，整理商品名、价格（IDR）、规格、评论痛点、卖家与来源 URL。Shopee、Tokopedia、TikTok Shop 等页面能否获取需实际验证；搜索结果不是平台真实销量，不把估计值当作已验证销售数据。

建议输出字段：品类、印尼语关键词、目标人群、价格区间、竞品链接、评价痛点、体积重量、证据日期、待核验事项。搜索工具用于搜集证据，不能单独证明利润或销量。
