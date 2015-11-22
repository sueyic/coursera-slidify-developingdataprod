---
title       : App to predict apartment price & size
subtitle    : using craigslist data
author      : Sue Chew
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
url:
  assets: ../../assets
---

## Shiny app to predict apartment price ($) and size (sqft)

<img src="assets/img/app_screenshot.png">

Link to app: [https://sueyic.shinyapps.io/shinyapp_apartment_pricesize_predictor](https://sueyic.shinyapps.io/shinyapp_apartment_pricesize_predictor)

---
## Data for models comes from craigslist

The prediction model was trained from craigslist posts obtained from the "apts/housing" category, for several cities in the United States. These are posts of residential apartments or housing for rent.

Example: "apts/housing" category for San Francisco bay area

<img src="assets/img/craigslist.png">

---

## How does it work?

1. Most recent 100 craigslist "apts/housing" posts from each of 8 US cities were downloaded.
2. Data includes city, title, price, the number of bedrooms (optional), and square feet (optional).
3. This data was used to train two linear models.
    - price ~ city + bedrooms
    - sqft ~ city + bedrooms
3. Shiny app was built to allow a user to input a given city and desired of bedrooms; which uses the models to return a predicted price and size of apartment.

More detailed writeup: [Data processing report](https://github.com/sueyic/shinyapp-craigslist-housing/blob/master/data_processing/data_processing_report.pdf)

--- &twocol

## Exploratory plots

*** =left

![plot of chunk unnamed-chunk-1](assets/fig/unnamed-chunk-1-1.png) 

*** =right
![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png) 

---

## Conclusion

- Code available at [github.com/sueyic/shinyapp-craigslist-housing](https://github.com/sueyic/shinyapp-craigslist-housing)
- Looking forward to feedback!
