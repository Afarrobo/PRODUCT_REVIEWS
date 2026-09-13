# EComReviews-BD

## A Benchmark Dataset for Aspect-Based Sentiment Analysis on Multilingual Bangladeshi E-Commerce Reviews

### Authors

**Raiyan Fardin Haque**<sup>[a]</sup>, **Afsin Sultana**<sup>[a]</sup>, **Md Sabbir Hossain**<sup>[a]</sup>, **Md Arafat Hossain**<sup>[a]</sup>, **Nishat Tasnim**<sup>[a][b]</sup>*

\* **Supervisor**

---

## Overview

**EComReviews-BD** is a multilingual Bangladeshi e-commerce review dataset designed as a benchmark for **Aspect-Based Sentiment Analysis (ABSA)**.

The dataset contains customer reviews collected from **Daraz Bangladesh** across multiple product categories. The reviews are written in **Bangla, Banglish, and English**, making the dataset suitable for multilingual sentiment analysis and aspect-level sentiment classification.

The dataset provides both overall sentiment information and aspect-level sentiment annotations, enabling research in:

- Aspect-Based Sentiment Analysis (ABSA)
- Multilingual Sentiment Analysis
- E-Commerce Review Analysis
- Natural Language Processing (NLP)
- Bangla and Banglish NLP
- Opinion Mining
- Customer Feedback Analysis

---

## Dataset Information

| Information | Value |
|---|---|
| **Dataset Name** | EComReviews-BD |
| **Total Reviews** | 20,685 |
| **Categories** | 19 |
| **Unique Products** | 297 |
| **Unique Brands** | 65 |
| **Aspects** | 74 |
| **Total Unique Reviews** | 19,590 |
| **Language** | Bangla, English, Banglish |

---

## Dataset Characteristics

Each review may contain information such as:

- Marketplace
- Product Category
- Product Name
- Brand
- Price
- Overall Rating
- Review Text
- Overall Sentiment
- Aspect-Level Sentiment

The **74 aspects** cover product- and category-specific attributes, allowing detailed analysis of customer opinions toward different characteristics of products.

---

## Languages

The dataset contains reviews in three language forms:

- **Bangla**
- **Banglish**
- **English**

This multilingual composition makes EComReviews-BD particularly useful for studying sentiment analysis in the context of Bangladesh's diverse online communication.

---

## Applications

EComReviews-BD can be used for:

1. **Aspect-Based Sentiment Analysis**
2. **Multilingual Sentiment Classification**
3. **Bangla NLP**
4. **Banglish NLP**
5. **E-Commerce Recommendation Systems**
6. **Customer Opinion Mining**
7. **Product Review Classification**
8. **Fine-tuning and evaluation of NLP models**
9. **Benchmarking multilingual language models**
10. **Customer feedback and market analysis**

---

## Dataset Files

The repository contains the following primary dataset files:

- `Product_Reviews_Main.xlsx` — Main multilingual review dataset with annotations.
- `Product_Reviews_ENGLISH.xlsx` — English-translated version of the review dataset.

---

## Citation

If you use **EComReviews-BD** in your research, please cite the dataset/paper as follows:

```bibtex
@dataset{ecomreviews_bd,
  title = {EComReviews-BD: A Benchmark Dataset for Aspect-Based Sentiment Analysis on Multilingual Bangladeshi E-Commerce Reviews},
  author = {
    Haque, Raiyan Fardin and
    Sultana, Afsin and
    Hossain, Md Sabbir and
    Hossain, Md Arafat and
    Tasnim, Nishat
  },
  year = {2026}
}
