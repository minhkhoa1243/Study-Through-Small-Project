# 04 — ML Systems, LLM Serving, MLOps & Recommender Systems (Backend + AI)

> Nhóm bài "Backend + AI" nhất: làm sao để mô hình **chạy nhanh, rẻ, ổn định ở quy mô lớn**. Đây là kiến thức giúp bạn khác biệt với người "chỉ biết train model".
> Ký hiệu: ⭐ nên đọc trước · 🆕 năm 2026 · 💻 có code · `P0x` dự án liên quan. Mã arXiv/DOI đã kiểm tra (29/09/2026).

---

## A. MLOps & ML trong production → `P01`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2015 | ⭐ **Hidden Technical Debt in Machine Learning Systems** — Sculley et al. (NeurIPS 2015) | Code model chỉ là phần nhỏ; nợ kỹ thuật nằm ở dữ liệu, pipeline, cấu hình, giám sát | [NeurIPS Proceedings](https://papers.nips.cc/paper_files/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html) |
| 2017 | **Ray: A Distributed Framework for Emerging AI Applications** | Nền tảng tính toán phân tán phổ biến cho ML | [1712.05889](https://arxiv.org/abs/1712.05889) |
| 2020 | **Challenges in Deploying Machine Learning: a Survey of Case Studies** | Các vấn đề thực tế khi triển khai ML | [2011.09926](https://arxiv.org/abs/2011.09926) |
| 2022 | **Machine Learning Operations (MLOps): Overview, Definition, and Architecture** | Định nghĩa & kiến trúc MLOps | [2205.02302](https://arxiv.org/abs/2205.02302) |

## B. Attention nhanh (GPU kernels)

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2022 | ⭐ **FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness** | Tối ưu truy cập bộ nhớ GPU → attention nhanh hơn nhiều | [2205.14135](https://arxiv.org/abs/2205.14135) |
| 2023 | **FlashAttention-2** | Song song hóa & chia việc tốt hơn | [2307.08691](https://arxiv.org/abs/2307.08691) |
| 2024 | **FlashAttention-3** | Tận dụng bất đồng bộ & low-precision trên GPU Hopper | [2407.08608](https://arxiv.org/abs/2407.08608) |

## C. LLM Inference & Serving → `P13`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2022 | **Fast Inference from Transformers via Speculative Decoding** | Model nhỏ "đoán trước", model lớn kiểm tra → nhanh hơn mà không đổi phân phối output | [2211.17192](https://arxiv.org/abs/2211.17192) |
| 2023 | ⭐ **Efficient Memory Management for LLM Serving with PagedAttention** (vLLM) | Quản lý KV cache như bộ nhớ ảo của hệ điều hành | [2309.06180](https://arxiv.org/abs/2309.06180) · 💻 [code](https://github.com/vllm-project/vllm) |
| 2023 | **SGLang: Efficient Execution of Structured Language Model Programs** | RadixAttention tái sử dụng prefix | [2312.07104](https://arxiv.org/abs/2312.07104) · 💻 [code](https://github.com/sgl-project/sglang) |
| 2024 | **DistServe: Disaggregating Prefill and Decoding for Goodput-optimized LLM Serving** | Tách prefill/decode ra máy khác nhau | [2401.09670](https://arxiv.org/abs/2401.09670) |
| 2024 | **EAGLE: Speculative Sampling Requires Rethinking Feature Uncertainty** | Speculative decoding ở mức feature | [2401.15077](https://arxiv.org/abs/2401.15077) |
| 2024 | ⭐ **Mooncake: A KVCache-centric Disaggregated Architecture for LLM Serving** | Kiến trúc lấy KV cache làm trung tâm (dùng trong production) | [2407.00079](https://arxiv.org/abs/2407.00079) |
| 2025 | **LMCache: An Efficient KV Cache Layer for Enterprise-Scale LLM Inference** | Lớp KV cache ngoài GPU, tái sử dụng giữa các request | [2510.09665](https://arxiv.org/abs/2510.09665) · 💻 [code](https://github.com/LMCache/LMCache) |
| 2026 | 🆕 **DualPath: Breaking the Storage Bandwidth Bottleneck in Agentic LLM Inference** | Nút thắt I/O của KV cache trong agent nhiều lượt | [2602.21548](https://arxiv.org/abs/2602.21548) |
| 2026 | 🆕 **SPEED-Bench: A Unified and Diverse Benchmark for Speculative Decoding** | Benchmark chuẩn hóa cho speculative decoding | [2604.09557](https://arxiv.org/abs/2604.09557) |

## D. Lượng tử hóa & Fine-tune hiệu quả

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2022 | **GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers** | Lượng tử hóa 3–4 bit sau huấn luyện | [2210.17323](https://arxiv.org/abs/2210.17323) |
| 2023 | ⭐ **QLoRA: Efficient Finetuning of Quantized LLMs** | Fine-tune LLM lớn trên 1 GPU | [2305.14314](https://arxiv.org/abs/2305.14314) |
| 2023 | **AWQ: Activation-aware Weight Quantization for LLM Compression and Acceleration** | Giữ lại trọng số quan trọng theo activation | [2306.00978](https://arxiv.org/abs/2306.00978) |
| 2024 | **LlamaFactory: Unified Efficient Fine-Tuning of 100+ Language Models** | Framework fine-tune thống nhất | [2403.13372](https://arxiv.org/abs/2403.13372) · 💻 [code](https://github.com/hiyouga/LlamaFactory) |

## E. Vector Search → `P02`, `P05`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2016 | ⭐ **Efficient and robust approximate nearest neighbor search using Hierarchical Navigable Small World graphs** (HNSW) | Thuật toán ANN phổ biến nhất trong vector DB | [1603.09320](https://arxiv.org/abs/1603.09320) |
| 2017 | **Billion-scale similarity search with GPUs** (FAISS) | Tìm kiếm tương tự quy mô tỷ vector | [1702.08734](https://arxiv.org/abs/1702.08734) · 💻 [code](https://github.com/facebookresearch/faiss) |

## F. Recommender Systems → `P11`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2016 | **Wide & Deep Learning for Recommender Systems** | Kết hợp ghi nhớ (wide) + tổng quát hóa (deep) | [1606.07792](https://arxiv.org/abs/1606.07792) |
| 2016 | ⭐ **Deep Neural Networks for YouTube Recommendations** — Covington et al. (RecSys 2016) | Kiến trúc 2 tầng candidate generation → ranking kinh điển | [DOI](https://doi.org/10.1145/2959100.2959190) |
| 2019 | **Deep Learning Recommendation Model for Personalization and Recommendation Systems** (DLRM) | Mô hình ranking của Meta | [1906.00091](https://arxiv.org/abs/1906.00091) |
| 2023 | ⭐ **Recommender Systems with Generative Retrieval** (TIGER) | Gợi ý bằng cách **sinh Semantic ID** của sản phẩm | [2305.05065](https://arxiv.org/abs/2305.05065) |
| 2024 | **Actions Speak Louder than Words: Trillion-Parameter Sequential Transducers for Generative Recommendations** (HSTU) | Scale recommender kiểu LLM | [2402.17152](https://arxiv.org/abs/2402.17152) |
| 2025 | **Generative Recommendation with Semantic IDs: A Practitioner's Handbook** | Hướng dẫn thực hành + framework GRID | [2507.22224](https://arxiv.org/abs/2507.22224) |

---

### Đọc gì trước
- Làm `P01`: *Hidden Technical Debt* → *Challenges in Deploying ML*.
- Làm `P13`: FlashAttention → PagedAttention (vLLM) → Speculative Decoding → DistServe → Mooncake.
- Làm `P11`: YouTube DNN → Wide & Deep → TIGER.
