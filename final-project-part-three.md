| [home page](https://bfriedel.github.io/portfolio/) | [visualizing debt](https://bfriedel.github.io/portfolio/visualizing-government-debt) | [critique by design](https://bfriedel.github.io/portfolio/critique-by-design) | [final project I](https://bfriedel.github.io/portfolio/final-project-part-one) | [final project II](https://bfriedel.github.io/portfolio/final-project-part-two) | [final project III](https://bfriedel.github.io/portfolio/final-project-part-three)

# Final Project Part 3: Congressional Stock Trading

 My final data story can be found on [Shorthand](https://carnegiemellon.shorthandstories.com/congressional-stock-trading/).

## Final Design Decisions and Changes Made Since Part II

Since Part 2, I have implemented several changes to the content. Notably, I removed the section attempting to illustrate the challenges the SEC faces in investigating individual trades. Instead, I replaced it with a timeline that details the allegations and investigations related to COVID insider trading. The reason for this alteration is that, upon analyzing the data, I realized that identifying potentially suspicious trades wasn't particularly difficult. However, it's crucial to note that the SEC initiates investigations only in response to specific complaints. Therefore, it didn't seem logical to assert that "they don't investigate because there are too many trades to review." While it is true that investigating every trade would be a substantial undertaking, their decision is fundamentally based on policy.

I also added the part about only one Congress Person being investigated since the STOCK Act was passed, as I was explaining this vocally anyway. I added the section on how many trades are not reported within 45 days to highlight how easy it is for Congress Members to not follow the rules. This information was derived from the date of the transaction and date reported. I found an additional source stating that there is no record of anyone facing a penalty for breaking the rule and included this for context. 

I have now clearly defined what I meant by "questionable trades," referring to trades which could be considered a conflict of interest based on the Committees that the Representative is on. I was somewhat loose with this term in both parts 1 and 2 and wanted to ensure that there is no confusion. I am not calling out these Members of Congress but drawing attention to the broken system in place.

I have also added sources to each visual, as suggested in my Part 2 feedback. The only visual I could not do this with was the Infogram since you have to have an upgraded account to embed hyperlinks into those graphics. I included those sources at the very bottom of the page.

For the visual design, I decided to go with a dark background and dark photos since this topic promotes distrust. I used one light-colored photo in my call to action to represent some kind of hope that we, as voters, do have some say.

In response to feedback regarding the red/blue motif potentially being confusing due to its association with political parties, I changed the colors in the context of the 45-day window and the chart showing trades by Congressperson. For these graphics, I opted for red and gray to emphasize key aspects in red. I have chosen to stick with these colors in the context of representing members who trade because they also are the colors on the US flag, and we are discussing the US government. Gray is used to represent Members who have not reported any trades over $1,000 since they are not involved in the analysis but should still be noted. Because I never use these colors in the context of political parties, it should be less confusing for the viewer.

Lastly, I made sure to make the topic more introductory, which I will discuss further in the next section.

### The Audience

My original audience was anyone above the age of 16 in the United States. As I was completing the final portion of this project, I narrowed down my audience to those over the age of 16 who are not well-informed on the topic of Congressional insider trading. As I was completing my interviews, one was with someone who is well-informed on the topic, one with someone who had briefly heard of the topic through news headlines but had never read up on it in full, and one was with someone who had no exposure to the topic. I found that going through the page with someone who knew a lot about the topic led to a lot of requests for deeper and more detailed information, and while I am also interested in the more detailed analysis, I realized my intention was to educate people on the issue.

In order to make this content more accessible, I refined my intro to make it more less detailed and a real introduction to the topic, assuming the audience did not know anything. I also refined the section on how the SEC has a hard time prosecuting insider trading crimes without a confession in order to make it clear that the only way to stop it would be to ban this act altogether.

### References

All of my references are included as embedded links on my Shorthand page.

## Final thoughts

This project was incredibly interesting to me, and every time I delved deeper into a facet of it, I felt like I learned something new. I had to restrain myself from delving further into individual Congress Members or Committees and remind myself that the point of the project was to present an introduction to the topic. I have received a lot of feedback that it is funny or weird that the way to fix the broken system is to plead to those that are taking advantage of a broken system and I completely agree with this sentiment, but besides calling attention to the issue and educating people on the topic, there are not really any alternatives.

It should be noted, that by flagging trades based on Committee assignment, is does leave out some analysis as there are members, like Nancy Pelosi and Kevin McCarthy, who do not sit on any Committees but still have access to a lot of information as the ranking person in their respective house. 

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

