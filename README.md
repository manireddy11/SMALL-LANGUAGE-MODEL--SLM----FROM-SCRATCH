🧠 Building a Small Language Model from Scratch






🌟 Introduction

Most people today fine-tune Hugging Face models or call APIs.
I chose the hard way: building a Small Language Model (SLM) from scratch.

This wasn’t just about writing code — it was about:

Understanding transformer internals step by step.

Training on a real dataset (TinyStories).

Watching the model learn from noise to meaning.

Spending hours on Google Colab T4 GPU, pushing past slow runs, memory limits, and warnings.

And I didn’t quit.
What I achieved is a working language model that generates coherent text stories — proof that I can build and train core NLP systems myself.

🛠️ Key Steps
🔹 Dataset Loading

I used the TinyStories dataset via Hugging Face.
This dataset provides a collection of short children’s stories — simple enough to train a small model, but rich enough to demonstrate learning.

<p align="center">
  <img src="https://raw.githubusercontent.com/manireddy11/SMALL-LANGUAGE-MODEL--SLM----FROM-SCRATCH/2473e314b2bb8796488226fa0dc782756027e238/Screenshot%202025-08-26%20220425.png" alt="Project screenshot" />
</p>


The progress bars show successful loading of millions of tokens into memory, with automatic train/validation splits.


🔹 Training Progress

The model was trained for 20,000 iterations with checkpoints at every 500 epochs.
I monitored both training loss and validation loss closely.


