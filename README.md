# Deepest Task

## Question3 Kaggle - CommonLit Readability Prize

### Submission

(TBD)

### Run

1. Setup environment.
``` Bash
# Python 3.7.10
>> pip install -r requirements.txt
```
2. Click **"Run All"** button in jupyter notebook.
3. Check the training results.

### Solution

- RoBERTa
- Pre-trained Model
- LP-FT: Naive full fine-tuning can distort the pretrained feature extractor. The test error of fine-tuning is high **when we initialize with a fixed or random head**. This is because while fine-tuning learns the head, the lower layers of the neural network change simultaneously and distort the pretrained features.

### Loss Graph

(TBD)

### References

- [RoBERTa Paper](https://arxiv.org/abs/1907.11692)
- [LP-FT Paper](https://arxiv.org/abs/2202.10054)
- [Pre-trained RoBERTa Kaggle Notebook](https://www.kaggle.com/code/andretugan/pre-trained-roberta-solution-in-pytorch/notebook)
