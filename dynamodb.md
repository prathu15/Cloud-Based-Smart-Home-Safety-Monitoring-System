# Amazon DynamoDB


* I created a table named `SensorDataTable`
* I set partition key as `houseId` and sort key as `timestamp`
* I connected Lambda to store incoming sensor data
* I fixed region mismatch issue to make Lambda access the table
* I verified stored data using Explore Items

## Result

Sensor data was successfully stored and retrieved from DynamoDB.

<img width="1066" height="328" alt="dynamo" src="https://github.com/user-attachments/assets/7d81bfe7-7cd5-4dea-81e8-48bccd53fa27" />

---

<img width="1322" height="538" alt="dynamo_db" src="https://github.com/user-attachments/assets/ac021075-4490-470d-aaef-8c35aaff08cc" />

---

<img width="1357" height="555" alt="dynamo_db-data" src="https://github.com/user-attachments/assets/6235fd3c-5470-4d01-bd31-7f60e0edf553" />
