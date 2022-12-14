# Deepest Task

## Question3 Kaggle - CommonLit Readability Prize

### Submission

![submission](assets/submission2.png)

### Run

1. Copy [this kaggle notebook](https://www.kaggle.com/code/andretugan/pre-trained-roberta-solution-in-pytorch/notebook).
2. Click **"File > Import Notebook"** and import deepest_question3_kaggle.ipynb file.
3. Click **"Run All"** button in [kaggle notebook](https://www.kaggle.com/code/shovelingpig2/roberta-solution/edit/run/105780148) or jupyter notebook.
4. Check the training results.

### Solution

- **RoBERTa**: (1) robustly optimized BERT approach. (2) training the model longer, with bigger batches over more data. (3) removing the next sentence prediction objective. (4) training on longer sequences. (5) dynamically changing the masking pattern applied to the training data.
- **Sentence Summary**: This model computes context vector as the weighted average of last hidden states.
- **Pre-training on CLRP**: This model is pre-trained on CommonLit Readability Dataset on MLM task.
- **LP-FT**: Naive full fine-tuning can distort the pretrained feature extractor. The test error of fine-tuning is high when we initialize with a fixed or random head. This is because while fine-tuning learns the head, the lower layers of the neural network change simultaneously and distort the pretrained features.

### Loss Graph

![loss](assets/loss2.png)

### References

- [RoBERTa Paper](https://arxiv.org/abs/1907.11692)
- [LP-FT Paper](https://arxiv.org/abs/2202.10054)
- [CLRP Pre-trained RpBERTa Checkpoint](https://www.kaggle.com/datasets/maunish/clrp-roberta-base)
- [RoBERTa Kaggle Notebook](https://www.kaggle.com/code/andretugan/pre-trained-roberta-solution-in-pytorch/notebook)
