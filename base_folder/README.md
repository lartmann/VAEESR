# Variational Autoencoder Embeddings Symbolic Regression (VAEESR)

This python package performs Symbolic Regression by creating an where semantically similar equations are close to each other and using MCMC sampling to find the equation that is the closest to the oberved data. 

## Install 
`pip install vaeesr`

## Tutorial
There are three main function:
1. create_dataset()
2. create_autoencoder()
3. perform_MCMC()

### 1. Create Dataset
The dataset is cusomizable to tune it to the problem and create an antoencoder that fits the problem at hand. 
- `spaces`: 
    - 
spaces = (
        ["sin", "exp", "cos", "sqr", "abs", "acos", "asin", "log"],
        ["+", "-", "*", "/", "min", "max", "**"],
        ["x_1", "x_1", "X"],
        ["c_0"]
        ),
    x_values = np.linspace(-1.0, 1.0, 50),
    latent_dims=4, 
    max_tree_depth=6, 
    num_equation_samples = 10000, 
    num_epochs = 500,
    batch_size = 50,
    learning_rate = 0.001,
    kl_weight = 0.0001,
    training_set_proportion = 0.8,
    inf_repacement = 1000,
    is_vae=True