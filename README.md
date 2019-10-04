# PoSE
PoSE is a search engine that queries a given set of documents for single and multiword queries. PoSE works in two modes, boolean and ranked retrieval, and support AND, NOT, OR, NEAR and phrase literal queries. Additionally the precision and recall of the search engine is tested using various scoring formulas. 

## Getting Started
1. Clone the repository and add additional libraries to project. 
  
    The necessary GSON library files are included in the repository. More information about GSON can be found [here](https://github.com/google/gson)
  
2. Build the index
    - Querying an index for the first time
    
       PoSE queries json files. If building a index from a large collection of documents, the operation can take a few minutes.  
    - Querying an existing index
    
       The index only needs to be built once, after the inital build a copy of the index is stored to the user's disk for quick retrieval. 
       
3. Querying the index

    - Boolean retrieval 
    
       Boolean retrieval runs on the default scoring formulas and can contain any of the following:
       - **Phrase literals**: Must be enclosed in double quotes
       - **AND queries**: default query operater, white space between words is considered an AND query operator
       - **OR queries**: queries must be joined by the '+' symbol
       - **NEAR queries**: keywords 'NEAR/k' must be used where k is the distance to the given word
       - **NOT queries**: query must be prefixed with a hyphen 
    
    - Ranked Retrieval 
    
       Cannot contain any of the above operators. This mode returns the top 10 documents containing the given query. The ranking of documents follows the scoring formulas found in Christopher Mannings's Introduction to Information Retrieval. Ranked Retrieval works with the four scoring formulas provided.
    
    - Precision Recall
       
       Returns the mean average percision, throughput and mean response time of the search engine. These calculations can be calculated using any of the four scoring formulas provided. 

    
