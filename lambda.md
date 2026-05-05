# AWS Lambda


* I created a Lambda function using Python runtime
* I configured IAM role to allow access to DynamoDB and SNS
* I connected Lambda with IoT Core using IoT Rule
* I wrote logic to process sensor data (temperature, smoke, fire)
* I handled data type issue (string vs number)
* I added condition checks for abnormal values
* I integrated SNS to send alerts when conditions are met

---

## Lambda Code

```python
import json
import boto3
from datetime import datetime

# DynamoDB
dynamodb = boto3.resource('dynamodb')
table = dynamodb.Table('SensorDataTable')

# SNS
sns = boto3.client('sns')
TOPIC_ARN = "arn:aws:sns:ap-south-1:120259362909:HomeAlertTopic"

def lambda_handler(event, context):
    print("Received Event:", event)

    houseId = event.get("houseId")
    sensorType = event.get("sensorType")
    value = event.get("value")

    # Fix type issue
    if isinstance(value, str):
        try:
            value = int(value)
        except:
            pass

    timestamp = event.get("timestamp", datetime.utcnow().isoformat())

    # Store data in DynamoDB
    table.put_item(
        Item={
            "houseId": houseId,
            "timestamp": timestamp,
            "sensorType": sensorType,
            "value": str(value)
        }
    )

    # Rule-based logic
    message = None

    if sensorType == "temperature" and float(value) > 80:
        message = f"High temperature in {houseId}"

    elif sensorType == "smoke" and value == True:
        message = f"Smoke detected in {houseId}"

    elif sensorType == "fire" and value == True:
        message = f"Fire alert in {houseId}"

    # Send alert
    if message:
        sns.publish(
            TopicArn=TOPIC_ARN,
            Message=message,
            Subject="Home Safety Alert"
        )

    return {
        "statusCode": 200,
        "body": json.dumps("Processed successfully")
    }
```

---
<img width="1359" height="537" alt="Connection_lambda" src="https://github.com/user-attachments/assets/9215d359-f26e-41b2-94f2-0d54cc8dcfe9" />

---

## Result

Lambda processed data in real time, stored it in DynamoDB and triggered alerts using SNS.
