
# Cloud-Based Smart Home Safety Monitoring System using AWS

## Problem Statement

I designed a home automation system which collects data from multiple sensors installed in different houses and process it on cloud. The system monitor conditions like temperature, smoke and fire and notify users if any dangerous situation is detected.

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

---

<img width="1071" height="467" alt="Screenshot 2026-05-05 135139" src="https://github.com/user-attachments/assets/b566200d-9c85-4df3-a3d2-f6a67d5cf2a6" />
---
<img width="948" height="495" alt="Screenshot 2026-05-05 135803" src="https://github.com/user-attachments/assets/1ae4f041-bebc-42dd-9af7-c5a8e6cd7027" />
---
<img width="1211" height="614" alt="sns" src="https://github.com/user-attachments/assets/28f94340-feed-4d64-a0eb-93b1a0d3b478" />
---

<img width="1039" height="435" alt="sns_notification" src="https://github.com/user-attachments/assets/37ca473b-ac32-452d-9b27-9202117bcb5a" />




