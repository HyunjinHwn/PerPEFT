# Figures

This directory contains the figures reported in the PerPEFT paper.

---

## Figure 1: Achievement of PerPEFT's Design Objective

**Caption**

(RQ4) Achievement of PerPEFT's design objective. PEFT modules specialized for different groups guide CLIP, a multimodal foundation model, to focus on different aspects of the same item.

**Contents**

This figure visualizes the token-level attention distributions produced by CLIP after personalization with different group-specific PEFT modules.

### Example 1: Golf Travel Bag

Item title:

> Padded Golf Travel Bag, Black

Comparison:

- Golf-group-specialized PEFT
- Camping-group-specialized PEFT

Observation:

- The golf-specialized PEFT places the largest attention on **"Golf"**.
- The camping-specialized PEFT focuses more on **"Travel"** and **"Bag"**.

This demonstrates that PerPEFT can adapt multimodal representations according to different user-group interests.
