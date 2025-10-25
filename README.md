# Optimizer in Deep Learning
A characteristic of AI problems is that, based on the features and labels ($X$ and $y$), the model updates its weights to solve various tasks. This weight adjustment process is known as optimization, and the methods used to perform it are called optimizers. The fundamental approach commonly employed in machine learning is Stochastic Gradient Descent (SGD).

From this foundation, two main directions have been developed to improve the SGD formula: optimizing the learning rate and optimizing the gradient. Each direction has given rise to different algorithms, which eventually converge conceptually in the Adam optimizer.

In this repository, I use a consistent experimental setup — including the loss function, model architecture, and weight initialization — while varying the optimizer to evaluate performance on the well-known FashionMNIST classification task, which is considered more challenging than the traditional MNIST dataset.

## Experimental Results

The results of the experiments are summarized in the table below:

| Optimizer              | Accuracy (%) |
|------------------------|--------------|
| SGD                    | 79.76        |
| SGD with Momentum      | 86.72        |
| Adagrad                | 87.92        |
| RMSProp                | 86.73        |
| Adam                   | 88.61        |
| **AdamW**              | **88.67**    | 

AdamW achieved the best performance among all tested optimizers, showing its strong balance between adaptive learning rate and effective weight decay regularization.  

## Evaluation and Future Improvements
For future work:
- Explore **learning rate scheduling** (e.g., cosine annealing, cyclical LR).  
- Combine optimizers with **Lookahead** or **Ranger** techniques for enhanced convergence.  
- Investigate **larger models** or **different initialization schemes** to assess optimizer scalability.  
