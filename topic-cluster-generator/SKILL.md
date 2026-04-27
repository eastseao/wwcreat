---
name: topic-cluster-generator
description: 生成主题簇并自动输出可直接发布的高质量文章草稿（SEO+爆款+去AI味）
version: 1.0.0
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