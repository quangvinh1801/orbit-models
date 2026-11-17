# Orbit models

Model files that Orbit (a personal, local-first desktop app) downloads once, when its user asks. Nothing else lives here.

## PhoWhisper-large, 16-bit ONNX

- **Model:** [PhoWhisper-large](https://huggingface.co/vinai/PhoWhisper-large) by VinAI Research: Whisper large fine-tuned on 844 hours of Vietnamese speech. Paper: [PhoWhisper: Automatic Speech Recognition for Vietnamese](https://arxiv.org/abs/2406.02555).
- **Licence:** BSD-3-Clause, © VinAI Research (see `LICENSE-PhoWhisper.txt` in the release).
- **Source:** the ONNX export by [huuquyet/PhoWhisper-large](https://huggingface.co/huuquyet/PhoWhisper-large), revision `1c2dc3659b1646ffd09c052d3433f899f6e1c789`.
- **Changes:** the encoder and the merged decoder are converted from 32-bit to 16-bit floats with the Transformers.js 3.8.1 tools (`scripts/quantize.py --modes fp16`), by the workflow in this repository. Weights are otherwise unchanged.
- **Files:** `encoder_model_fp16.onnx`, `decoder_model_merged_fp16.onnx`, the tokenizer and config files, and `manifest.json` with the size and SHA-256 of each file.
