| [home page]() | [visualizing debt]() | [critique by design]() | [final project I]() |

# Outline
In 2012, Congress passed the Stop Trading on Congressional Knowledge (STOCK) Act, which required that members of Congress report stock trades made by themselves or family within 45 days of the trade. This act was designed to combat insider trading following heavy volumes of trades made by members of congress. In the 10+ years since this Act has passed, it has widely been considered a failed effort. https://campaignlegal.org/update/stock-act-failed-effort-stop-insider-trading-congress

I am interested in showing how Congress People's stock trades could potentially conflict with the committees that they are on. For around two years on Tik Tok, some creators have established their platform on the basis of tracking Congress peoples' stock trades and highlighting certain trades and bills that could potentially be conflicts of interest. https://www.npr.org/2021/09/21/1039313011/tiktokers-are-trading-stocks-by-watching-what-members-of-congress-do
Last year, the New York Times did an analysis on all trades within and found 97 members of Congress that have made potentially conflicting trades based on the committees that they are on (https://www.nytimes.com/interactive/2022/09/13/us/politics/congress-stock-trading-investigation.html#:~:text=Stock%20Trades%20Reported%20by%20Nearly%20a%20Fifth%20of%20Congress%20Show%20Possible%20Conflicts,-By%20Kate%20Kelly&text=A%20New%20York%20Times%20analysis,by%20their%20legislative%20committee%20work.). Since that article was published, there have been 3 separate bills proposed to limit stock trading by members of congress, 2 of which have been shut down. The last one was proposed recently and will make it to the floor for voting within ____. 
Amid record low trust in the American government (https://www.pewresearch.org/politics/2023/09/19/americans-dismal-views-of-the-nations-politics/, https://www.pewresearch.org/politics/2023/09/19/public-trust-in-government-1958-2023/) it is important that we have more faith in our representatives. My call to action will be to urge people to call their congress people and express their support for the bill to stop Congress people from using insider information to increase theor own gains. 

Project Structure:


> A project structure that outlines the major elements of your story.  Your Good Charts text talks about story structure in Chapter 8 - you should describe what you hope to achieve.  Make sure the outline is detailed enough that we can see how you anticipate your story unfolding.  You can incorporate your Story Arc from the in-class exercise along with your user stories and one sentence summary to make the topic even more clear. 

- Introduction to stocks and insider trading
- STOCK Act requirements
- Why the act has failed (it's hard to prove insider trading)
- view trades values
- view which members have made potentially conflicting trades
- view the values of these trades
- congress stock performance versus american people stock performance (especially during COVID)


## Initial sketches
> Post images of your anticipated data visualizations (sketches are fine). They should mimic aspects of your outline, and include elements of your story.  

Text here...

# The data
> A couple of paragraphs that document your data source(s), and an explanation of how you plan on using your data. 

Because the STOCK Act requires disclosure of trades, the data is publically accessible through the SEC. Many different websites have built their platforms off of scraping this publicly accessible information so the data is easily accessible in many different places. I plan on using two main sources, Capitol Trades and Quiver Quantitative https://www.quiverquant.com/congresstrading/, which report the same data except Quiver Quantitative reports the performance of the stock since the purchase or sale, and Capitol Trades also has information on the committees the congress people are on. I also have access to an API on congress committees from 
I am planning to scrape the information I need, or I could do a free trial of the Quiver Quantitvative site to download the transactions. 


> A link to the publicly-accessible datasets you plan on using, or a link to a copy of the data you've uploaded to your Github repository, Box account or other publicly-accessible location. Using a datasource that is already publicly accessible is highly encouraged.  If you anticipate using a data source other than something that would be publicly available please talk to me first.
> 

| Name | URL | Description |
|------|-----|-------------|
| Capitol Trades | https://www.capitoltrades.com/trades | politician, trade issuer, traded, reported, filed after, type of trade, size of trade |
| Quiver Quantitative     | https://www.quiverquant.com/congresstrading/    |  table of politician, stock, transaction type, date of file, data of trade, and performance of the stock since purchase |
|   Market Beat   |  https://www.marketbeat.com/congress-stock-trades/#following-congress-stock-trades   |   Stock company, current price, member of congress, trade data, date filed, date traded, price after trade          |
| ProPublica | https://www.propublica.org/datastore/api/propublica-congress-api | API to get committees by member of congress |
| Open Secrets | https://www.opensecrets.org/open-data/api-documentation | many different APIs to get information on different committees |
|  Benzinga    |  https://www.benzinga.com/news/23/03/31521439/conflict-of-interest-congress-members-who-own-meta-goog-snap-shares-could-benefit-from-tiktok-ban   |   anecdotal evidence of stock trading gone wrong  |
| Smart Insider | https://www.smartinsider.com/politicians/  | politician, congress, stock, type of transaction, date of transaction, trade value range |

# Method and medium
I plan to complete this project using Shorthand and using Tableau and/or Flourish in order to complete any visualizations. 
