---
layout: post
title: Bootstrapping a custom snow, lift, and weather reporting API/service
client: Alterra Mountain Company
agency: Alterra Mountain Company
date: 2020-05-30 01:43:50
categories: [product, digital strategy, development]
excerpt: "Mountain Powder was developed because of a need to provide a unified solution to allow on mountain staff to report on mountain conditions as they change through the day. No off the shelf solution existed and this custom solution addresses all of Alterra Mountain Company's use cases."
featured-image: /images/thumbs/mtnpowderthumb.png
comments: false
---

### Overview

Mountain Powder is a complete business-critical system for all Alterra Mountain Company resorts to report on key mountain information in one centralized place before being distributed across many channels for consumption by the end user.

This product has evolved significantly from the initial problem this application sought to solve, and it has become a key part of the infrastructure at Alterra Mountain Company that informs customers and BI reporting systems.

### The Problem

Reporting daily on mountain conditions such as new snowfall, temperature, snow conditions, lift, trail, and activity status was a major chore for snow reporters and webmasters. With the previous setup, they would have to log into multiple systems every day, revising multiple fields in order to update their websites/emails on a site that was further limited by functioning only on the desktop computers for a limited set of browsers.

### The Solution

Build a responsive admin panel that served as the single point of truth for all relevant mountain statistics. A system that allows a snow reporter to update data in a single location and have that data update the website, email, text message, Alexa App, and other 3rd party consumers of the website

#### Approach

This project started the old-fashioned way: Sketches on a whiteboard, followed by markers on paper. Each of our six resorts reported on snow/weather slightly differently so many, many rounds of presentation/feedback/revision were necessary in order to determine the best UI and relevant data points that each resort required in order to communicate to their guests consistently and easily. Nailing the UI was pretty easy (the bar was quite low here), but agreeing on a consistent list of snow conditions proved to be difficult.

![Winter Park’s Snow Reporting in Tablet View](/images/QTA/Screenshot%202017-05-05%2010.15.55.png 'Winter Park’s Snow Reporting in Tablet View')
_Winter Park’s Snow Reporting in Tablet View_

What is being shown here is the interface the snow reporters use in order to update the mountain information everyday. It’s not a public facing view, and is only used for data entry. The intent was to be able to update as much as one can with the least amount of clicks. The old system required clicks into each item in order to update. This new layout, while very busy, makes it very easy to update many rows in one fell swoop. A key requirement of the now reporting team.

![Winter Parks Trail Reporting in Tablet view](/images/QTA/Screenshot%202017-05-05%2010.17.30.png 'Winter Parks Trail Reporting in Tablet view')
_Winter Parks Trail Reporting in Tablet View_

In addition to creating Snow/Lift/Trail/Activity reporting, the application also consumed weather feeds from our stations on the mountain. Prior to this project many ad-hoc weather station systems were set up. Through the course of this project the team migrated all of these stations to report from Aeris Weather. [Here](https://www.pwsweather.com/station/pws/basearea) is an example of Steamboat's Base.

Once all weather stations were migrated the app then pulled feed data from Aeris to the Mountain Powder app. From here, the app allowed snow reporters to override the data

![Winter Park Squirrels - Thanks to Patrick D for the photo](/images/QTA/Unknown.jpeg 'Winter Park Squirrels  Thanks to Patrick D for the photo.')
_Winter Park Squirrels Thanks to Patrick D for the photo._

The app provided this functionality because on mountain weather can be quite extreme, weather stations can freeze over with rime ice during as storm and report 32° when it’s actually -10° out. The anemometer can break so the wind say 0 MPG when it is really gusting at 80. Or, a hungry animal can get in the way and break the feed to the internet. This override feature allows snow reporters to address any of these situations while still providing accurate information to our customers.

The last problem solved for the reporters by this tool is audit logging.

![Overrides](/images/QTA/Screenshot%202017-05-05%2010.38.27.png 'Overrides')
_Override Options_

Previously, every time a reporter updated the report he or she printed up the updated page and added it to a file cabinet. So, there were literally reams of paper that showed when snowfall increased half an inch that change got printed up and filed. This had to be done for legal reasons as there was no other way to prove whether there was an update or not. The new Mountain Powder system provides a reporting tool that lets you select the category of changes you are interested in, plus the time range and you can download a detailed log of each and every change.

![History Download](/images/QTA/Screenshot%202017-05-05%2011.14.53.png 'History Download')
_History Download_

To recap the benefits for the reporters, this tool now allows them to update all mountain information in one place, lets them update anything from their mobile device and saves them time and paper printing up each and every change. These benefits alone would more than justify the development effort here. However, many customer benefits were also gained by this effort.

#### Customer Benefits

The most outward benefit is, of course, accurate weather reporting and mountain conditions on our redesigned websites. Users have basically an operations panel outlining the status of the mountain on one easy-to-understand page. [https://www.bluemountain.ca/mountain/conditions-report](https://www.bluemountain.ca/mountain/conditions-report)

![Stratton Weather Page](/images/QTA/Screenshot%202017-05-05%2011.23.59.png 'Stratton Weather Page')
_Stratton's Weather Page_

This page is powered by a JSON feed (with an XML feed also available) that powers many other customer facing experiences including….

![Printable Report](/images/QTA/printable.png 'Printable Report')
_A printable trail report used at the front desk of local lodging destinations_

![Digital Signage](/images/QTA/signage.png 'Digital Signage')
_Digital Signage used at the resorts._

![Winter Park Email](/images/QTA/Screenshot%202017-05-05%2014.15.33.png 'Winter Park Email')
_Winter Park Email Integration_
The app is also integrated with Watson (IBMs) Marketing Cloud API so that the data is included in the daily snow report email that our resorts send out. The app write to a DB table with updated data on a set publishing schedule, and then the data in that table gets automatically populated into the email and delivered to the customer.

<iframe width="766" height="431" src="https://www.youtube.com/embed/JhiBijpIYgA" frameborder="0" allowfullscreen></iframe>
 
Custom feeds were created that allowed us to create a custom Alexa Notification that can be added to customers flash briefing for an up to date description of the conditions at the Alterra Mountain Company resort of your choice. The creation of this app allows for seamless integration into your news day.

![Alert Signup](/images/QTA/Screenshot%202017-05-05.png 'Alert Signup')
_Text Alert Signup_

Lastly the website [http://alerts.quicktrax.com](http://alerts.quicktrax.com) was created to allow customers to sign up for text message alerts when specific user-selectable thresholds were met. For example if I wanted a photo of the snowstake whenever there is snow I can sign up for that, or if I only want to know when 12” has fallen, or is expected in the next 48 hours, I can sign up for those as well. This website allows our pass holders to rest easy knowing that they will never miss a powder day.

We knew it would be sensitive getting users to give their phone numbers to us, so I worked with our legal team to specifically create a wall between this website and our other more marketing-specific websites. Any phone number entered here will NEVER get spammed by us or sent any sort of marketing messages. This is a strictly transactional website. Customers get what they requested, nothing more, nothing less. Sign-ups here have been extremely successful with well over 100K text messages being successfully delivered every month of the season. If you are a skier and go to our mountains this is a fantastic app to sign up for as it stays out of your way when it isn’t snowing.

### Conclusion

As you can see, what started out a simple app to make the Snow Reporter experience more efficient turned out to become a multi-faceted product that provides value to our customers through a large number of verticals. Through smart planning and extensible technology the product was able to deliver a product that can work for users on their terms. I’m extremely proud of how this came out and look forward to many years of usage at all of our resorts.
