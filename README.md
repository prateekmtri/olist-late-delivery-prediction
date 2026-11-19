# Olist Late Delivery Prediction

Predict at purchase time whether an online order will arrive after the promised date.

## Business Problem
The shop promises a delivery date. Some orders arrive late. Late orders cause bad reviews, refunds and angry customers. This project finds risky orders at the moment of purchase, so the shop can act early.

## Label
- Use only delivered orders.
- late = 1 if the real delivery date is after the promised date.
- late = 0 otherwise.

## Prediction Time Rule
Use only information known when the customer clicks "buy". Do not use delivery dates, review scores or the final order status.

## Dataset
## Dataset
Olist Brazilian E-Commerce Public Dataset (Kaggle), by Olist.
- License: CC BY-NC-SA 4.0 (non-commercial use, credit required).
- Link: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
- 9 linked CSV tables, about 100k orders from 2016 to 2018.
- The data is NOT included in this repo. Download it from Kaggle and put the CSV files in `data/raw/`.
- Column rules (allowed at purchase time or not): see `docs/data_dictionary.md`.

## Status
## Status
- [x] Step 1: Problem definition
- [x] Step 2: Data collection