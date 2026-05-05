# AWS IoT Core



* I opened AWS IoT Core and used MQTT test client to simulate sensor data
* I designed topic structure like `home/{houseId}/{sensorType}` for multiple houses and sensors
* I published sample data for temperature, smoke and fire
* I created an IoT Rule to send data to Lambda
* I used SQL query: `SELECT * FROM 'home/+/+'` to capture all data

## Result

IoT Core successfully received sensor data and forwarded it to Lambda for processing.


![screenshot/Aws_iot_core.png]
