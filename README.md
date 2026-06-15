Natural Language Inference on the Stanford NLI Corpus using fastai
Overview
This project tackles Natural Language Inference (NLI) — the task of determining whether a hypothesis is entailed by, contradicts, or is neutral with respect to a given premise. It uses the Stanford Natural Language Inference (SNLI) corpus and the fastai deep learning library built on top of PyTorch.
Dataset
Source: Stanford NLI Corpus
Size: ~570,000 human-annotated sentence pairs
Labels: entailment, contradiction, neutral
Example:
Premise: "A man is playing a guitar on stage."
Hypothesis: "Someone is performing music."
Label: entailment
Tech Stack
Python, fastai, PyTorch
HuggingFace / fastai text modules
Jupyter Notebook
Approach
Data Preparation — loaded and preprocessed premise-hypothesis pairs; mapped string labels to integer classes
Tokenisation — applied fastai's text tokenisation and numericalization pipeline
Model Architecture — fine-tuned a pre-trained language model for sequence-pair classification
Training — used fastai's fit_one_cycle learning rate scheduler for efficient training
Evaluation — measured accuracy on the validation split across three classes
Results
Achieved multi-class classification accuracy on the SNLI validation set
Model successfully learned to distinguish subtle semantic relationships between sentence pairs
Key Learnings
Working with large NLP benchmark datasets
Fine-tuning pre-trained language models for classification tasks
fastai's TextDataLoaders pipeline for sequence pair tasks
Practical understanding of entailment, contradiction, and neutral inference
How to Run
# Clone the repo
git clone https://github.com/adeleke1508/Stanford_Natural_Language_Inference_Corpus_fastai.git
cd Stanford_Natural_Language_Inference_Corpus_fastai

# Install dependencies
pip install fastai torch jupyter

# Launch the notebook
jupyter notebook stanford-natural-language-inference-corpus-fastai.ipynb
Note: Training on the full SNLI corpus requires a GPU. Google Colab (free tier) works well for this project.
Author
Ismail Khaleed Ayobami — 300-Level Computer Science Student, FUTA
LinkedIn | GitHub
