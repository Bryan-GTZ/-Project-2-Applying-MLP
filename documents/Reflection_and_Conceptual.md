## Why did you choose the specific architecture for each model?

- We used smaller MLPs because the dataset is tabular and does not require deep networks
- Since we used one hot encoded data in our preprocessing this made the ReLU activation function to perform the best
- The goal of this model was to balance learning power and generalization, all while avoiding over complexity and this aproach did exactly that 

---

## How did you monitor and mitigate overfitting in your models?

- For our model, we used GridSearchCV with 3 fold cross validation   
- We also implemented early stopping to track validation accuracy  
- To help prevent overfitting, we applied L2 regularization, limited epochs, and smaller architectures 
- It is important to note that the model was evaluated on a 30% hold-out test set to make sure it had a fair performance assessment

---

## What ethical concerns might arise from deploying models trained on these datasets?

- The dataset contains sensitive attributes such as race, sex, and marital status, these traits are personal and some people might not feel safe sharing this 
- A main concern is that models could learn biased or unfair patterns toward certain groups, making this scary to certain demographics
- To avoid this, it is important to checks or exclude biased variables when appropriate 

---

## Why are activation functions necessary in neural networks

- Activation functions add nonlinearity, and this is what lets the model learn complex patterns
- Without activation functions, multiple layers would collapse into a single linear function
- We used ReLU to improve training speed and gradient stability, making it ready for tabular data, and it did just that
