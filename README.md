# GhanaTTS

A community-driven project to support training of offline-friendly Text-to-Speech (TTS) models for indigenous Ghanaian languages.

## Overview

As the field of speech synthesis evolves, high-quality Text-to-Speech (TTS) is becoming a vital tool for accessibility and digital inclusion. The GhanaTTS Project aims to establish a standard framework for developing natural-sounding voices for Ghanaian languages.

We primarily leverage [Piper TTS](https://github.com/OHF-Voice/piper1-gpl), a fast, local neural text-to-speech system. We chose Piper because it is optimized for low-power devices (like Raspberry Pi), works entirely offline, and offers high-quality synthesis with incredibly low latency—making it ideal for real-world applications in Ghana.

## Base Models for Fine-tuning

The following checkpoints are recommended as starting points for training your own voices.

| Model Name                                                   | Description / Source                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [GTTS Twi](https://huggingface.co/spaces/ghananlpcommunity/GhanaTTS/tree/main/piper-linux/voices/gtts-twi) | A useful starting point for those interested in training models for Twi or similar languages such as Fante, Abron, Nsema etc. It was trained using the [this dataset](https://huggingface.co/datasets/ghananlpcommunity/twi-female-speech-tts). |

## Available Datasets

These datasets provide the necessary speech-text pairs required for high-quality synthesis.

| Dataset Name                                                 | Description / Source                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [Asante Twi Bible Speech-Text](https://huggingface.co/datasets/ghananlpcommunity/asante-twi-bible-speech-text) | Speech-text from Bible.                                      |
| [Asante Twi Bible Speech-Text (Trigrams)](ghananlpcommunity/twi-trigrams-speech-text-parallel) | Speech-text from Bible split into trigrams. This trains faster but there are some pauses during inference. |

*Note: More checkpoints and datasets will be added as they become available.*

## Training Your Model

1. Ensure your audio files are in `.wav` format (22050Hz or 16000Hz) and paired with accurate text transcriptions and publish it to huggingface as an alligned audio text dataset. See how to prepare your dataset and push to HF [here](https://github.com/GhanaNLP/TTS-data-preparation). If you want to use one of our existing datasets [here](https://huggingface.co/collections/ghananlpcommunity/ghana-tts), then you can skip this step.
2. Use our ready-to-go Google Colab notebook to begin training a model from scratch or fine-tuning from one of our checkpoints:
   - 💻 **Train/Finetune a Piper TTS Model** — [Open in Colab](https://colab.research.google.com/drive/1b0KaAjK9ZyM4prUnUawDU2RZ4LBoIn8i?usp=sharing) | 🎥 [Watch the Tutorial](https://drive.google.com/file/d/1He2I8OlmVgpSQHyxzIUabYysAn-VlM7A/view?usp=sharing)

3. Once your model is trained, upload it here to see how it to our TTS server folder [here](https://huggingface.co/spaces/ghananlpcommunity/GhanaTTS/tree/main/piper-linux/voices/) to share it with the world, and hear how it sounds [here](https://huggingface.co/spaces/ghananlpcommunity/GhanaTTS).

## Support

If you have any questions or difficulty using the notebooks or datasets, please contact us at michseth@ghananlp.org.
