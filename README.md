# GhanaTTS

A community-driven project to support training of offline-friendly Text-to-Speech (TTS) models for indigenous Ghanaian languages.

## Overview

As the field of speech synthesis evolves, high-quality Text-to-Speech (TTS) is becoming a vital tool for accessibility and digital inclusion. The GhanaTTS Project aims to establish a standard framework for developing natural-sounding voices for Ghanaian languages.

We primarily leverage [Piper TTS](https://github.com/OHF-Voice/piper1-gpl), a fast, local neural text-to-speech system. We chose Piper because it is optimized for low-power devices (like Raspberry Pi), works entirely offline, and offers high-quality synthesis with incredibly low latency—making it ideal for real-world applications in Ghana.

## Base Models for Fine-tuning

The following checkpoints are recommended as starting points for training your own voices.

| Model Name                                                   | Description / Source                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [**GTTS Twi Male ONNX**](https://huggingface.co/ghananlpcommunity/gtts-twi-male_onnx/tree/main) | A useful starting point for those interested in training models for Twi or similar languages such as Fante, Abron, Nsema etc. |
| [**Piper Swahili Medium**](https://huggingface.co/rhasspy/piper-voices/tree/main/sw/sw_CD/lanfrica/medium) | Base starting point for any Ghanaian language.               |

## Available Datasets

These datasets provide the necessary speech-text pairs required for high-quality synthesis.

| Dataset Name                                                 | Description / Source                                |
| ------------------------------------------------------------ | --------------------------------------------------- |
| [**Twi Female Speech TTS**](https://huggingface.co/datasets/ghananlpcommunity/twi-female-speech-tts) | High-quality Twi speech-text pairs on Hugging Face. |
| [**Asante Twi Bible Speech**](https://huggingface.co/datasets/ghananlpcommunity/asante-twi-bible-speech-text) | Religious text corpus for expressive Twi synthesis. |

*Note: More checkpoints and datasets will be added as they become available.*

## Training Your Model

1. Ensure your audio files are in `.wav` format (22050Hz or 16000Hz) and paired with accurate text transcriptions and publish it to hugging face as an alligned audio text dataset. See examples from the datasets section. If you want to use one of our existing datasets, then you can skip this step.
2. Use our ready-to-go Google Colab notebook to begin training a model from scratch or fine-tuning from one of our checkpoints:
   - 💻 **Train/Finetune a Piper TTS Model** — [Open in Colab](https://colab.research.google.com/drive/1b0KaAjK9ZyM4prUnUawDU2RZ4LBoIn8i?usp=sharing) | 🎥 [Watch the Tutorial](https://youtube.com/)

Once your model is trained, share your checkpoint and a sample audio clip with us to be featured in the GhanaTTS showcase! We are looking for more checkpoints that can be used as starting points for training several languages.

## Support

If you have any questions or difficulty using the notebooks or datasets, please contact us at info@ghananlp.org.
