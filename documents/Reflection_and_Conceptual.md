## Why did you choose the specific architecture for each model?

We used smaller MLPs because the dataset is tabular and does not require deep networks.  
Since we used one hot encoded data in our preprocessing this caused the ReLU activation function to perform the best.  
The goal of this model was to balance learning power and generalization, all while avoiding over complexity and this aproach did exactly that.

---

## How did you monitor and mitigate overfitting in your models?

For our model, we used GridSearchCV with 3 fold cross validation.  
We also implemented early stopping to track validation accuracy.  
To help prevent overfitting, we applied L2 regularization, limited epochs, and smaller architectures.  
It is important to note that the model was evaluated on a 30% hold-out test set to ensure fair performance assessment.

---

## What ethical concerns might arise from deploying models trained on these datasets?

The dataset contains sensitive attributes such as race, sex, and marital status.  
A key concern is that models could learn biased or unfair patterns toward certain groups.  
To avoid this, it is important to checks or exclude biased variables when appropriate.

---

## Why are activation functions necessary in neural networks

Activation functions add nonlinearity, allowing the model to learn complex patterns.  
Without them, multiple layers would collapse into a single linear function.  
We used ReLU to improve training speed and gradient stability, making it ready for tabular data.
