---
title: "BBC Earth Daily"
summary: "How I built the BBC Earth Daily chatbot"

tags: [projects, chatbot]
---

I created a Telegram channel to share videos from the BBC Earth YouTube channel. Since this project did not warrant a server to be up 24/7, I leveraged on a serverless architecture to keep the cost low. I used [AWS Lambda](https://aws.amazon.com/lambda/) for the lambda functions and [AWS CloudWatch](https://aws.amazon.com/cloudwatch/) to trigger the lambda through scheduled events.

First I built a Telegram bot which fetches a random video from the BBC Earth YouTube channel and publishes it to a Telegram channel. I then have it run on a daily schedule.

The [BBC Earth Daily](https://t.me/s/BBCEarthDaily) channel can be viewed from a web browser or you can subscribe to the [channel](https://t.me/BBCEarthDaily) on Telegram. The code is [open sourced](https://github.com/jsstrn/bbc-earth-daily) so you can fork it and build your own.
