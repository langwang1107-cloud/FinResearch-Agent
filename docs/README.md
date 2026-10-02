# FinResearch-Agent

一个面向金融投研场景的智能分析 Agent 系统，基于 LangGraph、RAG 和大模型构建，支持股票行情、财经新闻、SEC 财报检索、财报问答、风险分析及结构化研报生成。

## 项目功能

- 股票行情与基础财务数据查询
- 财经新闻检索与事件分析
- SEC 10-K / 10-Q 财报获取与解析
- 基于 RAG 的财报知识检索与问答
- 基于 LangGraph + ReAct 的智能工具调用
- 结构化金融研报自动生成
- 基于 LLM-as-Judge 的结果可信度评测

## 技术栈

- Agent：LangGraph、ReAct、Tool Calling
- RAG：LlamaIndex、Pinecone、BGE Embedding
- 数据源：yfinance、NewsAPI、SEC EDGAR
- 后端：FastAPI、Celery
- 数据存储：Redis、PostgreSQL
- 模型评测：LLM-as-Judge
- 部署：Docker、vLLM

## 系统流程

```text
用户问题
   ↓
LangGraph Agent
   ↓
工具选择与任务执行
   ├── 股票行情
   ├── 财经新闻
   ├── SEC 财报
   └── 财报 RAG
          ↓
      大模型分析
          ↓
     结构化金融研报
          ↓
      可信度评测
