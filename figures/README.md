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

---

## Figure 3: Group-Specific Negative Sampling

**Caption**

An example case of our training technique for PerPEFT. When training for Group A, we draw negative samples only from items appearing in Group A users' purchase histories, instead of the full item set. The same holds for Group B.

**Contents**

This figure explains the group-specific negative sampling strategy.

### Conventional Negative Sampling

- Negative items are sampled from the entire item universe.
- Many negatives may be irrelevant to the target group's interests.

### PerPEFT Negative Sampling

- Negative candidates are restricted to items observed within the same user group.
- Training focuses on more challenging and semantically relevant negatives.

Benefits:

- Stronger discrimination among similar items.
- Better alignment with group-specific preferences.
- Improved personalization capability.
---

## Figure 4: Qualitative Recommendation Examples

**Caption**

Qualitative recommendation examples demonstrating how PerPEFT captures fine-grained user interests better than Global PEFT and mismatched group-specific PEFT modules.

**Contents**

The figure presents recommendation case studies from multiple domains.

### Sports & Outdoors

User purchase history:

- Camping backpacks
- Camping food products

Comparison:

- Camping-group PEFT
- Global PEFT
- Golf-group PEFT

Observation:

- Camping-group PEFT recommends camping food products that closely match the user's recent interests.
- Global PEFT and golf-group PEFT recommend only broadly related outdoor items.

### Toys & Games

User purchase history:

- LEGO vehicle-themed products

Comparison:

- LEGO-group PEFT
- Global PEFT
- Game-group PEFT

Observation:

- LEGO-group PEFT accurately recommends vehicle-related LEGO products.
- Alternative PEFT modules recommend more generic toys or unrelated game-themed items.

The examples demonstrate the practical effect of group-aware personalization.

---