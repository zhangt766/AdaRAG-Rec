This repository provides an **anonymous research implementation** of **AdaRAG-Rec**. AdaRAG-Rec addresses a key limitation of existing RAG-based recommenders: **the retrieval size is fixed and non-differentiable**. 

---

## Preparation

Prepare the environment:

```bash
git clone https://github.com/<anonymous>/AdaRAG-Rec.git
cd AdaRAG-Rec
pip install -r requirements.txt
```

Prepare the pre-trained HuggingFace model of **LLaMA2-7B**:

```
https://huggingface.co/meta-llama/Llama-2-7b-hf
```

---

## Training

Train AdaRAG-Rec with a single A100 GPU on the MovieLens dataset:

```bash
sh scripts/train_movielens.sh
```

---

## Evaluation

Test AdaRAG-Rec with a single A100 GPU on the MovieLens dataset:

```bash
sh scripts/test_movielens.sh
```
## Project Structure

```text
AdaRAG-Rec/
├── scripts/              # Training and evaluation scripts
│   ├── train_movielens.sh
│   └── test_movielens.sh
├── data/                 # Dataset processing and loading
├── models/               # Retriever and generator (LLM) modules
├── trainer/              # Training and optimization logic
├── utils/                # Utility functions
├── main.py               # Main entry point
└── requirements.tx
