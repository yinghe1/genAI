Use this doc to see what use cases we can use LLM to help us

1. Use LLM to analyze news and display what you want to read.
   Get news feed from free api like https://newsapi.org and developer api-key is free for study purpose see their documentation to see the json format. 
   Take a look at the output using commandline tool curl. using tee command so it can show both at standard output and write to a file at the same time 
   ```
   curl -s "https://newsapi.org/v2/top-headlines?country=us&apiKey=<useYourOwnAPIKey> 2>&1| tee 02022025news.json
   ```
2. Build a rag system to read real estate data and use LLM to answer your question about real estate, eg. retirement housing need, first-time home buying. Potentially we can use zillow free api tier. TODO
