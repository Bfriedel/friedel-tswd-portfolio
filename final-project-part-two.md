| [home page](https://bfriedel.github.io/portfolio/) | [visualizing debt](https://bfriedel.github.io/portfolio/visualizing-government-debt) | [critique by design](https://bfriedel.github.io/portfolio/critique-by-design) | [final project I](https://bfriedel.github.io/portfolio/final-project-part-one) | [final project II](https://bfriedel.github.io/portfolio/final-project-part-two) | [final project III](https://bfriedel.github.io/portfolio/final-project-part-three)

# Final Project Part 2

## Wireframe

You can view my wireframed story on [Shorthand](https://preview.shorthand.com/lRTrIqEY1pAI1Q4h).

## User research 

### Target audience

My target audience is anyone above the age of 16 in the United States. This includes people of voting age ans well as those who will be of voting age within two years as these are the people who will be able to influence their Congress People and who the Congress People should be representative of. If they are informed of possible corruption happening at the highest levels, they will be eager to see change (hopefully) and elect out anyone who does not prepresent their views and values. 

I will choose people who range from well-informed to not informed on the topic of insider trading and who are all registered voters. 

### Interview script

| Goal | Questions to Ask |
|------|------------------|
| Understand baseline knowledge of interviewee | Do you have any prior knowledge of insider trading? |
| Figure out if my story, as it stands provides full context of the issue at hand.   |    Do you understand what the issue is as I am presenting it?  |
|  Find out if I have enough context for why the SEC is able to do so little in the role of enforcement.   |  Would you want to see a case study on a "bad trade" where the Congress Person was not found guilty?   |
|  Find out if I elicited any emotions with the way I told the story  |   Did this information make you feel any strong emotions? and Do you think Congress People should be allowed to trade stocks? |


### Interview findings


| Questions               | Male, late 50s | Female, mid 20s | Female, late 50s |
|-------------------------|--------------------------------|-------------|-------------|
| Do you have any prior knowledge of insider trading?| Yes, I have read a lot about this topic  | Yes, I know it's an issue but don't know many details  | No, I don't know anything about trading stocks or what Congress has to do with it  |
| Do you understand what the issue is as I am presenting it? | Yes     | Yes   |  Yes   |
| Would you want to see a case study on a "bad trade" where the Congress Person was not found guilty?  | No, I know that happens all the time | Yes, specifically I want to see the case of the COVID Vaccines since that's the one that was a hot topic within the past few years. What was done with those congress people? Were any arrests made? |  Yes    |
| Is there anything else you would want to see? | I want to know why the SEC can't do more. I would also like to see how many congress people reported similar trades. For example, if they were on the same subcommittee, did they have similar trading habits within X days of a meeting? I would also like to see if any reported similar trades and if any reported opposite trades-- was anyone in Congress losing money?   | Just a case study.  like the small to big graphic showing just how many companies are affected | Just an example of trades where the laws were not enforced  |
| Did this information make you feel any strong emotions?  | I'm just confused as to why more is not being done because we know this is happening. This seems like a missed opportunity for implementing some machine learning models. I am unhappy with the end result being that you need to call your congressman. I want to see the rules enforced | Yes, these people are corrupt   | Yes, they are corrupt  |
| Do you think Congress People should be allowed to trade stocks?  |  No, but I don't think the solution to this problem includes banning trades for their spouses and dependent children. At that point it seems that you are infringing on the rights of private citizens.  | No, they're all corrupt. | No, but they will find ways around it |



## Identified changes for Part III

| Research synthesis                       | Anticipated changes for Part III                                                |
|------------------------------------------|---------------------------------------------------------------------------------|
| Everyone, regardless of previous exposure to the topic, was ok with the amount of background information provided, but I was asked a lot of questions about why the SEC cannot enforce the rules if they know insider trading is happening | In these cases, I described the one arrest that was made within the past 10 years and that they were only able to indict the Congress Person when he confessed to the crime and I will be adding this case study to the story to add context for how hard it is to enforce. |
| Those with more exposure to the topic previously were more interested in why, given all of this data, is there not a way to screen trades better.  | I will include a section which includes how my analysis was done for transparency and so it can be recreated if need be. |
| Those with more exposure to the topic previously were interested in seeing more detailed information on "bad trades." | While I also find this interesting, the point of the story is to informa and motivate, and going into the details will lose the interest of the regular voter, so I will keep the information more general. |
|  Everyone liked the soon-to-be graphic which shows just how many companies Congress has insight into and thought that provided a lot of context for how much information there is to sift through. | I will build this out more and have it include subcommittees, which meet more often than the committee at large, and also show how many Congress People are on each committee. I am still searching for a better way to create the graphic that would show impact of one conversation in a committee meeting. I think I may use Infogram, but am not sure. |
| Everyone wants to know why laws are not enforced and want to see more examples of when they are obviously borken but not enforced | I will add some more background information but will also be adding a simple graphic right at the beginning which shows that a lot of Congress People report their transactions well outside the window of 45 days. This will be to point out that even the simplest of the rules are not followed. |
| When explaining the concepts, I used many different terms to say "insider trading" including, but not limited to: bad trades, potentially bad trades, shady transactions, potential insider trading, conflict of interest, potential conflict of interest. | This was confusing to those who had less exposure to the topic so I will make sure to choose one term, define the term I use early, and include a disclaimer that I am not accusing anyone of insider trading, just pointing out where there are potential conflicts of interest. |


## Final Thoughts

Overall, I think my story, the way I am presenting it, is doing a good job conveying the issue. Without being too alarmist, I am able to impress upon the issue at hand and make people eager to see change (although I think the topic makes that relatively easy).  

The data cleaning and processing for this project was more than I anticipated and I have a new appreciation for how much work goes into saying something is insider trading without being in the room. I am using low estimates for my data (my relational database tying committees to market industries is based solely off of the top 20 industries that contribute to Congress People on Committees. I may change this if Ii find a better way moving forward, but other than going through every bill or press release, or going through every committee's jurisdiction, and making a judgment call as to what industries were affected, I think this is the most factual way to say one committee influences one industry. It would be interesting to see how available different committee and subcommittee meeting minutes are and using a ML model to indicate which industries were affected by that meeting. 


