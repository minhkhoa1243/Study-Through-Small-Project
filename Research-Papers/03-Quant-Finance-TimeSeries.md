# 03 — Quant, Financial ML & Time Series (ưu tiên 2024–2026)

> Ký hiệu: ⭐ nên đọc trước · 🏆 đạt giải · 🆕 năm 2026 · 🔥 trending · 💻 có code · `P0x` dự án liên quan.
> Bài trên arXiv: đã kiểm tra qua arXiv API. Bài tạp chí tài chính: đã kiểm tra qua Crossref (DOI) — 29/09/2026.
> Nhiều bài tài chính hàng đầu có bản working paper miễn phí trên SSRN/website tác giả — tìm theo tên bài.

---

## A. ⭐ Phương pháp luận bắt buộc (đọc TRƯỚC khi backtest bất cứ thứ gì) → `P07`–`P10`

| Năm | Bài báo | Vì sao phải đọc | Link |
|---|---|---|---|
| 2014 | ⭐ **The Deflated Sharpe Ratio: Correcting for Selection Bias, Backtest Overfitting, and Non-Normality** — Bailey & López de Prado, *J. Portfolio Management* | Sharpe "đẹp" sau khi thử nhiều chiến lược cần được "xì hơi" bao nhiêu | [DOI](https://doi.org/10.3905/jpm.2014.40.5.094) |
| 2016 | ⭐ **… and the Cross-Section of Expected Returns** — Harvey, Liu & Zhu, *Review of Financial Studies* | Hàng trăm "factor" được công bố — phần lớn có thể là may mắn; đề xuất ngưỡng t-stat cao hơn | [DOI](https://doi.org/10.1093/rfs/hhv059) |
| 2016 | ⭐ **The Probability of Backtest Overfitting** — Bailey, Borwein, López de Prado & Zhu, *J. Computational Finance* | Đo xác suất chiến lược tốt nhất in-sample là do overfit (PBO, CSCV) | [DOI](https://doi.org/10.21314/JCF.2016.322) |
| 2020 | ⭐ **Empirical Asset Pricing via Machine Learning** — Gu, Kelly & Xiu, *Review of Financial Studies* | So sánh có hệ thống các mô hình ML (tree, NN…) dự báo lợi suất cổ phiếu — bài "chuẩn" của ML trong quant | [DOI](https://doi.org/10.1093/rfs/hhaa009) |

## B. Deep Learning cho thị trường tài chính

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2018 | **Deep Hedging** — Buehler et al. | Dùng deep learning để phòng hộ phái sinh có chi phí giao dịch | [1802.03042](https://arxiv.org/abs/1802.03042) |
| 2018 | **DeepLOB: Deep Convolutional Neural Networks for Limit Order Books** | CNN + LSTM trên sổ lệnh (high-frequency) | [1808.03668](https://arxiv.org/abs/1808.03668) |
| 2019 | **Deep Learning in Asset Pricing** — Chen, Pelger & Zhu | Mô hình định giá tài sản bằng NN + điều kiện no-arbitrage (bản tạp chí: *Management Science*) | [1904.00745](https://arxiv.org/abs/1904.00745) |
| 2019 | **Enhancing Time Series Momentum Strategies Using Deep Neural Networks** (Deep Momentum Networks) | NN tối ưu trực tiếp Sharpe cho chiến lược momentum | [1904.04912](https://arxiv.org/abs/1904.04912) |
| 2019 | **Temporal Fusion Transformers for Interpretable Multi-horizon Time Series Forecasting** | Transformer dự báo nhiều bước, diễn giải được | [1912.09363](https://arxiv.org/abs/1912.09363) |
| 2020 | **Deep Learning for Portfolio Optimization** — Zhang, Zohren & Roberts | Tối ưu trực tiếp tỉ trọng danh mục bằng NN → `P10` | [2005.13665](https://arxiv.org/abs/2005.13665) |
| 2021 | **HIST: A Graph-based Framework for Stock Trend Forecasting via Mining Concept-Oriented Shared Information** | Đồ thị quan hệ giữa cổ phiếu | [2110.13716](https://arxiv.org/abs/2110.13716) |
| 2023 | ⭐ **(Re-)Imag(in)ing Price Trends** — Jiang, Kelly & Xiu, *Journal of Finance* | CNN "nhìn" ảnh biểu đồ giá để dự báo lợi suất — **bài gốc của `P08`** | [DOI](https://doi.org/10.1111/jofi.13268) · 💻 [replication](https://github.com/George-hardworking/reimaging-price-trends-replication-and-extension) |
| 2023 | **DoubleAdapt: A Meta-learning Approach to Incremental Learning for Stock Trend Forecasting** | Thích nghi khi phân phối thị trường thay đổi | [2306.09862](https://arxiv.org/abs/2306.09862) |
| 2023 | **MASTER: Market-Guided Stock Transformer for Stock Price Forecasting** | Transformer có thông tin thị trường dẫn hướng | [2312.15235](https://arxiv.org/abs/2312.15235) |
| 2024 | ⭐ **The Virtue of Complexity in Return Prediction** — Kelly, Malamud & Zhou, *Journal of Finance* | Lý thuyết + thực nghiệm: mô hình phức tạp hơn (nhiều tham số) có thể dự báo lợi suất tốt hơn — gây tranh luận lớn | [DOI](https://doi.org/10.1111/jofi.13298) |

## C. Nền tảng / Framework nghiên cứu Quant

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2020 | ⭐ **Qlib: An AI-oriented Quantitative Investment Platform** | Nền tảng quant AI của Microsoft | [2009.11189](https://arxiv.org/abs/2009.11189) · 💻 [code](https://github.com/microsoft/qlib) |
| 2020 | **FinRL: A Deep Reinforcement Learning Library for Automated Stock Trading** | Thư viện DRL cho giao dịch | [2011.09607](https://arxiv.org/abs/2011.09607) · 💻 [code](https://github.com/AI4Finance-Foundation/FinRL) |
| 2023 | **Generating Synergistic Formulaic Alpha Collections via Reinforcement Learning** (AlphaGen) | RL sinh bộ công thức alpha bổ trợ nhau → `P10` | [2306.12964](https://arxiv.org/abs/2306.12964) · 💻 [code](https://github.com/ICT-FinD-Lab/alphagen) |
| 2025 | ⭐ **R&D-Agent-Quant: A Multi-Agent Framework for Data-Centric Factors and Model Joint Optimization** | Agent tự động nghiên cứu factor + mô hình | [2505.15155](https://arxiv.org/abs/2505.15155) · 💻 [code](https://github.com/microsoft/RD-Agent) |

## D. Time-Series Forecasting & Foundation Models → `P07`, `P08`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2022 | ⭐ **Are Transformers Effective for Time Series Forecasting?** (DLinear) | Mô hình tuyến tính đơn giản đánh bại nhiều Transformer → luôn cần baseline đơn giản | [2205.13504](https://arxiv.org/abs/2205.13504) |
| 2022 | **A Time Series is Worth 64 Words** (PatchTST) | Chia chuỗi thành patch như ViT | [2211.14730](https://arxiv.org/abs/2211.14730) |
| 2023 | **iTransformer: Inverted Transformers Are Effective for Time Series Forecasting** | Attention theo chiều biến thay vì thời gian | [2310.06625](https://arxiv.org/abs/2310.06625) |
| 2023 | **A decoder-only foundation model for time-series forecasting** (TimesFM) | Foundation model zero-shot của Google | [2310.10688](https://arxiv.org/abs/2310.10688) · 💻 [code](https://github.com/google-research/timesfm) |
| 2024 | **Unified Training of Universal Time Series Forecasting Transformers** (Moirai) | Foundation model của Salesforce | [2402.02592](https://arxiv.org/abs/2402.02592) |
| 2024 | ⭐ **Chronos: Learning the Language of Time Series** | Token hóa chuỗi số → huấn luyện như LLM | [2403.07815](https://arxiv.org/abs/2403.07815) · 💻 [code](https://github.com/amazon-science/chronos-forecasting) |
| 2025 | **This Time is Different: An Observability Perspective on Time Series Foundation Models** (Toto) | TSFM cho dữ liệu vận hành hệ thống | [2505.14766](https://arxiv.org/abs/2505.14766) |
| 2025 | ⭐ **Kronos: A Foundation Model for the Language of Financial Markets** | Foundation model riêng cho **nến K-line**, tokenizer chuyên biệt | [2508.02739](https://arxiv.org/abs/2508.02739) · 💻 [code](https://github.com/shiyu-coder/Kronos) |
| 2025 | **Chronos-2: From Univariate to Universal Forecasting** | Hỗ trợ đa biến + biến ngoại sinh, zero-shot | [2510.15821](https://arxiv.org/abs/2510.15821) · 💻 [model](https://huggingface.co/amazon/chronos-2) |
| 2025 | **Moirai 2.0: When Less Is More for Time Series Forecasting** | Decoder-only, dự báo phân vị, nhỏ gọn hơn | [2511.11698](https://arxiv.org/abs/2511.11698) |
| 2026 | 🆕 ⭐ **Pretrained Time-Series Foundation Models for Financial Return Forecasting** | TSFM xếp hạng tốt hơn NN train từ đầu nhưng **chỉ hơn random walk rất ít** khi dự báo lợi suất cổ phiếu | [2606.27100](https://arxiv.org/abs/2606.27100) |
| 2026 | 🆕 **Forecasting Realized Volatility with Time Series Foundation Models: A Comparison with Econometric Benchmarks** | TSFM hiếm khi thắng mô hình kinh tế lượng Log-HAR; kết hợp cả hai tốt nhất | [2607.05291](https://arxiv.org/abs/2607.05291) |

## E. LLM & NLP trong tài chính → `P09`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2019 | **FinBERT: Financial Sentiment Analysis with Pre-trained Language Models** | BERT cho cảm xúc tin tài chính | [1908.10063](https://arxiv.org/abs/1908.10063) · 💻 [code](https://github.com/ProsusAI/finBERT) |
| 2023 | **BloombergGPT: A Large Language Model for Finance** | LLM 50B chuyên tài chính | [2303.17564](https://arxiv.org/abs/2303.17564) |
| 2023 | ⭐ **Can ChatGPT Forecast Stock Price Movements? Return Predictability and Large Language Models** — Lopez-Lira & Tang | Điểm cảm xúc do LLM chấm từ tiêu đề tin có dự báo lợi suất | [2304.07619](https://arxiv.org/abs/2304.07619) |
| 2023 | **FinGPT: Open-Source Financial Large Language Models** | LLM tài chính mã nguồn mở | [2306.06031](https://arxiv.org/abs/2306.06031) · 💻 [code](https://github.com/AI4Finance-Foundation/FinGPT) |
| 2023 | **FinanceBench: A New Benchmark for Financial Question Answering** | QA trên báo cáo tài chính thật | [2311.11944](https://arxiv.org/abs/2311.11944) |
| 2024 | **FNSPID: A Comprehensive Financial News Dataset in Time Series** | Dataset tin tức + giá quy mô lớn | [2402.06698](https://arxiv.org/abs/2402.06698) |
| 2024 | **FinBen: A Holistic Financial Benchmark for Large Language Models** | Benchmark tổng hợp | [2402.12659](https://arxiv.org/abs/2402.12659) |
| 2024 | ⭐ **Financial Statement Analysis with Large Language Models** — Kim, Muhn & Nikolaev | LLM phân tích BCTC dự báo thay đổi lợi nhuận | [2407.17866](https://arxiv.org/abs/2407.17866) |
| 2024 | **Large Language Model Agent in Financial Trading: A Survey** | Tổng quan agent LLM giao dịch | [2408.06361](https://arxiv.org/abs/2408.06361) |
| 2024 | 🔥 ⭐ **TradingAgents: Multi-Agents LLM Financial Trading Framework** | Mô phỏng công ty giao dịch bằng nhiều agent (analyst, trader, risk…) — đứng đầu Hugging Face trending ngày 29/09/2026 | [2412.20138](https://arxiv.org/abs/2412.20138) · 💻 [code](https://github.com/TauricResearch/TradingAgents) |
| 2025 | **AlphaAgent: LLM-Driven Alpha Mining with Regularized Exploration to Counteract Alpha Decay** | LLM sinh alpha, chống alpha decay | [2502.16789](https://arxiv.org/abs/2502.16789) |
| 2025 | **MultiFinBen: Benchmarking LLMs for Multilingual and Multimodal Financial Application** | Đa ngôn ngữ, đa phương thức | [2506.14028](https://arxiv.org/abs/2506.14028) |
| 2026 | 🆕 **QuantaAlpha: An Evolutionary Framework for LLM-Driven Alpha Mining** | Kết hợp tiến hóa + LLM để khai phá alpha → `P10` | [2602.07085](https://arxiv.org/abs/2602.07085) |
| 2026 | 🆕 **FinMCP-Bench: Benchmarking LLM Agents for Real-World Financial Tool Use under the Model Context Protocol** | Agent tài chính dùng tool qua MCP | [2603.24943](https://arxiv.org/abs/2603.24943) |

## F. ⚠️ Cạm bẫy — đọc để không tự lừa mình

| Năm | Bài báo | Bài học | Link |
|---|---|---|---|
| 2025 | ⭐ **The Memorization Problem: Can We Trust LLMs' Economic Forecasts?** | LLM "nhớ" dữ liệu kinh tế/tài chính trước knowledge cutoff → dự báo trong quá khứ bị thổi phồng | [2504.14765](https://arxiv.org/abs/2504.14765) |
| 2025 | **Can LLM-based Financial Investing Strategies Outperform the Market in Long Run?** | Chiến lược LLM kém đi khi kiểm tra trên giai đoạn dài & rộng hơn | [2505.07078](https://arxiv.org/abs/2505.07078) |
| 2025 | **Time Travel is Cheating: Going Live with DeepFund for Real-Time Fund Investment Benchmarking** | Chỉ đánh giá LLM trên dữ liệu **sau** thời điểm train mới công bằng | [2505.11065](https://arxiv.org/abs/2505.11065) |
| 2025 | **Detecting Lookahead Bias in LLM Forecasts** | Phương pháp thống kê phát hiện look-ahead bias | [2512.23847](https://arxiv.org/abs/2512.23847) |

---

### Lộ trình đọc cho Quant (3 tuần)
1. **Tuần 1 — tư duy đúng**: Harvey–Liu–Zhu → Deflated Sharpe → PBO → DLinear
2. **Tuần 2 — ML cho lợi suất**: Gu–Kelly–Xiu → Virtue of Complexity → (Re-)Imag(in)ing Price Trends → Qlib
3. **Tuần 3 — xu hướng mới**: Chronos-2 → Kronos → *TSFMs for Financial Return Forecasting* (2026) → TradingAgents → The Memorization Problem

Sách nên có: *Advances in Financial Machine Learning* (M. López de Prado, Wiley 2018); *Machine Learning for Algorithmic Trading* (S. Jansen) — notebook: [stefan-jansen/machine-learning-for-trading](https://github.com/stefan-jansen/machine-learning-for-trading).
