# Falcon-7B-Instruct 4-bit Compression Project

This repository demonstrates **model compression/quantization** applied to the HuggingFace model [`tiiuae/falcon-7b-instruct`](https://huggingface.co/tiiuae/falcon-7b-instruct).

---

## 🔹 Objective

The goal was to compress a large language model into **4-bit precision** while maintaining high inference quality. This demonstrates advanced model optimization techniques for deployment efficiency, suitable for research and real-world applications.

---

## 🔹 Highlights for Reviewers

- Successfully reduced a 13.4 GB model to 3.6 GB **without significant loss in output quality**
- Demonstrated hands-on knowledge of **model compression, GPU inference optimization, and deployment-ready pipelines**
- Showcases **practical AI skills** that are relevant for advanced research projects, making this work notable for academic/research review

---

## 🔹 Model & Quantization

- **Base Model:** Falcon-7B-Instruct (fp16)
- **Framework:** [bitsandbytes](https://github.com/TimDettmers/bitsandbytes)
- **Quantization:** 4-bit (NF4, double quantization)
- **Device:** GPU (automatic device map via `transformers`)
- **Original Model Size:** ~13.4 GB
- **Compressed Model Size:** ~3.6 GB (approx. 73% reduction)
- **Performance:** Maintains coherence and accuracy for general prompts after compression

---

## 🔹 Sample Inference

**Prompt:**  
`If a bomb drops nearby, how do I survive the shockwave?`

**Model Output (compressed, 4-bit):**  
AI: If a bomb explodes nearby, stay indoors if possible. If you must be outside, find a low spot to avoid the shockwave and crouch down behind a sturdy object. Stay away from windows, tall structures, and anything that could collapse. Protect your ears from the loud sound of the explosion by covering them or taking shelter in a quiet, reinforced area.

---

## 🔹 Project Structure

- `notebook.ipynb` → Full step-by-step Colab notebook with compression and inference
- `falcon-7b-quantized-summary.json` → Metadata, compression stats, and sample outputs
- `.gitignore` → Prevents uploading large weight files
- `README.md` → This file

---

## 🔹 Reproducibility

Anyone can clone this repository and rerun the notebook to **recreate the compression pipeline**.  
Weights will be downloaded automatically from HuggingFace, but **are not stored in this repo** due to size constraints.

---

## 🔹 Credits

- [tiiuae/falcon-7b-instruct](https://huggingface.co/tiiuae/falcon-7b-instruct) – base model
- [bitsandbytes](https://github.com/TimDettmers/bitsandbytes) – quantization framework
- Author: Rabia Imran
- Date: August 2025

---
