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
---

## Figure 2: Comparison Between Global PEFT and PerPEFT

**Caption**

An example case of (A) Global PEFT and (B) PerPEFT, our personalized PEFT for multimodal recommendation. Each item's multimodal information is encoded by CLIP with an attached PEFT module. Unlike Global PEFT, which uses the same PEFT module for all users, PerPEFT employs different PEFT modules according to inferred user-interest groups. Item representations are formed by combining multimodal and transductive embeddings and are then used by SASRec for recommendation.

**Contents**

This figure illustrates the overall architecture of PerPEFT.

### Global PEFT

- A single PEFT module is shared across all users.
- All users receive multimodal embeddings generated from the same personalized encoder.

### PerPEFT

- Multiple PEFT modules are maintained.
- Users are assigned to interest groups.
- Each group uses its own specialized PEFT module.
- Group-specific multimodal embeddings are combined with transductive item embeddings.
- SASRec generates personalized recommendations from the resulting item sequences.

The figure highlights the key idea of PerPEFT: **group-aware multimodal personalization**.
