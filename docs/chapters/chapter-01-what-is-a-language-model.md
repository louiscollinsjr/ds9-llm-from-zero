# Chapter 01 — What Is a Language Model?

**Summary:** A guessing machine — tokens, numbers, predictions.

## Objectives
- Explain tokens, vocabularies, and probability distributions.
- Show how models predict the next token.


A language model is a guessing machine. You give it part of a sentence, and it guesses what comes next. That's it.

Type this into your favorite AI chat app: "Humpty Dumpty sat on a ____." The model predicts "wall."

Language models learn from seeing millions of sentences, so their guesses aren't random — but they're also not understanding. The model doesn't know who Humpty Dumpty is. It just knows how "Humpty Dumpty" statistically relates to other words like "egg," "wall," "king's men."

Guessing even works for answering questions. Give it: "What is the capital of France?" The language model predicts "Paris" comes next.

Why? Because during training, it saw thousands of examples where that question pattern was followed by that answer pattern. It's not retrieving a fact — it's continuing the sequence in the most statistically likely way based on what it's seen before.

Same mechanism. The model doesn't distinguish between "finishing a sentence" and "answering a question" — both are just sequence prediction.

The reason it feels like understanding is because during training, it saw billions of question-answer pairs. So it learned: "When the sequence looks like a question about capitals, the next tokens are usually the capital's name."

So how does the model actually process "What is the capital of France?" It doesn't see words. It sees tokens.



## Tokens

**A token is a chunk of text.** Sometimes it's a whole word like “fall”. Sometimes it's part of a word like "un" or "break". Sometimes it's just punctuation.

Why not just use words? Because language is messy. 

If the model only knew complete words, what happens when it sees "unbreakable"? Does it need to memorize every possible combination — "breakable," "unbreakable," "unbreakably"? That's millions of words to store.

Here's "What is the capital of France?" broken into tokens:
["What", " is", " the", " capital", " of", " France", "?"]

Each token becomes a number:
[2254, 318, 262, 3139, 286, 4881, 30]

Now the model can do math. It takes these numbers, runs calculations, and predicts the next number. That number maps back to a token — like "Paris".


Words become tokens. Tokens become numbers. Numbers become predictions


## Notes
_TBD as the chapter is written._

## Checkpoint
- Suggested tag: `chapter-01-language-model`.
