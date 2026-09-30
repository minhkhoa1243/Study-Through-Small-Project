# 00 — Core Skills: Kiến thức nền cho Backend + AI Engineer

> Checklist dùng chung cho **mọi** dự án trong thư mục này. Không cần học hết trước khi bắt đầu — học tới đâu, áp dụng vào P01/P02 tới đó.
> Đánh dấu `[x]` khi bạn đã **dùng được trong code thật**, không phải chỉ đọc qua.

---

## 1. Python nâng cao

- [ ] Type hints (`typing`, `TypedDict`, `Protocol`, generics) + kiểm tra bằng `mypy`/`pyright`
- [ ] `async`/`await`, event loop, khi nào dùng async vs. thread vs. process (GIL)
- [ ] Context manager, decorator, generator/iterator
- [ ] Quản lý môi trường & package: [astral-sh/uv](https://github.com/astral-sh/uv), `pyproject.toml`
- [ ] Lint/format: [astral-sh/ruff](https://github.com/astral-sh/ruff)
- [ ] Test: `pytest`, fixture, mock, test coverage
- [ ] Logging có cấu trúc (JSON log), cấu hình qua biến môi trường

> Lỗi thực tế trong code của bạn: [`fb-messenger-bot/app.py`](../fb-messenger-bot/app.py) hàm `log()` dùng `unicode()` (chỉ có ở Python 2) → trên Python 3 sẽ ném `NameError` với mọi message không phải `dict`. Đây là bài tập sửa đầu tiên của P02.

## 2. Backend & API

- [ ] HTTP: method, status code, header, idempotency, REST vs. RPC
- [ ] [FastAPI](https://github.com/fastapi/fastapi) + Pydantic v2 (validation, settings)
- [ ] Cấu trúc project: [zhanymkanov/fastapi-best-practices](https://github.com/zhanymkanov/fastapi-best-practices), mẫu đầy đủ [fastapi/full-stack-fastapi-template](https://github.com/fastapi/full-stack-fastapi-template)
- [ ] Authentication: OAuth2 + JWT, API key, hash mật khẩu
- [ ] Upload file lớn, streaming response, **Server-Sent Events** (stream token LLM), WebSocket
- [ ] Background jobs & task queue: [Celery](https://github.com/celery/celery) / RQ / Arq + Redis
- [ ] Rate limiting, retry với exponential backoff, timeout, circuit breaker
- [ ] Webhook (nhận & xác thực chữ ký) — áp dụng trực tiếp ở P02
- [ ] Tài liệu API tự động (OpenAPI/Swagger)

## 3. Cơ sở dữ liệu & lưu trữ

- [ ] SQL chắc tay: JOIN, GROUP BY, window function, CTE, EXPLAIN
- [ ] PostgreSQL: index (B-tree, GIN), transaction, isolation level
- [ ] ORM: SQLAlchemy 2.0 + migration Alembic
- [ ] [Redis](https://github.com/redis/redis): cache, TTL, pub/sub, stream
- [ ] Vector DB: [pgvector](https://github.com/pgvector/pgvector) (khởi đầu), [Qdrant](https://github.com/qdrant/qdrant)
- [ ] Object storage (S3-compatible): [MinIO](https://github.com/minio/minio)
- [ ] Phân tích dữ liệu: [DuckDB](https://github.com/duckdb/duckdb), Parquet

## 4. System Design

- [ ] Caching, load balancing, horizontal scaling, stateless service
- [ ] Queue-based decoupling (producer/consumer), backpressure
- [ ] CAP, consistency, idempotent consumer
- [ ] Tài liệu: [donnemartin/system-design-primer](https://github.com/donnemartin/system-design-primer)

## 5. DevOps

- [ ] Git: branch, rebase, PR, conventional commits
- [ ] Docker: multi-stage build, image nhỏ, `docker compose`
- [ ] CI/CD: GitHub Actions (lint → test → build image → deploy)
- [ ] Linux cơ bản, Nginx reverse proxy, HTTPS
- [ ] Deploy lên cloud miễn phí/rẻ (Render, Fly.io, Railway, Google Cloud Run, Hugging Face Spaces)
- [ ] Observability: log, metric ([Prometheus](https://github.com/prometheus/prometheus) + [Grafana](https://github.com/grafana/grafana)), trace ([OpenTelemetry](https://github.com/open-telemetry/opentelemetry-python))
- [ ] Load test: [Locust](https://github.com/locustio/locust) hoặc [k6](https://github.com/grafana/k6) — đo p50/p95/p99, throughput

## 6. ML Engineering / MLOps

- [ ] PyTorch: `Dataset`/`DataLoader`, training loop, mixed precision, checkpoint
- [ ] Transfer learning với [timm](https://github.com/huggingface/pytorch-image-models) và [🤗 Transformers](https://github.com/huggingface/transformers)
- [ ] Experiment tracking: [MLflow](https://github.com/mlflow/mlflow) hoặc Weights & Biases
- [ ] Export & tối ưu: ONNX + [ONNX Runtime](https://github.com/microsoft/onnxruntime), quantization INT8, dynamic batching
- [ ] Model serving: FastAPI thuần → [BentoML](https://github.com/bentoml/BentoML) → [Triton](https://github.com/triton-inference-server/server) (khi cần)
- [ ] Giám sát data/model drift: [Evidently](https://github.com/evidentlyai/evidently)
- [ ] Đánh giá mô hình đúng cách: train/val/test split, cross-validation, **data leakage**, metric phù hợp bài toán
- [ ] Khóa học miễn phí: [GokuMohandas/Made-With-ML](https://github.com/GokuMohandas/Made-With-ML), [DataTalksClub/mlops-zoomcamp](https://github.com/DataTalksClub/mlops-zoomcamp), sách *Designing ML Systems* — [chiphuyen/dmls-book](https://github.com/chiphuyen/dmls-book)

## 7. LLM Engineering

- [ ] Gọi API LLM, streaming, **structured output** (JSON schema / Pydantic)
- [ ] Embeddings đa ngôn ngữ (hỗ trợ tiếng Việt), ví dụ [BAAI/bge-m3](https://huggingface.co/BAAI/bge-m3)
- [ ] RAG: chunking, hybrid search (BM25 + vector), reranking, trích dẫn nguồn
- [ ] Đánh giá: bộ câu hỏi vàng, LLM-as-judge, [Ragas](https://github.com/vibrantlabsai/ragas)
- [ ] Tool calling, agent loop, [Model Context Protocol (MCP)](https://github.com/modelcontextprotocol/python-sdk)
- [ ] Tracing LLM: [Langfuse](https://github.com/langfuse/langfuse)
- [ ] Chạy model local: [Ollama](https://github.com/ollama/ollama), [llama.cpp](https://github.com/ggml-org/llama.cpp); serving: [vLLM](https://github.com/vllm-project/vllm)
- [ ] Fine-tune nhẹ: LoRA/QLoRA với [Unsloth](https://github.com/unslothai/unsloth) hoặc [LlamaFactory](https://github.com/hiyouga/LlamaFactory)
- [ ] An toàn: prompt injection, không để lộ secret, giới hạn quyền của tool
- [ ] Khóa học miễn phí: [microsoft/generative-ai-for-beginners](https://github.com/microsoft/generative-ai-for-beginners), [microsoft/ai-agents-for-beginners](https://github.com/microsoft/ai-agents-for-beginners)

## 8. Toán cần cho từng hướng

| Hướng | Chủ đề |
|---|---|
| Chung | Đại số tuyến tính (ma trận, eigen, SVD), xác suất–thống kê, tối ưu (gradient descent) |
| Computer Vision | Tích chập, hình học ảnh (homography, camera model), IoU/NMS, metric mAP |
| Quant | Chuỗi thời gian (stationarity, autocorrelation), kiểm định giả thuyết, hồi quy, lý thuyết danh mục (Markowitz), rủi ro (volatility, drawdown, Sharpe), **multiple testing** |
| RecSys / Search | Metric xếp hạng (Recall@K, NDCG, MRR), ANN (HNSW, IVF) |

## 9. Kỹ năng "mềm" nhưng quyết định

- [ ] Viết README/Design doc rõ ràng (vấn đề → lựa chọn → đánh đổi)
- [ ] Đọc paper hiệu quả (xem [Research-Papers/README.md](../Research-Papers/README.md))
- [ ] Trình bày kết quả bằng số liệu + biểu đồ
- [ ] Tiếng Anh kỹ thuật (đọc doc, viết commit/PR)
