# lambda-in-python-tutorial
Creating a Lambda Function with the AWS Management Console

Author Lambda Function in Python

Navigate to Lambda.

Click Create function.

Make sure the Author from scratch option at the top is selected, and then use the following settings:

Function name: Type myfunction.
Runtime: Select the latest version of Python.
Expand Change default execution role section, and verify that Create a new role with basic Lambda permissions is selected.

Click Create function.

Once the function has been created, scroll down to the Code tab.

Under Code source, select lambda_function.py.

Replace the existing sample code with the following:
```
import json

def lambda_handler(event, context):
    message = 'Hello {} {}! Keep being awesome!'.format(event['first_name'], event['last_name'])  

    #print to CloudWatch logs
    print(message)

    return {
        'message' : message
    }  
 ```
Click Deploy.
