---
title: "General description"
weight: 10
description: "General description"
---

<script>
  MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['$$', '$$'], ['\\[', '\\]']],
      processEscapes: true,
      processEnvironments: true,
      packages: {'[+]': ['ams']}
    },
    options: {
      skipHtmlTags: ['script', 'noscript', 'style', 'textarea', 'pre']
    },
    loader: {
      load: ['[tex]/ams']
    }
  };
</script>
<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

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

**December 14, 2025**: We have added a comprehensive ["**Detailed Analysis**"](#detailed-analysis) section, including scoring methodologies and performance visualizations for both tracks.

**December 4, 2025**: We have updated the ranking results in the [“**Leaderboard**”](#leaderboard) section below.

**November 15, 2025**: We have updated the formula and threshold for calculating Top-Tier Accuracy with detailed information available at the ["**Evaluation**"](#evaluation) section below.

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

We will measure both system-level and utterance-level.

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
| 6    | LoveAImusic     | 0.507 |
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
| 8    | LoveAImusic     | 0.568 |
| 9    | MAIL            | 0.567 |
| 10   | Niuguangshuo    | 0.563 |
| 11   | Ah3Dui          | 0.553 |
| 11   | PIRL            | 0.553 |
| 13   | Harmonics       | 0.525 |
| 14   | DYME            | 0.501 |
| 15   | nk_hlt_group    | 0.499 |
| 16   | Hachimi         | 0.493 |
| 17   | nbu             | 0.484 |


**Note**: 🏆 indicates teams invited to submit ICASSP 2-page papers.

## Detailed Analysis


### **Track 1 Scoring Methodology**

The final score for Track 1 is derived from two test sets (Set1 and Set2). Each set is evaluated at both the Utterance (UTT) and System (SYS) levels.

- **Metric Calculation per Set**

For each dataset (Set 1 and Set 2), we first calculate the composite metrics for each team. Since the TTA metric exists only at the UTT level, it is used directly. For the other metrics (LCC, SRCC, KATU), we average the scores from the SYS and UTT levels:

<div>
$$\begin{aligned} \text{LCC}_{avg} &= \frac{\text{LCC}_{sys} + \text{LCC}_{utt}}{2} \\ \text{SRCC}_{avg} &= \frac{\text{SRCC}_{sys} + \text{SRCC}_{utt}}{2} \\ \text{KATU}_{avg} &= \frac{\text{KATU}_{sys} + \text{KATU}_{utt}}{2} \end{aligned}$$
</div>

- **Score Calculation per Set**

The score for a specific set is the average of these four metrics:

<div>
$$Score_{set} = \frac{\text{LCC}_{avg} + \text{SRCC}_{avg} + \text{KATU}_{avg} + \text{TTA}_{utt}}{4}$$
</div>

- **Final Track 1 Score**

The final score for Track 1 is a weighted average of the scores from Set 1(Easy) and Set 2(Hard), with a ratio of 2:8:

$$\text{Final Score (Track 1)} = 0.2 \times Score_{set1} + 0.8 \times Score_{set2}$$

<div style="text-align: center;">
    <img src="./images/track1_performance.svg" style="width: 1200px; max-width: 100%; height: auto; clip-path: inset(0 10% 0 0);">
</div>



### **Track 2 Scoring Methodology**

Track 2 evaluation involves five dimensions: Coherence, Naturalness, Memorability, Clarity, and Musicality. The calculation proceeds in three steps:

- **Average Calculation per Metric across Dimensions**

For each dimension (Coherence, Naturalness, Memorability, Clarity, Musicality), we first calculate the average of LCC, SRCC, and KATU at both UTT and SYS levels:

<div>
$$\text{LCC}_{avg\_dim} = \frac{\text{LCC}_{sys\_dim} + \text{LCC}_{utt\_dim}}{2}$$
$$\text{SRCC}_{avg\_dim} = \frac{\text{SRCC}_{sys\_dim} + \text{SRCC}_{utt\_dim}}{2}$$
$$\text{KATU}_{avg\_dim} = \frac{\text{KATU}_{sys\_dim} + \text{KATU}_{utt\_dim}}{2}$$
</div>

TTA is used directly from the UTT level, as it is only available there.

- **Calculate Final Score for Each Dimension**

For each dimension, we then calculate the average of LCC, SRCC, KATU, and TTA:

<div>
$$\text{Final Score}_{dim} = \frac{\text{LCC}_{avg\_dim} + \text{SRCC}_{avg\_dim} + \text{KATU}_{avg\_dim} + \text{TTA}_{utt\_dim}}{4}$$
</div>

- **Overall Track 2 Final Score**

Finally, we calculate the overall Track 2 score by averaging the final scores of all five dimensions:

$$\text{Final Score (Track 2)} = \frac{\sum_{d=1}^{5} \text{Final Score}_{dim}}{5}$$



<div style="text-align: center; max-width: 1600px; margin: 0 auto;">
    <img src="./images/track2_performance.svg" style="width: 110%; height: auto; clip-path: inset(0 15% 0 7%);">
</div>

**Note**: The LCC, SRCC, and KATU scores shown in the above figures are averaged from both utterance-level (UTT) and system-level (SYS) evaluations. For more detailed results, please refer to the [results folder](https://github.com/ASLP-lab/Automatic-Song-Aesthetics-Evaluation-Challenge/blob/main/static/results/).