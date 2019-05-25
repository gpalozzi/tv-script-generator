# tv-script-generator
This project generates Seinfeld TV scripts using Recurrent Neural Networks. It uses a Seinfeld dataset of scripts from 9 seasons. The trained model generates a new, "fake" TV script.

# Pre-processing
The dataset has been pre-processed in two steps:

## Lookup Table
To create a word embedding, a mapping between the words to ids and vice-versa has been created.

## Tokenize Punctuation
Splitting the script into a words using spaces as delimiters. Tokenizing punctuations like periods and exclamation marks can create multiple ids for the same word.
i.e. Tokenize the symbols and add the delimiter (space) around it. This separates each symbols as its own word, making it easier for the neural network to predict the next word.

# LSTM Model

An RNN using LSTM has been created with the following parameters:
## Data params

- Sequence Length = 10  # of words in a sequence
- Batch Size = 128

## Training parameters

- Number of Epochs = 10
- Learning Rate = 0.001

## Model parameters

- Embedding Dimension = 200
- Hidden Dimension = 256
- Number of RNN Layers = 2

# Result

This is an example of the generated script:

```
jerry: moops, rice.

hoyt: and what? what are?

george: no, no.

george: i thought we had a lot of money.

new witness: ladies, massachusetts, immaturity, massachusetts, and inconsequential.

hoyt: you know, i gotta get out of the time.

hoyt: i can't believe this.

hoyt: well, i think i could go.

vandelay: objection!!!

estelle: oh, i don't know.

jerry: oh, that's a good time.
```
