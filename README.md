# 谷歌评论 API

[![Promo](https://github.com/bright-cn/LinkedIn-Scraper/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://www.bright.cn/products/serp-api/google-search/reviews)

本仓库提供两种获取 Google 评论数据的方法：

1. 免费爬虫：适用于小型项目、测试、个人研究与教学场景的轻量方案。
2. Bright Data 谷歌评论 API：企业级、高并发、稳定可靠的数据提取方案，属于 [SERP API](https://www.bright.cn/products/serp-api) 的一部分。

## 目录

- [免费爬虫](#免费爬虫)
  - [设置](#设置)
  - [快速开始](#快速开始)
  - [示例输出](#示例输出)
  - [限制](#限制)
- [Bright Data 企业级解决方案](#bright-data-企业级解决方案)
  - [开始使用](#开始使用)
  - [直接 API 访问](#直接-api-访问)
  - [原生代理访问](#原生代理访问)
- [高级功能](#高级功能)
  - [功能 ID（fid）](#功能-id（fid）)
  - [本地化（hl）](#本地化（hl）)
  - [排序与过滤](#排序与过滤)
  - [分页](#分页)
- [支持与资源](#支持与资源)

## 免费爬虫
适合需要小规模提取评论的用户，快速上手、开箱即用。

<img width="700" alt="scrape-google-reviews-pizza-place" src="https://github.com/bright-cn/google-reviews-api/blob/main/images/420648584-8f8069c4-3521-49d1-ba77-8eb6e840de2b.png" />

### 设置

要求：

- Python 3.9 或更高版本
- 用于浏览器自动化的 [Playwright](https://playwright.dev/)

安装：

```bash
pip install playwright
playwright install
```

> 刚接触网络爬取？请查看我们的[Python 爬虫新手指南](https://www.bright.cn/blog/how-tos/web-scraping-with-python)。

### 快速开始

1. 打开 [google-reviews-scraper.py](https://github.com/bright-cn/Google-Reviews-API/blob/main/google-reviews-scraper/google-reviews-scraper.py) 并更新以下变量：
    - `url`：目标商家的 Google 地图 URL
    - `target_reviews`：需要抓取的评论数量
2. 运行脚本。

💡 提示：将 `HEADLESS = False` 可降低被谷歌反爬系统识别的概率。

### 示例输出

```json
{
    "reviewer_name": "Christopher Huntley (youcancallmemaurice)",
    "reviewer_link": "https://www.google.com/maps/contrib/116348973042381100705/reviews?hl=en-GB",
    "reviewer_image": "https://lh3.googleusercontent.com/a-/ALV-UjXgKzymRM7WTYFkhDuA2_lN5WfE7EYAoBAFPOf2YGxA1e_s72zD9A=w36-h36-p-rp-mo-ba5-br100",
    "rating": 5,
    "date": "a month ago",
    "text": "We took a local tip for the best pizza in Chicago. It's a dive vibe with a very regimented process. The garlic bread was good and the dipping sauce was a nice touch.\n\nPizza came fairly quickly. A standard deep dish with sausage, onion and pepper. Good crust, good flavor for sauce and toppings were perfect.\n\nService was quick and attentive. A great experience.",
    "photos": [
        "https://lh3.googleusercontent.com/geougc-cs/AIHozJIkCwzdm33OdIVsHIJcqdLPauk-Q3Xk0rRjj4SrzOaiMF1L_uQFW4T7jg86meLyB6So7wsJX0Pk6m8NuxUbUF_1OTvutnqJbmwU2olmmiS5Z1A6puOo8oPD6qqBSG0TXO5KyM_B=w300-h450-p",
        "https://lh3.googleusercontent.com/geougc-cs/AIHozJKiYAPlUmW7O1M79DDjuRgbeOJ92t2IqwuUDOXUFOABH6XBoZet4bGsYV_NxK1z2SkaFLktjjaAs1FoI2XMEwjt9uMZKQX2K904RjyymLZ1SA4LKq_a3vttOPJr7bMTJCpEx-Y=w300-h225-p",
        "https://lh3.googleusercontent.com/geougc-cs/AIHozJKvdP93huqqhLlxZZDv3VKpNYVriS8qq8lKoGiFydTTDAgZOtupYcgxfaSu4KPbE4wX16lD4sXMOY10vLRVk8_mrMe2N4Ul9hX1h46-JJ0rCmZcDcXogMr_YlIDIp_ao_S_wxVQgQ=w300-h225-p"
    ],
    "likes_count": "4"
}
```

👉 查看[完整 JSON 输出](https://github.com/bright-cn/Google-Reviews-API/blob/main/google-reviews-results/reviews_output.json)。

### 限制

免费爬虫存在以下限制：

- IP 被封风险高
- 请求量受限
- 容易遇到验证码
- 不适合大规模、稳定抓取

若需可靠的大规模数据采集，请考虑更高级的方案。

## Bright Data 企业级解决方案

[Bright Data 的谷歌评论 API](https://www.bright.cn/products/serp-api/google-search/reviews) 提供结构化评论数据，具备高级特性与可扩展性。基于与 [SERP API](https://www.bright.cn/products/serp-api) 相同的先进技术，优势包括：

- **全球位置精准**：可定向任意地理位置
- **按成功付费**：仅为成功的请求付费
- **实时数据**：秒级获取最新评论
- **可扩展性**：不限请求量
- **成本效率**：节省基础设施与维护成本
- **高可靠性**：内置反封锁措施，表现稳定
- **技术支持**：专家随时协助

### 开始使用

1. **前置条件**：
    - 注册 [Bright Data 账号](https://www.bright.cn/)（新用户赠送 $5 额度）
    - 获取[API 密钥](https://docs.brightdata.com/general/account/api-token)
2. **设置**：按照我们的[分步指南](https://github.com/bright-cn/Google-Reviews-API/blob/main/setup-serp-api-guide.md)集成 API
3. **接入方式**：
    - 直接 API 访问
    - 原生代理访问

### 直接 API 访问

直接向 API 端点发起请求。

cURL 示例：

```bash
curl https://api.brightdata.com/request \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer API_TOKEN" \
  -d '{
        "zone": "ZONE_NAME",
        "url": "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&brd_json=1",
        "format": "raw"
      }'
```

Python 示例：

```python
import requests
import json

url = "https://api.brightdata.com/request"
headers = {"Content-Type": "application/json", "Authorization": "Bearer API_TOKEN"}

payload = {
    "zone": "ZONE_NAME",
    "url": "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&brd_json=1",
    "format": "raw",
}

response = requests.post(url, headers=headers, json=payload)

with open("serp-direct-api.json", "w") as file:
    json.dump(response.json(), file, indent=4)

print("Response saved to 'serp-direct-api.json'.")
```

👉 查看[完整 JSON 输出](https://github.com/bright-cn/Google-Reviews-API/blob/main/google-reviews-api-results/serp-direct-api.json)。

> 注意：使用 `brd_json=1` 获取解析后的 JSON，或使用 `brd_json=html` 获取“解析后的 JSON + 完整嵌套 HTML”。

### 原生代理访问

也可使用我们的代理路由方式：

cURL 示例：

```bash
curl -i \
  --proxy brd.superproxy.io:33335 \
  --proxy-user "brd-customer-<customer-id>-zone-<zone-name>:<zone-password>" \
  -k \
  "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&brd_json=1"
```

**Python 示例：**

```python
import requests
import urllib3

urllib3.disable_warnings(urllib3.exceptions.InsecureRequestWarning)

host = "brd.superproxy.io"
port = 33335
username = "brd-customer-<customer-id>-zone-<zone-name>"
password = "<zone-password>"
proxy_url = f"http://{username}:{password}@{host}:{port}"

proxies = {"http": proxy_url, "https": proxy_url}
url = "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&brd_json=html"
response = requests.get(url, proxies=proxies, verify=False)

with open("serp-native-proxy.json", "w", encoding="utf-8") as file:
    file.write(response.text)

print("Response saved to 'serp-native-proxy.json'.")
```

👉 查看[完整 JSON 输出](https://github.com/bright-cn/Google-Reviews-API/blob/main/google-reviews-api-results/serp-native-proxy.json)。

> 注意：生产环境中，请按我们的[SSL 证书指南](https://docs.brightdata.com/general/account/ssl-certificate)加载 Bright Data 的 SSL 证书。

## 高级功能
Bright Data 的 API 支持多种高级参数，帮助你精细化提取评论数据。

### 功能 ID（fid）
<img width="700" alt="scrape-google-reviews-building" src="https://github.com/bright-cn/google-reviews-api/blob/main/images/420657506-0bc3b223-adf4-487a-9c75-11679b16907d.png" />

Feature ID 是商家或地点的唯一标识。查找方法：

1. 搜索目标商家名称
2. 在搜索结果页面右键选择“查看页面源代码”
3. 在页面中搜索 “data-fid”
4. 你会看到类似格式：`"fid":"0x89c259a9b3117469:0xd134e199a405a163"`

### 本地化（hl）

<img width="700" alt="google-reviews-scraper-building" src="https://github.com/bright-cn/google-reviews-api/blob/main/images/420665500-0f1b630e-cb2a-4125-a7de-64be656a2f5b.png" />

通过两位语言代码指定首选语言。

**示例：**

```bash
curl --proxy brd.superproxy.io:33335 \
     --proxy-user brd-customer-<customer-id>-zone-<zone-name>:<zone-password> \
     "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&hl=fr"
```

该示例将返回法语评论。

### 排序与过滤

可通过查询参数对评论进行排序和过滤：

1. **sort**：控制排序方式。

    **可选值：**
    
    - `sort=qualityScore`（默认）——最相关的评论优先
    - `sort=newestFirst`——最新评论优先
    - `sort=ratingHigh`——高评分优先
    - `sort=ratingLow`——低评分优先
    
    **示例：**
    
    ```bash
      curl --proxy brd.superproxy.io:33335 \
           --proxy-user brd-customer-<customer-id>-zone-<zone-name>:<zone-password> \
           "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&sort=ratingLow"
    ```

  该示例将优先返回最低评分的评论。

2. **filter**：仅返回包含特定关键字的评论。

    **示例**：
   
    ```bash
    curl --proxy brd.superproxy.io:33335 \
         --proxy-user brd-customer-<customer-id>-zone-<zone-name>:<zone-password> \
         "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&filter=excellent"
    ```
    
    该示例仅返回包含 “excellent” 的评论。

### 分页

通过以下参数控制每页数量与分页：

1. **start**：结果偏移量，用于分页。
    - `start=0`（默认）——第一页
    - `start=10`——第二页
    - `start=20`——第三页
    
    **示例**：
    ```bash
    curl --proxy brd.superproxy.io:33335 \
         --proxy-user brd-customer-<customer-id>-zone-<zone-name>:<zone-password> \
         "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&start=10"
    ```
该示例将返回第二页评论。

2. **num**：每页返回的结果数量。
    - `num=10`（默认）——每页 10 条
    - `num=20`——每页 20 条（最大）
    
    **示例**：
   
    ```bash
    curl --proxy brd.superproxy.io:33335 \
         --proxy-user brd-customer-<customer-id>-zone-<zone-name>:<zone-password> \
         "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&num=20"
    ```
    
    该示例将一次返回 20 条评论。

## 支持与资源

- **文档**：[SERP API 文档](https://docs.brightdata.com/scraping-automation/serp-api/)
- **SEO 场景**：[SEO 监测与洞察](https://www.bright.cn/use-cases/serp-tracking)
- **其他指南**：[Web Unlocker API](https://github.com/bright-cn/web-unlocker-api)、[SERP API](https://github.com/bright-cn/serp-api)、[Google Search API](https://github.com/bright-cn/google-search-api)、[Google 新闻爬虫](https://github.com/bright-cn/Google-News-Scraper)、[Google 趋势 API](https://github.com/bright-cn/google-trends-api)
- **技术文章**：
  - [最佳 SERP API 盘点](https://www.bright.cn/blog/web-data/best-serp-apis)
  - [使用 SERP API 构建 RAG 聊天机器人](https://www.bright.cn/blog/web-data/build-a-rag-chatbot)
- **技术支持**：[联系我们](mailto:support@brightdata.com)
