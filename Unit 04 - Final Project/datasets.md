# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Final Project Datasets

## Suggested Datasets

Below, we have sourced four suggested datasets that can be used for final projects. We've also provided three additional choices, but note that these "advanced" selections are more complicated and will require a substantial amount of effort. 

All of the curated data sets described below [can be found in Sailfish through this link](https://public.sailfish.boozallen.com/exchange/nets/177085/catches).


| Dataset Suggestions | 
| --- | 
|*Suggested Datasets* |
| [Option 1: Amazon Pricing Data](#option1) |
| [Option 2: Insurance Marketplace Data](#option2) | 
| [Option 3: Instacart Order Data](#option3) | 
| [Option 4: Loan Data](#option4) | 
| *Advanced Datasets* |
| [Option 5: Fuel Economy Data](#option5) | 
| [Option 6: Craft Beer Data](#option6) | 
| [Option 7: Trump Tweet Data](#option7) | 

> Note: Alternatively, instructors may optionally allow students to choose their own final projects dataset. Students should clearly indicate this preference and discuss their choice(s) with instructors ahead of time.

---

<a name="option1"></a>
## Option 1: Amazon Pricing Data

From ProPublica:

> ProPublica reporters examined Amazon’s shopping algorithm. We scraped data from the company's website to examine listings for 250 best-selling products across a wide range of categories, from electronics to household supplies, over a period of several weeks during summer 2016. We compared pricing and shipping costs for products offered by multiple vendors, including those sold by Amazon and sellers in the "Fulfilled by Amazon" program. In total, we examined 6,973 vendor listings.

**Possible Areas to Examine**

- How does vendor affect price?
- How does rank affect an item's price? Or vice versa?

---

<a name="option2"></a>
### Option 2: Health Insurance Marketplace

From Kaggle:

> The Health Insurance Marketplace Public Use Files contain data on health and dental plans offered to individuals and small businesses through the U.S. Health Insurance Marketplace.

**Possible Areas to Examine**

- How do plan rates and benefits vary across states?
- How do plan benefits relate to plan rates?
- How do plan rates vary by age?
- How do plans vary across insurance network providers?

> Note: This data set is quite large, and taking a random 10-percent sample by state (with justification) is acceptable.

---

<a name="option3"></a>
### Option 3: Instacart Orders

Instacart open-sourced 3 million orders from its databases. We recommend you read more via its engineering blog [here](https://tech.instacart.com/3-million-instacart-orders-open-sourced-d40d29ead6f2).

**Possible Areas to Examine**

- How does time of day affect an order?
- What types of items are reordered most often?
- How many different cart sizes do there appear to be among buyers, and what meaningful differences exist in those baskets of goods?
- How does order affect when a user adds something to their cart?

> Note: This data set is quite large, and taking a random 10-percent sample (with justification) is acceptable.

---

<a name="option4"></a>
### Option 4: Loan Data

From Kaggle:

> These files contain complete loan data for all loans issued through the 2007–2015, including the current loan status (current, late, fully paid, etc.) and latest payment information. The file containing loan data through the "present" contains complete loan data for all loans issued through the previous completed calendar quarter. Additional features include credit scores, number of finance inquiries, address including zip codes and state, and collections among others. The file is a matrix of about 890,000 observations and 75 variables. A data dictionary is provided in a separate file.

**Possible Areas to Examine:**

- What factors most explain on-time loan repayments?
- As a bank, what evaluation metric would you opt for to determine if a given load should be given? As a consumer, what evaluation metric would you opt for to determine if a given loan should be given? How does this affect your model's performance?

---

## Advanced Data Sets (Optional)

These "stretch" data sets are ordered by an estimated feasibility of analysis for your final project. The reason they are considered optional is denoted for each item. Even if you are unable to complete work with one these data sets, know that additional practice will unlock the skills necessary to complete a final project on any of the following suggestions.

<a name="option5"></a>
### Option 5: Fuel Economy Data

The U.S. Environmental Protection Agency publishes miles-per-gallon data following tests of vehicles on the road in the United States. Data sets from the years 2000–2018 are readily accessible for all make and models.

**Possible Areas to Examine**

- Predict the miles per gallon of a given brand and car type.
- Create a cross-sectional look at how car efficiencies have improved over the years. Predict future miles per gallon for models, brands, or car types.
- Predict the carbon impact for a given brand or car type.

**Difficulty Assessment**

The multi-year nature of the data set may prove to be a data-wrangling challenge. Nonetheless, the overall size of the set across years makes it approachable — perhaps even more so than prior options.

> Moreover, forecasting is not explicitly covered in this portion of the course, so model selection may be a panel OLS by year or a decision tree regressor.

---

<a name="option6"></a>
### Option 6: Craft Beers

Craftcans.com maintains a continuously updated data set of (as of July 2017) 2,962 craft beers. The data contains the beer name, brewery, location, style, size, ABV, and IBUs.

**Possible Areas to Examine.**

- Predict the ABV based on other factors.
- Cross-reference this data with the [ratebeers.com API](https://www.ratebeer.com/api.asp) to predict quality of beer using the other factors provided.

**Difficulty Assessment**

The multi-year nature of the data set may prove to be a data-wrangling challenge. Nonetheless, the overall size of the set across years makes it approachable — perhaps even more so than prior options.

> Moreover, forecasting is not explicitly covered in this portion of the course, so model selection may be a panel OLS by year or a decision tree regressor.

---

<a name="option7"></a>
### Option 7: All Trump Tweets

A live-updating JSON database is available containing all of President Donald J. Trump's tweets. The data set also includes basic metadata: time tweeted, retweets, favorites, and more. It is updated hourly.

**Possible areas to examine:**

- How does specific word choice affect engagement?
- How does word choice change over time?

**Difficulty Assessment**

Natural language processing is taught relatively late in our curriculum. Thus, this data set relies on an aggressive back-loaded project schedule. Moreover, this data set is available in JSON, meaning the user will need to explore it independently  using Pandas or use the `JSON` package in Python to read it in. 

> This is a great example of data you should use to continue practicing your new skill set beyond this course.
