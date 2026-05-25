BacterAE-Knowledge-Transfer-Protocol
The Mission: Moving Beyond "Vague Tutorials"
This project is an exercise in Open Knowledge. I found that most AI tutorials are fundamentally incomplete: they discuss concepts without providing the specific datasets, model weights, precise training parameters, or the reasoning behind the data structure.
The goal of this repository is not just to "train a model." The goal is to provide a fully reproducible protocol for taking an LLM from zero knowledge to domain expertise.
Why Bacter AE?
I run a shrimp aquarium as a side project. When I queried my base model about "Bacter AE," it had absolutely no idea what the product was, what it was used for, or how to dose it safely.
This made it the perfect test subject: a "Tabula Rasa" (Blank Slate) problem.
• The Journey: We move from absolute ignorance to technical proficiency.
• The Methodology: I am documenting the entire path—from the raw dataset structure and line length specifications to the exact LoRA training parameters and final loss curves.
Transparency Standards
To ensure this research is useful to the community, every experiment in this repo includes:
1. The Dataset: Raw .jsonl files specifying the exact number of lines and complexity used.
2. Hyperparameters: Full disclosure of LoRA rank, alpha, learning rates, and gradient accumulation steps.
3. Reproducibility: Scripts (train_all_small.sh) that allow anyone to replicate the training on their own hardware.
4. Weights: Links to download the resulting model weights so the community can audit the "expertise" acquired.
The Open Knowledge Manifesto
If you want to train a model to know something specific, you shouldn't have to guess how others did it. By sharing the dataset, the parameters, and the results, we turn "AI training" from a dark art into a transparent engineering process.
Project Structure
• dataset_X/: Contains the Chain-of-Thought (CoT) datasets, categorized by line count.
• train_X.sh: Individual scripts documenting the specific parameters for each experiment.
• logs/: Empirical results showing the convergence (loss curves) of the model.
• weights/: Download links for the final fine-tuned adapters.
This repository is dedicated to those who prefer data over hype.

Why the gemma-4-e2b-it-4bit model?
I have chosen the gemma-4-e2b-it-4bit model because it is a current model that features a Mixture of Experts (MoE) architecture and built-in chain-of-thought reasoning. The 4-bit compression makes it significantly more compact and accessible, allowing more people to train this model on their own home hardware. My objective is to enable others to experiment locally, avoiding the need to pay for dedicated servers for large-scale training unless they decide to scale up in the future.
I am not an amateur in Machine Learning—quite the contrary. I do not intend to provide a masterclass; I am simply documenting a process. I am sharing this workflow so that others can achieve what I am doing without having to rely on vague tutorials that say nothing and provide no real value. I am tired of that kind of content, and this project is the antithesis of it.

This is an ongoing, iterative process. Training a model is time-consuming, and I am not training just once; I am running the same experiment multiple times to gather and share comprehensive results.
