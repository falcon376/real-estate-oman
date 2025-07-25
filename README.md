# 🏠 Dubizzle and Bayuti Oman Property

A Python web scraper that extracts real estate listings from [Dubizzle Oman - Properties for Sale](https://www.dubizzle.com.om/en/properties/properties-for-sale/) and saves them into a structured CSV file.# 🏢 Bayut Oman Property Scraper

This Python script also scrapes property listings from [Bayut Oman - Properties for Sale](https://www.bayut.om/en/oman/properties-for-sale/) and saves structured data into a CSV file for analysis or modeling.

---

## ✅ Features

- Extracts detailed fields for each listing:
  - `title`, `price`, `location`, `size_sqm`
  - `bedrooms`, `bathrooms`, `listing_type`, `listing_id`
  - `property_type`, `purpose`, `furnishing`, `link`
- Handles pagination with configurable delays
- Modular and well-structured code
- Saves output to `bayut_properties.csv`

---

## 📦 Output Format

Each row in the output CSV will include the following:



---

## ✅ Features

- Scrapes structured fields:
  - `title`, `price`, `location`, `size_sqm`
  - `bedrooms`, `bathrooms`, `furnishing`
  - `property_type`, `purpose`, `listing_id`, `listing_type`, `link`
- Handles multiple pages with delay for safety
- Saves clean tabular data into `dubizzle_properties.csv`

---

## 🔧 Preprocessing Summary

After scraping the raw data from Bayut, several preprocessing steps were applied to make the dataset clean, consistent, and ready for analysis or modeling.

### ✅ Steps Performed

1. **Price Cleaning**  
   The price values like `"OMR 90,000"` were cleaned by removing the currency symbol and commas, converting them to floats:
   ```python
   df["price_omr"] = df["price"].str.replace("OMR", "").str.replace(",", "").astype(float)


