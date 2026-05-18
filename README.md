# MiniGPT

MiniGPT is a small GPT-style autoregressive language model implemented from scratch in PyTorch.

The notebook rebuilds the main GPT workflow: tokenization, causal self-attention, Transformer blocks, next-token training, validation loss tracking, checkpoint selection, and text generation.

The implementation is inspired by Karpathy's nanoGPT design, but the code is written from scratch.

MiniGPT is submitted to the Journal of Open Source Education (JOSE) as a computational learning module.

## Open in Colab

Run the notebook directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jibin10/MiniGPT/blob/main/MiniGPT_Notebook.ipynb)

## Notebook

Main notebook: `MiniGPT_Notebook.ipynb`

The notebook is designed to run in Colab without local setup.

## Statement of Need

Many GPT explanations show the model as a high-level diagram, while many real implementations include extra engineering details that can be hard to follow at first.

MiniGPT is created to fill this gap. It gives a simple, runnable notebook that shows the full GPT-style pipeline from raw text to generated samples.

The goal is not to build a state-of-the-art language model. The goal is to help learners understand how a small decoder-only Transformer is built, trained, evaluated, and used for text generation.

## Target Audience

This learning module is useful for:

- students learning deep generative models
- students learning NLP or language modeling
- instructors who want a small GPT notebook for a class or lab
- practitioners who want to understand GPT training from first principles
- self-learners who want a runnable example in Colab

Basic Python and PyTorch knowledge will be helpful.

## Learning Objectives

After completing the notebook, learners should be able to:

- understand character-level tokenization
- explain token embeddings and positional embeddings
- implement causal multi-head self-attention
- build a small decoder-only Transformer block
- train a GPT-style model with next-token cross-entropy loss
- track training and validation loss
- select a checkpoint using validation loss
- generate text autoregressively
- understand how model size, context length, and sampling temperature affect output quality

## Dataset

The notebook uses the Tiny Shakespeare dataset with character-level tokenization.

| Item | Value |
|---|---:|
| Total tokens | 1,115,394 |
| Vocabulary size | 65 |
| Train/validation split | 90% / 10% |

## Results

| Model | Parameters | Context length | Best / final validation loss | Training time on Colab A100 |
|---|---:|---:|---:|---:|
| Baseline MiniGPT | 826,433 | 128 | 1.7236 | 50.79 seconds |
| Stronger MiniGPT | 10.77M | 256 | 1.4780 | 4.76 minutes |

The stronger model learns better local Shakespeare-style structure, but it is still a small character-level model, so long text is not fully coherent.

## Requirements

The notebook is designed to run in Colab without local setup.

Main packages used:

- torch
- matplotlib
- requests

If running locally, install the dependencies with:

```bash
pip install -r requirements.txt
```

This is enough. Do **not** use `pip freeze > requirements.txt` from your full local environment, because it may add many unnecessary packages. For MiniGPT, keep it simple.

## How to Run

1. Click the Open in Colab button.
2. Select GPU runtime.
3. Run the notebook cells from top to bottom.

Recommended Colab setting:

```text
Runtime → Change runtime type → GPU
```

The baseline model can run quickly. The stronger model is better to run with a GPU.

## How Instructors Can Use This Module

This notebook can be used as:

- a short lab on GPT-style language modeling
- a practical assignment on Transformers
- a walkthrough for causal self-attention
- a classroom demo for next-token prediction
- a self-study module for students

For a shorter session, use only the baseline model.

For a longer GPU-backed session, run the stronger model and compare the loss curves and generated samples.

## Repository Contents

| File | Purpose |
|---|---|
| `MiniGPT_Notebook.ipynb` | Main learning module notebook |
| `README.md` | Project overview and usage instructions |
| `requirements.txt` | Minimal package list for local runs |
| `paper.md` | JOSE paper |
| `paper.bib` | JOSE bibliography |
| `LICENSE` | License information |
| `CONTRIBUTING.md` | How to contribute or report issues |
| `CODE_OF_CONDUCT.md` | Community behavior guidelines |

## Support

If something does not work, please open a GitHub issue.

Useful details to include:

- whether you used Colab or local Python
- whether you used CPU or GPU
- the error message
- which notebook cell failed

Small differences in loss values or generated text are normal because training can change with GPU type, PyTorch/CUDA version, and random sampling.

## Contributing

Contributions are welcome if they make the module clearer, easier to run, or easier to understand.

Please see `CONTRIBUTING.md` before opening a pull request.

## Citation

If you use this learning module, please cite:

```text
Jibin Joseph. MiniGPT: A Colab-Runnable Learning Module for Rebuilding GPT from First Principles. 2026.
https://github.com/jibin10/MiniGPT
```

## License

This repository uses two licenses:

- **Code and code cells:** MIT License
- **Learning materials, notebook explanations, paper text, figures, and tables:** Creative Commons Attribution 4.0 International License (CC BY 4.0)

This means the code can be reused under the MIT License, and the learning content can be shared or adapted with attribution.

## Acknowledgements

This project is inspired by Andrej Karpathy’s nanoGPT.

This learning module was developed as part of coursework in Advances in Deep Generative Models (MS AI) at The University of Texas at Austin.