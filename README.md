# Serverless-project

### Create DynamoDB Table Peaople and create item

![image](https://github.com/felixdagnon/Serverless-project/assets/91665833/85665394-5e5f-4d5e-8940-0a7ea3ce46cd)

### Below is a "PersonRecords" table with primary key as "PersonID" (unique identifier).

// first person

{
    "LastName": "Smith",
    "FirstName": "Fred",
    "PersonID": 1,
    "Phone": "700-123-4456"
}

// Second person

{
 "FirstName": "Jan",
 "LastName": "Smith",
  "PersonID": 2,
 "Phone": "700-123-4456",
 "Address": {
  "City": "London",
  "Country": "England",
  "Street": "123 Baker road"
 }
}

// Third person

{
 "PersonID": 3,
 "Address": {
  "City": "London",
  "Country": "England",
  "Street": "123 Baker road"
 },
 "FirstName": "Scott",
 "LastName": "Smith",
 "Phone": "700-123-4456"
}


### Insertting into DynamoDB using lambda function

```json
{
import json
import boto3

def lambda_handler(event, context):
    # TODO implement
    dynamodb = boto3.resource('dynamodb')
    table = dynamodb.Table('People')
    try:
        # TODO: write code...
        response = table.put_item(
          Item=event)
        return "Done"
    except:
        raise
}
```


![image](https://github.com/felixdagnon/Serverless-project/assets/91665833/3622a96f-ff8b-4b3c-8337-7e8f8cb2bba9)






