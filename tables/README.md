# Tables

This directory contains the tables reported in the PerPEFT paper.

---

## Table 1: Dataset Statistics

**Caption**

Dataset statistics. *Avg. Seq. Len.* indicates the mean length of users' purchase-history sequences, and *Density* indicates the total number of user–item interactions divided by the product of the numbers of users and items.

**Contents**

The table summarizes the characteristics of the four Amazon product domains used in the experiments:

- Sports & Outdoors
- Toys & Games
- Beauty & Personal Care
- Arts, Crafts & Sewing

For each domain, the table reports:

- Number of users
- Number of items
- Average purchase-history sequence length
- Interaction density

---

## Table 2: Multimodal Recommendation Performance (RQ1)

**Caption**

(RQ1) Multimodal recommendation performance. All metrics are multiplied by 100 for better readability. Numbers in parentheses indicate standard deviation. H@K and N@K denote Hit-Ratio@K and NDCG@K, respectively. Best results are highlighted with a green box. Notably, PerPEFT outperforms the baseline methods in 44 out of 48 settings.

**Contents**

This table evaluates recommendation performance across four product domains:

- Sports & Outdoors
- Toys & Games
- Beauty & Personal Care
- Arts, Crafts & Sewing

Metrics:

- H@20
- H@30
- N@20
- N@30

Compared methods include:

### Non-PEFT Baselines
- w/o MM
- Frozen MM

### LoRA-based Methods
- Global PEFT
- User-level 1
- User-level 2
- Group-level 1
- Group-level 2
- PerPEFT (Ours)

### (IA)³-based Methods
- Global PEFT
- User-level 1
- User-level 2
- Group-level 1
- Group-level 2
- PerPEFT (Ours)

### IISAN-based Methods
- Global PEFT
- User-level 1
- User-level 2
- Group-level 1
- Group-level 2
- PerPEFT (Ours)

The results demonstrate that PerPEFT consistently achieves superior recommendation performance across most evaluation settings.

---

## Table 3: Ablation Study (RQ5)

**Caption**

(RQ5) Ablation study. All metrics are multiplied by 100 for better readability. Numbers in parentheses indicate standard deviation. H@K and N@K denote Hit-Ratio@K and NDCG@K, respectively. Best results are highlighted with a green box. Notably, PerPEFT outperforms its variants in 15 out of 16 settings.

**Contents**

This table analyzes the contribution of each component in PerPEFT through several ablation variants:

- w/o textual modality
- w/o visual modality
- w/o group-specific negatives
- Large Global PEFT
- Random grouping
- PerPEFT (Ours)

Evaluation is conducted on the same four domains:

- Sports & Outdoors
- Toys & Games
- Beauty & Personal Care
- Arts, Crafts & Sewing

Metrics:

- H@20
- H@30
- N@20
- N@30

The results show that removing any major component generally degrades performance, indicating that each design choice contributes to the effectiveness of PerPEFT.