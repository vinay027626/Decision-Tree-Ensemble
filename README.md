# Decision-Tree-Ensemble

## Understanding the Business Problem
TalkingData is a Chinese big data company, and one of their areas of expertise is mobile advertisements.

In mobile advertisements, click fraud is a major source of losses. Click fraud is the practice of repeatedly clicking on an advertisement hosted on a website with the intention of generating revenue for the host website or draining revenue from the advertiser.

In this case, TalkingData happens to be serving the advertisers (their clients). TalkingData cover a whopping approx. 70% of the active mobile devices in China, of which 90% are potentially fraudulent (i.e. the user is actually not going to download the app after clicking).

You can imagine the amount of money they can help clients save if they are able to predict whether a given click is fraudulent (or equivalently, whether a given click will result in a download).

Their current approach to solve this problem is that they've generated a blacklist of IP addresses - those IPs which produce lots of clicks, but never install any apps. Now, they want to try some advanced techniques to predict the probability of a click being genuine/fraud.

In this problem, we will use the features associated with clicks, such as IP address, operating system, device type, time of click etc. to predict the probability of a click being fraud.

## Project on Bagging and Boosting ensemble model:
The data contains observations of about 240 million clicks, and whether a given click resulted in a download or not (1/0):

The detailed data dictionary is mentioned here:<br>
    - ```ip```: ip address of click.<br>
    - ```app```: app id for marketing.<br>
    - ```device```: device type id of user mobile phone (e.g., iphone 6 plus, iphone 7, huawei mate 7, etc.)<br>
    - ```os```: os version id of user mobile phone<br>
    - ```channel```: channel id of mobile ad publisher<br>
    - ```click_time```: timestamp of click (UTC)<br>
    - ```attributed_time```: if user download the app for after clicking an ad, this is the time of the app download<br>
    - ```is_attributed```: the target that is to be predicted, indicating the app was downloaded<br>
