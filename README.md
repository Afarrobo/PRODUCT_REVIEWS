# EComReviews-BD

**A Multi-Category Bangladeshi E-Commerce Review Dataset with Aspect-Level Polarity Annotations**

Collected from [Daraz](https://www.daraz.com.bd/) — one of South Asia's leading e-commerce platforms.

---

## Overview

EComReviews-BD is a structured sentiment dataset of customer reviews spanning **19 product categories** and **483 products**. Reviews are written in Bangla, Banglish, and English, reflecting the natural multilingual writing patterns of Bangladeshi consumers.

Each review is annotated with:
- An **overall sentiment polarity** label
- **Fine-grained aspect-level sentiment** labels (aspects vary by category)

Suitable for sentiment analysis, aspect-based sentiment analysis (ABSA), and recommendation system research.

---

## Key Statistics

| Metric | Value |
|---|---|
| Product Categories | 19 |
| Products Reviewed | 483 |
| Languages | 3 (Bangla, Banglish, English) |
| Polarity Classes | 3 (Positive, Neutral, Negative) |

---

## Languages

Reviews are written organically in:
- **Bangla** (বাংলা)
- **Banglish** (Romanized Bangla)
- **English**

---

## Annotation Schema

Each review is annotated at two levels using a three-class polarity scheme:

| Label | Polarity |
|---|---|
| `+1` | Positive |
| `0` | Neutral |
| `-1` | Negative |

**Review-Level:** A single polarity label for the review as a whole.

**Aspect-Level:** Separate polarity labels for individual product aspects (e.g. Quality, Battery, Connectivity) mentioned in the review. Aspects vary by category.

---

## Annotated Aspects by Category

| Category | Aspects |
|---|---|
| PowerBank | Quality, Capacity, Charging, Cable, Indicator, Heat, Design, Packaging, Delivery, Seller, Price, Authenticity |
| CellPhone | Quality, Battery, Charger, Audio, Display, Features, Network, Packaging, Delivery, Seller, Price, Authenticity |
| SmartPhone | Battery, Display, Charging, Connectivity, Sound, Packaging, Delivery, Seller, Authenticity, Price |
| Keyboard | Build, Keys, Noise, Layout, Lighting, Connectivity, Durability, Packaging, Delivery, Seller, Price, Warranty, Authenticity |
| Mouse | Quality, Performance, Click_Buttons, Scroll_Wheel, Comfort_Design, Build_Quality_Durability, Connectivity, Battery, RGB_Lighting, Packaging, Delivery, Seller, Authenticity, Price |
| Router | Speed, Range, Stability, Setup, Firmware, Heating, Ports, Security, Authenticity, Packaging, Delivery, Seller, Price, Warranty |
| WebCam | Quality, LowLight, WideAngle, Microphone, Heating, Software, Packaging, Delivery, Seller, Authenticity, Price, Warranty |
| Microphone | Sound, Noise, Authenticity, Packaging, Delivery, Seller, Price, Compatibility, Accessories, Setup, Durability, Warranty |
| Wireless Earbuds | Sound, Bass, Mic, Battery, ANC_ENC, Comfort_Fit, Connectivity, Controls, Build_Design, Case_Accessories, Packaging, Delivery, Seller, Price, Authenticity |
| Ear/Headphone | Sound_Quality, Microphone, Build_Quality, Comfort, Design, Battery, Connectivity, Controls, Noise_Cancellation, Packaging, Price_Value, Authenticity, Delivery_Service, Performance, Compatibility |
| SmartWatch | Battery, Display, Strap, Connectivity, Sensors, Sound, Build, Packaging, Delivery, Seller, Authenticity, Price |
| ChargingAdapter | Speed, Wattage, Heating, Authenticity, Packaging, Delivery, Seller, Cable, Compatibility, Warranty, Price, Durability |
| ChargingCable | Speed, Wattage, Quality, Durability, Compatibility, Connector, Data, Length, Authenticity, Price, Delivery, Seller |
| HDMI Cable | Quality, Length, Video, Audio, Resolution, Compatibility, Packaging, Delivery, Seller, Price, Authenticity, Durability |
| Pendrive | Speed, Capacity, Heating, Build, Compatibility, Authenticity, Warranty, Packaging, Delivery, Price |
| Memory Cards | Speed, Capacity, Reliability, Compatibility, Authenticity, Corruption, Packaging, Delivery, Seller, Price |
| Mini Printer | Print, Photo, Text, Clarity, Paper, Battery, Connectivity, Packaging, Delivery, Price |
| CCTV Camera | Video_Quality, Night_View, Network, App, Motion, Sound, Durability_and_Quality, Packaging, Price |
| PC Speaker | Sound Quality & Performance, Bass & Loudness, Build Quality and Design, Durability and Budgets, Wires & Ports, Delivery, Packaging & Seller Service |

---

## Dataset Files

### `Product_Reviews.xlsx`
The primary dataset file. Contains all customer reviews in their original language (Bangla, Banglish, or English), with overall sentiment polarity and aspect-level labels. The workbook has **19 sheets**, one per product category.

### `Product_Reviews_ENG.xlsx`
An English-translated version of the dataset, produced using the [NLLB-200](https://huggingface.co/facebook/nllb-200-distilled-600M) multilingual neural machine translation model (`facebook/nllb-200-distilled-600M`) via the Hugging Face Transformers framework. Useful for researchers who need a monolingual English corpus or want to apply English-centric NLP pipelines.

---

## Column Schema

Each sheet in `Product_Reviews.xlsx` shares the following structure:

| Column | Type | Description |
|---|---|---|
| Marketplace | string | Source platform (Daraz) |
| Category | string | Product category (one of 19 classes) |
| Product Name | string | Name of the reviewed product |
| Brand | string | Brand or manufacturer |
| Price | float | Listed price at time of collection (BDT) |
| Overall Rating | float | Aggregate star rating |
| Reviews | string | Raw review text (Bangla, Banglish, or English) |
| Sentiment | int | Overall polarity: `-1` Negative, `0` Neutral, `1` Positive |
| Aspect Columns | int | One column per aspect (category-specific). Values: `-1`, `0`, or `1` |

---

## Translation Methodology

Translation was performed using the **NLLB-200** model, specifically the distilled 600M-parameter variant (`facebook/nllb-200-distilled-600M`), applied via the Hugging Face Transformers framework for high-quality cross-lingual transfer from Bangla and Banglish into English.

---

## Citation

If you use this dataset in your research, please cite:

```bibtex
@dataset{ecomreviews_bd,
  title  = {EComReviews-BD: A Multi-Category Bangladeshi E-Commerce Review Dataset
             with Aspect-Level Polarity Annotations},
  year   = {2026},
  note   = {Collected from Daraz; 19 categories, 483 products; Bangla, Banglish, and English}
}
```

---

*Platform: Daraz Bangladesh · Translation: NLLB-200 (facebook/nllb-200-distilled-600M)*