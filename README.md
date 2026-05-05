
# Cloud-Based Smart Home Safety Monitoring System using AWS

## Problem Statement

I designed a home automation system which collects data from multiple sensors installed in different houses and process it on cloud. The system monitor conditions like temperature, smoke, fire and motion, and notify users if any dangerous situation is detected.

---

## Objective

* I built a scalable cloud based system for multiple houses
* I processed sensor data in real time
* I stored data securely on cloud
* I detected abnormal conditions using rule based logic
* I sent alerts to user in critical cases

---

## Architecture Overview

IoT Core → IoT Rule → Lambda → DynamoDB + SNS → User

* IoT Core: I used it to receive sensor data
* IoT Rule: I used it to forward data to Lambda
* Lambda: I processed and analysed data
* DynamoDB: I stored sensor data
* SNS: I sent alerts to user

---

## AWS Services Used

* AWS IoT Core
* AWS Lambda
* Amazon DynamoDB
* Amazon SNS
* AWS IAM
* Amazon CloudWatch

---

## Implementation Steps

1. I configured MQTT topics for multi house and multi sensor data
2. I created Lambda function to process incoming data
3. I connected IoT Rule with Lambda
4. I stored data in DynamoDB
5. I integrated SNS for sending alerts
6. I tested system with different scenarios


## Features

* I supported multiple houses
* I supported different sensors (temperature, smoke, fire)
* I implemented real time data processing
* I created automatic alert system
* I designed scalable cloud architecture

---

## Security & Privacy

* I used IAM role based access control
* I ensured no public access to database
* I used secure communication through IoT Core
* I ensured data encryption at rest

---
## Conclusion

I built a scalable and secure IoT based home safety system using AWS. It process real time data, store it securely and send alerts when required.
