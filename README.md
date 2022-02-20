# eth-denver-do-or-daont
Eth Denver Hackathon Project
<br/><br/>

### Link to pitch and prototype: 
https://www.figma.com/proto/0mehVw7XtYBGFH6l0xe1jt/DAOCheck?page-id=0%3A1&node-id=60%3A405&viewport=306%2C48%2C0.17&scaling=scale-down-width&starting-point-node-id=60%3A405
<br/><br/>

# Background
More and more people are currently getting interested in joining a DAO and also see them as a real alternative to a traditional company job.
But after various scams that already happened in the DAO world, how do people know that they can trust a DAO and if it’s even a good fit for them?
There are many questions to consider before joining a DAO:
- Is the community in this DAO active?
- Do they have a working governance?
- Is the token equally distribution?
- Are they transparent?
- Is the treassury growing?
- Is it fun to work in this DAO?
<br/><br/>


# Market Analysis
Currently, there are already tools like DeepDao out there that give insights into various DAOs. But especially for newbies, it is hard to understand what all those metrics really mean.
<br/><br/>


# Introduction to DoOrDAOn't
Therefore, to support new DAO joiners, we developed Do or DAON’t. DoOrDon't supports new DAO joiners to evaluate the transparency and decentralization of a DAO. With the help of our trust scores, they will only join DAOs that align with their values!

New joiners go to our website and look for the DAO they are interested in. The first thing they notice is our trust score:
Our trust score is built up of different metrics. The highest trust score is 100 points and the higher the score is, the more decentralized, transparent, and active is the DAO. In general, the score is calculated based on various metrics. For this MVP, we have the following categories:
<br/><br/>

# Trust Score Calculations
The priority of each metrics is based on interviews and a survey we conducted with different DAO members. 
But since we still know that our defined trust score is quite subjective, we also allow user the option to set their own preferences. After updating the preferences, the trust score then gets calculated based on those changed priorities. 

## Governance - 30 points

**Question to answer:** Are there regular proposals and do members actively vote on them?

### Avg. amount of completed proposals per month (last 6 months)
15 points = 3 or more
10 points = 2-3
5 points = 1
0 points = less than 1

### Avg. active voters per month (last 6 months)
15 points = 50%
10 points = 25-50%
5 points = 10-25%
2.5 points = 5-10%
0 points = 0-5%
<br/><br/>

## Token Distribution - 30 points

**Question to answer:** Is the token equally / properly distributed?

**Parameter:** All tokens / all token holder = equal amount of tokens for each member

### Calculation:
30 points = equal distribution (+-3% more)
25 points = 1% of members own 5-10%
20 points = 1% own 10-15%
15 points = 1% own 15-20%
10 points =1% own 20-25%
0 = 1% own 25-100%
If 1% would result in a number <1 (only 20 members), then 1% rounds up to 1.

### How can we make sure people don’t play the system, create many wallets and “fake” an equal distribution?
Wallets who hold more than 5% of tokens and do not vote regularly are a red flag
Proof of humanity: But what stops people to verify their main wallet with poh and then create various other wallets?

### Next phase:
Create different calculations depending on the size of the DAO (DAO with 1000 members has different distribution than DAO with 10k)
<br/><br/>

## Treasury - 20 points

**Question to answer:**
- Does the DAO have a legit treasury?
- Is the treasury growing and moving?

### Calculation:
>10k = 2
10-20k= 4
20-50k= 6
50-100k= 8
100-200k= 10
200-300K= 12
300-500k= 14
500k-1M= 16
>1M=18
2 extra points for diversification

### Next phase:
Where does the treasury come from? Like Crunchbase for DAOs
Where does the treasury go? Are there recurring expenses?
Does the treasury have a multi-sync wallet?
Different calculations depending on the size of the DAO
<br/><br/>

## Social Media - 10 points

**Question to answer:**
- Is the community active?
- Is the growth natural?

### Calculation:
5 points for Twitter, 5 points for Discord
over 5k followers: 5 points
2,5k-5k followers: 4 points
1k-2.5k: 3 points
500-1k: 2 points
0-500: 1 point

### Next phase: 
- Include followers, engagement, tweet frequency
<br/><br/>

## Ratings/Reviews - 10 points

**Question to answer:** Do people enjoy being part of this DAO?

### Calculation:
10 points = 5 star rating
x points = ratingsx2
→ e.g. 8.8 points for 4,4 rating

### How do we prevent scammers and liars?
Anonymous review but we verify that they hold an NFT or token from this DAO → Only NFT and token holder can create a comment.
Holders need to be holding the tokens for at least two weeks to create a comment.

### Next phase:
Token rewards for posting rating → Incentive
<br/><br/>


## Future Metrics
These are all our current metrics we can get through various apis.
But they are way more metrics and information we plan to include to improve our trust score further.

**Examples:**
- DAO structure: Who is working in this DAO and who is in the core team? Tools like Sobol.io or Discord roles
- Bounties and payouts: Dework or Utopia
- Twitter milestones: Coinfeeds 
- Furthermore we also want to include a DAO comparison page.

For us, DAOs are all about transparency and due to that it is only a matter of time until even more APIs open up and let us get their data to get even better insights. This means, the more DAO tools and DAO in general develop, the more insights people will gain through our tool. 
<br/><br/>

# Revenue Streams
### Enhanced Credibility
DAOs can contact us to conduct a in-depth check to receive a verification checkmark. This checkmark add extra points to the trust score.

### In-depth analytics
We provide in-depth analytics and reviews to support DAOs to further increase their credibility.

### Preference Data
We provide insights into anonymized user searches and preferences to help DAOs understand the members needs.
<br/><br/>

# Team
- Valerie Grappendorf (UX/UI Designer)
- Sianoi Kimari (Organizational Development & Leadership Researcher)
- Mayur Mistry (Applications Developer & Design Technologist)
