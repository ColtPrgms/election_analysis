# **Election_Analysis**
## *Challenge 3 bootcamp - election_analysis*

#### **Overview**
    The goal of this analysis was to aduit the recent election using the voter data provided.

#### **Results**
##### *Total  Votes*
    The Total amount of votes for the election provided in the data is 369,711

##### *Vote Percentages*
    The percentages of votes from each of the colonies are as follows:
> County Votes:
> > Jefferson: 10.5% (38,855)
> > Denver: 82.8% (306,055)
> > Arapahoe: 6.7% (24,801)

    These Amounts where found by the following block of code:
'''
    county_percentage = float(votes_by_county) / float(total_votes) * 100
    county_results = (
        f"{county_name}: {county_percentage:.1f}% ({votes_by_county:,})")
'''

##### *Largest County*
    From the county percentage data, it is shown that Denver had the largest turnout of voters for the election. 

##### *Candidate Vote Breakdown*
    The percentage and total number of vote per each candidate are as follows:
>Charles Casper Stockham: 23.0% (85,213)
>Diana DeGette: 73.8% (272,892)
>Raymon Anthony Doane: 3.1% (11,606)

    These amounts where found by the following block of code:
'''
    votes = candidate_votes.get(candidate_name)
    vote_percentage = float(votes) / float(total_votes) * 100
    candidate_results = (
        f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")
'''
##### *Election Winner*
    From the Candidate percentage data, it is shown that Diana DeGette won the popular vote by over 50% (187,679 votes) more of the runner-up. 

#### **Future Usage**
    This script has been created with future proofing in mind. Meaning that as long as the voter data is in the dame format, this script can provide the total votes, percentages, and winners for county and candidate for any election. If this script was expanded to larger scopes, such as state or federal level, it would still provided results but would have to be modified to make the out easy to understand given the large changes. 
