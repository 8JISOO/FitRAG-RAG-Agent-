# FitRAG

🚀 **FitRAG 是一个基于 RAG 与 Agent 架构的智能减脂辅助系统，结合知识库问答与个性化方案生成，帮助用户科学制定饮食与训练计划。**

---

## 📌 项目简介

FitRAG 旨在解决传统大模型在健康与减脂场景中“回答不准确、缺乏依据”的问题。
通过引入 **RAG（检索增强生成）** 技术构建专业知识库，并结合 **Agent 任务规划能力**，实现从知识问答到个性化减脂方案生成的完整闭环。

---

## ✨ 核心功能

* 📚 **知识问答（RAG）**

  * 基于专业减脂/营养知识库进行问答
  * 支持答案来源溯源（可解释性）

* 🧠 **个性化减脂方案生成（Agent）**

  * 根据用户身体数据生成专属饮食与训练计划
  * 支持多维度输入（身高、体重、年龄等）

* 📊 **健康指标计算**

  * BMI（身体质量指数）
  * BMR（基础代谢率）
  * TDEE（每日能量消耗）

* 🤖 **任务级智能决策**

  * 自动识别用户意图（问答 / 计划生成 / 计算）
  * 调用不同模块完成任务

---

## 🛠 技术栈

* **后端框架：** FastAPI
* **RAG框架：** LangChain
* **向量数据库：** FAISS
* **前端框架：** Streamlit
* **大模型：** OpenAI / DeepSeek

---

## 🏗 系统架构

```text   ' ' '文本
用户输入
   ↓
Agent（意图识别 & 任务规划）
   ↓
├── RAG模块（知识检索）
├── 计算模块（BMI / 热量）
   ↓
LLM生成结果
   ↓
返回个性化方案
```

---

## 📂 项目结构

```text   ' ' '文本
fitrag/
│
├── backend/              # 后端服务
│   ├── api/              # 接口层
│   ├── rag/              # RAG模块
│   ├── agent/            # Agent模块
│   ├── services/         # 计算服务
│   ├── llm/              # 大模型调用
│
├── frontend/             # 前端（Streamlit）
│
├── data/                 # 知识库数据
├── vector_store/         # 向量数据库
│
├── docs/                 # 项目文档（架构/接口）
├── tests/                # 测试代码
│
├── requirements.txt
└── README.md
```

---

## 🚀 快速开始

### 1️⃣ 克隆项目

```bash   ”“bash   “bash”;“bash```bash   ”“bash   “bash”;“bash
git clone https://github.com/你的用户名/fitrag.git
cd fitrag
```

---```bash   ”“bash   “bash”;“bash

### 2️⃣ 安装依赖

```bash   ”“bash   “bash”;“bash```bash   ”“bash   “bash”;“bash
pip install -r requirements.txtPIP install -r requirements.txt
```

---

### 3️⃣ 启动后端服务

```bash   ”“bash   “bash”;“bash
uvicorn backend.main:app --reloaduvicorn后端。主要:应用——重载
```

---

### 4️⃣ 启动前端（可选）

```bash   ”“bash   “bash”;“bash```bash   ”“bash   “bash”;“bash
streamlit run frontend/app.py流光运行前端/app.py
```

---

## 📖 使用示例

### 💬 知识问答

```text   ' ' '文本
减脂期间可以吃米饭吗？
```

---

### 🧠 生成减脂方案

输入：

```json   ' ' ' json‘ ’ ‘ json ’ ‘ ’ ' json
{
  "weight": 85,   "weight": 85,"weight": 85,   "weight": 85,
  "height": 180,   "height": 180,"height": 180,   "height": 180,
  "age": 22,   "age": 22,"age": 22,   "age": 22,"age": 22,   "age": 22,"age": 22,   "age": 22,
  "gender": "male"   "gender": "male""gender": "male"   "gender": "male"
}
```

输出：

```text   ' ' '文本
个性化饮食 + 训练计划
```

---

## 🧩 项目亮点

* ✅ 基于 RAG 提升大模型回答准确性，减少“幻觉问题”
* ✅ 引入 Agent 实现任务级智能，而非简单问答
* ✅ 结合规则计算与大模型生成，提高结果可靠性
* ✅ 支持结果溯源，增强系统可解释性

---

## 🚧 开发计划

* [x] 项目初始化与架构设计
* [ ] RAG知识库构建
* [ ] Agent任务调度实现
* [ ] 前端交互界面
* [ ] 个性化推荐优化

---

## 📌 未来优化方向

* 🔄 多用户系统支持
* 📊 数据可视化（体重变化趋势）
* 🧠 更精细化饮食推荐模型
* ☁️ 云端部署与API服务化

---

## 📄 License   # #📄勘探许可证

MIT License   与条款

---

## 👨‍💻 作者

温俊杰

---
