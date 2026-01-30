# Neuro-Inspired Self-Learning 

This project is a beginner-friendly, neuro-inspired machine learning notebook built in **Google Colab**.
It demonstrates how a simplified brain-like architecture can learn representations (self-supervised learning)
and then perform classification (supervised learning) on **MNIST**.

> Note: This is **not** a biologically exact brain simulation. It is an educational, neuroanatomy-inspired design
that mirrors the *idea* of modular brain processing (vision - memory - gating - decision).

---

## What this notebook includes

A simplified pipeline inspired by neuroanatomy:

- **Retina (early filters)** — first convolutional layer
- **Thalamus / LGN (attention gate)** — learned gating that amplifies/suppresses channels
- **Visual cortex (V1/V2/V4)** — convolutional feature extraction stages
- **IT cortex (object embedding)** — a compact representation vector
- **Hippocampus (episodic memory)** — k-NN style memory retrieval in embedding space
- **Basal ganglia (gating)** — decides how much to trust memory vs. cortex prediction
- **PFC (decision)** — final classifier head
- **Cerebellum (self-learning support)** — reconstruction decoder used for self-supervised pretraining

---

## Learning stages

1. **Self-supervised pretraining (reconstruction)**
   - The model learns useful representations by reconstructing input images.
2. **Supervised learning (classification)**
   - The model predicts MNIST classes (0–9), optionally mixing:
     - cortical classifier logits
     - hippocampal memory retrieval logits
     - basal ganglia gating between them

---

## How to run

Open the notebook in **Google Colab** and run the cells from top to bottom.

Recommended:
- Runtime → Change runtime type → **GPU** (if available)

---

## Files

- `cerebellum-SL.ipynb` — main Colab notebook (recommended entry point)
- (optional) `cerebellum.py` — exported Python version

---

## Output

- Training curves (loss)
- Test accuracy on MNIST
- Visualization of:
  - reconstructed images (self-learning)
  - thalamic attention gates
  - basal ganglia memory-trust gate values

---

## Educational goals

- Show how “brain-inspired” modular design can be represented in code
- Teach beginners the difference between:
  - self-supervised learning
  - supervised learning
  - memory-based retrieval vs. learned classification
- Provide an interpretable, hackable starting point for further exploration

---

## License

MIT
