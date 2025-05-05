# Applying mechanistic interpretability to a single layer transformer

Currently this repo only contains the notebook with my most recent training parameters of a single layer tranformer trained on an algorithmic dataset.

I know this might be dissappointing to some one reading this but I havent trained the sparse auto encoder to interpret the learned features yet.

# The data

the transformer has been trained on a synthetic dataset of addition of two numbers.

While one would generally expect data in this dataset to look like this:

10+1=11

or

5948+73=6021

the samples in this dataset look like this:

0100000000+1000000000=1100000000

and

8495000000+3700000000+1206000000

All numbers have been inverted and zero padded. Here is why:
1. zero padding means the transformer can learn fixed position embeddings of each significant figure.
2. inverted so that the transformer can learn to carry like we humans do. If left the other way round the transformer would have to learn to estimated the most significant figure first.

Those two points above are just wild guesses, although experiments seem to support them.
