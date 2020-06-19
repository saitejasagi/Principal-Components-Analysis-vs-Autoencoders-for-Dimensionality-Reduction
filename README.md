# Principal-Components-Analysis-vs-Autoencoders-for-Dimensionality-Reduction
Using both Machine Learning and Deep Learning approaches for dimensionality reduction and comparing the performance by calculating the reconstruction error

# Autoencoder

Autoenoder is an unsupervised learning where neural network are subject to task of Representation learning. In Simple word it imposed a bottleneck in network.(Bottleneck forces a compressed knowledge representation of input). As with any neural network there is a lot of flexibility in how autoencoders can be constructed such as the number of hidden layers and the number of nodes in each. With each hidden layer the network will attempt to find new structures in the data. In general autoencoders are symmetric with the middle layer being the bottleneck. The first half of the autoencoder is considered the encoder and the second half is considered the decoder.

# PCA

PCA reduces the data frame by orthogonally transforming the data into a set of principal components. The first principal component explains the most amount of the variation in the data in a single component, the second component explains the second most amount of the variation, etc. By choosing the top k principal components that explain say 80-90% of the variation, the other components can be dropped since they do not significantly benefit the model. This procedure retains some of the latent information in the principal components which can help to build better models.

# Differences between PCA and autoencoders

To summarise, the key differences for consideration between PCA and autoencoders are:

- There are no guidelines to choose the size of the bottleneck layer in the autoencoder unlike PCA. With PCA, the top k components can be chosen to factor in x% of the variation. Often PCA can be used as a guide to choose k.
- The autoencoder tends to perform better when k is small when compared to PCA, meaning the same accuracy can be achieved with less components and hence a smaller data set. This is important when dealing with very large data sets.
- When visualising the PCA output, in general the first 2 or 3 components are used. The drawback is the other components are not visable on the plot and therefore not seeing all the information. Different combinations of dimensions will need to be plotted. Autoencoders can be constructed to reduce the full data down to 2 or 3 dimensions retaining all the information which can save time.
- Autoencoders require more computation than PCA. Although, for very large data sets that can’t be stored in memory, PCA will not be able to be performed. The autoencoder construction using keras can easily be batched resolving memory limitations.
