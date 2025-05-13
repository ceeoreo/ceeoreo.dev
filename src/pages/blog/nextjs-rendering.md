---
layout: ../../layouts/BlogLayout.astro
title: Next.js in A Nutshell: Rendering
description: Learn the basics of Next.JS with this series. This post focuses on rendering in Next.js
tags: ['nextjs', 'coding', 'beginner', 'frontend']
time: 4
featured: true
timestamp: 2023-12-05T02:39:03+00:00
filename: nextjs-rendering
---
Next.JS is one of the most popular modern React frameworks out there. I’ve spent the past few months building with Next.JS and learning the ins and outs of the language. Next.JS caught my eye initially because it offers a more seamless experience by abstracting away some of the tedious tasks that come with working with React like bundling and compiling. These are the things that usually make me want to pull my hair out so I had to try out Next.JS when I discovered that these things are automatically configured for you.

As I’ve been building, I’ve learned a lot along the way and I wanted to wrap my findings up into a blog post series that will cover a few things:

- Core concepts in Next.JS
    - Server side rendering vs Client side rendering
    - Pages Router vs App router
- What to do after learning the basics
- Helpful resources

This post will specifically focus on rendering. We’ll cover routing and next steps in the future posts. My goal is to give you an introduction to Next.JS and a place to start so you can move forward and learn more on your own! I’m also happy to write more articles on specific Next.JS topics. Feel free to leave any requests in the comments!

## Core Concepts👩🏾‍💻

Next.JS is built around some React concepts that you’ll be familiar with if you’ve worked with React before. But there are obviously a few things that make Next.JS a bit different. Next.JS has some enhancements that give it an added edge over React or other frameworks. I already mentioned the compiling and bundling improvements. Next.JS also comes with image and font optimizations that enhance user experience and site performance. Images are lazy-loaded and automatically resized based on device size. You can read more details on font optimization in the Next.JS documentation. 

Next.JS's main claim to fame is how rendering and routing are handled. Even if you haven’t worked with Next.JS before, you’ve probably at least heard terms like “Server-side rendering” and “Client-side rendering”. It’s really important to understand these concepts when you’re building applications with Next.JS. So let’s dive in. 

## Server Side Rendering vs Client Side Rendering⚙️

In Next.JS, you can choose where you want your components to be rendered: on the server side or on the client side. Next.JS is all about performance optimization and for that reason, Next.JS uses server side rendering by default. **Server side rendering** improves performance in a few ways:

- Data fetching → When data fetching is done on the server side, the time it takes to retrieve data is reduced since the server is architecturally closer to the data source
- Caching → When you render on the server, results can be easily and quickly cached which leads to faster response times for future requests.
- Bundling → Large dependencies can now be kept on the server which reduces the size of your bundle on the client side

There are other benefits but I think these 3 really highlight how server side rendering can improve performance. These changes might seem small but they add up quickly. If you want to know more about the mechanics of server side rendering, check out [this documentation](https://nextjs.org/docs/app/building-your-application/rendering/server-components#how-are-server-components-rendered).

### Static rendering, dynamic rendering, and streaming🔧

Server side rendering can be done in 3 ways: *static, dynamic, or streaming.* **Static rendering** is the default. Information is rendered at build time meaning it’s preloaded before a request is made and cached. This is perfect for data that doesn’t need to be customized per user. Any information that is the same for every user can be statically generated. Again, this is a huge performance optimization. With **dynamic rendering,** data is rendered on each request. This is good for data that is unique to each user or for information that changes quickly. 

When I first learned about static and dynamic rendering, I panicked a bit because I assumed that I would have to decide how each possible route and every piece of data on my site should be rendered. The great thing is that Next.JS automatically chooses for you. You still have control when you want to because you can specify when to cache or revalidate certain data. You can also choose to **stream** some data in your UI.

**Streaming** is a new feature of Next.JS that’s only available with the App Router (which we’ll dive into soon). Streaming allows you to progressively render data from the server. Using this rendering method allows you to keep displaying parts of a page immediately while the streamed data is still loading. Instead of the whole page loading and forcing your user to stare at a blank screen, streaming allows you to pinpoint the data that needs more time to render while still displaying the rest of the page.

To put all of this into context, an About page would be statically rendered since the information won’t change no matter who’s viewing it. Components on a profile page that can be changed such as display name or status would be dynamically rendered. For large amounts of data that can take time to load such as product reviews, posts on a social media feed, and the like, streaming can be used. 

### Client side rendering🔨

Now, what about **client side rendering**? **Client side rendering** is rendered on the client side at request time. Server side rendering is the default so in order to use client side rendering, you have to opt in. Next.JS automatically handles whether server side components will be rendered statically or dynamically but it doesn’t do the same for client components. You have to manually specify when you want client side rendering to be used. 

When should you use client side rendering? Since you can use state and event listeners with client components, it’s perfect for interactive components that are meant to produce an immediate result for users. So think of liking a post or comment on a social media site. This kind of feature could be built with client components since liking something involves interactivity, data that changes quickly, and displaying said data to users immediately. 

## Conclusion👩🏾‍🏭

So we’ve covered the basics of rendering in Next.JS. This is an overview and there’s obviously more that goes into rendering especially under the hood. If you want to learn more of the nitty gritty details, check out some of these resources:

- [Next.JS docs: Rendering](https://nextjs.org/docs/app/building-your-application/rendering)
- [Next.JS Course: Chapter 8 on Static and Dynamic rendering](https://nextjs.org/learn/dashboard-app/static-and-dynamic-rendering)
- [Next.JS Course: Chapter 9 on Streaming](https://nextjs.org/learn/dashboard-app/streaming)

The main take away you should walk away from this post with is: Next.JS really prioritizes performance. Relying primarily on server side rendering is done to enhance performance and user experience. If performance is important for the project you're working on, Next.JS might be the right choice for you!

I’ll post part 2 of this series shortly! The information is already drafted so don’t worry it’s coming soon! If you have any questions or comments, please leave them below! I’ll try to get to as many of them as possible! Thanks for reading :)
