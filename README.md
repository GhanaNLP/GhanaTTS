# GhanaTTS

A community-driven project to support training of offline-friendly Text-to-Speech (TTS) models for indigenous Ghanaian languages.

## Overview

As the field of speech synthesis evolves, high-quality Text-to-Speech (TTS) is becoming a vital tool for accessibility and digital inclusion. The GhanaTTS Project aims to establish a standard framework for developing natural-sounding voices for Ghanaian languages.

We support two primary architectures:

1. **Piper TTS:** Optimized for low-power devices (like Raspberry Pi), works entirely offline, and offers high-quality synthesis with incredibly low latency.
2. **StyleTTS2:** A state-of-the-art architecture that leverages style diffusion for human-level expressiveness and emotion, ideal for high-fidelity applications.

## Base Models for Fine-tuning

The following checkpoints are recommended as starting points for training your own voices.

| Model Name                                                   | Architecture | Description / Source                                         |
| ------------------------------------------------------------ | ------------ | ------------------------------------------------------------ |
| [GTTS Twi (Piper)](https://huggingface.co/spaces/ghananlpcommunity/GhanaTTS/tree/main/piper-linux/voices/gtts-twi) | Piper        | A useful starting point for Twi or similar languages (Fante, Abron, Nsema). Trained on the [female speech dataset](https://huggingface.co/datasets/ghananlpcommunity/twi-female-speech-tts). |
| [StyleTTS2 Twi (Demo)](https://www.google.com/search?q=https://huggingface.co/ghananlpcommunity/styletts2-twi) | StyleTTS2    | A demo checkpoint showcasing expressive Asante-Twi synthesis. Trained for 7 epochs on the Bible dataset. |

## Available Datasets

These datasets provide the necessary speech-text pairs required for high-quality synthesis.

| Dataset Name                                                 | Description / Source                                |
| ------------------------------------------------------------ | --------------------------------------------------- |
| [Asante Twi Bible Speech-Text](https://huggingface.co/datasets/ghananlpcommunity/asante-twi-bible-speech-text) | Full speech-text pairs from the Bible.              |
| [Asante Twi Bible Speech-Text (Trigrams)](https://huggingface.co/datasets/ghananlpcommunity/twi-trigrams-speech-text-parallel) | Bible data split into trigrams for faster training. |

*Note: More checkpoints and datasets will be added as they become available.*

## Training Your Model

1. **Data Preparation:** Ensure your audio files are `.wav` (22050Hz or 16000Hz) paired with accurate text. See our [Data Prep Guide](https://github.com/GhanaNLP/TTS-data-preparation) to push your dataset to Hugging Face.
2. **Choose Your Architecture:** Use our ready-to-go Google Colab notebooks to begin training:
   - 💻 **Piper TTS (Fast/Offline)** — [Open in Colab](https://colab.research.google.com/drive/1b0KaAjK9ZyM4prUnUawDU2RZ4LBoIn8i?usp=sharing) | 🎥 [Watch Tutorial](https://drive.google.com/file/d/1He2I8OlmVgpSQHyxzIUabYysAn-VlM7A/view?usp=sharing)
   - 💻 **StyleTTS2 (Expressive/HQ)** — [Open in Colab](https://colab.research.google.com/github/GhanaNLP/notebooks/blob/main/tts/StyleTTS2_Twi_Finetune_working_final.ipynb)
3. **Deployment:** Once trained, contribute your model to our TTS server folder [here](https://huggingface.co/spaces/ghananlpcommunity/GhanaTTS/tree/main/piper-linux/voices/) and hear it live on the [GhanaTTS Demo Space](https://huggingface.co/spaces/ghananlpcommunity/GhanaTTS).

## Support

If you have any questions or difficulty using the notebooks or datasets, please contact us at michseth@ghananlp.org.
