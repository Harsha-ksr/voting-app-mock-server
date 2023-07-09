# voting-app-mock-server
This is a mock-server used by voting application to save/retrieve data.
This server needs to be up and running before running the actual voting-application.

Steps to Run the Mock Server:
1. Run npm install and make sure all dependent packages are installed.
2. Once the project is loaded, Open terminal, go to root directory and run -> "npm run mock:server" to start up the server.
3. The server starts on localhost port 3000.

Test the APIs:
1. Use Postman or any other testing tool to test the APIs. Below are the Curl commands provided which you can import into postman and run.

--> Get Results By question:
curl --location 'http://localhost:3000/api/getResultsByQuestion'

--> Cast Vote
curl --location 'http://localhost:3000/api/castVote' \
--header 'Content-Type: application/json' \
--data '{
    "votedQuestions": [
        {
            "question": "Who is gonna win world-war 3?",
            "userId": "mkoride",
            "vote": "Yes"
        }
    ]
}'

--> Get All Questions
curl --location 'http://localhost:3000/api/questions'

--> Create a question
curl --location 'http://localhost:3000/api/createQuestion' \
--header 'Content-Type: application/json' \
--data '{
    "question": "This is a test questiosssn"
}'
