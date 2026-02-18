# DS9 — Let's Build an LLM

> *What I cannot create, I do not understand.* — Richard Feynman

A ground-up LLM build: character-level transformer trained on DS9 scripts to demystify attention and sequence modeling.

---

## What is this?

In 2017, a team at Google published "Attention Is All You Need." The transformer was born. And it changed everything.

This series builds a character-level language model from scratch, trained on Star Trek: Deep Space Nine scripts, that generates new scenes. By the end, you'll understand how transformers actually work — not from reading about them, but from building one.

We follow the philosophy of Andrej Karpathy's [LLM101n](https://github.com/karpathy/LLM101n) — but we're building it. Python and PyTorch only. No prerequisites beyond curiosity.

---

## What you'll build

A single file — `ds9_transformer.py` — that:

1. Downloads DS9 scripts automatically
2. Trains a small decoder-only transformer
3. Generates new scenes in the style of Deep Space Nine

---

## Syllabus

| # | Section | What we cover |
|---|---------|--------|
| 0 | **Introduction** | What we're building and why it matters |
| 1 | **What Is a Language Model?** | A guessing machine — tokens, numbers, predictions |
| 2 | **Getting the Data** | Scraping DS9 scripts and preparing them for training |
| 3 | **The Bigram Model** | The simplest possible guesser — one character at a time |
| 4 | **Why Bigrams Fail** | What happens when context matters and we have none |
| 5 | **Self-Attention from Scratch** | Teaching the model to look back at what it's already seen |
| 6 | **Multi-Head Attention** | Looking at the same sequence from multiple angles at once |
| 7 | **The Transformer Block** | Wiring attention, normalization, and feed-forward into one unit |
| 8 | **Stacking + Positional Encoding** | Going deeper, and giving the model a sense of order |
| 9 | **Training for Real** | Loss, gradients, AdamW, and when to stop |
| 10 | **Generating Text** | Sampling from the model — temperature, randomness, control |
| 11 | **Reading the Output** | What did it actually learn? Interpreting generated DS9 scenes |
| 12 | **Tokenization Done Right** | Why characters aren't enough — intro to byte pair encoding |
| 13 | **Fine-Tuning** | Adapting a trained model with less data and fewer resources |
| 14 | **RLHF** | Teaching the model what "good output" means using feedback |
| 15 | **Where to Go Next** | The gap between our toy model and production LLMs |

---

## Getting started

```bash
git clone https://github.com/louiscollinsjr/ds9-llm-from-zero.git
cd ds9-llm-from-zero
pip install torch requests
python ds9_transformer.py
```

The script downloads the data automatically. No setup beyond Python and PyTorch.

**Recommended hardware:** M1 Mac or any GPU. CPU works too — training is just slower.  
**No GPU?** Use [Kaggle Notebooks](https://www.kaggle.com/code) — free T4 GPU, no setup required.

---

## Following along

This project is being built live, section by section, published on LinkedIn and GitHub.

Each section is written to stand alone — you can read them in order or jump to whatever interests you. The full series is designed for two audiences: people with no AI background, and technical folks who want to see the internals clearly.

---

## Philosophy

This project builds on foundational work — from the researchers who introduced the transformer architecture, to educators like Andrej Karpathy, and the writers of Star Trek: Deep Space Nine whose scripts make the dataset possible.

All code here is written from scratch. We start with counting character pairs and work our way up to a full transformer, including fine-tuning. The goal is understanding through construction — learning the mechanics by implementing them.

If you’ve read about transformers but want to truly understand how they work under the hood, this repository is for you.

---

## License

MIT