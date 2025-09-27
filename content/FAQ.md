---
title: "FAQ"
description: "Frequently Asked Questions"
menu: main
weight: 200
---


## General Information


**Q: What does Track 1's "single holistic aesthetic score" refer to?**


A: Track 1 requires predicting the "Overall Musicality" dimension specifically (one of the five aesthetic dimensions), not an average of all five dimensions.

## Registration and Participation

**Q: How do I register for the challenge?**


A: Teams can complete registration through the [official Google Form](https://docs.google.com/forms/d/e/1FAIpQLSejinwosfchGsyN0Xoh3cfz6TIC79c9WUKNLCI2T5yS-pKRUg/viewform?usp=sharing&ouid=102700557983879249800). Fill in the required team details and submit. You will receive confirmation once your registration is successfully processed.


**Q: Can individuals participate, or is team participation required?**


A: Yes, individuals are welcome to participate. They should register as a team of one.

## Dataset

**Q: What is the training dataset?**

A: The official SongEval dataset is provided, containing 2,399 full-length songs (approximately 140.3 hours of generated music) covering various genres and languages, including Pop, Rock, Jazz, Hip-hop, Classical, etc., supporting both English and Mandarin Chinese.

**Q: What is the rating scale for the aesthetic scores?**

A: The aesthetic scores are rated on a 5-point scale, from 1 (lowest quality) to 5 (highest quality). For more details on the annotation methodology, please refer to the official SongEval paper.

**Q: Can I use additional external datasets?**

A: No. Participants are **only allowed to use the provided official dataset for training and validation**. The use of any additional external datasets is strictly prohibited.

**Q: Can I use pretrained models?**

A: Yes. Participants are free to use any open-source pretrained models to support system development. In the final technical report, participants must clearly specify which pretrained models were used and provide corresponding open-source links or references.

## Evaluation and Submission

**Q: What is Top-Tier Accuracy?**

A: Top-Tier Accuracy measures the accuracy of identifying top-performing songs by comparing the model's top-ranked songs with the actual top-ranked songs. In music evaluation, we typically care more about whether models can accurately identify excellent songs rather than distinguish mediocre ones. Songs are categorized into "top songs" and "non-top songs" based on a threshold.


**Q: How is the final ranking determined from the four evaluation metrics?**

A: The final ranking is determined by the weighted average of four normalized evaluation metrics. Each metric carries equal weight.


**Q: What are the ground truth labels based on?**

A: All evaluation metrics use ground truth labels that are the **average of four expert raters' scores**.

## Technical Requirements

**Q: Is a baseline system provided?**

A: Yes. The competition provides a [baseline system](https://github.com/ASLP-lab/SongEval) built upon SongEval. The baseline leverages a trained aesthetic evaluation model on SongEval, enabling automatic scoring of generated songs across five perceptual dimensions.

**Q: What are the input format requirements?**

A: Models need to process full-length audio inputs. Specific audio format requirements  with the following specifications：
- File Format: MP3
- Sample Rate: 44,100 Hz
- Channels: Stereo (2 channels)