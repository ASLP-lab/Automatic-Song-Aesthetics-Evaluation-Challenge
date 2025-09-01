---
title: "Dataset"
description: "The official dataset of the challenge"
menu: main
weight: 80
---

To support model development, we have curated the [SongEval](https://huggingface.co/datasets/ASLP-lab/SongEval) dataset—an open-source benchmark containing **2,399 full-length songs** (approx. **140.3 hours** of generated song) from a variety of genres and languages. These songs have been annotated across five aesthetic dimensions:
- **Overall Coherence**
- **Memorability**
- **Naturalness of Vocal Breathing and Phrasing**
- **Clarity of Song Structure**
- **Overall Musicality**

The dataset covers a wide range of genres including **Pop, Rock, Jazz, Hip-hop, Classical**, and more. It includes songs in both **English** and **Mandarin Chinese**, making it a diverse resource for training models. For more details concerning the dataset, we refer to [dataset paper](https://arxiv.org/pdf/2505.10793).

# Evaluation Dataset

To rigorously assess the capabilities of participating models, we have prepared two distinct datasets, one for each competition track. 

## Track 1: Overall Musicality Assessment

The objective of Track 1 is to predict a single, holistic score for the overall musical quality of a generated song. The evaluation dataset for this track is built for breadth and diversity, reflecting the current landscape of AI music generation. 

We have collected a comprehensive set of songs from over 10 prominent open-source and commercial music generation models and APIs. This includes: SUNO, Udio, Seed-Music, Mureka, YUE, DiffRhythm ACE-step, SongGeneration, JAM, Songbloom, etc.


## Track 2: Multi-Dimensional Aesthetic Assessment

The objective of Track 2 is to perform a more fine-grained evaluation by predicting scores across five distinct subjective dimensions of musicality.

Unlike the broad collection in Track 1, the dataset for Track 2 is a purpose-built, curated collection of generated music. It has been specifically constructed to cover and validate model performance across the five target dimensions. The songs in this dataset were carefully selected and, in some cases, specially generated to exhibit a wide range of characteristics. This ensures the dataset contains examples that might score high on one dimension (e.g., melody) but low on another (e.g., rhythmic coherence).

