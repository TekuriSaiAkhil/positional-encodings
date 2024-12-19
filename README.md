# positional-encodings

### Suppose that we design a deep architecture to represent a sequence by stacking self-attention layers with positional encoding. What could be issues?


Stacking self-attention layers with positional encoding can cause some issues during training because of its deep architecture and as well as fixed sinusoidal positional encodings. 

Vanishing or exploding gradient: We may observe vanishing or exploding gradient problems while training very deep self-attention models.
Positional Information Dilution: When the model is deeper, the positional encoding may lose its significance over token representation because positional encoding is added at the input level and their significance may be lost by the transformations performed by stacking self-attention layers.
Fixed Positional Encodings: Fixed positional encoding may not generalize well for all the tasks because it’s not flexible and independent of the dataset.
Limitations for Long Sequences: Transformers use sinusoidal positional encodings. This has limitations for very long sequences. If the input sequence is very long the positional encoding may become too similar because of its sinusoidal nature. This defeats the purpose of adding positional encodings.

We can optimize the training process of deep architectures by having residual connections, layer normalizations, adaptive learning rate, gradient clipping, and learnable positional encodings etc.


### 
