# EComReviews-BD

**A Multi-Category Bangladeshi E-Commerce Review Dataset with Aspect-Level Polarity Annotations**

## Overview

EComReviews-BD contains customer reviews collected from **Daraz Bangladesh** across **19 product categories** and **483 products**. Reviews are written in **Bangla, Banglish, and English**.

Each review includes:
- Overall sentiment (`-1`, `0`, `1`)
- Aspect-level sentiment labels (category-specific)

Suitable for sentiment analysis and aspect-based sentiment analysis (ABSA).

## Statistics

| Metric | Value |
|---|---|
| Categories | 19 |
| Products | 483 |
| Languages | Bangla, Banglish, English |
| Sentiment Classes | Positive, Neutral, Negative |

## Dataset Files

- **Product_Reviews.xlsx** – Original multilingual reviews with annotations.
- **Product_Reviews_ENG.xlsx** – English-translated version using **NLLB-200** (`facebook/nllb-200-distilled-600M`).

## Data Format

Each sheet contains:
- Marketplace
- Category
- Product Name
- Brand
- Price
- Overall Rating
- Review
- Overall Sentiment
- Aspect Sentiment Columns (category-specific)

## Citation

```bibtex
@dataset{ecomreviews_bd,
  title = {EComReviews-BD: A Multi-Category Bangladeshi E-Commerce Review Dataset with Aspect-Level Polarity Annotations},
  year = {2026}
}
```