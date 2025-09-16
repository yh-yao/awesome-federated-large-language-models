# Awesome Federated Large Language Models (FedLLM) [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of resources on **Federated Large Language Models (FedLLMs)** – an emerging paradigm that trains or adapts large language models (LLMs) across distributed data sources while preserving privacy.  

---

## 📑 Contents
* [Surveys](#-surveys)
* [Federated Fine-Tuning](#-federated-fine-tuning)
* [Federated Prompt Learning](#-federated-prompt-learning)
* [Potential Directions](#-potential-directions)
* [LLMs for Federated Learning](#-llms-for-federated-learning)
* [Applications](#-applications)


---

## 📚 Surveys

| Title | Year | Link |
|-------|------|------|
| Federated Large Language Models: Current Progress and Future Directions | 2024 | [arXiv:2409.15723](https://arxiv.org/abs/2409.15723) |
---

## 🎯 Federated Fine-Tuning

| Area | Topic | Approaches |
|---|---|---|
| **Heterogeneity** | **Data Heterogeneity** | [FedDAT](https://arxiv.org/abs/2308.12305), [AAAI’24 version](https://dl.acm.org/doi/10.1609/aaai.v38i10.29007); [RaFFM](https://arxiv.org/abs/2310.00247), [OpenReview](https://openreview.net/forum?id=JLulsRraDc); [FedKC](https://dl.acm.org/doi/10.1145/3485447.3511988) |
|  | **Model Heterogeneity** | [FedLoRA / pFedLoRA](https://arxiv.org/abs/2310.13283); [HetLoRA](https://arxiv.org/abs/2401.06432); [FlexLoRA](https://arxiv.org/abs/2402.11505) ([NeurIPS’24 poster](https://neurips.cc/virtual/2024/poster/94124)); [FedPCL (pretrained models)](https://ui.adsabs.harvard.edu/abs/2022arXiv220910083T/abstract); [FedBRB (robust LoRA)](https://arxiv.org/abs/2405.01106) |
| **Privacy and Security** | **Security & Robustness** | [Vulnerabilities of FM-FL](https://arxiv.org/abs/2401.14484); [Survey – NIST blog](https://www.nist.gov/blogs/cybersecurity-insights/privacy-attacks-federated-learning) |
|  | **Privacy** | [FedPIT (Fed Instruction Tuning)](https://arxiv.org/abs/2305.05644); [FFA-LoRA (ICLR’24)](https://proceedings.iclr.cc/paper_files/paper/2024/file/4e243e95c913b367775d71d7182b99d9-Paper-Conference.pdf) |
|  | **Attacks** | [Recovering Private Text](https://arxiv.org/abs/2205.08514); [Decepticons](https://arxiv.org/abs/2201.12675); [Unveiling Vulnerabilities](https://aclanthology.org/2023.gem-1.10.pdf) |
|  | **Defense** | [FedML-HE](https://arxiv.org/abs/2303.10837); [FedBiOT](https://arxiv.org/abs/2406.17706) ([code](https://github.com/harliwu/fedbiot)) |
| **Efficiency** | **Training Efficiency** | [Grouper](https://proceedings.neurips.cc/paper_files/paper/2023/file/066e4dbfeccb5dc2851acd5eca584937-Paper-Conference.pdf); [FedYOLO](https://arxiv.org/abs/2307.04905); [FedTune/FedPETuning](https://aclanthology.org/2023.findings-acl.632/) |
|  | **Communication Efficiency** | [CEFHRI](https://arxiv.org/abs/2308.14965); [FedKSeed](https://arxiv.org/abs/2312.06353); [FedRDMA](https://dl.acm.org/doi/10.1145/3704452.3708944) |
|  | **Parameter Efficiency** | [Exploring PEFT in FL](https://arxiv.org/abs/2212.10025); [FedPETuning](https://aclanthology.org/2023.findings-acl.632/); [SLoRA](https://arxiv.org/abs/2308.06522); [FFA-LoRA](https://proceedings.iclr.cc/paper_files/paper/2024/file/4e243e95c913b367775d71d7182b99d9-Paper-Conference.pdf); [FlexLoRA](https://arxiv.org/abs/2402.11505); [LP-FL](https://arxiv.org/abs/2307.13896) |
| **Frameworks** | **Cross-Silo** | [FedRDMA](https://dl.acm.org/doi/10.1145/3704452.3708944); [CrossLM](https://arxiv.org/abs/2312.05842) |
|  | **Cross-Device** | [FwdLLM](https://arxiv.org/abs/2308.13894); [Edge FL](https://dl.acm.org/doi/abs/10.1145/3650203.3663331) |
|  | **Decentralized Training** | [OpenFedLLM](https://arxiv.org/abs/2402.06954) |
|  | **Black-box & Transfer Learning** | [Fed-BBPL](https://arxiv.org/abs/2308.06522); [ZooPFL](https://arxiv.org/abs/2305.05655); [Grounding](https://aclanthology.org/2023.emnlp-main.84/) |
|  | **Instruction Tuning** | [FederatedScope-LLM](https://arxiv.org/abs/2309.00363); [FedIT](https://arxiv.org/abs/2305.05644) |
| **Evaluation** | **Datasets** | [FederatedScope-LLM datasets](https://federatedscope.io/docs/llm/); [OpenFedLLM](https://arxiv.org/abs/2402.06954) |
|  | **Benchmarks** | [FedLLM-Bench](https://arxiv.org/abs/2406.04845) ([GitHub](https://github.com/rui-ye/FedLLM-Bench)) |
|  | **Convergence Analysis** | [FedPEAT](https://arxiv.org/abs/2310.09064); [FedMeZO](https://arxiv.org/abs/2405.03291) |                                                                                                                                                                                                                                                                                                                                                       |


---

## ✨ Federated Prompt Learning

| Area                  | Topic                                                                 |
|-----------------------|------------------------------------------------------------------------|
| Prompt Generation     | [FedTPG](https://arxiv.org/abs/2310.06123) · [Code](https://github.com/boschresearch/FedTPG), [TPFL](https://arxiv.org/abs/2310.04455) |
| Few-Shot              | [FedFSL](https://arxiv.org/abs/2104.00365) |
| Chain-of-Thoughts     | [Fed-SP-SC](https://arxiv.org/abs/2304.13911), [FedLogic](https://arxiv.org/abs/2308.15324) |
| Personalization       | [pFL (pFedPrompt)](https://dl.acm.org/doi/10.1145/3543507.3583518), [FedLogic](https://arxiv.org/abs/2308.15324), [Fed-DPT](https://arxiv.org/abs/2310.03103) |
| Multi-Domain          | [FedAPT](https://ojs.aaai.org/index.php/AAAI/article/view/29434), [Profit](https://arxiv.org/abs/2310.04627) |
| Parameter Efficient   | [FedPepTAO](https://arxiv.org/abs/2310.15080), [FedLoRA](https://openreview.net/forum?id=bZh06ptG9r) |
| Communication Efficient | [FedPrompt](https://arxiv.org/abs/2208.12268) |
| Blackbox              | [FedBPT](https://arxiv.org/abs/2310.01467) |
| Retrieval-Augmented   | [FeB4RAG](https://arxiv.org/abs/2402.11891) |
| Applications          | [Multilingual (Breaking Borders 2023)](https://arxiv.org/abs/2309.15723), [Recommender (Guo 2024)](https://arxiv.org/abs/2401.14678), [Medical VQA (Zhu 2024)](https://arxiv.org/abs/2402.09677), [Weather Forecasting (Chen 2023)](https://arxiv.org/abs/2305.14244), [Virtual Reality (Zhou 2024)](https://arxiv.org/abs/2402.09729) |

---

## 🔮 Potential Directions

| Area | Topic |
|------|-------|
| Real-World Deployment | Personalized FL on Confidential Data; Collaborative FL |
| Multi-Modality | Modality Co-optimization |
| Federated Pre-Training | Efficient Data Exchange; Model Architecture Design |
| Federated Inference | Real-time On-device Inference |
| LLMs for FL | Synthetic Data Generation; Capacity-Augmented FL; Responsible and Ethical LLM4FL |

---

## ⚙️ LLMs for Federated Learning

| Area | Contribution |
|------|--------------|
| Synthetic Data Generation | Use LLMs to generate diverse training data to mitigate scarcity |
| Capacity-Augmented FL | Leverage LLM knowledge distillation and prompt engineering |
| Responsible & Ethical LLM4FL | Ensure compliance with privacy, fairness, and law |

---

## 🌍 Applications

| Domain | Example Works |
|--------|---------------|
| Multilingual |  |
| Recommender Systems |  |
| Medical VQA | |
| Weather Forecasting |  |
| Virtual Reality |  | 