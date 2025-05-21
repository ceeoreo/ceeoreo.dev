---
layout: ../../layouts/BlogLayout.astro
title: Wait... Serverless Isn't Actually Serverless?
description: Serverless doesn't actually mean serverless
tags: ['cloud', 'aws', 'beginner']
time: 4
featured: false
timestamp: 2020-10-30T02:39:03+00:00
filename: serverless
---
Before we get into the topic of this article, I want to tell a little story. I started learning more about cloud engineering and AWS a few months ago. I had finally wrapped my head around what cloud actually was. Then I was introduced to this concept of serverless computing and... I was thoroughly confused to say the least.  
{% twitter 1296188715417636866 %}
I finally started to understand some AWS foundational concepts and resources and now I was learning about serverless. This absolutely threw me for a loop. You might relate to how I felt a few months ago. If so, this post is just for you.

I'm going to break down what serverless computing actually is. I'll also point out some essential AWS serverless resources to know. But to understand serverless computing, it's good to first understand cloud computing. So let's begin by first establishing what cloud computing is.

## What is cloud computing?

Your code needs to be hosted on a server. Depending on the size of your code and the amount of users you expect to use your product or website, you might need many servers. Companies used to have their own facilities and warehouses that held their servers and many still do. But for many, this is not ideal.

**Servers can be difficult to maintain**. I'm not sure about you but sometimes when I have a lot of tabs open and lots of apps running on my laptop, my laptop starts to act a little funny. Sometimes if I'm using my computer on my bed where vents are blocked by blankets, my computer starts to act strange. You’ve probably experienced the same thing before. Something similar happens with servers too.

Servers may begin to malfunction when there is lots of code running and many users accessing that code. Servers are also affected by changing temperatures. Maintaining servers and the buildings that house them can become expensive too. Over time, these issues can become hard to manage. That's where AWS and other cloud providers come in.

**Cloud computing is basically renting out servers and data storage that's owned by someone else.** With AWS, that means using servers owned by Amazon. This cuts out the need to buy and maintain physical servers. The issues I mentioned earlier are no longer a problem. AWS offers more than storage which is obvious as their list of services seems to never end. Through AWS, you gain access to resources like storage services, servers, networking, analytics, AI, and more.

Aside from the wealth of resources cloud computing allows you to access, there are many other benefits:

- You pay only for what you use. This can be very cost effective.
- You can easily spin up and use new servers when needed, allowing you to scale quickly.
- You can deploy applications globally.
- All of this leads to quicker development and deployment.

Cloud computing might seem great and it is (for the most part). So where does serverless computing come in? And why is it necessary? What even _is_ it? Let's start there first.

## What is Serverless?

With cloud computing, you don't have to worry about server maintenance. But you can decide what type of server to deploy, how much computing power you'll require, how many servers you want, and much more. **You don't own the servers but you still have a lot of control over them**.

Serverless takes cloud computing to the next level. You don't have to worry about the servers **at all**. Here's one key thing to remember: **serverless does not mean there aren't any servers**. Check the meme I shared in the intro for a reminder. You still need servers to host and run your code. **With serverless computing, you let go of the responsibilities and control you have with cloud computing**. This means that you can completely focus on your code without having to configure your servers to meet your needs.

This is **really** powerful! You don't have to learn any infrastructure to deploy code using serveless computing. All your time can be spent focusing on your code and you still get many of the benefits of cloud computing. Serverless can be very low cost and it's super easy to scale up or down with serverless. Of course, like everything, there are some drawbacks to going the serverless route. It may not be the best option for you depending on what your needs are. But we won't get into that right now. (Maybe in a future edition of Learn AWS With Me?)

At this point, you now know what past me struggled with! You know the difference between cloud computing and serverless computing. You also know that serverless isn't _actually_ serverless. Now, let's cover some of the serverless resources AWS has to offer.

## AWS Serverless Resources You Should Know

AWS has a **lot** to offer. So, as you can imagine, there are a lot of serverless resources available. I'll point you to the ones I use the most and the ones you might be interested in too!

1. Lambda  
AWS Lambda is super useful! This service allows you to run serverless functions. You only pay for the time your code runs. I've used AWS Lambda to run Twitter bots. There are tons of things you can do with AWS Lambda.
2. S3  
S3 stands for Simple Storage Service. S3 offers you simple, secure storage. This is a great resource to play around with. Try hosting a static site with S3. This was my first AWS project and it's a great place to start!
3. DynamoDB  
Amazon DynamoDB is a noSQL database service. I haven't gotten to work with DynamoDB (yet). But this [What is DynamoDB?](https://www.dynamodbguide.com/what-is-dynamo-db/) article from the [DynamoDB guide](https://www.dynamodbguide.com/) site is a great place to learn from!
4. SNS  
SNS stands for Simple Notification Service. This service allows you to automatically send emails or text messages based on certain occurrences within your AWS account. We used SNS in the [Never Get an Unexpected AWS Bill Again!](https://www.ceoraford.com/posts/never-get-an-unexpected-aws-bill-again!/) lesson. If you want to get a better idea of how SNS works, follow along with the lesson and create your own billing alarm.

If you want to experiment with some of these resources, check out this [article with 3 serverless projects](https://www.thedevcoach.co.uk/serverless-beginner-project/) you can start working on.

---

## Conclusion

To sum all this up, no, serverless is **not** actually serverless. Now that I understand what serverless is, I find it really fascinating! I'm now able to utilize serverless resources offered by AWS and other companies and it honestly makes my life so much easier (most of the time😂). With this new knowledge, you can jump into building and deploying amazing things! If you do, make sure to share with me!

If there's an AWS topic you'd like me to cover, feel free to let me know in the comments below! Thanks for reading!!