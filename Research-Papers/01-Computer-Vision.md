# 01 — Computer Vision (ưu tiên 2024–2026)

> Ký hiệu: ⭐ nên đọc trước · 🏆 đạt giải · 🆕 năm 2026 · 🔥 preprint trending 9/2026 · 💻 có code · `P0x` dự án liên quan.
> Mọi mã arXiv đã kiểm tra qua arXiv API (29/09/2026). Năm = năm xuất hiện bản arXiv đầu tiên.

---

## A. Real-time Object Detection & Tracking → `P03`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2021 | **ByteTrack: Multi-Object Tracking by Associating Every Detection Box** | Tận dụng cả box điểm thấp khi ghép track → tracking đơn giản mà mạnh | [2110.06864](https://arxiv.org/abs/2110.06864) · 💻 [code](https://github.com/FoundationVision/ByteTrack) |
| 2023 | ⭐ **DETRs Beat YOLOs on Real-time Object Detection** (RT-DETR) | DETR đầu tiên đạt tốc độ real-time cạnh tranh YOLO | [2304.08069](https://arxiv.org/abs/2304.08069) |
| 2024 | **YOLOv10: Real-Time End-to-End Object Detection** | Huấn luyện không cần NMS khi suy luận | [2405.14458](https://arxiv.org/abs/2405.14458) |
| 2024 | **D-FINE: Redefine Regression Task in DETRs as Fine-grained Distribution Refinement** | Hồi quy box dạng phân phối tinh chỉnh dần | [2410.13842](https://arxiv.org/abs/2410.13842) |
| 2025 | **YOLOv12: Attention-Centric Real-Time Object Detectors** | Đưa attention vào lõi YOLO | [2502.12524](https://arxiv.org/abs/2502.12524) |
| 2025 | **Real-Time Object Detection Meets DINOv3** (DEIMv2) | Dùng đặc trưng DINOv3 cho detector real-time, nhiều cỡ từ GPU tới mobile | [2509.20787](https://arxiv.org/abs/2509.20787) |
| 2025 | ⭐ **RF-DETR: Neural Architecture Search for Real-Time Detection Transformers** | NAS chia sẻ trọng số để tối ưu accuracy–latency; license Apache-2.0 | [2511.09554](https://arxiv.org/abs/2511.09554) · 💻 [code](https://github.com/roboflow/rf-detr) |
| 2026 | 🆕 **Ultralytics YOLO26: Unified Real-Time End-to-End Vision Models** | Họ model NMS-free, đa tác vụ (detect/segment/pose) | [2606.03748](https://arxiv.org/abs/2606.03748) · 💻 [code](https://github.com/ultralytics/ultralytics) |

## B. Open-vocabulary Detection & Segmentation → `P03`, `P06`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2023 | **Grounding DINO** | Phát hiện vật thể theo câu mô tả tự do | [2303.05499](https://arxiv.org/abs/2303.05499) · 💻 [code](https://github.com/IDEA-Research/GroundingDINO) |
| 2023 | ⭐ **Segment Anything** (SAM) | Segmentation theo prompt (điểm/box), dataset SA-1B | [2304.02643](https://arxiv.org/abs/2304.02643) |
| 2024 | **YOLO-World: Real-Time Open-Vocabulary Object Detection** | Open-vocabulary ở tốc độ real-time | [2401.17270](https://arxiv.org/abs/2401.17270) · 💻 [code](https://github.com/AILab-CVC/YOLO-World) |
| 2024 | **SAM 2: Segment Anything in Images and Videos** | Mở rộng SAM sang video với bộ nhớ | [2408.00714](https://arxiv.org/abs/2408.00714) · 💻 [code](https://github.com/facebookresearch/sam2) |
| 2025 | ⭐ **SAM 3: Segment Anything with Concepts** | Segment + track **mọi thực thể của một khái niệm** từ prompt chữ/ảnh mẫu | [2511.16719](https://arxiv.org/abs/2511.16719) · 💻 [code](https://github.com/facebookresearch/sam3) |
| 2025 | 🏆 **SAM 3D: 3Dfy Anything in Images** | Tái tạo 3D vật thể từ 1 ảnh — CVPR 2026 Best Paper Honorable Mention | [2511.16624](https://arxiv.org/abs/2511.16624) |

## C. Visual Foundation Models & Representation Learning → `P05`, `P06`, `P08`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2023 | **Sigmoid Loss for Language Image Pre-Training** (SigLIP) | Thay softmax contrastive bằng sigmoid → hiệu quả hơn CLIP | [2303.15343](https://arxiv.org/abs/2303.15343) |
| 2023 | **DINOv2: Learning Robust Visual Features without Supervision** | Đặc trưng tự giám sát dùng chung cho nhiều tác vụ | [2304.07193](https://arxiv.org/abs/2304.07193) |
| 2025 | **SigLIP 2: Multilingual Vision-Language Encoders…** | Đa ngôn ngữ, định vị tốt, đặc trưng dày → hợp truy vấn tiếng Việt | [2502.14786](https://arxiv.org/abs/2502.14786) |
| 2025 | **Perception Encoder: The best visual embeddings are not at the output of the network** | Embedding tốt nhất nằm ở lớp giữa | [2504.13181](https://arxiv.org/abs/2504.13181) |
| 2025 | **V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning** | Học từ video không nhãn → hiểu, dự đoán, lập kế hoạch cho robot | [2506.09985](https://arxiv.org/abs/2506.09985) |
| 2025 | ⭐ **DINOv3** | Scale học tự giám sát, khắc phục suy giảm đặc trưng dày | [2508.10104](https://arxiv.org/abs/2508.10104) · 💻 [code](https://github.com/facebookresearch/dinov3) |
| 2026 | 🆕 **V-JEPA 2.1: Unlocking Dense Features in Video Self-Supervised Learning** | Đặc trưng dày cho ảnh & video | [2603.14482](https://arxiv.org/abs/2603.14482) |

## D. 3D / 4D Vision (hình học feed-forward — hướng rất nóng)

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2023 | **3D Gaussian Splatting for Real-Time Radiance Field Rendering** | Biểu diễn cảnh 3D bằng Gaussian, render real-time | [2308.04079](https://arxiv.org/abs/2308.04079) |
| 2023 | **DUSt3R: Geometric 3D Vision Made Easy** | Tái tạo 3D từ cặp ảnh không cần calib | [2312.14132](https://arxiv.org/abs/2312.14132) |
| 2024 | **Depth Anything V2** | Ước lượng độ sâu 1 ảnh mạnh, dễ dùng | [2406.09414](https://arxiv.org/abs/2406.09414) |
| 2025 | 🏆 ⭐ **VGGT: Visual Geometry Grounded Transformer** | 1 lượt forward suy ra camera, depth, point map — **CVPR 2025 Best Paper** | [2503.11651](https://arxiv.org/abs/2503.11651) · 💻 [code](https://github.com/facebookresearch/vggt) |
| 2025 | **Depth Anything 3: Recovering the Visual Space from Any Views** | Transformer thường cho hình học từ số view bất kỳ | [2511.10647](https://arxiv.org/abs/2511.10647) · 💻 [code](https://github.com/ByteDance-Seed/Depth-Anything-3) |
| 2025 | 🏆 ⭐ **Efficiently Reconstructing Dynamic Scenes One D4RT at a Time** | Tái tạo hình học + chuyển động cảnh 4D từ video — **CVPR 2026 Best Paper** | [2512.08924](https://arxiv.org/abs/2512.08924) |
| 2025 | 🏆 **Native and Compact Structured Latents for 3D Generation** | Biểu diễn voxel thưa (O-Voxel) cho sinh 3D — **CVPR 2026 Best Student Paper** | [2512.14692](https://arxiv.org/abs/2512.14692) |

## E. Vision-Language Models & Document AI → `P04`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2023 | ⭐ **Visual Instruction Tuning** (LLaVA) | Công thức gốc ghép vision encoder + LLM | [2304.08485](https://arxiv.org/abs/2304.08485) |
| 2025 | **SmolDocling** | VLM 256M tham số chuyển đổi tài liệu end-to-end | [2503.11576](https://arxiv.org/abs/2503.11576) · 💻 [docling](https://github.com/docling-project/docling) |
| 2025 | **MinerU2.5** | VLM 1.2B parse tài liệu độ phân giải cao, coarse-to-fine | [2509.22186](https://arxiv.org/abs/2509.22186) · 💻 [code](https://github.com/opendatalab/MinerU) |
| 2025 | **PaddleOCR-VL** | VLM 0.9B parse tài liệu đa ngôn ngữ | [2510.14528](https://arxiv.org/abs/2510.14528) · 💻 [code](https://github.com/PaddlePaddle/PaddleOCR) |
| 2025 | ⭐ **DeepSeek-OCR: Contexts Optical Compression** | Nén ngữ cảnh dài thành ít "vision token" — góc nhìn mới về OCR và long-context | [2510.18234](https://arxiv.org/abs/2510.18234) · 💻 [code](https://github.com/deepseek-ai/DeepSeek-OCR) |
| 2025 | **Qwen3-VL Technical Report** | VLM mở mạnh, ngữ cảnh dài, đa ngôn ngữ | [2511.21631](https://arxiv.org/abs/2511.21631) · 💻 [code](https://github.com/QwenLM/Qwen3-VL) |
| 2026 | 🆕 **PaddleOCR-VL-1.6** | Hậu huấn luyện tiến dần, tinh chỉnh vùng yếu — SOTA trên OmniDocBench (theo tác giả) | [2606.03264](https://arxiv.org/abs/2606.03264) |
| 2026 | 🆕 **Unlimited OCR Works** | Attention cửa sổ trượt tham chiếu → OCR nhiều trang không tăng bộ nhớ | [2606.23050](https://arxiv.org/abs/2606.23050) |

## F. Generative Models (diffusion / flow)

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2022 | **Flow Matching for Generative Modeling** | Nền của nhiều model sinh ảnh/video hiện đại | [2210.02747](https://arxiv.org/abs/2210.02747) |
| 2022 | ⭐ **Scalable Diffusion Models with Transformers** (DiT) | Thay U-Net bằng Transformer trong diffusion | [2212.09748](https://arxiv.org/abs/2212.09748) |
| 2025 | **Mean Flows for One-step Generative Modeling** | Sinh ảnh chất lượng cao trong 1 bước | [2505.13447](https://arxiv.org/abs/2505.13447) |
| 2025 | **Diffusion Transformers with Representation Autoencoders** (RAE) | Thay VAE bằng encoder biểu diễn pretrained | [2510.11690](https://arxiv.org/abs/2510.11690) |
| 2025 | **Back to Basics: Let Denoising Generative Models Denoise** | Cho mạng dự đoán ảnh sạch thay vì nhiễu | [2511.13720](https://arxiv.org/abs/2511.13720) |
| 2026 | 🆕 **Scaling Text-to-Image Diffusion Transformers with Representation Autoencoders** | Mở rộng RAE cho text-to-image quy mô lớn | [2601.16208](https://arxiv.org/abs/2601.16208) |
| 2026 | 🆕 🏆 **ChordEdit: One-Step Low-Energy Transport for Image Editing** | Chỉnh sửa ảnh 1 bước bằng optimal transport — CVPR 2026 Best Student Paper HM | [2602.19083](https://arxiv.org/abs/2602.19083) |

## G. World Models & Embodied / Game Agents

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2025 | **Cosmos World Foundation Model Platform for Physical AI** | Nền tảng world model cho robot/xe tự hành | [2501.03575](https://arxiv.org/abs/2501.03575) |
| 2026 | 🆕 🏆 **NitroGen: An Open Foundation Model for Generalist Gaming Agents** | Model vision-action học từ gameplay, tổng quát hóa nhiều game — CVPR 2026 Best Paper HM | [2601.02427](https://arxiv.org/abs/2601.02427) |
| 2026 | 🔥 **WorldCrafter: Consistent Video World Model with Implicit 3D-aware Memory** | World model video nhất quán theo thời gian/góc nhìn | [2609.24984](https://arxiv.org/abs/2609.24984) |
| 2026 | 🔥 **Training Object Permanence in World Models** | Dạy world model "vật thể vẫn tồn tại khi bị che" | [2609.28654](https://arxiv.org/abs/2609.28654) |

## H. Anomaly Detection (công nghiệp) → `P06`

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2021 | ⭐ **Towards Total Recall in Industrial Anomaly Detection** (PatchCore) | Memory bank đặc trưng patch + kNN; baseline rất mạnh | [2106.08265](https://arxiv.org/abs/2106.08265) · 💻 [anomalib](https://github.com/open-edge-platform/anomalib) |
| 2023 | **WinCLIP: Zero-/Few-Shot Anomaly Classification and Segmentation** | Dùng CLIP + prompt cho zero-shot | [2303.14814](https://arxiv.org/abs/2303.14814) |
| 2023 | **AnomalyCLIP: Object-agnostic Prompt Learning for Zero-shot Anomaly Detection** | Prompt học được, không phụ thuộc loại vật thể | [2310.18961](https://arxiv.org/abs/2310.18961) · 💻 [code](https://github.com/zqhang/AnomalyCLIP) |
| 2026 | 🆕 **LiZAD: A Lightweight Zero-Shot Anomaly Detection Framework for Industrial Manufacturing** | DINOv3 + MobileCLIP2, nhẹ cho thiết bị biên | [2607.01949](https://arxiv.org/abs/2607.01949) |

## I. Computer Vision / VLM cho tiếng Việt (cơ hội nghiên cứu bản địa)

| Năm | Bài báo | Điểm chính | Link |
|---|---|---|---|
| 2024 | **Vintern-1B: An Efficient Multimodal LLM for Vietnamese** | VLM nhỏ cho OCR/trích xuất tài liệu tiếng Việt | [2408.12480](https://arxiv.org/abs/2408.12480) · 💻 [model](https://huggingface.co/5CD-AI/Vintern-1B-v3_5) |
| 2025 | **VMMU: A Vietnamese Multitask Multimodal Understanding and Reasoning Benchmark** (tên phiên bản đầu: *ViExam*) | VLM còn kém trên đề thi đa phương thức tiếng Việt | [2508.13680](https://arxiv.org/abs/2508.13680) |
| 2026 | 🆕 **ViCLIP-OT: The First Foundation Vision-Language Model for Vietnamese Image-Text Retrieval with Optimal Transport** | CLIP cho truy xuất ảnh–chữ tiếng Việt | [2602.22678](https://arxiv.org/abs/2602.22678) |

---

### Đọc gì trước (lộ trình 2 tuần cho CV)
1. RT-DETR → RF-DETR → YOLO26 (hiểu detector hiện đại cho P03)
2. SAM → SAM 3 (segmentation theo khái niệm)
3. DINOv2 → DINOv3, SigLIP 2 (biểu diễn nền cho P05, P06)
4. LLaVA → DeepSeek-OCR → PaddleOCR-VL (Document AI cho P04)
5. VGGT → D4RT (xu hướng 3D/4D, hiểu vì sao đoạt giải)
