[Paper Link](https://arxiv.org/pdf/1909.10351)

### Notes
- Uses the pre-trained BERT-base, with its weights frozen as the teacher, a large scale text corpora as the training data, to distil the weights into a smaller BERT model, that is 7.5x small and 9.4x faster on inference than BERT-base.
- ![[Figure_1.png]]
- 