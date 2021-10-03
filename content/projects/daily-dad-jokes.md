---
title: "Daily Dad Jokes"
summary: "How I built an event-driven serverless Telegram bot to deliver dad jokes to you daily"

tags: [projects, chatbot]
---

I created a Telegram channel to deliver dad jokes every day. I did not want to build a Node.js server and host it on Digital Ocean or Linode because that would be cost inefficient. Instead, I wanted to build an event-driven serverless architecture. We can achieve this with [AWS Lambda](https://aws.amazon.com/lambda/) for the lambda functions and [AWS CloudWatch](https://aws.amazon.com/cloudwatch/) to trigger the lambda through scheduled events.

First I created a bot and added it to a channel. The bot fetches a dad joke from [icanhazdadjoke.com](https://icanhazdadjoke.com/api) and publishes it to the channel. The last step was to trigger the lambda function on a regular schedule.

You can visit the [Daily Dad Jokes](https://t.me/s/DailyDadJokes) public channel or subscribe to the [channel](https://t.me/DailyDadJokes) on Telegram. 
