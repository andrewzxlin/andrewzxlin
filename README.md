# Andrew Lin

我正在建立一組面向 **Agentic Workflow / LLM Engineering / AI Automation** 的作品集。重點不是做單一 chatbot，而是展示如何把 LLM 接進可驗證、可觀測、可審核的工作流。

## Portfolio Focus

- Agentic workflow orchestration
- Tool use / routing / structured output
- RAG、citations、confidence、evals
- Guardrails 與 human-in-the-loop
- Code-aware review agents
- Observability：traces、latency、tokens、cost、failure states

## Featured Projects

| 專案 | 展示能力 | Repo |
|---|---|---|
| Agentic Idea Validator | startup idea 拆解、競品 mapping、risk critic、scoring、7 天驗證計畫 | [agentic-idea-validator](https://github.com/andrewzxlin/agentic-idea-validator) |
| Customer Reply Agent | intent routing、evidence timeline、guardrails、human approval package | [customer-reply-agent](https://github.com/andrewzxlin/customer-reply-agent) |
| RAG Knowledge Base with Evals | ingestion、chunking、retrieval、citations、confidence、low-confidence fallback、evals | [rag-knowledgebase-evals](https://github.com/andrewzxlin/rag-knowledgebase-evals) |
| Repo PR Review Agent | unified diff parsing、code-aware risk detection、structured findings、test suggestions | [repo-pr-review-agent](https://github.com/andrewzxlin/repo-pr-review-agent) |
| Agent Observability Dashboard | JSONL traces、run/step metrics、latency、tokens、cost estimate、failure analysis、HTML report | [agent-observability-dashboard](https://github.com/andrewzxlin/agent-observability-dashboard) |

## Engineering Principles

這些作品刻意先採用 deterministic workflow，而不是一開始就依賴外部 LLM API。原因是：

1. 可以本機直接跑 demo 和測試。
2. 每個 workflow step 都能被單獨檢查。
3. eval cases 可以穩定驗證，不會因模型輸出波動而失真。
4. 之後可以把 deterministic step 替換成 OpenAI、Anthropic、LangGraph 或 Agents SDK。

每個專案都包含中文 README、中文架構文件、可重現 CLI demo 與 regression tests。

## What I Am Building Toward

我想把自己定位成：

> Full-stack / AI Engineer focused on agentic workflows, LLM evaluation, RAG, guardrails, and production automation.

下一步會補強：

- OpenAI Agents SDK / LangGraph integration
- GitHub Actions / CI demos
- OpenTelemetry 或 AgentOps 類 observability
- 更完整的 eval suites
- Web UI demos

## Resume Bullets

- Built multiple agentic workflow projects covering market research, customer support drafting, RAG retrieval, PR review, and observability.
- Designed deterministic eval suites for routing, retrieval quality, guardrails, risk detection, and trace aggregation.
- Implemented portfolio projects with Chinese documentation, reproducible CLI demos, structured outputs, and GitHub-ready READMEs.
