---
layout: post
title: Text Emergency Alerts Alerts
client: Intrawest
agency: Intrawest
date: 2017-05-30 01:43:50 
categories: [digital strategy, technology]
tags: [intrawest, technology, digital strategy]
excerpt: "A text message notification system for quick communication of incident data to a wide variety of groups."
featured-image: /images/qtsos.jpg
comments: false
author: 
 name: Steven Hubert
 twitter: stevenhubertron
 bio: Marketing Technologist and Digital Strategy Leader.
 image: sh.jpg
---


![QTSOS Messages Screen](/images/qtsos-messages.png)


### Opportunity

The opportunity to create this product came from a member of Winter Park's ski patrol team, Will, and was just too good pass up, especially when we knew it would be an easy bolt-on to the efforts already undertaken on the [QTA](https://www.stevenhubert.com/works/quicktrax-alerts/) customer notification app. 

When a safety issue, such as a skier's injury, arises on the mountain, the most common method of communication is your typical phone/CB radio tree. The ski patrol that is present on scene makes a call to his or her supervisor, who then calls persons A,B,and C depending on the situation. Will had a great idea to expand the QTA app to allow for private messaging groups to send one-way alerts at each stage of the safety-issue-escalation process. For example, if someone breaks his leg, the organization of the notification tree would be structured very differently than in the event something more serious occurred, and structured differently still in the event of a mechanical issue vs a personnel issue. Being able to define custom groups allows for easier and  more efficient escalation and communication paths. 

Given the urgent nature of these alerts, we opted to keep the UI as simple as possible and divide it into 3 major sections:

####Add Recipients
Put simply, this allows for the creation of users that can receive text messages.

####Create/Edit Groups
User can assign the previously added recipients to specific notification groups.

####Send Message
User can select the desired group, send the message with logging of messages sent

As you can see, simple and straightforward. This product isn't revolutionary by any means, and there are many SaaS products that exist loosely in this space, but this app functions well for a ski resort's individual needs, for a nominal monthly cost (cost of message, plus modest hosting on Heroku).  And, at the end of the day, this application helps employees on the mountain to deal with urgent situations a bit more easily, hopefully resulting in better outcomes and improved overall satisfaction. 

The QuickTrax SOS product is currently rolling out across the Intrawest family of resorts: Winter Park, Steamboat, Stratton, Blue, Tremblant and Snowshoe, but will expand further as there is need.

Future expansion plans include providing an inbox for sorts? for incoming messages, but because this isn't a web interface that is monitored 24/7, a few more questions need to be answered before we can begin building that feature. Some ideas we have been throwing around include:


* Forwarding to a specific set of numbers responsible for management
* Push alerts via SafariEdgeChrome's notification tools
*   Email alerts, or perhaps a native electron app similar to Slack but much more lightweight. 


If you have additional ideas on this to share to make this app even better please let me know on [Twitter](https://twitter.com/stevenhubertron). 







