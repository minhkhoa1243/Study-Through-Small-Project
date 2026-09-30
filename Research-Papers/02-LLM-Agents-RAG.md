# 02 — LLM, Reasoning, Agents & RAG (ưu tiên 2024–2026)

> Ký hiệu: ⭐ nên đọc trước · 🏆 đạt giải · 🆕 năm 2026 · 🔥 preprint trending 9/2026 · 💻 có code · `P0x` dự án liên quan.
> Mọi mã arXiv đã kiểm tra qua arXiv API (29/09/2026).

---

## A. Technical report của các mô hình mở (hiểu "state of the art" được xây thế nào)

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2024 | **DeepSeek-V3 Technical Report** | MoE lớn, huấn luyện chi phí thấp, MLA attention | [2412.19437](https://arxiv.org/abs/2412.19437) |
| 2025 | ⭐ **DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning** | Reasoning bằng RL thuần (R1-Zero) + nhiều giai đoạn; mở đường cho "reasoning model" mã nguồn mở. Bản bình duyệt đăng trên *Nature* (09/2025) | [2501.12948](https://arxiv.org/abs/2501.12948) · [Nature](https://doi.org/10.1038/s41586-025-09422-z) |
| 2025 | **Qwen3 Technical Report** | Họ model mở đa kích cỡ, chế độ suy nghĩ/không suy nghĩ | [2505.09388](https://arxiv.org/abs/2505.09388) |
| 2025 | **Kimi K2: Open Agentic Intelligence** | MoE tối ưu cho agent; optimizer MuonClip | [2507.20534](https://arxiv.org/abs/2507.20534) |
| 2025 | **gpt-oss-120b & gpt-oss-20b Model Card** | Model open-weight của OpenAI | [2508.10925](https://arxiv.org/abs/2508.10925) |
| 2026 | 🆕 **Qwen3.5-Omni Technical Report** | Model đa phương thức (âm thanh–hình ảnh) quy mô lớn | [2604.15804](https://arxiv.org/abs/2604.15804) |
| 2026 | 🆕 ⭐ **DeepSeek-V4: Towards Highly Efficient Million-Token Context Intelligence** | Ngữ cảnh 1 triệu token hiệu quả nhờ hybrid attention | [2606.19348](https://arxiv.org/abs/2606.19348) |

> Theo [Stanford AI Index 2026](https://hai.stanford.edu/ai-index/2026-ai-index-report), DeepSeek-R1 từng bắt kịp model hàng đầu của Mỹ vào 02/2025 — ví dụ rõ nhất cho sức mạnh của mô hình mở.

## B. Reasoning & Reinforcement Learning cho LLM

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2024 | **Scaling LLM Test-Time Compute Optimally…** | Tăng compute lúc suy luận có thể hiệu quả hơn tăng tham số | [2408.03314](https://arxiv.org/abs/2408.03314) |
| 2025 | **s1: Simple test-time scaling** | Chỉ ~1k mẫu + "budget forcing" vẫn cho reasoning tốt | [2501.19393](https://arxiv.org/abs/2501.19393) |
| 2025 | **DAPO: An Open-Source LLM Reinforcement Learning System at Scale** | Công thức RL mở, sửa các điểm yếu của GRPO | [2503.14476](https://arxiv.org/abs/2503.14476) |
| 2025 | 🏆 ⭐ **Does Reinforcement Learning Really Incentivize Reasoning Capacity in LLMs Beyond the Base Model?** | RLVR chủ yếu "lọc" năng lực có sẵn của base model? — **NeurIPS 2025 Runner-up** | [2504.13837](https://arxiv.org/abs/2504.13837) |
| 2025 | **Group Sequence Policy Optimization** (GSPO) | Tỉ lệ importance ở mức chuỗi thay vì từng token → RL ổn định hơn (nhóm Qwen) | [2507.18071](https://arxiv.org/abs/2507.18071) |

## C. Kiến trúc & huấn luyện (những ý tưởng mới đáng chú ý)

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2023 | **Mamba: Linear-Time Sequence Modeling with Selective State Spaces** | Thay thế attention bằng state-space, tuyến tính theo độ dài | [2312.00752](https://arxiv.org/abs/2312.00752) |
| 2025 | 🏆 **Native Sparse Attention** | Sparse attention huấn luyện được, tối ưu phần cứng — **ACL 2025 Best Paper** | [2502.11089](https://arxiv.org/abs/2502.11089) |
| 2025 | **Large Language Diffusion Models** (LLaDA) | LLM dạng diffusion thay vì autoregressive | [2502.09992](https://arxiv.org/abs/2502.09992) |
| 2025 | 🏆 ⭐ **Gated Attention for Large Language Models** | Thêm cổng sigmoid sau attention → ổn định, hết "attention sink" — **NeurIPS 2025 Best Paper** | [2505.06708](https://arxiv.org/abs/2505.06708) |
| 2025 | 🏆 **The Polar Express: Optimal Matrix Sign Methods and Their Application to the Muon Algorithm** | Tối ưu tính toán cho optimizer Muon — **ICLR 2026 Honorable Mention** | [2505.16932](https://arxiv.org/abs/2505.16932) |
| 2025 | 🏆 **Superposition Yields Robust Neural Scaling** | Giải thích scaling law qua hiện tượng superposition — **NeurIPS 2025 Runner-up** | [2505.10465](https://arxiv.org/abs/2505.10465) |
| 2025 | 🏆 **Transformers are Inherently Succinct** | Lý thuyết: Transformer mã hóa khái niệm "gọn" hơn RNN và các mô hình khác — **ICLR 2026 Outstanding Paper** | [2510.19315](https://arxiv.org/abs/2510.19315) · [OpenReview](https://openreview.net/forum?id=Yxz92UuPLQ) |
| 2026 | 🆕 🏆 **The Flexibility Trap: Rethinking the Value of Arbitrary Order in Diffusion Language Models** | Sinh theo thứ tự tùy ý lại hạn chế reasoning của diffusion LM — **ICML 2026 Outstanding Paper** | [2601.15165](https://arxiv.org/abs/2601.15165) |

## D. Hành vi, đánh giá & giới hạn của LLM

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2023 | ⭐ **Lost in the Middle: How Language Models Use Long Contexts** | LLM bỏ sót thông tin ở giữa ngữ cảnh dài → ảnh hưởng thiết kế RAG | [2307.03172](https://arxiv.org/abs/2307.03172) |
| 2023 | **SWE-bench: Can Language Models Resolve Real-World GitHub Issues?** | Benchmark coding agent chuẩn (AI Index 2026: gần bão hòa) | [2310.06770](https://arxiv.org/abs/2310.06770) |
| 2025 | 🏆 ⭐ **LLMs Get Lost In Multi-Turn Conversation** | LLM tụt mạnh khi yêu cầu được đưa dần qua nhiều lượt — **ICLR 2026 Outstanding Paper** → rất liên quan chatbot `P02` | [2505.06120](https://arxiv.org/abs/2505.06120) |
| 2025 | 🏆 **Artificial Hivemind: The Open-Ended Homogeneity of Language Models (and Beyond)** | Các LLM khác nhau trả lời giống nhau đến mức đồng nhất — **NeurIPS 2025 Best Paper** | [2510.22954](https://arxiv.org/abs/2510.22954) |

## E. Retrieval-Augmented Generation → `P02`, `P04`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2020 | **ColBERT: Efficient and Effective Passage Search via Contextualized Late Interaction** | Late interaction — retrieval chính xác hơn 1 vector | [2004.12832](https://arxiv.org/abs/2004.12832) |
| 2023 | **Ragas: Automated Evaluation of Retrieval Augmented Generation** | Metric đánh giá RAG không cần nhãn đầy đủ | [2309.15217](https://arxiv.org/abs/2309.15217) · 💻 [code](https://github.com/vibrantlabsai/ragas) |
| 2023 | **Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection** | Model tự quyết khi nào truy xuất & tự phê bình | [2310.11511](https://arxiv.org/abs/2310.11511) |
| 2024 | **RAPTOR: Recursive Abstractive Processing for Tree-Organized Retrieval** | Cây tóm tắt nhiều tầng cho tài liệu dài | [2401.18059](https://arxiv.org/abs/2401.18059) |
| 2024 | ⭐ **M3-Embedding** (BGE-M3) | Embedding đa ngôn ngữ (có tiếng Việt), dense + sparse + multi-vector | [2402.03216](https://arxiv.org/abs/2402.03216) · 💻 [model](https://huggingface.co/BAAI/bge-m3) |
| 2024 | ⭐ **From Local to Global: A Graph RAG Approach to Query-Focused Summarization** (GraphRAG) | RAG trên đồ thị tri thức cho câu hỏi tổng quát | [2404.16130](https://arxiv.org/abs/2404.16130) · 💻 [code](https://github.com/microsoft/graphrag) |
| 2025 | **Agentic Retrieval-Augmented Generation: A Survey on Agentic RAG** | Tổng quan RAG có agent | [2501.09136](https://arxiv.org/abs/2501.09136) |
| 2025 | **Towards Agentic RAG with Deep Reasoning: A Survey of RAG-Reasoning Systems** | Kết hợp suy luận và truy xuất | [2507.09477](https://arxiv.org/abs/2507.09477) |

## F. Agents, Tools, Memory & MCP → `P12`, `P13`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2023 | **Toolformer: Language Models Can Teach Themselves to Use Tools** | LLM tự học gọi API | [2302.04761](https://arxiv.org/abs/2302.04761) |
| 2023 | ⭐ **Generative Agents: Interactive Simulacra of Human Behavior** | Agent có memory, reflection, planning | [2304.03442](https://arxiv.org/abs/2304.03442) |
| 2023 | **AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation** | Framework multi-agent | [2308.08155](https://arxiv.org/abs/2308.08155) · 💻 [code](https://github.com/microsoft/autogen) |
| 2023 | **DSPy: Compiling Declarative Language Model Calls into Self-Improving Pipelines** | "Lập trình" thay vì "viết prompt" | [2310.03714](https://arxiv.org/abs/2310.03714) · 💻 [code](https://github.com/stanfordnlp/dspy) |
| 2023 | **MemGPT: Towards LLMs as Operating Systems** | Quản lý bộ nhớ nhiều tầng cho agent | [2310.08560](https://arxiv.org/abs/2310.08560) |
| 2024 | **SWE-agent: Agent-Computer Interfaces Enable Automated Software Engineering** | Thiết kế "giao diện" cho agent quan trọng như model | [2405.15793](https://arxiv.org/abs/2405.15793) |
| 2024 | **OpenHands: An Open Platform for AI Software Developers as Generalist Agents** | Nền tảng coding agent mã nguồn mở | [2407.16741](https://arxiv.org/abs/2407.16741) |
| 2025 | **Zep: A Temporal Knowledge Graph Architecture for Agent Memory** | Memory dạng đồ thị có thời gian | [2501.13956](https://arxiv.org/abs/2501.13956) |
| 2025 | ⭐ **Model Context Protocol (MCP): Landscape, Security Threats, and Future Research Directions** | Toàn cảnh + rủi ro bảo mật MCP | [2503.23278](https://arxiv.org/abs/2503.23278) |
| 2025 | **Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory** | Memory production cho agent | [2504.19413](https://arxiv.org/abs/2504.19413) · 💻 [code](https://github.com/mem0ai/mem0) |
| 2025 | ⭐ **A Survey of Context Engineering for Large Language Models** | "Context engineering" — kỹ năng cốt lõi của AI Engineer | [2507.13334](https://arxiv.org/abs/2507.13334) |
| 2025 | **Paper2Agent: Reimagining Research Papers As Interactive and Reliable AI Agents** | Biến paper thành agent tương tác (ý tưởng cho `P12`) | [2509.06917](https://arxiv.org/abs/2509.06917) |
| 2026 | 🆕 ⭐ **From Question Answering to Task Completion: A Survey on Agent System and Harness Design** | Tổng quan thiết kế "harness" quanh model | [2606.20683](https://arxiv.org/abs/2606.20683) |

### F2. 🔥 Đang trending (09/2026): *agent harness tự cải thiện* — preprint, đọc có phê phán

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2026 | 🔥 **ARIS: Autonomous Research via Adversarial Multi-Agent Collaboration** | Harness nghiên cứu tự động, nhiều model phản biện nhau | [2605.03042](https://arxiv.org/abs/2605.03042) |
| 2026 | 🔥 **SkillOpt: Executive Strategy for Self-Evolving Agent Skills** | Tối ưu "skill" của agent trong không gian văn bản | [2605.23904](https://arxiv.org/abs/2605.23904) |
| 2026 | 🔥 **NeoHorse-1: Towards Recursive Self-Improvement via Agentic Post-Training with Routing Harness** | Post-training agent + routing | [2609.08183](https://arxiv.org/abs/2609.08183) |
| 2026 | 🔥 **Dream-RSI: Recursive Self-Improvement through Evolving Worlds** | Tự cải thiện nhờ đánh giá offline từ lịch sử khám phá | [2609.14858](https://arxiv.org/abs/2609.14858) |
| 2026 | 🔥 **SoL-Pi: Recursively Scaling Auto-Research Loops for Efficient Agent Harness** | Hiệu quả token cho coding agent chạy dài hạn | [2609.20519](https://arxiv.org/abs/2609.20519) |
| 2026 | 🔥 **RRSI: Regularized Recursive Self-Improvement of Agent Harnesses** | Tự động cải thiện harness có điều chuẩn | [2609.24972](https://arxiv.org/abs/2609.24972) |

## G. NLP tiếng Việt → `P02`, `P09`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2020 | ⭐ **PhoBERT: Pre-trained language models for Vietnamese** | BERT đơn ngữ tiếng Việt, baseline chuẩn | [2003.00744](https://arxiv.org/abs/2003.00744) · 💻 [code](https://github.com/VinAIResearch/PhoBERT) |
| 2023 | **ViSoBERT: A Pre-Trained Language Model for Vietnamese Social Media Text Processing** | Cho văn bản mạng xã hội (teencode, viết tắt) | [2310.11166](https://arxiv.org/abs/2310.11166) |

---

### Đọc gì trước (lộ trình 2 tuần cho Backend + AI)
1. RAG (00) → Lost in the Middle → BGE-M3 → GraphRAG → Ragas (làm `P02`)
2. ReAct (00) → Generative Agents → Context Engineering survey → MCP survey (làm `P12`)
3. DeepSeek-R1 → "Does RL Really Incentivize…" (hiểu tranh luận lớn nhất 2025)
4. LLMs Get Lost In Multi-Turn Conversation (thiết kế chatbot tốt hơn)
