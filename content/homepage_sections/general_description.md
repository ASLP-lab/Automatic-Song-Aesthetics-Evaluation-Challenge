---
title: "General description"
weight: 10
description: "General description"
---

<style>
table {
    table-layout: fixed;
    width: 100%;
    border-collapse: collapse;
}
table th,
table td {
    border: 1px solid #e0e0e0;
    padding: 0.75em 1em;
}
table th:first-child,
table td:first-child {
    width: 80px;
    text-align: center;
}
table th:nth-child(2),
table td:nth-child(2) {
    width: 250px;
    text-align: center;
}
table th:last-child,
table td:last-child {
    width: 120px;
    text-align: right;
}
table thead th {
    background-color: #f5f5f5;
    font-weight: 600;
}
table tbody tr:hover {
    background-color: #fafafa;
}
</style>

## News and Updates

**December 4, 2025**: We have updated the ranking results with detailed information available in the "Leaderboard" section below.

**November 15, 2025**: We have updated the formula and threshold for calculating Top-Tier Accuracy with detailed information available at the Evaluation section below.

**November 10, 2025**: We have sent the test set and submission Instructions to all successfully registered teams via email. These are also available in the respective track pages. Kindly note that the final submission deadline is **23:59 November 20, 2025 (AoE time)**.


## Call for Participation

With the rapid growth of generative music models, such as song generation (composing melodies, lyrics, harmonies, and vocals), we are entering an exciting new era of personalized music, virtual artists, and multimedia content creation. Despite these advancements, the evaluation of the aesthetic quality of generated music remains a challenge. Traditional metrics like pitch accuracy and signal clarity fall short of capturing the complex emotional and artistic dimensions of music that matter most to listeners.
This challenge aims to create a benchmark for assessing the aesthetic quality of automatically generated songs. Participants will develop models that predict human ratings of songs based on musicality, emotional engagement, vocal expressiveness, and overall enjoyment.

**Join us to push the boundaries of song aesthetics evaluation and contribute to the future of generative music!**



## Challenge Overview

The ICASSP 2026 Automatic Song Aesthetics Evaluation Challenge is designed to foster the development of models that can predict human aesthetic ratings of full-length generated songs. We focus on generating songs that align with human perceptions of musicality, emotional depth, and vocal expressiveness. Participants will be tasked with developing models that predict subjective ratings based on audio inputs.

Objective: Create models that can predict human ratings of aesthetic quality in songs, including dimensions like overall musicality, emotional engagement, and vocal expressiveness.


## Track Settings
The competition consists of two tracks:

**Track 1: Overall Musicality Score Prediction** Participants must predict a single holistic aesthetic score for each song, representing an overall musical impression of the song's artistic quality.

**Track 2: Fine-Grained Aesthetic Dimension Prediction** Participants to predict five specific aesthetic dimensions for each song.

## Evaluation
Each track will use correlation-based metrics as follows:
- **Linear Correlation Coefficient**
- **Spearman’s rank correlation coefficient**
- **Kendall's Rank Correlation Coefficient**
- **Top-Tier Accuracy**

We will mesure both system-level and utterance-level.

### Top-Tier Accuracy Calculation Rules & Thresholds

**Quantification Method**: Top-Tier Accuracy is uniformly measured using the F1 score.

- F1 Score Formula: F1 = 2 × (Precision × Recall) / (Precision + Recall)

- Brief Definition: Precision = True Positives / (True Positives + False Positives); Recall = True Positives / (True Positives + False Negatives)

**Top-Tier Song Thresholds**:

- Track 1 (Overall Musicality): Score ≥ 4.0
- Track 2 (Subdivided Aesthetic Dimensions):
  - Coherence ≥ 4.0
  - Memorability ≥ 3.75
  - Naturalness ≥ 4.0
  - Clarity ≥ 3.75
  - Musicality ≥ 4.0


## Submission Instructions

Final results can be submitted using Google form: [ICASSP2026 ASAE Challenge Final Submission Form](https://docs.google.com/forms/d/e/1FAIpQLSdVt-TUGRr8sSG4IxgnMEUssGXEatlwFjYcrUl54Zveb4uySA/viewform?usp=dialog)

### Prediction files
Each participating team must submit one SCP file per track.
- Track 1 submission format:

    Each line should contain: utt score

- Track 2 submission format:

    Each line should contain: utt score1 score2 score3 score4 score5

Please ensure that the utt IDs exactly match those in the provided test sets.

All predicted scores are in a valid numeric format.

Files are named as track1_set1_pred.scp, track1_set2_pred.scp and track2_pred.scp, respectively.

### System description (2 pages)

  - Each team must submit a two-page system description summarizing their method, model architecture, training strategy, and any relevant implementation details.(excluding references)

  - The format should follow the [ICASSP official paper template](https://cmsworkshops.com/ICASSP2026/papers/paper_kit.php#Templates) (available on the ICASSP 2026 website) 


**Submission of both the prediction files and the system description is required. Missing either will lead to cancellation of the challenge ranking.**

## Baseline System

The competition provides a [baseline system](https://github.com/ASLP-lab/SongEval) built upon SongEval. The baseline toolkit leverages a trained aesthetic evaluation model on SongEval, enabling automatic scoring of generated songs across five perceptual dimensions, closely aligned with professional musicians’ judgments.

The baseline test validation IDs are available in the [`val_ids.txt`](https://github.com/ASLP-lab/Automatic-Song-Aesthetics-Evaluation-Challenge/blob/main/static/val_ids.txt) file.

This baseline serves as a reproducible and extensible starting point, helping participants better benchmark their systems and ensuring fair comparison across different approaches.


## Leaderboard

### Track 1: Overall Musicality Score Prediction

| Rank | Team Name       | Score |
|:----:|:---------------:|:-----:|
| 1🏆    | Hachimi         | 0.575 |
| 2🏆   | BAL-RAE         | 0.556 |
| 3🏆    | qualifier       | 0.529 |
| 4    | HyperCritic     | 0.518 |
| **5**    | **Baseline**    | **0.510** |
| 6    | yyyf            | 0.507 |
| 6    | LoveAlmusic     | 0.507 |
| 8    | LeVo            | 0.503 |
| 9    | Ah3Dui          | 0.497 |
| 9    | Niuguangshuo    | 0.497 |
| 11   | nbu             | 0.496 |
| 12   | mi-whu          | 0.476 |
| 13   | BHE-AIM         | 0.469 |
| 14   | Harmonics       | 0.438 |
| 15   | Team_Mingda     | 0.429 |
| 16   | MAIL            | 0.426 |
| 17   | IITJVision      | 0.425 |
| 18   | PIRL            | 0.424 |
| 19   | DYME            | 0.388 |


### Track 2: Fine-Grained Aesthetic Dimension Prediction


| Rank | Team Name       | Score |
|:----:|:---------------:|:-----:|
| 1🏆    | LeVo            | 0.655 |
| 2🏆    | HyperCritic     | 0.604 |
| 3    | Team Resonance  | 0.598 |
| 4    | mi-whu          | 0.596 |
| 5    | BAL-RAE         | 0.589 |
| **6**    | **Baseline**    | **0.574** |
| 7    | yyyf            | 0.573 |
| 8    | LoveAlmusic     | 0.568 |
| 9    | MAIL            | 0.567 |
| 10   | Niuguangshuo    | 0.563 |
| 11   | Ah3Dui          | 0.553 |
| 11   | PIRL            | 0.553 |
| 13   | Harmonics       | 0.525 |
| 14   | DYME            | 0.501 |
| 15   | nk_hlt_group    | 0.499 |
| 16   | Hachimi         | 0.493 |
| 17   | nbu             | 0.484 |