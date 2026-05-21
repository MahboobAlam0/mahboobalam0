<h1 align="center">Hi, I'm Mahboob Alam 👋</h1>

<p align="center">
  <b>ML Engineer · Computer Vision · LLM &amp; RAG</b><br>
  Building end-to-end ML systems that stay valid <i>outside</i> notebooks — leakage-free evaluation, deployable architectures, and decisions over metrics.
</p>

<p align="center">
  📍 Pune, India &nbsp;·&nbsp; 🎓 M.Tech Data Science @ DIAT (DRDO) &nbsp;·&nbsp; 💼 Open to Full-Time
</p>

<p align="center">
  <a href="https://mahboob-alam-portfolio.netlify.app"><img src="https://img.shields.io/badge/Portfolio-0A66C2?style=for-the-badge&logo=netlify&logoColor=white" alt="Portfolio"></a>
  <a href="https://www.linkedin.com/in/mahboobalam786"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://www.kaggle.com/armahboobalam"><img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle"></a>
  <a href="mailto:mahboobalam7131@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## 🔭 What I work on

- **Computer vision & segmentation** — physics-informed and lightweight architectures, not depth for its own sake
- **LLMs & RAG** — QLoRA/PEFT fine-tuning, retrieval pipelines, evidence-grounded QA
- **Production ML** — FastAPI services, Docker, CI/CD, calibrated thresholds, and cost-aware decisioning

I care about correct problem framing before modeling, leakage-free evaluation, models small enough to deploy, and turning outputs into **real decisions**.

---

## 🚀 Featured Projects

### 🌊 Computer Vision & Segmentation — *MoES-sponsored research, published*

A suite of underwater fish-segmentation models built during my research internship at DIAT, trained on an NVIDIA RTX 6000 Ada (48 GB) with mixed precision.

#### PIAU-Net — Physics-Informed Attention U-Net *(Published)*
`PyTorch` · `Attention U-Net` · `Physics-Informed DL`

- Embedded the **Jaffe–McGlamery optical scattering model** directly into an Attention U-Net — the **first physics-informed architecture for underwater fish segmentation**.
- Reached **97.38% mIoU (LFish)** and **93.98% (AquaOV255)**, outperforming DeepLabV3+ by **+3.44 pp**.

🔗 [github.com/MahboobAlam0/piaunet](https://github.com/MahboobAlam0/piaunet)

#### FishSegDet — High-Accuracy Detection + Segmentation
`PyTorch` · `ConvNeXt-V2-L` · `BiFPN` · `TAL`

- ConvNeXt-V2-L backbone with **BiFPN** feature fusion and **Task-Aligned Learning**, reaching **70.0% mAP, 95.1% mAP50, 99.1% pixel accuracy**.
- Surpassed YOLOv11l-seg by **+7.10 pp mAP50**.

🔗 [github.com/MahboobAlam0/FishSegDet](https://github.com/MahboobAlam0/FishSegDet)

#### LiteFishSeg — Lightweight Real-Time Segmentation
`PyTorch` · `MobileNetV3` · `BiFPN` · `FCOS`

- Compact **9.08M-parameter** model (MobileNetV3 + BiFPN + FCOS) hitting **80.3% mIoU** — at **2.7× fewer parameters** than YOLOv10l-seg.

🔗 [github.com/MahboobAlam0/LiteFishSeg](https://github.com/MahboobAlam0/LiteFishSeg)

---

### 🧠 LLMs & RAG

#### Distill — Fine-Tuned Qwen2.5-3B for Text-to-SQL (QLoRA)
`Python` · `QLoRA` · `PEFT` · `BitsAndBytes` · `FastAPI` · `Docker`

- Fine-tuned **Qwen2.5-3B** for natural-language → SQL on a free Kaggle T4 using QLoRA (4-bit NF4, LoRA r=16/α=32) over 28K examples, with a custom harness scoring **exact match, BLEU, and SQLite execution accuracy**.
- Lifted exact-match **2.33% → 30.67% (13×)** and reached **55.03% execution accuracy** on 7,858 tests — then shipped a **114 MB LoRA adapter** (vs a 6 GB full model) via FastAPI, Docker, and GitHub Actions.

🔗 [github.com/MahboobAlam0/Distill---Fine-tuned-Qwen2.5-3B](https://github.com/MahboobAlam0/Distill---Fine-tuned-Qwen2.5-3B)

#### AI Clinical RAG — Evidence-Grounded QA over PubMed
`Sentence-Transformers` · `Qdrant` · `Groq Llama-3.3-70B` · `FastAPI` · `Docker`

- Fine-tuned `all-MiniLM-L6-v2` on 4,500 PubMedQA pairs (MultipleNegativesRankingLoss) and indexed **5,355 abstracts** in Qdrant, with a cosine-score estimator flagging answers **HIGH / MED / LOW** confidence.
- Improved **nDCG@10 0.806 → 0.926 (+12%)** and **Accuracy@1 0.700 → 0.823**; served SSE streaming at **874 ms avg latency** with LRU caching, per-IP rate limiting, request tracing, and **80% test coverage** in CI.

🔗 [github.com/MahboobAlam0/ai-clinical-rag](https://github.com/MahboobAlam0/ai-clinical-rag)

---

### ⚙️ Applied ML & Decision Systems

#### Policy-Aware Credit Decision Engine
`LightGBM` · `SHAP` · `FastAPI` · `Streamlit` · `Docker Compose` · `GitHub Actions`

- Decoupled a **Platt-scaled LightGBM** probability-of-default model from a configurable business-policy layer (**EL = PD × LGD × EAD**) with dual-threshold approve/review/decline logic and fairness controls — replacing a monolith where ML risk and business rules couldn't be audited independently.
- Mapped **SHAP attributions → regulatory adverse-action reason codes**, making every rejection explainable under lending compliance.

🔗 [github.com/MahboobAlam0/policy-aware-credit-decision-engine](https://github.com/MahboobAlam0/policy-aware-credit-decision-engine)

#### HMT-ECGNet — Lightweight Cardiac Triage Classifier
`PyTorch` · `PTB-XL` · `FastAPI` · `Docker`

- Built a **338K-parameter 1D CNN** on PTB-XL (12-lead, multi-label) with **Asymmetric Focal Loss** to replace ResNet-1D (8.7M params) in CPU-constrained clinical settings.
- Achieved **Macro-AUROC 0.92, MI AUROC 0.98, Macro-F1 0.73** at **26× fewer parameters**, with **10–30 ms CPU inference** per ECG, served via Dockerized FastAPI.

🔗 [github.com/MahboobAlam0/hmt_ecgnet](https://github.com/MahboobAlam0/hmt_ecgnet)

> More: [FinSight-AI](https://github.com/MahboobAlam0/finsight-ai) (financial-news NLP) · [Churn Intervention System](https://github.com/MahboobAlam0/businesschurn) (business-metric-driven retention)

---

## 📄 Publication

**Mahboob Alam**, S. V. Dhavale, D. Srikanth. *PIAUNet: An Enhanced U-Net Framework for Underwater Segmentation in Aquaculture.* **IJTE, ISTE**, Vol. 48, No. 2, Dec 2025. *(Peer-reviewed)*

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-02569B?style=flat)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat&logo=huggingface&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)

**Focus areas:** CNNs · Transformers · Semantic Segmentation · Physics-Informed Neural Networks · QLoRA/PEFT · Retrieval-Augmented Generation · SHAP · Grad-CAM

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=MahboobAlam0&show_icons=true&hide_border=true&count_private=true" alt="GitHub Stats" height="165">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=MahboobAlam0&layout=compact&hide_border=true" alt="Top Languages" height="165">
</p>

---

<p align="center"><i>Open to Full-Time ML Engineer / Data Scientist roles — let's talk.</i></p>
