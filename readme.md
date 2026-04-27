# Irish Home Cookbook — FastSpring Integration

A single-page product landing page for a digital cookbook, integrated with FastSpring's Store Builder Library (SBL) for localised pricing and popup checkout.

## Overview

The page displays product details (name, price, image) pulled dynamically from FastSpring via SBL data attributes. Clicking **Buy Now** opens FastSpring's popup checkout. Price and currency are auto-localised based on the visitor's location (EUR for Ireland/Europe, USD for US, GBP for UK, etc.).

**Stack:** HTML, CSS, vanilla JavaScript, FastSpring SBL v1.0.7

**FastSpring product ID:** `irish-home-cookbook`  
**Storefront:** `testtariq.test.onfastspring.com/popup-testtariq`

## How It Works

1. The FastSpring SBL script loads and fires the `afterMarkup` callback.
2. `afterMarkup` calls `fastspring.builder.add("irish-home-cookbook")` to register the product in the session.
3. SBL populates all `data-fsc-item-*` elements with live product data (price, name, image).
4. The Buy Now button calls `fastspring.builder.checkout()` to open the popup checkout.

## Running the Page

### Option A — GitHub Pages (no setup required)

https://tariqh19.github.io/fastspringcheckout/

### Option B — Run Locally

Download the index.html and run the file using the live server built in to vscode

## Test Card Details

Use these in the FastSpring popup checkout to simulate a purchase without real charges.

| Field       | Value                  |
| ----------- | ---------------------- |
| Card Number | `4242 4242 4242 4242`  |
| Expiry      | Any future date        |
| CVV         | \*65WU                 |
| Name        | Any name               |
| Billing Zip | Any valid zip/postcode |
