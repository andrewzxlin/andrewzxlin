# Andrew Lin

我正在建立一組 **Agentic Workflow / LLM Engineering / AI Automation** 實驗專案。重點不是做單一 chatbot，而是把 LLM 系統拆成可觀察、可測試、可審核、可延伸的工作流。

## 這組專案在補哪張學習拼圖

| 拼圖 | 為什麼重要 | 對應專案 |
|---|---|---|
| 任務拆解與流程編排 | Agent 不該只是一段 prompt，而要能把複雜任務拆成明確步驟 | [agentic-idea-validator](https://github.com/andrewzxlin/agentic-idea-validator) |
| Routing 與安全邊界 | 真實 workflow 需要根據輸入走不同路徑，也需要 guardrails | [customer-reply-agent](https://github.com/andrewzxlin/customer-reply-agent) |
| RAG 與引用來源 | Agent 回答問題時需要能查資料、附來源、信心不足時拒絕亂答 | [rag-knowledgebase-evals](https://github.com/andrewzxlin/rag-knowledgebase-evals) |
| Code-aware analysis | Agent 不能只處理自然語言，也要能讀 diff、找風險、產生結構化建議 | [repo-pr-review-agent](https://github.com/andrewzxlin/repo-pr-review-agent) |
| Observability | 多步 agent workflow 需要 trace、latency、tokens、cost、failure analysis | [agent-observability-dashboard](https://github.com/andrewzxlin/agent-observability-dashboard) |
| Workflow orchestration | 多步任務需要依賴順序、retry、approval gate、failure propagation | [workflow-action-runner](https://github.com/andrewzxlin/workflow-action-runner) |
| Memory / state management | Agent 需要記住偏好與規則，但不能亂存敏感資料 | [agent-memory-store](https://github.com/andrewzxlin/agent-memory-store) |
| Learning design / onboarding | 好的 agentic workflow 學習路徑要能降低門檻，用錯題重現與間隔複習把概念變成直覺 | [agent-quest-academy](https://github.com/andrewzxlin/agent-quest-academy) |

## Featured Projects

| 專案 | 它能做什麼 | Repo |
|---|---|---|
| Agentic Idea Validator | 把一個模糊 idea 拆成競品、風險、評分與 7 天驗證計畫 | [agentic-idea-validator](https://github.com/andrewzxlin/agentic-idea-validator) |
| Customer Reply Agent | 把客服、退款、帳單紀錄整理成證據時間線、guardrails 與回覆草稿 | [customer-reply-agent](https://github.com/andrewzxlin/customer-reply-agent) |
| RAG Knowledge Base with Evals | 讀取知識庫、retrieval、附 citations，並測低信心拒答 | [rag-knowledgebase-evals](https://github.com/andrewzxlin/rag-knowledgebase-evals) |
| Repo PR Review Agent | 讀 unified diff，找出 secret、XSS、吞錯、destructive SQL 等風險 | [repo-pr-review-agent](https://github.com/andrewzxlin/repo-pr-review-agent) |
| Agent Observability Dashboard | 讀 JSONL traces，整理 latency、tokens、cost、failure states 與改善建議 | [agent-observability-dashboard](https://github.com/andrewzxlin/agent-observability-dashboard) |
| Workflow Action Runner | 讀 JSON workflow，依依賴順序執行 steps，支援 retry 與 human approval gate | [workflow-action-runner](https://github.com/andrewzxlin/workflow-action-runner) |
| Agent Memory Store | 從對話抽取偏好、規則、專案資訊，經 privacy filter 後保存並檢索 | [agent-memory-store](https://github.com/andrewzxlin/agent-memory-store) |
| Agent Quest Academy | 用 Duolingo 式選擇題、複選題、少量簡答、錯題重現與間隔複習，幫初學者建立 Agentic Workflow 直覺 | [agent-quest-academy](https://github.com/andrewzxlin/agent-quest-academy) |

## 設計原則

這些專案刻意先採用 deterministic workflow，而不是一開始就依賴外部 LLM API。原因是：

1. 可以本機直接跑 demo 和測試。
2. 每個 workflow step 都能被單獨檢查。
3. eval cases 可以穩定驗證，不會因模型輸出波動而失真。
4. 之後可以把 deterministic step 替換成 OpenAI、Anthropic、LangGraph 或 Agents SDK。

每個專案都包含中文 README、可重現 demo、regression tests 與 GitHub Actions CI。

## 下一步

- OpenAI Agents SDK / LangGraph integration
- GitHub Actions / CI demos 的進一步自動化
- OpenTelemetry 或 AgentOps 類 observability
- 更完整的 eval suites
- Web UI demos 與互動式學習產品
