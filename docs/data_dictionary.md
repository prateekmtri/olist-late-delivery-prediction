# Data Dictionary

Rule: use only information known when the customer clicks "buy".

## orders
| Column | Allowed? | Note |
|---|---|---|
| order_id | key | link to other tables |
| customer_id | key | link to customers |
| order_status | NO | final status is known later |
| order_purchase_timestamp | YES | the moment of purchase |
| order_approved_at | NO | payment approval happens after the click |
| order_delivered_carrier_date | NO | carrier pickup is known later |
| order_delivered_customer_date | NO | used ONLY to build the label |
| order_estimated_delivery_date | YES | the promised date, shown at purchase |

## order_items
| Column | Allowed? | Note |
|---|---|---|
| order_id | key | |
| order_item_id | YES | item number inside the order |
| product_id | key | |
| seller_id | key | |
| shipping_limit_date | YES | seller deadline, set at purchase |
| price | YES | |
| freight_value | YES | |

## order_payments
| Column | Allowed? | Note |
|---|---|---|
| order_id | key | |
| payment_sequential | YES | |
| payment_type | YES | chosen at checkout |
| payment_installments | YES | chosen at checkout |
| payment_value | YES | |

## customers
| Column | Allowed? | Note |
|---|---|---|
| customer_id | key | |
| customer_unique_id | key | |
| customer_zip_code_prefix | YES | |
| customer_city | YES | |
| customer_state | YES | |

## sellers
| Column | Allowed? | Note |
|---|---|---|
| seller_id | key | |
| seller_zip_code_prefix | YES | |
| seller_city | YES | |
| seller_state | YES | |

## products
| Column | Allowed? | Note |
|---|---|---|
| product_id | key | |
| product_category_name | YES | |
| product_name_lenght | YES | (spelling is from the original data) |
| product_description_lenght | YES | |
| product_photos_qty | YES | |
| product_weight_g | YES | |
| product_length_cm, product_height_cm, product_width_cm | YES | |

## geolocation
| Column | Allowed? | Note |
|---|---|---|
| geolocation_zip_code_prefix | key | |
| geolocation_lat, geolocation_lng | YES | used later for distance |
| geolocation_city, geolocation_state | YES | |

## order_reviews
All columns: **NO**. Reviews are written after delivery. We do not use this table.