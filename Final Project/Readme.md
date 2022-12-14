# Predicting the return on investment of Cryptopunks with gender and skin tone factors using Ridge Regression
## Project information
- **Author**: Yutong Sun, Applied Math, Class of 2023, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to the Final Project for STATS201 Introduction to Machine Learning for Social Science, 2022 Autumn Term (Seven Week - Second) instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: I would like to express my greatest gratitude to Prof. Luyao Zhang for her inspiring supporting and instructions on STATS201 Introduction to Machine Learning for Social Science. And I would like to express my greatest gratitude to my peer Isabella Kroon for her inspiring comments on the draft poster and summary. 

## Project Summary: [Summarize the Background/Motivation, Research Questions, Application Scenario (Data Source), Results, Intellectual Merits and Practical impacts of your project.]

- **Background and Motivation:** With the development of Non-Fungible Tokens, there are many related art products created based on them, and CryptoPunks is one of them. CryptoPunks are 24x24 pixel portraits created in 2017 (An example of Cryptopunks is shown in Figure 1. “What Is CryptoPunk - Zipmex” 2022). And they were created by Larva Labs and provide their users for free (Ante 2022). Users can now trade Cryptopunks on the secondary market, and different Cryptopunks will bring different Return on Investment (ROI). The ROI of Cryptopunks is influenced by many factors, including market factors, news and the characteristics of the Cryptopunks themselves, etc (Kampakis and Schaar 2022). However, the gender and skin tone factors are not well studied yet regarding the ROI of Cryptopunks. In this research, I will explore the question: how do the gender and skin tone factors influence the prediction of the ROI of Cryptopunks?  It is important to explore the impact of different factors on the ROI of Cryptopunks. Because we need to use these factors to predict the market ROI of Cryptopunks and to make investment decisions accordingly. In addition, the gender and skin tone factors are also important for Cryptopunks' ethical issue, we also want to explore whether the difference in Cryptopunks’ gender and skin tone will influence people’s valuation of them, and whether there is discrimination regarding the gender and skin tone of Cryptopunks.


- **Research Question:** How do the gender and skin tone factors influence the prediction of the ROI of Cryptopunks?  

- **The discussion of literature under intellectual merits and practical impacts:** 
  - **Intellectual Merits:** 
  - There is much literature exploring the influence factors of Cryptopunks’ return. For example, Kong and Lin summarize some literature that analyzes the influence factor in the NFT market, and they conclude that the price and return are influenced greatly by factors like other traditional markets’ behavior, the token’s rarity, and the aesthetic of people (Kong and Lin 2021). Urom, Ndubuisi, and Guesmi use the quantile regression model to predict the Cryptopunks return with the market volume and market uncertainty risk index and other markets’ behavior as the predictor variable, and they conclude that these factors are good predictors, especially under extreme market conditions. And they also find that increasing in bitcoin market price will reduce the return of NFT market (Urom, Ndubuisi, and Guesmi 2022). Previous studies on Cryptopunks’ returns mostly focus on their relation to other markets and the cryptocurrency market. However, these papers do not analyze specific attributes like gender and skin tone’s influence on Cryptopunk return. Our research will contribute to the literature with gender and skin tone factors’ influence on Cryptopunks’ return analysis. 
  - Many machine learning models are applied to predict the price of Cryptopunks. For example, Kraeussl and Tugnetti summarize and compare the literature on predicting models of Cryptopunks’ value and discuss their application scenarios (Kraeussl and Tugnetti 2022). Kampakis and Schaar explore the influence of the rarity of the attributes of Cryptopunks’ images on Cryptopunks’ price using the hedonic regression model, and they find that the rarity of attributes of Cryptopunk has a positive influence on the price of Cryptopunks (Kampakis and Schaar 2022). And Ho et al. study the influence of the utility factor for NFT price prediction using XGBoost regression, and they find that the Crtptopunks that bring higher utility for people are valued higher (Ho et al. 2022).  However, most of these regression models are used for Cryptopunks’ price prediction, and no research predicts the return on investment (ROI) of Cryptopunks using Ridge Regression. Our research will contribute to the literature by using the Ridge model for the prediction of Cryptopunks’ return rather than price.
  - In addition, some research discusses the ethical issue of Cryptppunks. For example, Zhang et al. discuss and summarize the gender and skin tone’s influence on the difference in Cryptopunks’ price by visualization (Zhang et al. 2022). In addition, many papers apply the prediction of Cryptopunks’ price to analyze the ethical issue of Cryptopunks quantitively. For example, Loi and Tang use the Hedonic Pricing model to predict the price of Cryptopunks with many facial features like gender and “have a nose or not”, and they conclude that male Cryptopunk in general has a higher price (Loi and Tang 2022). In addition, Nguyen analyzes the influence of skin tone on the price of Cryptopunk using hedonic regression and concludes that there is some discrimination in pricing regarding the skin tone type in the Cryptopunk market (Nguyen 2022). However, no research applies prediction of Cryptopunks’ ROI to analyze the Cryptopunks’ethic issue yet. In this research, we combine two factors, skin tone and gender factors, in predicting the ROI of Cryptopunks and discussing the ethical issue. Our research combines the two factors with the previous price of Cryptopunks to predict the return. The literature structure is shown in Figure 1 in the Splotlight section.


  - **Practical Use:** Our research explores the impact of the gender and skin tone factors on the prediction ROI of Cryptopunks. And the research results could be used by investors when making investment decision in the Cryptopunks market. 


- **Application Scenario:** This project uses a [Kaggle dataset](https://www.kaggle.com/code/baotramduong/generate-nft-cryptopunks-with-dggan), and this data set is drawn from the Cryptopunks Transaction board using API (DUON 2021). The original dataset contains information about the transaction date, the transaction address, the price of Cryptopunks, the gender, and other attributes of the Cryptopunks’ image. I use the percentage change of Cryptopunk price to get the return on investment value, which is the Y variable. And gender and skin tone are X variables. In Figure 2 in the Splotlight section, I visualize the ROI time series data with the x-axis being time and the y-axis ROI values.

- **Methods:**
  - This research uses Ridge Regression to predict the ROI with gender and skin tone factors. Ridge regression is a method for estimating the coefficient of a multiple regression model. Compared to linear regression, this method improves the coefficient estimation accuracy and assigns different weights to the features (Hoerl and Kennard 1970). Using the regression formula with estimated coefficients from Ridge regression, we could conduct prediction.
In python, we could use the ridge regression function (Ridge. coef_), it will return a coefficient of each variable for the regression model. From these coefficients, we could check what’s the influence each gender and skin tone type has on the prediction of Cryptopunks’ ROI. Because gender and skin tone factors are all categorical variables, so we set them as dummy X variables that only have values of 0 or 1. Then the ridge regression formula  is:
$$y=b_{0}+b_{1}*X_{female}+b_{2}*X_{light}+b_{3}*X_{medium}+b_{4}*X_{alboni}$$

  - $b_{0}$ is the expected ROI when the Cryptopunk is in male and dark skin, and $b_{1}$ is the number of increase(or decrease) comparing to $b_{0}$ in ROI when the Cryptopunk is in female and dark skin. If the $b_{1}$ is positive number, that means female Cryptopunks are expected to return higher value for investment. Similarly, $b_{2}$ means the number of increase(or decrease) comparing to $b_{0}$ in ROI prediction when the Cryptopunk is in male and light skin. If the $b_{2}$ is positive number, that means Cryptopunks in light skin tone are expected to return higher value for investment than dark skin. Similar explanation works for $b_{3}$ and $b_{4}$.


- **Expected Results:** I expect that predict ROI should be close to the real ROI as shown in Figure 3. In Figure 3 in the Splotlight section, the x-axis is the ROI value, and the y-axis is the counts. So the overall figure shows the distribution of the predicted ROI (in green bar) and real ROI (in blue bar). The more overlapped part of the two ROI data, the more accurate our prediction is. And I also expect that the predicted ROI will be higher for female in Alboni skin tone because the number of Cryptopunks in this type is the least. Because Cryptopunks are only limited to 1000 tokens stored on Ethereum blockchain (Kong and Lin 2021). And Cryptopunks are fixed in total number so the scarceness of this type of Cryptopunks will not be changed in a short time and there is potential for this type of Cryptopunks to increase in price, and thus are expected to have higher ROI (Kampakis and Schaar 2022). The results could be used as reference for investors for picking Cryptopunks according to the gender and skin tone attributes. 


Figure 3. The expected result of the predicted ROI and the true ROI

## Table of Contents
- [data](#data)
- code
- spotlight
- More about the author
- References

## Data


| Data source   | [Kaggle Cryptopunks data](https://www.kaggle.com/code/baotramduong/generate-nft-cryptopunks-with-dggan)|[API](https://dune.com/queries/10021/19914) |
| ------------- |:-------------:| -----:|
| Query data        | [Query data](https://raw.githubusercontent.com/SunYutongAmber/portfolio/main/Final%20Project/data/final_queried_data..csv) | |
| Classification data | [Training data](https://raw.githubusercontent.com/SunYutongAmber/portfolio/main/Final%20Project/data/Final_Classification_Train.csv)      |   [Testing data](https://raw.githubusercontent.com/SunYutongAmber/portfolio/main/Final%20Project/data/Final_Classification_Test.csv) |
| Regression data    | [Training data](https://raw.githubusercontent.com/SunYutongAmber/portfolio/main/Final%20Project/data/Final_Regression_Train_Cryptopunks.csv)     |  [Testing data](https://raw.githubusercontent.com/SunYutongAmber/portfolio/main/Final%20Project/data/Final_Regression_Test_Cryptopunks.csv) |


## Code
- Query Data
- Process Data
- Analyze Data
- ...

## Spotlight

- Figures


![Figure 1. The literature of intellectual merits](https://github.com/SunYutongAmber/portfolio/blob/main/Final%20Project/Splotlight/Stats201%20Final%20Project%20Literature%20Flow%20chart.png)
Figure 1. The literature of intellectual merits

![Figure 2. The ROI time series data](https://github.com/SunYutongAmber/portfolio/blob/main/Final%20Project/Splotlight/Scatter%20Plot%20for%20ROI%20over%20time.png) 
Figure 2. The ROI time series data

![Figure 3. The expected result of the predicted ROI and the true ROI](https://github.com/SunYutongAmber/portfolio/blob/main/Final%20Project/Splotlight/Ridge%20Regression%20Predicted%20and%20True%20Value.png) 

- Posters


- Slides
- Presentations
- Review articles
- Media appearance

## References

### Data Source
- Data Source Title and URL
### Code Source
- Code Source Title and URL
### Articles
- Article Source Title and URL
### Literature
- Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

Levin, Dan, and Luyao Zhang. 2020. “Bridging Level-K to Nash Equilibrium.” *The Review of Economics and Statistics* 104 (6): 1329–40. https://doi.org/10.1162/rest_a_00990.

```
@article{levin2022bridging,
  title={Bridging level-k to nash equilibrium},
  author={Levin, Dan and Zhang, Luyao},
  journal={Review of Economics and Statistics},
  volume={104},
  number={6},
  pages={1329--1340},
  year={2022},
  publisher={MIT Press One Rogers Street, Cambridge, MA 02142-1209, USA journals-info~…}
}
```

