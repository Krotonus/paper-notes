[Paper Link](https://arxiv.org/pdf/1909.10351)

### Notes
- Uses the pre-trained BERT-base, with its weights frozen as the teacher, a large scale text corpora as the training data, to __distil__ (i.e. __Knowledge Distillation__) the weights into a smaller BERT model, that is 7.5x small and 9.4x faster on inference than BERT-base.
- ![[Figure_1.png]]
- Has 3 different types of loss functions, to distil knowledge from:
	- Embedding Matrix
	- Attention Linear Layers, eg W_q, W_k etc.
	- Output Logits.
- 2 stage learning framework: 
	- General Distillation
	- Task Specific Distillation
- The authors claim that the approach can achieve more than 96.8% of the performance of the teacher model, while having ~13.3% fewer params (Lol. Is that enough?) and ~10.6% lesser inference time.
- The loss function used for student-teacher distillation objective.
- $$ \mathcal{L}_{\text{model}} = \sum_{x \in X} \sum_{m=0}^{M+1} \lambda_m \mathcal{L}_{\text{layer}} \left( f_m^S(x), f_{g(m)}^T(x) \right) $$
