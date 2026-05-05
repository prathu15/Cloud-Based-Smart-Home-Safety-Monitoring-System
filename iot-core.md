# AWS IoT Core



* I opened AWS IoT Core and used MQTT test client to simulate sensor data
* I designed topic structure like `home/{houseId}/{sensorType}` for multiple houses and sensors
* I published sample data for temperature, smoke and fire
* I created an IoT Rule to send data to Lambda
* I used SQL query: `SELECT * FROM 'home/+/+'` to capture all data

## Result

IoT Core successfully received sensor data and forwarded it to Lambda for processing.

<img width="1361" height="539" alt="Aws_iot_core" src="https://github.com/user-attachments/assets/ccdf973b-6bee-4a6f-a894-083588c63438" />




<img width="1332" height="543" alt="aws_iot_core_publish" src="https://github.com/user-attachments/assets/0c24e74c-f0c4-4880-9b4c-66f43c9c2c8a" />





