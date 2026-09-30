# 06 — Ý tưởng nghiên cứu (rút ra từ khoảng trống trong các bài báo)

> Mỗi ý tưởng dưới đây xuất phát từ **một khoảng trống cụ thể** trong các bài báo ở thư mục này, được chọn sao cho **sinh viên làm được** (GPU Colab/Kaggle, dữ liệu công khai hoặc tự thu thập), và có "góc Việt Nam" — lợi thế cạnh tranh tự nhiên của bạn (dữ liệu/ngôn ngữ/thị trường mà nhóm nghiên cứu quốc tế ít chạm tới).
> Đây là **gợi ý khởi điểm**, không phải kết luận: trước khi làm, hãy tìm trên Semantic Scholar/Google Scholar xem đã có ai làm chưa (related work) và trao đổi với giảng viên hướng dẫn.

---

## Bảng tổng hợp

| # | Đề tài | Hướng | GPU cần | Dự án nền |
|---|---|---|---|---|
| R1 | Dự báo lợi suất bằng ảnh biểu đồ trên thị trường Việt Nam | CV × Quant | Thấp–TB | P07, P08 |
| R2 | Time-series foundation models có thắng random walk trên cổ phiếu VN? | Quant × TS | Thấp | P07 |
| R3 | LLM có "nhớ" thị trường chứng khoán Việt Nam? Đo look-ahead bias | LLM × Quant | Thấp (API) | P09 |
| R4 | Benchmark VLM nhỏ cho tài liệu/chứng từ tiếng Việt | CV × NLP | TB | P04 |
| R5 | Open-vocabulary detection trong giao thông mật độ xe máy cao | CV | TB | P03 |
| R6 | "Lạc lối" trong hội thoại nhiều lượt — tái lập bằng tiếng Việt | LLM | Thấp (API) | P02 |
| R7 | "Artificial Hivemind" trong tiếng Việt | LLM | Thấp (API) | P02 |
| R8 | Backbone nào cho anomaly detection few-shot: DINOv2 vs DINOv3 vs CLIP? | CV | Thấp–TB | P06 |
| R9 | LLM sinh alpha trên thị trường VN — có sống sót qua kiểm định overfitting? | LLM × Quant | Thấp (API) | P07, P10 |
| R10 | Semantic cache cho ứng dụng LLM tiếng Việt: tiết kiệm vs. sai lệch | ML Systems | Thấp | P13 |

---

## R1. Image-based return prediction ở thị trường cận biên (Việt Nam)

- **Khoảng trống**: Jiang–Kelly–Xiu (JF 2023, [DOI](https://doi.org/10.1111/jofi.13268)) chứng minh CNN trên ảnh biểu đồ có sức dự báo ở Mỹ; đã có bản tái lập mở rộng sang Trung Quốc ([repo](https://github.com/George-hardworking/reimaging-price-trends-replication-and-extension)). Thị trường có **biên độ giá**, nhà đầu tư cá nhân chiếm tỉ trọng lớn, thanh khoản phân hóa như VN thì sao?
- **Câu hỏi**: (1) Có chênh lệch lợi suất decile sau phí/thuế? (2) Ảnh có hơn chuỗi số (1D-CNN/LightGBM) không? (3) Transfer từ model Mỹ có giúp không? (4) Ngày chạm trần/sàn ảnh hưởng thế nào?
- **Phương pháp**: xem [P08](../Project-Ideas/P08-Chart-Image-CNN-Research/README.md). Đánh giá bằng Deflated Sharpe + PBO ([03-Quant](03-Quant-Finance-TimeSeries.md)).
- **Kết quả âm tính vẫn có giá trị** nếu phương pháp chặt chẽ.

## R2. TSFM zero-shot vs. baseline đơn giản trên cổ phiếu Việt Nam

- **Khoảng trống**: *Pretrained TSFMs for Financial Return Forecasting* ([2606.27100](https://arxiv.org/abs/2606.27100)) và *Forecasting Realized Volatility with TSFMs* ([2607.05291](https://arxiv.org/abs/2607.05291)) — cả hai đều năm 2026 — cho thấy lợi thế của TSFM là rất nhỏ so với random walk / mô hình kinh tế lượng. Kronos ([2508.02739](https://arxiv.org/abs/2508.02739)) được huấn luyện riêng cho K-line. Thị trường Việt Nam là một "test set" độc lập tốt.
- **Câu hỏi**: Chronos-2 / TimesFM / Moirai 2.0 / Kronos (zero-shot và fine-tune) so với random walk, HAR, LightGBM, DLinear — cho **lợi suất** và **volatility**.
- **Chỉ số**: MSE/MAE, Rank IC, lợi nhuận danh mục sau phí, Diebold–Mariano test.
- **Khả thi**: chỉ cần suy luận (inference) → CPU/Colab đủ.

## R3. LLM có "nhớ" thị trường Việt Nam không?

- **Khoảng trống**: *The Memorization Problem* ([2504.14765](https://arxiv.org/abs/2504.14765)), *Detecting Lookahead Bias in LLM Forecasts* ([2512.23847](https://arxiv.org/abs/2512.23847)), *Time Travel is Cheating* ([2505.11065](https://arxiv.org/abs/2505.11065)) chủ yếu xét dữ liệu tiếng Anh/thị trường lớn. Với **ngôn ngữ ít tài nguyên** và **thị trường nhỏ**, mức độ ghi nhớ có thấp hơn không → backtest bằng LLM có "sạch" hơn không?
- **Phương pháp**: cho LLM chấm sentiment/dự báo trên tin tiếng Việt **trước** và **sau** knowledge cutoff; so sánh hiệu năng; áp dụng thống kê phát hiện look-ahead bias; thử "che" tên công ty/ngày.
- **Dự án nền**: [P09](../Project-Ideas/P09-Financial-News-NLP-Event-Study/README.md).

## R4. Benchmark VLM nhỏ cho chứng từ tiếng Việt

- **Khoảng trống**: làn sóng VLM parse tài liệu cỡ nhỏ — DeepSeek-OCR ([2510.18234](https://arxiv.org/abs/2510.18234)), PaddleOCR-VL ([2510.14528](https://arxiv.org/abs/2510.14528)), MinerU2.5 ([2509.22186](https://arxiv.org/abs/2509.22186)), SmolDocling ([2503.11576](https://arxiv.org/abs/2503.11576)) — nhưng VMMU ([2508.13680](https://arxiv.org/abs/2508.13680)) cho thấy VLM còn yếu với nội dung đa phương thức tiếng Việt.
- **Đóng góp**: một bộ dữ liệu nhỏ (300–1.000 chứng từ tiếng Việt đã che thông tin cá nhân) + bảng đánh giá **CER, lỗi dấu thanh, field accuracy, latency, VRAM** cho 5–7 model; phân tích lỗi đặc thù tiếng Việt.
- **Nơi công bố phù hợp**: hội nghị trong nước/khu vực (RIVF, SoICT, KSE, MAPR), workshop VLSP.

## R5. Open-vocabulary detection trong giao thông nhiều xe máy

- **Khoảng trống**: Grounding DINO, YOLO-World, SAM 3 được đánh giá chủ yếu trên COCO/LVIS; cảnh **xe máy dày đặc, che khuất nặng** (đặc trưng Đông Nam Á) ít được đo.
- **Phương pháp**: tự quay & gán nhãn 1–2 nghìn frame; đo zero-shot vs. fine-tune (RF-DETR/YOLO26); phân tích lỗi theo mức che khuất/mật độ; thử auto-labeling bằng open-vocabulary rồi fine-tune detector nhỏ (tiết kiệm công gán nhãn bao nhiêu?).
- **Dự án nền**: [P03](../Project-Ideas/P03-Traffic-Video-Analytics/README.md).

## R6. LLMs Get Lost in Multi-Turn Conversation — phiên bản tiếng Việt

- **Khoảng trống**: bài **ICLR 2026 Outstanding** ([2505.06120](https://arxiv.org/abs/2505.06120)) đo trên tiếng Anh. Suy giảm có nặng hơn ở tiếng Việt? Có khác khi có RAG?
- **Phương pháp**: dịch/thích nghi giao thức "sharded instructions" sang tiếng Việt; thử 5–8 LLM qua API; đo accuracy & độ tin cậy; thử các chiến lược giảm thiểu (tóm tắt lại yêu cầu, hỏi lại).
- **Ưu điểm**: chi phí thấp (chỉ API), tái lập một bài đạt giải = luyện kỹ năng nghiên cứu cực tốt.

## R7. "Artificial Hivemind" trong tiếng Việt

- **Khoảng trống**: bài **NeurIPS 2025 Best Paper** ([2510.22954](https://arxiv.org/abs/2510.22954)) cho thấy các LLM khác nhau cho câu trả lời mở đồng nhất đáng kể. Hiện tượng này trong tiếng Việt, văn hóa Việt (ca dao, ẩm thực, lịch sử địa phương)?
- **Phương pháp**: bộ prompt mở tiếng Việt; đo độ đa dạng (embedding similarity, n-gram); so sánh model quốc tế vs. model hỗ trợ tiếng Việt tốt.

## R8. Backbone cho few-shot anomaly detection: DINOv2 vs. DINOv3 vs. CLIP/SigLIP 2

- **Khoảng trống**: PatchCore ([2106.08265](https://arxiv.org/abs/2106.08265)) dùng backbone CNN pretrained ImageNet; DINOv3 ([2508.10104](https://arxiv.org/abs/2508.10104)) tuyên bố đặc trưng dày tốt hơn; LiZAD ([2607.01949](https://arxiv.org/abs/2607.01949)) bắt đầu dùng DINOv3 cho zero-shot. Một **ablation có hệ thống** (backbone × số ảnh bình thường × loại lỗi) trên MVTec AD/VisA còn đáng làm.
- **Dự án nền**: [P06](../Project-Ideas/P06-Industrial-Defect-Detection/README.md).

## R9. LLM-driven alpha mining trên thị trường VN — sống sót qua kiểm định?

- **Khoảng trống**: AlphaAgent ([2502.16789](https://arxiv.org/abs/2502.16789)), QuantaAlpha ([2602.07085](https://arxiv.org/abs/2602.07085)), R&D-Agent-Quant ([2505.15155](https://arxiv.org/abs/2505.15155)) báo cáo kết quả chủ yếu trên thị trường lớn; câu hỏi "bao nhiêu alpha do LLM sinh ra vượt qua **Deflated Sharpe / PBO** và không suy giảm out-of-sample?" ít được trả lời trực tiếp.
- **Phương pháp**: chạy pipeline LLM sinh alpha trên dữ liệu VN (P07), so với genetic programming (P10) và factor cổ điển; báo cáo tỉ lệ "sống sót".

## R10. Semantic cache cho ứng dụng LLM tiếng Việt

- **Khoảng trống**: semantic cache là kỹ thuật tiết kiệm chi phí phổ biến trong gateway (P13), nhưng **ngưỡng tương đồng** nào an toàn cho tiếng Việt (dấu thanh, từ đồng nghĩa, câu hỏi phụ thuộc thời gian)? Đánh đổi hit-rate ↔ tỉ lệ trả lời sai ít được đo có hệ thống.
- **Phương pháp**: log truy vấn thật từ chatbot P02; gán nhãn cặp "cùng ý/khác ý"; so sánh embedding model và ngưỡng; đo tiết kiệm chi phí/latency.
- **Hướng**: ML systems — rất hợp CV "Backend + AI".

---

## Từ dự án → bài báo: checklist

- [ ] **Câu hỏi nghiên cứu** 1 câu, trả lời được bằng thực nghiệm
- [ ] **Related work**: đọc ≥ 15–20 bài gần nhất (dùng [Connected Papers](https://www.connectedpapers.com/) + Semantic Scholar); ghi rõ bạn khác họ ở đâu
- [ ] **Baseline mạnh & đơn giản** (random walk, 1/N, TF-IDF, zero-shot…) — reviewer luôn hỏi
- [ ] **Chia dữ liệu đúng** (theo thời gian với tài chính; không rò rỉ)
- [ ] **Kiểm định thống kê** (nhiều seed, khoảng tin cậy, t-test/Diebold–Mariano, Deflated Sharpe)
- [ ] **Ablation**: bỏ từng thành phần xem ảnh hưởng
- [ ] **Reproducibility**: code + config công khai, seed cố định, README chạy lại bảng kết quả
- [ ] **Hạn chế & đạo đức**: dữ liệu cá nhân, license dữ liệu, rủi ro sử dụng sai
- [ ] Viết LaTeX trên Overleaf, quản lý trích dẫn bằng [Zotero](https://www.zotero.org/)
- [ ] Nơi nộp gợi ý: NCKH sinh viên cấp trường → hội nghị trong nước/khu vực (RIVF, SoICT, KSE, MAPR, VLSP) → workshop của CVPR/NeurIPS/ICLR/ACL (thường nhận bài ngắn, phù hợp người mới)
