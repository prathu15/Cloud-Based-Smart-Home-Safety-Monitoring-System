# Amazon DynamoDB


* I created a table named `SensorDataTable`
* I set partition key as `houseId` and sort key as `timestamp`
* I connected Lambda to store incoming sensor data
* I fixed region mismatch issue to make Lambda access the table
* I verified stored data using Explore Items

## Result

Sensor data was successfully stored and retrieved from DynamoDB.
