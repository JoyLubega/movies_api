# Movies API
This movies api is configured with dynamoDB-local
### Getting started:
#### setting up DynamoDB locally
- Download Docker on your machine from here:
https://www.docker.com/get-started

- Download the DynamoDB (Downloadable version) on your Computer from here :
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.DownloadingAndRunning.html
- Move the unzipped file to a location of you choice and run:

    ``` cd dynamodb-local-latest ```
- To run DynamoDB on your computer, you must have the Java Runtime Environment (JRE) version 6.x or newer.     The application doesn't run on earlier JRE versions.
- Run the command below: 

    `java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb`
- Before you can access DynamoDB programmatically or through the AWS Command Line Interface (AWS CLI), you must configure your credentials to enable authorization for your applications. Downloadable DynamoDB requires any credentials to work:

- Run : 
    `pip install awscli` then 
    `aws configure` to add the key and the ID. The output format is always json

- Run  the docker server on your machine:

    `docker run -p 8000:8000 amazon/dynamodb-local`
- To list all tables :
    `aws dynamodb list-tables --endpoint-url http://localhost:8000`