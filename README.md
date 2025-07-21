# Amazon Case Study Data Analysis Report

## Introduction
This report presents an analysis of the provided Amazon case study Excel file, focusing on product data, pricing, discounts, ratings, and potential revenue. The objective is to extract key insights that can inform business decisions.

## Data Overview
The Excel file contains several sheets, with the primary data residing in the 'amazon' sheet and processed data in 'Table1' (which is identical to 'Table1_1 (2)' and 'Table1_1 (3)'). The 'PIVOT' sheet contains pre-aggregated data.

### Key Data Points from 'amazon' sheet:
- `product_id`: Unique identifier for each product.
- `product_name`: Name of the product.
- `category`: Product category (hierarchical).
- `discounted_price`: Price after discount.
- `actual_price`: Original price.
- `discount_percentage`: Percentage discount applied.
- `rating`: Product rating.
- `rating_count`: Number of ratings received.
- `review_id`, `review_title`, `review_content`: Details about product reviews.

### Key Data Points from 'Table1' sheet:
This sheet contains similar data to 'amazon' but with additional processed columns:
- `Product Category`: Cleaned product category.
- `Potential Revenue`: Estimated revenue (discounted_price * rating_count).
- `High Discount`: Indicates if the product has a high discount.
- `Price Range Bucket`: Categorization of products by price range.
- `Low Review`: Indicates if the product has a low number of reviews.

## Analysis and Key Findings

### 1. Product Category Analysis

#### Top Categories by Product Count:




The following chart illustrates the top 10 product categories based on the number of products available:

![Top 10 Product Categories by Number of Products](https://private-us-east-1.manuscdn.com/sessionFile/ju4guX9jLphVhT7uWPhKGT/sandbox/qbg14CB08SXRf5rVusZpzg-images_1753136789607_na1fn_L2hvbWUvdWJ1bnR1L3RvcF9jYXRlZ29yaWVzX2J5X3Byb2R1Y3RfY291bnQ.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvanU0Z3VYOWpMcGhWaFQ3dVdQaEtHVC9zYW5kYm94L3FiZzE0Q0IwOFNYUmY1clZ1c1pwemctaW1hZ2VzXzE3NTMxMzY3ODk2MDdfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzUnZjRjlqWVhSbFoyOXlhV1Z6WDJKNVgzQnliMlIxWTNSZlkyOTFiblEucG5nIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzk4NzYxNjAwfX19XX0_&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=GX7Pw~M1nph3LQ2HxaRvyKLiV2HRkuQ3qHxb7BFz0yklz40pvfA-7zjwxipssFzuR6L8eEBTVUA6-qmBIVULv9qpP0xKo9MYah9VwjoAagGKDdv7DjdsA7QRDoRhWhHk2YL7vfVTX4sQFC8lnV~Q7nNlsEHbyTyicjJ8~M1RxTRKboJoAvVp1zV3p6tTpCuJTk36WwBmuYWhNC~slHDx299PJwirEVG5s~DwMzAr9qn70b5ZFxgrvsEaZD9molGVcJQGDM5hnFtvVGLUa~~ywMxXELQGzbr6Ol7C01ZcXc4-kudSgBOkkBrJ~UUzVwRsEruhlNqFMqm1-Em7VS9U2g__)

### 2. Pricing and Discount Analysis

- **Average Discount Percentage**: 47.26%
- **Median Discount Percentage**: 50.00%
- **Maximum Discount Percentage**: 94.00%

#### Discount Distribution:

![Distribution of Discount Percentages](https://private-us-east-1.manuscdn.com/sessionFile/ju4guX9jLphVhT7uWPhKGT/sandbox/qbg14CB08SXRf5rVusZpzg-images_1753136789609_na1fn_L2hvbWUvdWJ1bnR1L2Rpc2NvdW50X3BlcmNlbnRhZ2VfZGlzdHJpYnV0aW9u.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvanU0Z3VYOWpMcGhWaFQ3dVdQaEtHVC9zYW5kYm94L3FiZzE0Q0IwOFNYUmY1clZ1c1pwemctaW1hZ2VzXzE3NTMxMzY3ODk2MDlfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwyUnBjMk52ZFc1MFgzQmxjbU5sYm5SaFoyVmZaR2x6ZEhKcFluVjBhVzl1LnBuZyIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTc5ODc2MTYwMH19fV19&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=pmXJShFYiIrCJ45STjLSIAV89IqL56rPE8UHc3Uo7MkLH~bJ4upogM1M65RsdYrrZhfCDzJ-f~zo4m9dvs7BReiMNtEC7-JBdsBLSVfWrmFY6TQSYU1QeKQ5719Xs4gSEmDq3hngv4efv6G0eCVI3YHYkJmITKoYcWbp5e4bsIc89MnKOxyShxyxNoBqMBjHfdFsvJNVzYaC1DPFmy0c-Gsgych-JZtP43A2PdeVyR8uTFT3cQMJqBvAaPXu47hHB~2wrHqb71J63Ll49TOL8jlV8gn3jC5BjgfZj8fHGgwGkcYtFHXkl9PqCQ5d0OuG6a~pEMB~bLPsquNj5KHCIQ__)

This histogram shows that a significant portion of products fall within the 40-60% discount range.

### 3. Rating Analysis

- **Average Rating**: 4.09
- **Median Rating**: 4.10

#### Rating Distribution:

![Distribution of Product Ratings](https://private-us-east-1.manuscdn.com/sessionFile/ju4guX9jLphVhT7uWPhKGT/sandbox/qbg14CB08SXRf5rVusZpzg-images_1753136789610_na1fn_L2hvbWUvdWJ1bnR1L3JhdGluZ19kaXN0cmlidXRpb24.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvanU0Z3VYOWpMcGhWaFQ3dVdQaEtHVC9zYW5kYm94L3FiZzE0Q0IwOFNYUmY1clZ1c1pwemctaW1hZ2VzXzE3NTMxMzY3ODk2MTBfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzSmhkR2x1WjE5a2FYTjBjbWxpZFhScGIyNC5wbmciLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=KwwXBxYB7ttWMGwcyMvZT5zLBA7-csbEsH5a1KXFL~YJl6qhWGi-uUxnayhn4aVkbLtIsSyUMcXqqAHZsKCzQMV1r2nagNnRG68Cqu1hJIJd3hg4LumDoFwEBq06eEYfs75OkOHgad6NK7fJSlcFf4OW4~Pp6t4ifZxVPA7DLXG4NeW6sKYNkP6b6fP2bkdCZfMJqLR48Jxwd0JGyP1VxbVBBgVCWuJyFcv6OOpGSjtKY6lNwR56w5CjWgR3TovAQLJXlmPihjNJlSmd1S5XLJUY-x2pUVdlvoCYe7Rsih2qVS6ZJnOIv5TaOJ7uBQoEfqP4gAv01C6Zfp-gyfuViA__)

The majority of products have ratings between 3.8 and 4.3, indicating generally positive customer feedback.

#### Discount Percentage vs. Product Rating:

![Discount Percentage vs. Product Rating](https://private-us-east-1.manuscdn.com/sessionFile/ju4guX9jLphVhT7uWPhKGT/sandbox/qbg14CB08SXRf5rVusZpzg-images_1753136789611_na1fn_L2hvbWUvdWJ1bnR1L2Rpc2NvdW50X3ZzX3JhdGluZ19zY2F0dGVycGxvdA.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvanU0Z3VYOWpMcGhWaFQ3dVdQaEtHVC9zYW5kYm94L3FiZzE0Q0IwOFNYUmY1clZ1c1pwemctaW1hZ2VzXzE3NTMxMzY3ODk2MTFfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwyUnBjMk52ZFc1MFgzWnpYM0poZEdsdVoxOXpZMkYwZEdWeWNHeHZkQS5wbmciLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=nHF5Faw5Uo29Sxk9xtyRpRN19vJUQmC-tHsTXwC4UEJUMunqw3BnOuBvsapw6HJRCXJ~77h-MNjUUiz7fTTUBx7ngbmrwVwZfccElW8vuMusu0rLPePox~JQe1-06eIGDf3JooCwHV4xjXiIWZntwMuMgDJ9Fzp2E6fSbxfoAMn5598X0kWsbzl~NMMJKxb3LbnlzACQp9p9c5B2ALpED739sgmTbfwlVyM4bKCm2In0FVxgp1gEd5XlzxmKIWlx3b3V1YJS4Uyfq5LBMsoDoLgiYN1YqIap9sZ91fDEVLjw4DRxuvInE~y2QTTy8YunS0uo0JA242X0olPuPTlcpw__)

This scatter plot shows the relationship between discount percentage and product rating. There doesn't appear to be a strong linear correlation, suggesting that higher discounts don't necessarily lead to lower or higher ratings.

### 4. High-Value Products

#### Top 5 Most Expensive Products:

| Product Name | Category | Discounted Price | Rating |
|---|---|---|---|
| Sony Bravia 164 cm (65 inches) 4K Ultra HD Sma... | Electronics|HomeTheater,TV&Video|Televisions|SmartTelevisions | 77990.0 | 4.7 |
| OnePlus 163.8 cm (65 inches) U Series 4K LED S... | Electronics|HomeTheater,TV&Video|Televisions|SmartTelevisions | 61999.0 | 4.1 |
| VU 164 cm (65 inches) The GloLED Series 4K Sma... | Electronics|HomeTheater,TV&Video|Televisions|SmartTelevisions | 54999.0 | 4.3 |
| Samsung 138 cm (55 inches) Crystal 4K Neo Seri... | Electronics|HomeTheater,TV&Video|Televisions|SmartTelevisions | 47990.0 | 4.3 |
| LG 139 cm (55 inches) 4K Ultra HD Smart LED TV... | Electronics|HomeTheater,TV&Video|Televisions|SmartTelevisions | 47990.0 | 4.3 |

#### Top 5 Most Popular Products (by rating count):

| Product Name | Category | Rating Count | Rating | Discounted Price |
|---|---|---|---|---|
| AmazonBasics Flexible Premium HDMI Cable (Blac... | Computers&Accessories|Accessories&Peripherals|Cables&Accessories|Cables|USBCables | 426973.0 | 4.2 | 219.0 |
| Amazon Basics High-Speed HDMI Cable, 6 Feet - ... | Computers&Accessories|Accessories&Peripherals|Cables&Accessories|Cables|USBCables | 426973.0 | 4.2 | 309.0 |
| Amazon Basics High-Speed HDMI Cable, 6 Feet (2... | Computers&Accessories|Accessories&Peripherals|Cables&Accessories|Cables|USBCables | 426973.0 | 4.2 | 309.0 |
| AmazonBasics Flexible Premium HDMI Cable (Blac... | Computers&Accessories|Accessories&Peripherals|Cables&Accessories|Cables|USBCables | 426973.0 | 4.2 | 219.0 |
| boAt Bassheads 100 in Ear Wired Earphones with... | Electronics|Headphones,Earbuds&Accessories|Headphones|In-Ear | 345188.0 | 4.2 | 349.0 |

### 5. Revenue Potential Analysis

#### Top 10 Categories by Potential Revenue:

![Top 10 Categories by Potential Revenue](https://private-us-east-1.manuscdn.com/sessionFile/ju4guX9jLphVhT7uWPhKGT/sandbox/qbg14CB08SXRf5rVusZpzg-images_1753136789612_na1fn_L2hvbWUvdWJ1bnR1L3RvcF9jYXRlZ29yaWVzX2J5X3JldmVudWU.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvanU0Z3VYOWpMcGhWaFQ3dVdQaEtHVC9zYW5kYm94L3FiZzE0Q0IwOFNYUmY1clZ1c1pwemctaW1hZ2VzXzE3NTMxMzY3ODk2MTJfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzUnZjRjlqWVhSbFoyOXlhV1Z6WDJKNVgzSmxkbVZ1ZFdVLnBuZyIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTc5ODc2MTYwMH19fV19&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=VXnIFg7b7K6IyJqnZ1RvGtqK4bni92-29KA460PvnCpmuhYTOPAsvnBqkx7tNl-BprTytZGyhl2g~0fQxnB55kEbvuU~ynnCnX3Hro63WCLMMB1I-BjLL2kv9qjwWRkGzzSbf7EM-3HdiofD7DSeYgeoQhIBvOGa07yqM7VMbaTNSoLMnt7pMQy6T~eqlMUVDI7CcO7NT13vEzVSYEpE~bTWzEV14SaUTNpvTUqCKWkBty6jGD825VjDAD3Nn8phFwroAOQJJ1JXkhpfjun6peR8yVNXdoR15ZpiH86w1GqmUTb2gft2-d~2vKhsUUa4QM5sOnBB6qFvG6qFYbJhJg__)

Electronics categories, particularly "Mobiles&Accessories" and "HomeTheater,TV&Video", show the highest potential revenue, indicating strong market demand and high-value products within these segments.

### 6. Insights from PIVOT Sheet

The PIVOT sheet contains several pre-aggregated tables. Key insights extracted include:

- **Average Discount Percentage by Product Category**: This table provides a quick overview of discount strategies across different product categories.
- **Products with the Highest Average Ratings**: Identifies top-rated products, which can be valuable for marketing and product promotion.
- **Average Actual Price vs Discounted Price per Category**: Useful for understanding pricing strategies and the impact of discounts at a category level.
- **Products with 50% Discount or More**: Highlights products with aggressive pricing, potentially for clearance or promotional campaigns.
- **Distribution of Product Rating**: Provides a detailed breakdown of how ratings are distributed.
- **Total Potential Revenue by Category**: Confirms the high-revenue categories identified in our analysis.
- **Rating Relation to Level of Discount**: Further explores the relationship between discounts and ratings.
- **Product with the Highest Discounts**: Lists individual products with the largest discounts.
- **Top 5 Products in Terms of Rating & Number of Reviews Combined**: Identifies products that are both highly rated and popular.

## Conclusion

This analysis provides a comprehensive overview of the Amazon product data, highlighting key trends in pricing, discounts, ratings, and revenue potential. The insights can be used to optimize pricing strategies, identify popular and high-value products, and understand customer sentiment. Further deep-dives into specific categories or product segments could yield more granular insights.

