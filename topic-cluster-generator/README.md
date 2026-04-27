
# 📦 主题簇生成技能 项目结构

```plaintext
topic-cluster-generator-v4/
├── skill.md
├── config.yaml
├── prompt/
│   ├── intent_parse.md
│   ├── seed_expand.md
│   ├── cluster_build.md
│   ├── seo_optimize.md
│   ├── draft_generate.md      # ⭐新增：文章生成核心
│   ├── deai.md                # ⭐去AI味
│   ├── explode.md             # ⭐爆款增强
│   ├── style_adapt.md         # ⭐平台适配
│   ├── output_format.md
├── templates/
│   ├── article.md             # ⭐文章模板
│   ├── cluster_table.md
│   ├── content_plan.md
├── memory/
│   └── Memory.md
```

---

# 🧠 skill.md（V4核心）

```markdown
---
name: TopicClusterGenerator
description: 生成主题簇并自动输出可直接发布的高质量文章草稿（SEO+爆款+去AI味）
version: 4.0.0
author: Gervas System Lab
tags:
  - SEO
  - 内容生成
  - 爆款文章
  - 自动写作
  - 内容矩阵
input_schema:
  core_topic:
    type: string
  target:
    type: string
  depth:
    type: integer
  audience:
    type: string
  platform:
    type: string
    description: 发布平台（公众号 / 小红书 / 知乎 / 网站）
  article_count:
    type: integer
    description: 生成文章数量
output_schema:
  clusters:
    type: list
  articles:
    type: list
    description: 可直接发布的文章
---

# 🧩 SKILL: Topic Cluster Generator V4

## 🎯 核心能力（V4）

在 V3 基础上升级：

✅ 自动生成主题簇  
✅ 自动生成选题  
✅ **批量生成完整文章（可发布）**  
✅ 去AI味（拟人化表达）  
✅ 爆款结构优化  
✅ 多平台适配  

---

## ⚙️ 工作流

### 1️⃣ 意图解析
`intent_parse.md`

---

### 2️⃣ 关键词扩展
`seed_expand.md`

---

### 3️⃣ 主题簇构建
`cluster_build.md`

---

### 4️⃣ SEO优化
`seo_optimize.md`

---

### 5️⃣ ✍️ 文章生成（核心）
`draft_generate.md`

对每个子主题生成：

- 标题（3个备选）
- 开头（强钩子）
- 正文结构
- 结尾（引导互动）

---

### 6️⃣ 🧠 去AI味
`deai.md`

处理：

- 去模板化
- 加入口语化
- 增加人类情绪

---

### 7️⃣ 🔥 爆款增强
`explode.md`

优化：

- 标题点击率
- 情绪张力
- 反常识点

---

### 8️⃣ 📱 平台适配
`style_adapt.md`

适配：

- 公众号：深度+逻辑
- 小红书：短句+种草
- 知乎：专业+结构
- 网站：SEO优先

---

### 9️⃣ 输出
`output_format.md`

---

## 🧠 Memory机制

记录：

- 已生成文章
- 已用标题
- 避免重复内容
```

---

# ⚙️ config.yaml（V4）

```yaml
version: 4.0

generation:
  article_length: 1200-2000
  paragraph_style: mixed
  tone: natural

content:
  hook_strength: high
  storytelling: true
  emotion_level: medium

seo:
  keyword_density: 1-2%
  include_h2_h3: true

explode:
  enable: true
  curiosity_gap: true
  emotional_trigger: true

deai:
  enable: true
  remove_patterns: true
  humanize: true

platform:
  wechat:
    style: 深度+故事
  xiaohongshu:
    style: 短句+情绪
  zhihu:
    style: 专业+结构
```

---

# ✍️ prompt/draft_generate.md（核心引擎）

```markdown
# 任务：生成完整文章草稿

输入：
- 子主题
- 关键词
- 目标人群
- 平台

输出一篇完整文章：

## 1. 标题（3个）
要求：
- 有吸引力
- 包含关键词
- 有点击欲

---

## 2. 开头（Hook）
- 提问 / 反常识 / 场景
- 3秒抓人

---

## 3. 正文

结构：

### H2 小标题
内容要：
- 有信息密度
- 有案例
- 有逻辑

---

## 4. 结尾

- 总结
- 引导互动
- CTA（评论 / 收藏）

---

要求：
- 不要模板化
- 像真人写的
```

---

# 🧠 prompt/deai.md（去AI味）

```markdown
# 去AI味处理

处理以下问题：

- 删除“首先/其次/最后”
- 避免教科书语气
- 增加口语表达
- 插入自然停顿
- 加入轻微情绪

目标：
让读者感觉是“人写的”
```

---

# 🔥 prompt/explode.md（爆款增强）

```markdown
# 爆款优化

增强：

1. 标题：
- 加入冲突
- 制造悬念

2. 内容：
- 加入反常识点
- 增加情绪波动

3. 结构：
- 前3段必须抓人
```

---

# 📱 prompt/style_adapt.md

```markdown
# 平台适配

根据 platform 调整：

公众号：
- 深度内容
- 段落适中

小红书：
- 短句
- 强情绪
- 多断句

知乎：
- 逻辑清晰
- 专业表达

网站：
- SEO优先
- 关键词自然分布
```

---

# 📝 templates/article.md

```markdown
# {{title}}

{{hook}}

---

## {{section1}}

内容

## {{section2}}

内容

---

## 总结

{{summary}}

👉 欢迎评论交流
```

---

# 📤 prompt/output_format.md

```markdown
# 输出结构

## 一、主题簇

## 二、文章列表

每篇文章包含：

- 标题（3个）
- 正文
- 关键词
- 适用平台

---

## 三、发布建议

- 发布时间
- 频率
```

---

# 🧠 memory/Memory.md

```markdown
# Memory

## 已生成文章
-

## 标题池
-

## 内容覆盖
-

## 未覆盖机会点
-
```

---

# 🚀 这套 V4 实际效果

你输入：

```yaml
core_topic: 枸杞菊花决明子饮
target: SEO+带货
depth: 3
audience: 养生人群
platform: 公众号
article_count: 5
```

👉 输出：

* 1套完整主题矩阵
* 5篇**可直接发布文章**
* 每篇：

  * 爆款标题
  * 完整正文
  * 已去AI味
  * 已SEO优化

---

# 🔥 可以再往上升级（下一步）

如果你要继续进化，我可以帮你做：

### V5（商业级）

* 接入真实搜索数据（百度/抖音）
* 自动判断“能不能爆”

### V6（自动赚钱）

* 自动插入带货结构
* 自动生成商品话术
* 转化率优化

### V7（内容工厂）

* 日更100篇
* 自动排期发布
* 多账号矩阵

---

