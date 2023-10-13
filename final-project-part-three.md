

# Congressional Stock Trading

 My final data story can be found on [Shorthand](https://carnegiemellon.shorthandstories.com/congressional-stock-trading/).

# Changes made since Part II

Since Part 2, I have made several content changes, including the removal of the section that attempted to illustrate the challenges the SEC faces in investigating individual trades. Instead, I replaced it with a timeline detailing the COVID insider trading allegations and investigations. I made this change because, as I analyzed the data, I realized that identifying potentially suspicious trades wasn't particularly difficult. However, it's important to note that the SEC initiates investigations only in response to specific complaints. Therefore, it didn't seem logical to assert that "they don't investigate because there are too many trades to review." While it is true that investigating every trade would be a substantial undertaking, their decision is fundamentally based on policy.


## The Audience

My original audience was anyone above the age of 16 in the United States. As I was completing the final portion of this project, I narrowed down my audience to those over the age of 16 who are not well-informed on the topic of Congressional insider trading. As I was completing my interviews, one was with someone who is well-informed on the topic, one with someone who had briefly heard of the topic through news headlines but had never read up on it in full, and one was with someone who had no exposure to the topic. I found that going through the page with someone who knew a lot about the topic led to a lot of requests for deeper and more detailed information, and while I am also interested in the more detailed analysis, I realized my intention was to educate people on the issue.

In order to make this content more accessible, I refined my intro to make it more less detailed and a real introduction to the topic, assuming the audience did not know anything. I also refined the section on how the SEC has a hard time prosecuting insider trading crimes without a confession in order to make it clear that the only way to stop it would be to ban this act altogether.

## Final design decisions
> You can specifically break out your design decisions here, or include it under *Changes made since Part II* and delete this section. Talk about the design decisions you had to make along the way, and reflect on anything in particular that stands out to you that you learned working through the process.  Include any other information that helps round out your data story. 

Text here!

## References

All of my references are included as embedded links on my Shorthand page.

# Final thoughts

This project was incredibly interesting to me, and every time I delved deeper into a facet of it, I felt like I learned something new. I had to restrain myself from delving further into individual Congress Members or Committees and remind myself that the point of the project was to present an introduction to the topic.

Below, I have listed the steps of my analysis, as the dataset was assembled by me through multiple different sources:

Creating the data set: 
1. Membership to [Quiver Quantitative](https://www.quiverquant.com/export/) to download Congress Member Stock Trades (earliest trade: July 25, 2014, latest trade: September 21, 2023). This data provided the date of the transaction, the date it was reported, the Representative, ticker, amount, party, house, and range of trade. During the cleaning process, I added additional columns: days to report (the number of days between the transaction and reporting), under 45 days (to create a donut chart showing how many trades were not reported within that window), and split the range into lower and upper.
2. Membership to [Stock Analysis](https://stockanalysis.com/list/) to download companies by industry. There are 11 sectors recognized by the Global Industry Classification Standard (GICS), and many industries within each sector. I downloaded the following lists from this site: Listed on NASDAQ, Listed on NYSE, All REITs, All SPACs. This list provided every ticker (symbol), the name of the company, the industry it is in, as well as the sector. I merged all of these into one dataset.
3. I got all Congress Committees rosters from [House of Representatives](https://www.house.gov/committees) and [Senate](https://www.senate.gov/committees/membership.htm) websites. One of the things that was very interesting to me is how hard the Senate and House of Representative websites are to navigate. I copy and pasted the data from the sites into [ChatGPT](https://chat.openai.com/) to format it into tables which could easily be made into Pandas DataFrames. 
4. Determining which Committees impact which sectors and industries was, by far, the most challenging part of the project, and I was initially uncertain how to approach it. I ended up examining each committee's jurisdiction to relate each committee to different industries. Since this method is subject to interpretation, I used [The New York Time's analysis](https://www.nytimes.com/interactive/2022/09/13/us/politics/congress-members-stock-trading-list.html) o refine my lists. To do this, I spot-checked a few of my committee-to-industry lists by examining what companies they had listed under which committees and ensuring that the industry was included in my list for that committee. The reason they were able to identify more in their analysis is because they worked backward in time; although it is not common for Representatives to move between committees often, it does happen. This approach also leaves room for error in my analysis, as I am examining what committees they are presently assigned to and all trades from 2019 to the present. This means that they may not have been assigned to a committee when they made a trade that falls into an industry affected by that committee. I believe I could spend a week refining these lists and still not achieve perfection, so I kept my assumptions conservative to avoid making too significant of an assumption.
5. I cleaned the data, which included splitting all name columns into Title, First, Middle, Last, and Suffix, and then joining lists based on the first and last names. It's interesting that their names could be listed differently on so many official documents and that matching up the names required so much individual refinement.
I converted the committee rosters into a dictionary (key: Committee, value: Representative) and also converted the committee-to-industry relationships into a dictionary (key: industry, value: Committees impacting that industry).
I merged the stock lists and trades DataFrames using the ticker/symbol of the stock.
I created a function that examined every row of the trades DataFrame, used the industry and the first and last name of the Representative, and examined every committee that Representative is in. If the representative is in a committee that affects the industry corresponding to the stock's ticker, the function returned 'yes'; otherwise, it returned 'no.'
Once I had a new column labeled 'questionable,' I performed various data grouping analyses to examine the trades by person, party, or house. Ultimately, I focused on the data by person while keeping the primary goal of my project in mind.

Overall, it was a lot of work to refine the data, but it yielded some interesting results. 

