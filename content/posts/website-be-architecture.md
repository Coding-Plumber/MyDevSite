---
author: "Kyle McAndrew"
title: "Backend website architecture"
date: "2024-05-21"
tags:
  - aws
  - architecture
---

<p>I always like to work on projects that achieve multiple goals. Since I want to focus on backend and cloud development for the next few months, I decided to create a real-world application that I'll actually use. This led me to build a comprehensive plumbing website using the following technologies:</p>

<ul>
<li>React with Next.js</li>
<li>TypeScript</li>
<li>Tailwind CSS</li>
<li>AWS (Amazon Web Services)</li>
<li>Go (Golang)</li>
</ul>

<p>Having already created a straightforward plumbing website, I wanted version 2 to focus on automating as much of the process as possible, from booking to job completion.</p>

Having already created a straightforward plumbing website, I wanted version 2 to focus on automating as much of the process as possible, from booking to job completion.

I've created an MVP (Minimum Viable Product) architecture diagram, but I have many more ideas to implement. My focus is on getting the core functionality up and running, then iteratively adding new features in an agile manner.

<br>

![planned mvp digram](/images/heating-medics-be-arc.svg)

<h2>How the MVP is Designed</h2>

<ul>
<li><b>Form Submission:</b> The user submits a form, triggering a Lambda function that processes the data and stores it in a database.</li>
<li><b>Calendar Integration (Challenge):</b> The trickier part involves syncing available booking times with my phone's calendar. The idea is that events added to my Google Calendar will trigger a Lambda function to update the database, blocking off those times for bookings.</li>
</ul>

<h2>Additional Features</h2>

<ul>
<li><b>Frontend Postcode Checker:</b> A postcode radius checker on the frontend will determine if a user's location is within the service area. This will be implemented using a JSON-based hash map for fast (O(1)) lookups, ensuring a smooth user experience.</li>
<li><b>Dynamic Booking Calendar:</b> After passing the postcode check, users will see a calendar displaying available booking times fetched from the backend. This gives me granular control over the days and times offered for each service.</li>
</ul>

<h2>Mobile Calendar Integration</h2>

<p>The more complex aspect is integrating this functionality with my mobile calendar. Adding an event to my Google Calendar should automatically update the database, blocking off those times for bookings.</p>

<h2>The Road Ahead</h2>

<p>I have many more features in mind, but I prefer to start with an MVP, tackling smaller tasks and gradually adding complexity once the core application is functional.</p>

<p>If anybody has implemented anything similar with google calender would be interesting to hear.</p> 
