# Who owns Congress?
Lobbying is a legal form of bribery. There's some good arguments about citizens banding together to protect their ideals and the protection of minority interests, but our reality is one where the uber-rich can use vast amounts of wealth to influence political outcomes and further concentrate said wealth.
We hear about it a lot, "money in politics" and all that, but it tends to get lost among the bureaucracy. I used network graphs to visualize the flow of money from various industries to congressmembers - to make it easy to see who's in who's pocket.
## Data
Campaign donations from lobbying groups for the 2018 115th Congress, courtesy of the Center for Responsive Politics (opensecrets.org).
## Process
- Scrape all congress_member_ids in Selenium
- Call the CRP's API for XML requests
- Parse into JSON/dict format
- Convert to graph in NetworkX
  - Visualize in Gephi
  - Push to Neo4J database for explorative querying
  - Run community algos in neo

### Currently
All the data's in Neo, and I've been messing around with graphical EDA, plumbing second and third-depth relationships between nodes.
The process has been successfully completed, but needs improvement in several areas.
- Now working on:
    - community detection algorithms in Neo, possible overall visualization in Gephi
    - hosting Neo server remotely for others to query
    - create frontend for non-tech users to query congresspeople
