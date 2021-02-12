---
layout: post
title: "Quantifying Friendship"
date: 2021-01-27
tags: facebook EDA analytics
author: Aliya
---

Continuing my previous post on analyzing Facebook Messenger data... We're about to get a little bit more personal! My last entry focused on macro-level EDA - things like overall chat volume and sentiments, comparing different behaviors in different threads, and finding correlations. For this post, I've decided to pivot and focus on just one person to see if I can find any fun insights on our friendship over time.

## The backstory

Meet Sender_6. Sender_6 is a college friend, someone I've known since the very first day I set foot on Carnegie Mellon's campus in 2013. We hit it off during orientation, when he grilled me on my life choices, judged my character flaws mercilously, and flooded me with film trivia that to this day, never stops. (He has graciously agreed to serve as my test subject and allowed me to post this analysis online.)

Let's dive in with a brief timeline overview.

![Timeline]({{site.url}}/assets/facebook-deepdive/image-1-timeline.png)

Given this backstory, I was floored to find out that we didn't text each other over Facebook until 2014. This meant that we either used SMS texting (lame) or didn't text at all (more lame) for up to six months before transfering to Facebook. And anyway clearly we didn't text all that much at that point - under 200 messages a month until the summer. We see our first peak in the summer of 2021 for what we can assume to be two reasons: 1) off-campus lives meant no in-person interaction and 2) I was abroad for much of the summer and physically couldn't send an SMS.

Our text volume really peaked in 2016. I had my first breakup over the summer of that year, forcing me to lean on my support network while I was interning in a brand new city all by myself. Sender_6 and I stayed close, and got even closer at the end of that year, halfway through our second to last semester on campus.

After graduation, we moved to different cities, but stayed in touch! You can see that our data for 2017 through 2020 is cyclical, suggesting a, dare I say, _deliberate_ effort to check in with each other every few months for life updates. We also see another peak in mid 2019 for more breakup support, and another in right at the end of 2020 as we start bouncing ideas off each other for this very analysis.

## Sentiments

As mentioned in my previous post, I wanted to do a deeper dive in to the vaderSentiment package and get a better understanding of how it scores different messages. First, let's check the obvious - who's the optimist in the group?

![Sentiment]({{site.url}}/assets/facebook-deepdive/image-2-sentiment.png)

As it happens, both and/or neither of us? It looks like overall we match each other quite well. We both hover around the 0.12 mark for compound score ratings, each taking turns dipping above and below without any major changes.

A few of our most positive messages included:

![Positives]({{site.url}}/assets/facebook-deepdive/image-3-positives.png)

And a few of our most negative ones:

![Negatives]({{site.url}}/assets/facebook-deepdive/image-4-negatives.png)

## Who's the bigger talker?

Sender_6. Hands down. Sender_6 sent a whopping **13,303 messages** to my 9,764. Does this just mean he's a spam-texter with limited content per text? Sending **474,247 total characters** to my paltry 284,761 points to a no. In fact, if anyone sends short texts out of the two of us, it's actually me - averaging 29 characters per text to his 35.

In all honesty this is actually a pattern across all of my friendships - I send shorter texts, fewer characters, and fewer messages than most of my friends. As much fun as it may be to roast Sender_6 here, I think the real fault for the imbalance here might be mine.

## Quirks

On a more positive note, let's take a look at emoticon. Facebook doesn't store emoji in a usable format so there's not much to say here, but luckily I still prefer to go old school and drop in a ":)" now and then. The data supports this:

![Emoji]({{site.url}}/assets/facebook-deepdive/image-5-emoji.png)

Sender_6 also prides himself on avoiding profanity altogether. While he might not pass my better-profanity package's fifth-grade-teacher standards, his stats still make me look like an angry sailor by comparison.

![Profanity]({{site.url}}/assets/facebook-deepdive/image-7-profanity.png)

My last insight was minor but caught both of us off-guard: we barely text on weekends. In retrospect, this makes sense given our office jobs (and my current grad student status), but it's probably not data we should be showing off to future employers.

![Weekdays]({{site.url}}/assets/facebook-deepdive/image-6-dayofweek.png)

## Conclusion

I don't know if this is because I've been looking at the same data for so long, but very few of these findings feel out of the ordinary. Sender_6 and I could have probably predicted most of these results spot on, but there is still something to be said for seeing the quantifiable results on paper.

How much of this can be taken further? Could we argue that with a current average text volume of 200 messages per month, we're 80% less close compared to our peak in 2016? I don't think so. In some more malicious parts of the internet, this type of analysis could be applied to policing friendship, tracking behavior and engagement with the precision of a marketing analytics tool. In this case, I prefer to stick to the findings that bring me joy - at over 20,000 messages sent back and forth over 8 years and counting, I can be pretty confident we'll be friends a long time to come.
