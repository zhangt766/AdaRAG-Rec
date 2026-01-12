# AdaRAG-Rec
Adaptive Retrieval-Augmented Generation for LLM-based Sequential Recommendation.

This repository provides an anonymous research implementation of **AdaRAG-Rec**, an adaptive RAG framework for sequential recommendation that:
- replaces fixed top-k retrieval with a **learnable threshold-based retriever** (adaptive retrieval size),
- makes retrieval **differentiable via smooth relaxation**,
- enables **end-to-end joint training** of retriever and generator.

## Preparation

Prepare the environment:

```bash
git clone https://github.com/<anonymous>/AdaRAG-Rec.git
cd AdaRAG-Rec
pip install -r requirements.txt

Prepare the pre-trained huggingface model of LLaMA2-7B:

https://huggingface.co/meta-llama/Llama-2-7b-hf

## Train AdaRAG-Rec

Train AdaRAG-Rec with a single A100 GPU on MovieLens dataset:

```bash
sh scripts/train_movielens.sh

## Evaluate AdaRAG-Rec

Test AdaRAG-Rec with a single A100 GPU on MovieLens dataset:

```bash
sh scripts/test_movielens.sh

