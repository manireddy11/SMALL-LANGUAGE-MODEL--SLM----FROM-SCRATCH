🧠 Building a Small Language Model from Scratch

<p align="center">
  <img src="https://img.shields.io/badge/🧠%20Building%20a%20Small%20Language%20Model%20from%20Scratch-000000?style=for-the-badge&logoColor=white&labelColor=000000&color=000000" width="700"/>
</p>






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

<p align="center">
  <a href="https://github.com/manireddy11/SMALL-LANGUAGE-MODEL--SLM----FROM-SCRATCH/blob/94c4ac9a33e5d72d36d45778d15ef665a37b07a5/Screenshot%202025-08-26%20220314.png" target="_blank" rel="noopener noreferrer">
    <img src="https://raw.githubusercontent.com/manireddy11/SMALL-LANGUAGE-MODEL--SLM----FROM-SCRATCH/94c4ac9a33e5d72d36d45778d15ef665a37b07a5/Screenshot%202025-08-26%20220314.png" alt="Project screenshot" style="max-width:100%; height:auto;" />
  </a>
</p>


Here’s what we observe:

Training loss decreases steadily from ~9.4 → ~4.3.

Validation loss follows the same downward trend, proving generalization.

The green progress bar shows GPU-backed training across ~3.5 hours.

This wasn’t just code running; it was proof of learning.

🔹 Text Generation

Once trained, I gave the model seed sentences like:

“Once upon a time there was a pumpkin.”

“A little girl went to the woods.”


<p align="center">
  <a href="https://github.com/manireddy11/SMALL-LANGUAGE-MODEL--SLM----FROM-SCRATCH/blob/bb648b742326b34f117a766f1a1267d267152c4f/Screenshot%202025-08-26%20215919.png" target="_blank" rel="noopener noreferrer">
    <img src="https://raw.githubusercontent.com/manireddy11/SMALL-LANGUAGE-MODEL--SLM----FROM-SCRATCH/bb648b742326b34f117a766f1a1267d267152c4f/Screenshot%202025-08-26%20215919.png" alt="Project screenshot" style="max-width:100%; height:auto;" />
  </a>
</p>


The model’s responses show:

Coherent sentence structures.

Story-like continuity.

Occasional randomness (expected from small models).

For example:

“A little girl went to the woods and saw some fish. She was scared and so she ran away… Mary had a great time with her special surprise.”

This is the beauty of training from scratch — seeing text emerge from noise into meaning.

<p align="center">
  <a href="https://github.com/manireddy11/SMALL-LANGUAGE-MODEL--SLM----FROM-SCRATCH/blob/bb648b742326b34f117a766f1a1267d267152c4f/Screenshot%202025-08-26%20215852.png" target="_blank" rel="noopener noreferrer">
    <img src="https://raw.githubusercontent.com/manireddy11/SMALL-LANGUAGE-MODEL--SLM----FROM-SCRATCH/bb648b742326b34f117a766f1a1267d267152c4f/Screenshot%202025-08-26%20215852.png" alt="Project screenshot" style="max-width:100%; height:auto;" />
  </a>
</p>


⚡ Skills Demonstrated

Transformer Internals: Built attention, embeddings, and positional encoding manually.

PyTorch Engineering: Implemented training loops, schedulers, and optimizers.

Resourcefulness: Managed with Colab T4 GPU constraints.

Visualization: Monitored losses, dataset loading, and outputs with clear logs.

Persistence: Spent hours fine-tuning and debugging until convergence.



.

🚀 How to Run

Clone the repo:

git clone https://github.com/your-username/small-language-model-scratch.git
cd small-language-model-scratch


Open the notebook in Colab or Jupyter:

jupyter notebook "Small Language Model Scratch Final.ipynb"


Train the model and generate your own text completions.

🔮 Future Work

Train on larger text corpora.

Add sampling strategies (top-k, nucleus sampling).

Scale layers/heads for better fluency.

Deploy as a lightweight text generation API.

❤️ Personal Reflection

This project wasn’t just about code.
It was about proving to myself — and to recruiters — that I can:

Go beyond tutorials.

Build complex systems under real constraints.

Stick with the process until I get results.

It took hours of patience, multiple reruns, and GPU limitations.
But now I know: given the right resources, I can scale this into a real production-ready LLM pipeline.

✨  This isn’t another Hugging Face fine-tune — it’s proof that I can engineer, persist, and deliver.



