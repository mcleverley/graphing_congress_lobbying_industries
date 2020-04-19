# Who owns Congress?
Lobbying is a legal form of bribery. There's some good arguments about citizens banding together to protect their ideals and the protection of minority interests, but our reality is one where the uber-rich can use vast amounts of wealth to influence political outcomes and further concentrate said wealth.
We hear about it a lot, "money in politics" and all that, but it tends to get lost among the bureaucracy. I used network graphs to visualize the flow of money from various industries to congressmembers - to make it easy to see who's in who's pocket.
- Tools used:
  - Neo4j
  - Py2Neo
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
- Data uploaded to Neo
- Completed:
  - basic querying
  - community detection, pagerank
- Now working on:
    - transfer to Gephi for cleaner big-picture visualization
    - hosting Neo server remotely on AWS for others to query
    - create frontend for non-tech users to query congresspeople
    
### Blog posts
Graphing, querying in neo, community detection algorithms
https://medium.com/@mark.s.cleverley/graphing-congressional-lobbying-549e9e5ecc87
https://medium.com/@mark.s.cleverley/querying-congressional-lobbying-in-neo4j-25cecc8a7ce8https://medium.com/@mark.s.cleverley/algorithmic-detection-in-congressional-lobbying-fdb4a8e98ada
