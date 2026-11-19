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
Olist Brazilian E-Commerce Public Dataset (Kaggle). Data is not included in this repo.

## Status
- [x] Step 1: Problem definition (in progress)