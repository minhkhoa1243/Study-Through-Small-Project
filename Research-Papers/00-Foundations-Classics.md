# 00 — Foundations & Classics (kinh điển nền tảng)

> Những bài "gốc rễ" mà gần như mọi nghiên cứu 2025–2026 đều xây dựng lên. Được sắp theo **bài học trong khóa [AI-For-Beginners](https://github.com/microsoft/AI-For-Beginners)** bạn đã học → đọc paper gốc của đúng mô hình bạn vừa học.
> Tất cả mã arXiv đã kiểm tra qua arXiv API (29/09/2026).

---

## Computer Vision (bài 07–12, X1)

| Năm | Bài báo | Vì sao quan trọng | Bài học | Link |
|---|---|---|---|---|
| 2015 | ⭐ **Deep Residual Learning for Image Recognition** (ResNet) — He et al. | Kết nối tắt (residual) giúp train mạng rất sâu; backbone của vô số mô hình | 07, 08 | [arXiv:1512.03385](https://arxiv.org/abs/1512.03385) |
| 2015 | **You Only Look Once: Unified, Real-Time Object Detection** (YOLO) — Redmon et al. | Detection một giai đoạn, real-time; khởi đầu dòng YOLO | 11 | [arXiv:1506.02640](https://arxiv.org/abs/1506.02640) |
| 2015 | 🏆 **Faster R-CNN** — Ren, He, Girshick, Sun | Region Proposal Network; **NeurIPS 2025 Test of Time Award** | 11 | [arXiv:1506.01497](https://arxiv.org/abs/1506.01497) |
| 2015 | **U-Net** — Ronneberger et al. | Encoder–decoder + skip connection cho segmentation; về sau là "xương sống" của diffusion | 12 | [arXiv:1505.04597](https://arxiv.org/abs/1505.04597) |
| 2017 | **Mask R-CNN** — He et al. | Instance segmentation | 12 | [arXiv:1703.06870](https://arxiv.org/abs/1703.06870) |
| 2020 | ⭐ **An Image is Worth 16x16 Words** (ViT) — Dosovitskiy et al. | Đưa Transformer vào thị giác | 07, 18 | [arXiv:2010.11929](https://arxiv.org/abs/2010.11929) |
| 2020 | **End-to-End Object Detection with Transformers** (DETR) — Carion et al. | Detection như bài toán tập hợp, bỏ NMS/anchor; gốc của RT-DETR, RF-DETR | 11 | [arXiv:2005.12872](https://arxiv.org/abs/2005.12872) |
| 2021 | ⭐ **Learning Transferable Visual Models From Natural Language Supervision** (CLIP) — Radford et al. | Ảnh–chữ chung không gian vector; zero-shot | X1 | [arXiv:2103.00020](https://arxiv.org/abs/2103.00020) |
| 2021 | **Emerging Properties in Self-Supervised Vision Transformers** (DINO) — Caron et al. | Học biểu diễn không cần nhãn; tiền thân DINOv2/v3 | 08 | [arXiv:2104.14294](https://arxiv.org/abs/2104.14294) |
| 2021 | **Masked Autoencoders Are Scalable Vision Learners** (MAE) — He et al. | Autoencoder che ảnh → pretrain mạnh | 09 | [arXiv:2111.06377](https://arxiv.org/abs/2111.06377) |

## Generative models (bài 09, 10, 17)

| Năm | Bài báo | Vì sao quan trọng | Bài học | Link |
|---|---|---|---|---|
| 2013 | **Auto-Encoding Variational Bayes** (VAE) — Kingma & Welling | Nền của mô hình sinh xác suất; VAE vẫn dùng trong latent diffusion | 09 | [arXiv:1312.6114](https://arxiv.org/abs/1312.6114) |
| 2014 | **Generative Adversarial Networks** — Goodfellow et al. | Huấn luyện đối kháng | 10 | [arXiv:1406.2661](https://arxiv.org/abs/1406.2661) |
| 2020 | ⭐ **Denoising Diffusion Probabilistic Models** (DDPM) — Ho et al. | Khởi đầu kỷ nguyên diffusion | 10, 17 | [arXiv:2006.11239](https://arxiv.org/abs/2006.11239) |
| 2021 | **High-Resolution Image Synthesis with Latent Diffusion Models** — Rombach et al. | Nền tảng Stable Diffusion | 10 | [arXiv:2112.10752](https://arxiv.org/abs/2112.10752) |

## NLP & Language Models (bài 13–20)

| Năm | Bài báo | Vì sao quan trọng | Bài học | Link |
|---|---|---|---|---|
| 2017 | ⭐ **Attention Is All You Need** — Vaswani et al. | Kiến trúc Transformer | 18 | [arXiv:1706.03762](https://arxiv.org/abs/1706.03762) |
| 2018 | **BERT** — Devlin et al. | Pretrain hai chiều; nền của PhoBERT, FinBERT | 18, 19 | [arXiv:1810.04805](https://arxiv.org/abs/1810.04805) |
| 2019 | **HuggingFace's Transformers** — Wolf et al. | Thư viện bạn sẽ dùng hằng ngày | 18 | [arXiv:1910.03771](https://arxiv.org/abs/1910.03771) · 💻 [code](https://github.com/huggingface/transformers) |
| 2020 | **Language Models are Few-Shot Learners** (GPT-3) — Brown et al. | In-context learning | 20 | [arXiv:2005.14165](https://arxiv.org/abs/2005.14165) |
| 2020 | **Scaling Laws for Neural Language Models** — Kaplan et al. | Quy luật mở rộng theo compute/data/params | 20 | [arXiv:2001.08361](https://arxiv.org/abs/2001.08361) |
| 2020 | ⭐ **Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks** (RAG) — Lewis et al. | Gốc của RAG | 20 | [arXiv:2005.11401](https://arxiv.org/abs/2005.11401) |
| 2021 | **LoRA: Low-Rank Adaptation of Large Language Models** — Hu et al. | Fine-tune rẻ; dùng khắp nơi | 20 | [arXiv:2106.09685](https://arxiv.org/abs/2106.09685) |
| 2022 | **Training Compute-Optimal Large Language Models** (Chinchilla) — Hoffmann et al. | Cân bằng dữ liệu vs. tham số | 20 | [arXiv:2203.15556](https://arxiv.org/abs/2203.15556) |
| 2022 | **Training language models to follow instructions with human feedback** (InstructGPT) — Ouyang et al. | RLHF → ChatGPT | 20, 22 | [arXiv:2203.02155](https://arxiv.org/abs/2203.02155) |
| 2022 | **Chain-of-Thought Prompting Elicits Reasoning in LLMs** — Wei et al. | Suy luận từng bước | 20 | [arXiv:2201.11903](https://arxiv.org/abs/2201.11903) |
| 2022 | ⭐ **ReAct: Synergizing Reasoning and Acting in Language Models** — Yao et al. | Nền của LLM agent | 20, 23 | [arXiv:2210.03629](https://arxiv.org/abs/2210.03629) |
| 2023 | **Direct Preference Optimization** (DPO) — Rafailov et al. | Alignment không cần reward model riêng | 20 | [arXiv:2305.18290](https://arxiv.org/abs/2305.18290) |
| 2024 | **DeepSeekMath** — Shao et al. | Giới thiệu **GRPO**, thuật toán RL đứng sau DeepSeek-R1 | 20, 22 | [arXiv:2402.03300](https://arxiv.org/abs/2402.03300) |

## Reinforcement Learning (bài 22)

| Năm | Bài báo | Vì sao quan trọng | Bài học | Link |
|---|---|---|---|---|
| 2013 | **Playing Atari with Deep Reinforcement Learning** (DQN) — Mnih et al. | Khởi đầu Deep RL | 22 | [arXiv:1312.5602](https://arxiv.org/abs/1312.5602) |
| 2016 | 🏆 **Asynchronous Methods for Deep Reinforcement Learning** (A3C) — Mnih et al. | Actor-critic bất đồng bộ; **ICML 2026 Test of Time Award** | 22 | [arXiv:1602.01783](https://arxiv.org/abs/1602.01783) |
| 2017 | ⭐ **Proximal Policy Optimization Algorithms** (PPO) — Schulman et al. | Thuật toán RL phổ biến nhất (robot, game, RLHF, trading) | 22 | [arXiv:1707.06347](https://arxiv.org/abs/1707.06347) |

---

**Gợi ý thứ tự đọc (8 bài đầu tiên):** ResNet → Transformer → ViT → CLIP → DDPM → RAG → ReAct → PPO.
