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

### Currently
The process has been successfully completed, but needs improvement in several areas.
- Fixing mismatched years in id_scrape URL (API calling 2018 congressmembers using IDs from 2020 is not great)
- Importing correct labels to Neo4J
  - 'neonx' networkx-to-neo4j library is helpful, but can mishandle edge and node labels
  - currently exploring Py2neo as alternative option
