This repository provides an **anonymous research implementation** of **AdaRAG-Rec**, a novel adaptive Retrieval-Augmented Generation (RAG) framework for LLM-based sequential recommendation.

AdaRAG-Rec addresses a key limitation of existing RAG-based recommenders: **the retrieval size is fixed and non-differentiable**. Instead, our framework enables:

- 🔁 **Adaptive retrieval size** via a **learnable threshold-based retriever**
- 🧮 **Differentiable retrieval** through **smooth relaxation**
- 🔗 **End-to-end joint training** of the retriever and generator

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

