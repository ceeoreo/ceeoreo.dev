---
layout: ../../layouts/BlogLayout.astro
title: Never Get an Unexpected AWS Bill Again!
description: A how to guide on setting up price alerts in AWS to avoid unexpected bills
tags: ['aws', 'cloud', 'beginner']
time: 6
featured: true
timestamp: 2020-09-08T02:39:03+00:00
filename: aws-bill-management
---
One of the things that prevents a lot of people from exploring AWS is the cost. Some AWS services are very expensive. Accidentally forgetting to cut something off and getting charged is the worst feeling. Trust me, I know.

![Meme of guy looking confused. This how I am when I get an unexpected AWS bill](https://www.ceoraford.com/static/img/aws-billp-meme.JPG)

Is this an irrational fear? Is this something people think of just as an excuse for not getting started? Absolutely not. This is definitely, 1000% a valid fear. I'm sure most people involved with AWS have a horror story about getting charged unexpectedly. The great thing is that there are steps you can take to prevent this from happening. For the first installation of Learn AWS With Me, I'm going to cover 3 things you can do to make sure you don't get billed unexpectedly.

---

## 1. Cut Things Off IMMEDIATELY

This might seem really obvious but I mean it. Seriously. This is something you should get into the habit of doing early. If you're just practicing and you want to make sure you know how to navigate the AWS console, make sure to undo your work immediately!! Did you just spin up an EC2 instance? Great!! SHUT IT DOWN!! You just figured out how to use RDS? Amazing! Shut. It. DOWN!!!!!

Not all AWS services are expensive. AWS Lambda is one example. Leaving a practice lambda running won't cost you a whole lot. But this definitely isn't always the case. I mentioned EC2 and RDS earlier because I know from experience that those two can be VERY expensive. So, again, **MAKE SURE TO SHUT THINGS DOWN ONCE YOU FINISH PRACTICING**.

## 2. Set Up Billing Alerts

Did you know that you can set up billing alerts on AWS? I didn't learn this until it was too late (more on that later). Setting up a billing alert can save you sooo much pain, heartache, and most importantly, money. Follow these steps to set up billing alerts right now!

- In the AWS management console, search for a service called **CloudWatch**  
![Image of AWS console CloudWatch service](https://www.ceoraford.com/static/img/cost-step1.png)

- On the left hand corner of the CloudWatch dashboard, click **Billing**  
![Image of Billing tab under CloudWatch service](https://www.ceoraford.com/static/img/cost-step2.png)

- Click **Create Alarm**  
![Create Alarm button](https://www.ceoraford.com/static/img/cost-step3.png)

- For Step 1, we have to track a metric. We want this alarm to track **EstimatedCharges** as our metric. Set the currency to whatever fits your location.  
![Image of metric tracking page](https://www.ceoraford.com/static/img/cost-step4.png)

- At the bottom of the page, you can define your price limit. You can set the limit to 0 if you don't want to go past the free tier limits. After you've defined your price limit, click **Next**  
 ![Price field and next button](https://www.ceoraford.com/static/img/cost-step5.png)

- For Step 2, define what kind of notification you want to receive. You should set this to **In Alarm**

- For **Select an SNS topic** click **Create new topic**.  
 ![SNS topic page](https://www.ceoraford.com/static/img/cost-step6.png)

- You can SNS topic whatever you like. I chose, 'toomuchmoney'. Now set it to whatever email you want the notifications to be sent to. Click **Create Topic**.  
![Choosing SNS Topic name](https://www.ceoraford.com/static/img/cost-step7.png)

- Click **Next** on the bottom right-hand corner.

- For Step 3, choose alarm name next. You can give this the same name as your topic if you like. You can also add a description for this alarm if you want to.

- Step 4 is just previewing what you've already done. If everything looks good, you can finish things off by clicking **Create alarm**

Now you have an alarm that will tell you whenever you get close to passing your price threshold.

## 3. Open a Support Case

What if you're past the point of no return? What if you already got the email from AWS telling how much you'll be charged? Does it sound like this is something I'm remembering? Well, that's because this happened to me recently and I was devastated. Thankfully, there _is_ something you can do to fix this.

You can open up a support case! How?

- Click on the **Support** button in the top right hand corner and choose **Support Center**. You can also search for support in the AWS Management Console.
- Click **Create Case** and click **Account and billing support**
- Fill out the details that best fits your situation.

It's important to keep in mind that you don't want to take advantage of this method too often. I've only had to submit a support case once and someone from the AWS support team got back to me within a few days and waived my bill. But I have heard that they aren't always so forgiving after the first time. So don't rely on this feature too much. It might not turn out well for you all the time.

--- 

## Conclusion

AWS can be expensive. But I don't want that to stop you from learning how to use some of the services AWS has to offer. If you follow some of the advice outlined in this post, you can be sure that unexpected costs won't be something you have to struggle with. And if you slip up, you can always try option 3. Look out for the next Learn AWS With Me post coming soon! If you want to be notified when that drops, follow me here. And of course, if you have any requests, leave them in the comments below. Thanks for reading!