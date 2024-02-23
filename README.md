# GPT Generator
A repository to generate text based on Andrej Karpathy's tutorial series.

I created a tokenizer based on bigrams. The tokenizer can be trained on any custom dataset. I find the most common bigram and make it a single token. This process is done iteratively until a certain limit is reached, which can be specified in the code. This sub-word tokenizer performs significantly better than the previous character-level encoding.

I trained my tokenizer on a Shakespeare text, and then I trained my GPT on the same corpus. The GPT trained with the following parameters:

    #Set a block size to train the model. This is the maximum amount of tokens being attended to at a time <br>
    BLOCK_SIZE = 128
    #Set a batch size (number of random blocks we will select)
    BATCH_SIZE = 32
    #The size of our vocabulary will be the number of distinct tokens
    VOCAB_SIZE = 512
    #The length of our embeddings
    N_EMBED=120
    #Set our learning rate for Adam to the recommended rate
    LR = 3e-4
    #Choose the number of heads for multi-headed attention (heads per block)
    N_HEAD=6
    #Set the number of times to repeat the block
    N_LAYER = 6
    #Choose a dropout percentage (prevent overfitting)
    DROPOUT = 0.2
    #Choose the number of times to iterate while training
    MAX_ITER = 5000
    #Set an interval at which to evaluate the loss of the network
    EVAL_ITER = 100


Below is an example of 500 generated tokens from the GPT:

<em>LUCIO: <br>
All most be? what hone?<br>
I will we could this is saymain<br>
Thou which done my life in ads of Lord of our deeems,<br>
This fond, in his acque his city,<br>
But evinously of thine a son and ans<br>
asid a trie as not me, too triive femper<br>
My ext not intell: look, that, all it as a<br>
peies, dove you he us not true.<br>

LUCIO:<br>
Most mine memes them king?<br>

First Lord:<br>
The pagours shall; therebroth meance of thy saficers,<br>
Who handed, we'll be or by king out of Caster. So<br>
y Larewear me. Nursem: let meet him, forth in<br>
Are well use that from this asleday.<br>

P shallapege:<br>
How, fear thou hear a thants he like you did;<br>
orn very enters; from the hoody courtues.<br>

HUn:<br>
What is it so, you?<br>

CORIOLANUS:<br>
What is grave to--the den wowerous as on, and I in mays, hath to<br>
Than o'therdving worrow me foughther sauck.<br>

CAMENESBY:<br>
Evens field, the mighty, what never<br>
neives, town'd name to his brother.<br>

ANGARET:<br>
Thank off sister to he e of the fhat<br>
I whose cinterss where we pardon as none.<br>

GLOUCESTER:<br>
His name for forbernate murth:<br>
If din the bring thy head.<br>

WISASTA:<br>
Yes we it bec</em>
