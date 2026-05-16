# MiniGPT

MiniGPT is a small GPT-style autoregressive language model implemented from scratch in PyTorch.

The notebook rebuilds the main GPT workflow: tokenization, causal self-attention, Transformer blocks, next-token training, validation loss tracking, checkpoint selection, and text generation.

The implementation is inspired by Karpathy's nanoGPT design, but the code is written from scratch.

## Open in Colab

Run the notebook directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jibin10/MiniGPT/blob/main/MiniGPT_Notebook.ipynb)

## Notebook

Main notebook: `MiniGPT_Notebook.ipynb`

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

## How to Run

1. Click the Open in Colab button.
2. Select GPU runtime.
3. Run the notebook cells from top to bottom.

Recommended Colab setting:

Runtime → Change runtime type → GPU

## License

Code: MIT  
Text and figures: CC BY 4.0

## Acknowledgement

This project is inspired by Andrej Karpathy’s nanoGPT.