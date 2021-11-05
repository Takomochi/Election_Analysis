# Election_Analysis

## Project Overview
A Colorado Board of Elections employee has given me the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

## Resources
- Data Source: [election_results.csv](https://github.com/Takomochi/Election_Analysis/blob/main/Resources/election_results.csv)
- Software: Python 3.8.12, Visual Studio Code

## Summary
The analysis of the election show that:
- There were 369,711 votes cast in the election.

- The candidates were:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane
    
- The candidate results were:
    - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
    - Diana DeGette received 73.8% of the vote and 272,892 number of votes.
    - Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.
    
- The winner of the election was:
    - Diana DeGette, who received 73.8% of the vote and 272,892 number of votes.

## Challenge Overview
### Purpose
The purpose of this analysis is to show some additional data. The election commission requested to find out the voter turnout for each county, the percentage of votes from each county and the county with the highest turnout.

## Challenge Results
### Analysis

[Election results - election_analysis.txt](https://github.com/Takomochi/Election_Analysis/blob/main/analysis/election_analysis.txt)
- How many votes were cast in this congressional election?
    - Total 369,711 votes were cast in the election.
    
- Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.
    - Jefferson: 10.5% (38,855)
    - Denver: 82.8% (306,055)
    - Arapahoe: 6.7% (24,801)
    
- Which county had the largest number of votes?
    - Denver had the largest number of votes.
    
- Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
    - Charles Casper Stockham: 23.0% (85,213)
    - Diana DeGette: 73.8% (272,892)
    - Raymon Anthony Doane: 3.1% (11,606)

- Which candidate won the election, what was their vote count, and what was their percentage of the total votes?
    - Diana DeGette won the election with 272,892 vote count and 73.8% of the total votes.


This is an [image](https://github.com/Takomochi/Election_Analysis/blob/main/Resources/Output_Command_Line.PNG) of the output to the command line.<br>

<img src="https://github.com/Takomochi/Election_Analysis/blob/main/Resources/Output_Command_Line.PNG" width="300" height="400">


## Challenge Summary
### Business Proposal
The script is complete with outputting the result of the election. However, we need to modify the script to be used for other elections. There are two modifications we can make.

- First of all, data to be read should be modified. THe code below is a path that leads to the data file "election_results.csv". We need to change the second argument to get the data we want.
```
# Add a variable to load a file from a path.
file_to_load = os.path.join("Resources", "election_results.csv")
```

- The order and the number of the columns might be different for other elections. To get the correct values, we need to be careful about which index contains what information. We need to add variables like the code below if we want to extract other information such as state name or political party name.
```
# Get the candidate name from each row.
        candidate_name = row[2]

        # 3: Extract the county name from each row.
        county_name = row[1]
```

If we add a variable, make another if statement, for loop the dictionary and write a summary of the result. 

By dividing the script into several blocks, we can see that the script is repeating the same tasks.
This script is relatively straightforward to modify and use for other elections.