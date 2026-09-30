# Research Papers — Theo dõi thế giới AI đang làm gì (cập nhật 29/09/2026)

> Thư mục tuyển chọn các bài báo **có thật, chính thống, có tầm ảnh hưởng**, ưu tiên **mới & đột phá (2025–2026)**, sắp theo các hướng bạn quan tâm: **Computer Vision, Quant/Tài chính, LLM/Agents, Backend + AI (ML Systems)**.
> Mục tiêu: biết thế giới đang làm gì, đang thiếu gì → **lên ý tưởng nghiên cứu** ([06-Research-Ideas.md](06-Research-Ideas.md)) và chọn dự án ([`../Project-Ideas/`](../Project-Ideas/README.md)).

## ✅ Cách danh sách này được kiểm chứng

- **Toàn bộ 215 mã arXiv** trong thư mục này và thư mục `Project-Ideas/` đã được đối chiếu tự động với **arXiv API chính thức** (`export.arxiv.org`) ngày 29/09/2026: mã tồn tại và tiêu đề khớp.
- Các bài đăng tạp chí tài chính (không có trên arXiv) được kiểm tra qua **Crossref DOI** (tiêu đề, tạp chí, năm khớp). Trang nhà xuất bản đôi khi chặn công cụ tự động nhưng mở bình thường trên trình duyệt.
- Giải thưởng hội nghị được lấy từ **trang công bố chính thức** (CVPR, ICLR, ICML, NeurIPS, ACL) — link nguồn ở [05-Awards-2025-2026.md](05-Awards-2025-2026.md).
- Bài đánh dấu 🔥 là **preprint mới đang trending** (chưa qua bình duyệt/kiểm chứng thời gian) — đọc để biết xu hướng, nhưng hãy đọc với thái độ phê phán.

## Ký hiệu

| Ký hiệu | Ý nghĩa |
|---|---|
| ⭐ | Nên đọc trước trong nhóm |
| 🏆 | Đạt giải Best/Outstanding Paper hoặc Test of Time tại hội nghị hàng đầu |
| 🆕 | Công bố năm 2026 |
| 🔥 | Preprint đang trending trên Hugging Face Papers (tháng 9/2026) |
| 💻 | Có code/model công khai (link kèm theo) |
| `P0x` | Liên quan trực tiếp tới dự án trong `Project-Ideas/` |

## Mục lục

| File | Nội dung | Số bài |
|---|---|---|
| [00-Foundations-Classics.md](00-Foundations-Classics.md) | Kinh điển nền tảng — gắn với từng bài học trong khóa AI-For-Beginners | ~30 |
| [01-Computer-Vision.md](01-Computer-Vision.md) | Detection, segmentation, foundation models, 3D/4D, VLM & Document AI, generative, anomaly detection, CV tiếng Việt | ~55 |
| [02-LLM-Agents-RAG.md](02-LLM-Agents-RAG.md) | Mô hình mở, reasoning & RL, kiến trúc mới, RAG, agents & MCP, NLP tiếng Việt | ~55 |
| [03-Quant-Finance-TimeSeries.md](03-Quant-Finance-TimeSeries.md) | Phương pháp luận quant, deep learning cho thị trường, time-series foundation models, LLM trong tài chính, **cạm bẫy** | ~50 |
| [04-ML-Systems-MLOps-RecSys.md](04-ML-Systems-MLOps-RecSys.md) | MLOps, LLM serving/inference, lượng tử hóa, vector search, recommender systems | ~30 |
| [05-Awards-2025-2026.md](05-Awards-2025-2026.md) | Tổng hợp bài đạt giải CVPR 2026, ICML 2026, ACL 2026, ICLR 2026, NeurIPS 2025, CVPR/ACL 2025 | ~35 |
| [06-Research-Ideas.md](06-Research-Ideas.md) | **Khoảng trống nghiên cứu** rút ra từ các bài trên + 10 đề tài gợi ý cho sinh viên | — |

---

## Xu hướng lớn 2025–2026 (tóm tắt từ danh sách)

1. **Reasoning bằng Reinforcement Learning** — DeepSeek-R1 mở đường; GRPO → DAPO → GSPO; nhưng câu hỏi "RL có thật sự tạo năng lực mới?" vẫn còn tranh luận (NeurIPS 2025 runner-up).
2. **Agents & "harness"** — trọng tâm chuyển từ bản thân model sang **hệ thống bao quanh model** (tool, memory, context engineering, MCP). Tháng 9/2026, trending trên HF là các bài về *agent harness tự cải thiện* (RRSI, SkillOpt, NeoHorse-1…).
3. **Foundation models cho thị giác đã "đủ tốt"** — DINOv3, SAM 3, SigLIP 2, Perception Encoder → dự án thực tế chủ yếu là *fine-tune/ghép nối*, không train từ đầu.
4. **Hình học 3D/4D feed-forward** — VGGT (CVPR 2025 Best Paper) → D4RT (CVPR 2026 Best Paper), Depth Anything 3, SAM 3D.
5. **Document AI bằng VLM nhỏ** — DeepSeek-OCR, PaddleOCR-VL, MinerU2.5: model < 2B tham số parse tài liệu tốt → cơ hội lớn cho tiếng Việt.
6. **World models** — Cosmos, V-JEPA 2/2.1, NitroGen; nhiều bài trending về video world model.
7. **Time-series foundation models** — Chronos-2, TimesFM, Moirai 2.0, Kronos (tài chính); nhưng các nghiên cứu 2026 cho thấy **lợi thế trong dự báo lợi suất cổ phiếu là rất nhỏ** → khoảng trống nghiên cứu.
8. **LLM trong tài chính & cạm bẫy look-ahead bias** — LLM "nhớ" dữ liệu quá khứ → backtest bị thổi phồng; nhiều bài 2025–2026 đo lường vấn đề này.
9. **Hiệu quả suy luận (inference efficiency)** — KV cache, tách prefill/decode, speculative decoding: kỹ năng Backend + AI "đắt giá".
10. **Diffusion vượt ra khỏi ảnh** — diffusion language models (LLaDA, *The Flexibility Trap* — ICML 2026 Outstanding).

Báo cáo tổng quan nên đọc:
- [Stanford HAI — AI Index Report 2026](https://hai.stanford.edu/ai-index/2026-ai-index-report) (xu hướng R&D, kinh tế, giáo dục, chính sách).
- [State of AI Report](https://www.stateof.ai/) (ra hằng năm vào khoảng tháng 10).

---

## Nguồn theo dõi bài báo mới (nên kiểm tra hằng tuần)

| Nguồn | Dùng để |
|---|---|
| [Hugging Face Papers — Daily](https://huggingface.co/papers) · [Trending](https://huggingface.co/papers/trending) | Bài mới được cộng đồng quan tâm, thường kèm code/model |
| [arXiv cs.CV](https://arxiv.org/list/cs.CV/recent) · [arXiv q-fin](https://arxiv.org/list/q-fin/new) | Nguồn gốc preprint (CV, tài chính định lượng) |
| [alphaXiv](https://www.alphaxiv.org/) | Thảo luận/hỏi đáp trên từng paper arXiv |
| [Semantic Scholar](https://www.semanticscholar.org/) · [Connected Papers](https://www.connectedpapers.com/) | Tra trích dẫn, tìm bài liên quan |
| Trang giải thưởng hội nghị (xem [05-Awards](05-Awards-2025-2026.md)) | Lọc bài chất lượng cao nhất năm |
| [SkalskiP/top-cvpr-2026-papers](https://github.com/SkalskiP/top-cvpr-2026-papers) | Tuyển chọn paper CVPR 2026 kèm code/demo |
| [FeijiangHan/Top-Conference-Best-Papers](https://github.com/FeijiangHan/Top-Conference-Best-Papers) | Danh sách best paper nhiều hội nghị 2022–2026 |
| [Epoch AI](https://epoch.ai/) | Số liệu về compute, xu hướng mô hình |
| Dự án [P12 Paper Radar](../Project-Ideas/P12-Paper-Radar-Multi-Agent/README.md) | Tự động hóa tất cả việc trên 🙂 |

## Cách đọc paper hiệu quả (phương pháp 3 lượt)

Theo S. Keshav, [*How to Read a Paper*](http://ccr.sigcomm.org/online/files/p83-keshavA.pdf) (ACM SIGCOMM CCR, 2007):
1. **Lượt 1 (5–10 phút)**: tiêu đề, abstract, intro, các heading, kết luận, lướt hình → trả lời 5C: *Category, Context, Correctness, Contributions, Clarity*.
2. **Lượt 2 (~1 giờ)**: đọc kỹ hình/bảng, ghi chú các bài tham khảo quan trọng; bỏ qua chứng minh.
3. **Lượt 3 (vài giờ)**: "tái hiện" bài báo trong đầu (hoặc bằng code) — tìm giả định ngầm, điểm yếu → **đây là nơi sinh ra ý tưởng nghiên cứu**.

Mẫu ghi chú cho mỗi bài (thêm vào cuối file tương ứng):
```markdown
### <Tên bài> (<năm>, <hội nghị/arXiv id>)
- Vấn đề:
- Ý tưởng chính (1 câu):
- Kết quả chính (số liệu):
- Hạn chế / giả định:
- Ý tưởng cho tôi (dự án / nghiên cứu):
```

Công cụ: [Zotero](https://www.zotero.org/) (quản lý trích dẫn) + Overleaf (viết LaTeX).
