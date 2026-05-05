# Amazon DynamoDB


* I created a table named `SensorDataTable`
* I set partition key as `houseId` and sort key as `timestamp`
* I connected Lambda to store incoming sensor data
* I fixed region mismatch issue to make Lambda access the table
* I verified stored data using Explore Items

## Result

Sensor data was successfully stored and retrieved from DynamoDB.


<img width="1357" height="555" alt="dynamo_db-data" src="https://github.com/user-attachments/assets/6235fd3c-5470-4d01-bd31-7f60e0edf553" />
