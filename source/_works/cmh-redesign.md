---
layout: post
title: CMH Heli-Skiing Website Redesign
client: Intrawest
agency: Intrawest
date: 2017-04-15 01:43:50
featured-image: /images/CMH/dreams.png
categories: [digital strategy, technology, development]
tags: 
  - Intrawest
  - Technology
  - Digital Strategy
  - Development
excerpt: "A complete re-envisioning of CMH's online experience built using the latest front-end technology and featuring a static site CMS."
comments: false
---

### History

The original CMH website was built on a very old version of Sitecore alongside our resort websites. It was a very heavy handed IT decision that didn't work well for CMH. Customers and CMH employees alike were not happy with the website. At times, in order to load the list of available heli-trips users, would have to wait full minutes. The site was also poorly organized because a UX designed for a ski resort was being forced upon a heli-skiing site. We also looked at click stream data and noticed customers we having troubling finding what they were looking for.


### The Project

![CMH Home](/images/CMH/CMH-Home.png)
*Homepage of new CMH website*

Through a number of collaborative working sessions with the CMH and agency teams we worked through a very detailed understanding of our customers’ flow through the website, including the type of information they are looking for and how to find more of it. We used our intuition and also tested small sets of users. Once these decisions were made, designs were created that attempted to solve the many UX issues outstanding with the old sites. We involved many team members to weigh in and to really challenge our assumptions and research in order to create a content hierarchy that balances the very different top user paths taken by those new to heli vs seasoned fliers. 


As we got ready to move into development we knew we wanted to go small, fast and nimble with this site. After the experience of having an overkill CMS, and a team with fairly technical chops the decision was made to go with the [JAMSTACK](https://jamstack.org/) approach to have a truly static site powered by APIs for both its feed and CMS data. To accomplish this we used [Contentful](https://www.contentful.com/) for the CMS, [Netlify](https://www.netlify.com/) for the hosting and building of of the static pages, and [Jekyll](https://jekyllrb.com/) as the build tool allowing for easily templating of the website.

A lot of time was spent getting the trip grid right. It had to be familiar to existing customers while also being much more usable then the old one. The CMH and agency team spent went through many iterations to get this right in the design phase, and as a result, it’s working splendidly.

![Booking Grid](/images/CMH/booking.png)
*Sample of the new booking grid*

The agency team also integrated a JSON feed that provided a mix of weather information from actual boots-on-the-ground observations and automated weather stations in order to provide an easy to understand view of ski conditions at lodges with additional specific lodge forecasts.

####Weather Reporting
![Lodge Weather](/images/CMH/lodge-weather.png)
*Lodge Weather*

![Lodge Weather](/images/CMH/weather-detail.png)
*Lodge Weather Details*

**Sample JSON**

  ```
  [{  
    "name": "Bobbie Burns",  
    "snowpack_depth": "400",
    "air_temp_high": "8",
    "air_temp_low": "-4",
    "snowfall_yesterday": "5",
    "snowfall_week": 67,
    "atmospheric_conditions": "Scattered cloud. Moderate V wind.",
    "timestamp": "2017-04-23T00:00:00.000-06:00"
  },
  {
    "name": "Bugaboos",
    "snowpack_depth": "350",
    "air_temp_high": "6",
    "air_temp_low": "-5",
    "snowfall_yesterday": "15",
    "snowfall_week": 82,
    "atmospheric_conditions": "Snowing <1cm/hr. Light W wind.",
    "timestamp": "2017-04-23T00:00:00.000-06:00"
  }]
  ```

### The Results

The site launch only just occurred, so conversion based results are hard to report on a this time. I can say that by going with the JAMSTACK approach we were able to accomplish a lot more on a very limited budget while also giving customers a completely new experience that helped them understand what a CMH trip is like on a screaming fast responsive website. Both CMH and the c-level team are impressed with the design, usability and of course the budget that we were able to hit.

