# Directed Feature Splitting

Feature splitting has been observed in sparse autoencoders, as features are not atomic. When increasing the width of a sparse autoencoder (number of features), the model will split features into smaller, more general features. Typically, we only care about the specificity of specific clusters of features, not the specificity of every feature. As a result, we would like to direct feature splitting!

We propose an algorithm that allows directed feature splitting. We first train a small width sparse autoencoder on gpt2-small with width 1536. Then, we autointerp this model to find features that we are interested in splitting. 