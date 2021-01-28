# Third Week links and code

## Sites to register to
- [https://os.mbed.com/mbed-os/](https://os.mbed.com/mbed-os/)
- [https://console.aws.amazon.com/iot](https://console.aws.amazon.com/iot) It can take up to 24 hours for Amazon to setup the account allowing you to create "Things" and "Policies". There is a limit of 2000 messages per month using the free account.

## Policy to be pasted in AWS

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "iot:Connect",
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": "iot:Publish",
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": "iot:Subscribe",
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": "iot:Receive",
      "Resource": "*"
    }
  ]
}
```

## Importing Mbed code
[https://os.mbed.com/compiler/#import:https://github.com/AlbinMartinsson/L475VG-IOT01A-Mbed-AWS-IoT](https://os.mbed.com/compiler/#import:https://github.com/AlbinMartinsson/L475VG-IOT01A-Mbed-AWS-IoT)

## Topic to subscribe to
Subscribe to ```stm32/sensor```

## Payload to publish
Publish to topic ```stm32/action``` with JSON string

```
{
       "action": "turn on"
}
```

or

```
{
       "action": "turn off"
}
```

## AWS IoT
- What is AWS IoT? YouTube [video](https://youtu.be/WAp6FHbhYCk)

