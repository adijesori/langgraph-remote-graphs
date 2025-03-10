This is a simple example of express application that uses two remote lang graphs
It uses the following two repositories:
- https://github.com/adijesori/langgraph-research-agent
- https://github.com/adijesori/langgraph-creative-agent

It is using the following workflow:

In order to run it:
1. Clone the repository
2. Run `npm i`
3. Add `.env` file in the root directory with the following content:
```
LANGSMITH_API_KEY=${YOU_LANGSMITH_API_KEY}
LANGSMITH_TRACING=true
```
4. Run locally the two remote graphs mentioned above. (You can use their README.md for how to do that). 
5. Run `npm start ` or `npm run dev` to use hot reload
6. Use this simple curl (you can import to Postman) to test the application:
```
curl --location 'http://localhost:3000/generate' \
--header 'Content-Type: application/json' \
--data '{
    "topic": "zoom"
}'
```
7. You can also use the following curl (you can import to Postman) to get the workflow image:
```
curl --location 'http://localhost:3000/graph'
```
