# Project information
With the development of Non-Fungible Token, there are many related arts products created based on it, and CryptoPunks is one of the them [(Ante 2022)](https://www.tandfonline.com/doi/abs/10.1080/10438599.2022.2119564). [CryptoPunks](https://www.coindesk.com/learn/cryptopunks-cryptocats-and-cryptokitties-how-they-started-and-how-theyre-going/) are 24x24 pixel portraits that were originally offered by Larva Labs for free in June 2017. 

In this project, I aim to use the previous Cryptopunks price to predict the future price. 
In part I, I firstly visulize the data for explaination.
For Part II, I query Cryptopunks transaction data from [Kaggle](https://www.kaggle.com/code/baotramduong/generate-nft-cryptopunks-with-dggan). This data set contains information about the transaction date, transaction price, transfer address, and the type of Cryptopunks. transaction price (eth) is set as Y variable, and the shift version of Y is set as X variable. I use X to classify and predict Y.

# Table of Content (Data, Code, and Image)


| Tables        | Part I Explaination           | Part II Prediction and Classification   |
| ------------- |:-------------:| -----:|
| code        | [code for explaination](https://github.com/SunYutongAmber/portfolio/blob/main/Problem_set2/code/Explanatory_Cryptopunks_Data_Analysis.ipynb) | [code for query data](https://github.com/SunYutongAmber/portfolio/blob/main/Problem_set2/code/Query_CryptoPunks_Data_yutong_sun.ipynb),[code for process data](https://github.com/SunYutongAmber/portfolio/blob/main/Problem_set2/code/Process_Cryptopunk_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb),[code for prediction and classification](https://github.com/SunYutongAmber/portfolio/blob/main/Problem_set2/code/Analyze_Cryptopunks_Data_Machine_Learning_for_Predicting_Market_Congestion.ipynb) |
| data        | [data for Part I](https://github.com/SunYutongAmber/portfolio/blob/main/Problem_set2/data/queried_cryptopunks_data.csv)      |   [data for Part II](https://github.com/SunYutongAmber/portfolio/tree/main/Problem_set2/data) |
| image      | [explaination image for Part I](https://github.com/SunYutongAmber/portfolio/blob/main/Problem_set2/image/Histogram_Contour%20plot%20for%20Cryptopunks%20average%20price.png)     |  [Confusion matrix and ROC curve for Part II](https://github.com/SunYutongAmber/portfolio/tree/main/Problem_set2/image) |


# Splotlight for Explainatory Part:
For this part, I create a histogram contour map for the Time series cryptopunks price data. The graph is shown below:
![image](https://github.com/SunYutongAmber/portfolio/blob/main/Problem_set2/image/Histogram_Contour%20plot%20for%20Cryptopunks%20average%20price.png). The darker the section means the higher transaction price for Cryptopunks, and from this graph, we would say that the overall trend for the histogram is increasing overtime, and the highest price is achieved in Oct 2021 (the max date in the date set is Oct 2021). I also graw the histogram to visulaize the distribution of transaction data of Cryptopunks, and it is skewed to the right, which means that there are many extreme large value of some cryptopunks. ![image](https://github.com/SunYutongAmber/portfolio/blob/main/Problem_set2/image/distribution%20of%20price.png)


# Splotlight for Classification and Prediction Part:
For classidication, I use Neural network models (supervised) to classify the price data. Here is the matrix: !{image](https://github.com/SunYutongAmber/portfolio/blob/main/Problem_set2/image/confusion%20matrix%20for%20classification.png)
This matirx shows that there are 63 False Negtive and 268 True Negtive. That means the neural network model does not perform well, because all results are predicted as negtive, but there are only 80.97% are predicted correctly.


# References:
DUON, BAO TRAM. (2021). Generate NFT CryptoPunks with DGGAN. Kaggle.com. Retrieved from 
https://www.kaggle.com/code/baotramduong/generate-nft-cryptopunks-with-dggan.
Marcobello, Mason. (2022). CryptoPunks, CryptoCats and CryptoKitties: How They Started and How They’re Going. Www.coindesk.com. March 17, 2022. Retrieved from https://www.coindesk.com/learn/cryptopunks-cryptocats-and-cryptokitties-how-they-started-and-how-theyre-going/.
Zhang, L. (Sunshine). (2022). Machine Learning for Predictions. Machine Learning for Social
Science. Retrieved from https://ms.pubpub.org/pub/ml-prediction
Zhang, L. (Sunshine). (2022). Venues for Computer Security and Beyond. Machine Learning for
Social Science. Retrieved from https://ms.pubpub.org/pub/security
Zhang, L. (Sunshine). (2022). Venues for Machine Learning&nbsp; Machine Learning for
Social Science. Retrieved from https://ms.pubpub.org/pub/ml
Zhang, L. (Sunshine). (2022). Computing Platforms: Set up the Workspace for Machine
Learning Projects. Machine Learning for Social Science. Retrieved from
https://ms.pubpub.org/pub/computing
Zhang, L. (Sunshine). (2022). Resources for Blockchain Network Studies. Machine Learning for
Social Science. Retrieved from https://ms.pubpub.org/pub/network
Instructions for GitHub Readme:
https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatt
ing-on-github/basic-writing-and-formatting-syntax
Sample Code for Prediction:
https://github.com/Rising-Stars-by-Sunshine/stats201-tutorial-prediction
