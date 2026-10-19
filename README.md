<div align="center">

# Mahboob Alam

<img src="https://readme-typing-svg.demolab.com?font=Inter&weight=500&size=20&pause=1400&color=4F8EF7&center=true&vCenter=true&width=560&lines=I+build+things+with+computer+vision+and+LLMs;From+training+runs+to+deployed+APIs;Currently+open+to+AI%2FML+engineering+roles" alt="Typing SVG" />

<a href="https://mahboobalam.netlify.app"><img src="https://img.shields.io/badge/Portfolio-111827?style=for-the-badge&logo=netlify&logoColor=white" alt="Portfolio" /></a>
<a href="https://www.linkedin.com/in/mahboobalam786/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="https://huggingface.co/mahboobalam0"><img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face" /></a>
<a href="mailto:mahboobalam7131@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>

</div>

<br>

Hey, I'm Mahboob. I recently finished my M.Tech in Data Science at DIAT, Pune, and I spend most of my time somewhere between computer vision and language models.

What I enjoy most is the full journey of a project: cleaning up messy data, getting a model to actually learn something useful, measuring it honestly, and then wrapping it in an API so other people can use it. A model that only lives in a notebook never feels finished to me.

Right now I'm a research intern working on underwater computer vision, which is a surprisingly fun problem. Murky water, strange lighting, and color distortion make even simple tasks hard, and that's a big part of why I like it.

I'm based in Pune and looking for AI Engineer or ML Engineer roles. If you're working on something interesting, I'd love to hear about it.

<br>

## Things I've built

### Distill &nbsp;<sub>Text-to-SQL assistant</sub>

I wanted to see how far a small open model could go at turning plain English into SQL. I fine-tuned Qwen2.5-3B on around 28K examples using QLoRA, which kept training cheap enough to run on modest hardware. Out of the box the model got only 2.33% of queries exactly right. After fine-tuning, that went up to **30.67%**. It's served through FastAPI and packaged with Docker.

`PyTorch` · `QLoRA` · `PEFT` · `FastAPI` · `Docker`

### AI Clinical RAG &nbsp;<sub>Question answering over clinical knowledge</sub>

A retrieval-augmented system that looks up the right context before answering clinical questions. Most of the work went into making retrieval better, using sentence embeddings with Qdrant for semantic search. Getting the right document to the top pushed Accuracy@1 from 70.0% to **82.3%**.

`Python` · `Qdrant` · `Sentence Transformers` · `FastAPI`

### PIAUNet &nbsp;<sub>Underwater image segmentation</sub>

This one grew out of my research. It's an Attention U-Net that brings physics into the model to deal with how light behaves underwater, built for segmentation in aquaculture. It reached **97.38% mIoU**, and the work was published in the *Indian Journal of Technical Education*.

`PyTorch` · `Computer Vision` · `Segmentation`

### HMT-ECGNet &nbsp;<sub>Lightweight ECG classification</sub>

I wanted an ECG classifier small enough to run almost anywhere without giving up much accuracy. The final model has just **0.34M parameters** and still hits a **0.92 Macro-AUROC**. It's deployed behind a FastAPI endpoint.

`PyTorch` · `CNN` · `FastAPI`

<br>

## What I work with

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Transformers](https://img.shields.io/badge/Transformers-1F2937?style=flat-square)
![PEFT](https://img.shields.io/badge/PEFT%20%2F%20QLoRA-6D28D9?style=flat-square)
![RAG](https://img.shields.io/badge/RAG-6D28D9?style=flat-square)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

Day to day that means PyTorch and Hugging Face for modeling, OpenCV for anything image-related, Qdrant when I need vector search, and FastAPI plus Docker whenever something needs to leave my laptop.

<br>

## Publication

**Physics-Informed Attention U-Net (PIAUNet): An Enhanced U-Net Framework for Underwater Segmentation in Aquaculture**
<br>
*Indian Journal of Technical Education*, 2025

<br>

---

<div align="center">
<sub>Always happy to talk about ML, swap ideas, or collaborate. The quickest way to reach me is <a href="mailto:mahboobalam7131@gmail.com">email</a> or <a href="https://www.linkedin.com/in/mahboobalam786/">LinkedIn</a>.</sub>
</div>
