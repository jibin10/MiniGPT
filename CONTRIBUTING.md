# Contributing to MiniGPT

Thank you for your interest in MiniGPT.

MiniGPT is a small learning module for rebuilding a GPT-style language model from first principles in PyTorch. The goal is to keep the project simple, readable, and easy to run in Google Colab.

This repository is mainly for learning. So contributions should help make the notebook clearer, easier to run, or easier to understand.

## What you can contribute

Good contributions include:

- fixing typos or unclear explanations
- improving comments in the notebook
- fixing small bugs
- improving Colab compatibility
- improving figures, tables, or README instructions
- adding small tests or sanity checks
- improving `paper.md` or documentation
- suggesting better learning objectives or instructor notes

Please avoid large changes that make the project harder to understand. For example, adding a full training framework, many extra files, or a large new model is probably outside the scope of this learning module.

## Reporting issues

If something does not work, please open a GitHub issue.

When reporting an issue, please include:

- what you were trying to do
- what went wrong
- the error message, if there is one
- whether you were using Colab, local Python, CPU, or GPU
- the Python and PyTorch versions, if you know them

A small screenshot or copied error message is helpful.

## Asking for support

For general questions, please open a GitHub issue.

Examples:

- "The notebook is not running in Colab"
- "I do not understand this part of causal attention"
- "The generated text is different from the paper"
- "The loss curve looks different on my machine"

Small differences in results are normal because training can change with GPU type, PyTorch/CUDA version, random sampling, and runtime settings.

## Pull request workflow

If you want to make a change:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Test the notebook or the changed section.
5. Open a pull request.

Please keep pull requests small when possible. A focused pull request is easier to review.

## Style guide

Please use simple English.

This project is written for learners, so explanations should be clear and direct. Avoid overly formal or robotic writing. If a technical term is needed, briefly explain it.

For code:

- keep the code readable
- add comments where they help understanding
- avoid unnecessary abstractions
- do not add heavy dependencies unless really needed
- keep the notebook Colab-friendly

## Scope of the project

MiniGPT is not trying to be a state-of-the-art language model.

The main goal is to show the full GPT-style workflow:

- character-level tokenization
- token and positional embeddings
- causal self-attention
- Transformer blocks
- next-token training
- validation loss tracking
- checkpoint selection
- text generation

Please keep this goal in mind when suggesting changes.

## License for contributions

By contributing to this repository, you agree that your contribution will be released under the same licenses as the project:

- code and code cells: MIT License
- learning materials, text, figures, tables, and documentation: CC BY 4.0

Thank you for helping improve MiniGPT.
