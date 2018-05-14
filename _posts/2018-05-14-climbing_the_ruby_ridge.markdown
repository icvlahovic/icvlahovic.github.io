---
layout: post
title:      "CLImbing the Ruby Ridge"
date:       2018-05-14 04:29:59 -0400
permalink:  climbing_the_ruby_ridge
---


It looms off in the distance, a daunting mountain, awesome and formidable, casting an omnipresent shadow on its surroundings.  All roads lead to its mysterious, cloud-shrouded summit; no roads wind around its base to the other side.  The journey over is long and tedious, often frustrating and arduous, but this is the only way forward in your quest, and you know that sustenance and bounty lie just beyond.  Fortunately, you have ample gear and provisions, experienced guides to help you, and an unwavering sense of adventure and determination.  You can picture the view from the top in your mind’s eye, and it is truly spectacular!   You can, you must, you **WILL** conquer this titanic colossus…all you have to do is take the first step and start the slow march forward!  Which great peak is it, then?  Everest?  Kilimanjaro?  Denali?

<iframe src="https://giphy.com/embed/yKthZMxnPo84o" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/everest-yKthZMxnPo84o"></a></p>

Oh.  It’s just your first Flatiron Project, building a CLI Data Gem.

I’ll admit that this metaphor might be a bit excessive.  **SPOILER ALERT:** in hindsight, working on this project was actually a lot of fun, and finishing it in a timely manner was less of a hassle than I initially made it out to be.  However, a few short weeks ago, it seemed to be a much taller task: how could I, a novice programmer, possibly build a working application?  Moreover, how could I possibly build a working application without an idea for a working application?  I have so much going on in my life!  How could I possibly find the time to think of an idea for an app and then build that app?!  I just couldn’t even.

<iframe src="https://giphy.com/embed/npU3G4FMQtYLm" width="480" height="269" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/i-cant-npU3G4FMQtYLm"></a></p>

Another **SPOILER ALERT:** I survived (I often tend towards the dramatic).  [This blog post](http://blog.flatironschool.com/5-steps-finishing-coding-project/) by Josh Owens was particularly helpful starting point.  I definitely recommend reading it before starting the project, or if you’re stuck like I was with no idea where to begin.  I particularly liked his tip about “finding pain points in your own personal life” and turning them into simple solutions to a problem.  Maybe there are things that bother you about existing technology—why isn’t there an indicator on the dashboard of my car that tells me when one of my lights goes out?  Get on it, Elon Musk!—or things that don’t exist yet, like an EZPass for street parking in New York City.  Parking meters?  How neanderthal!

<iframe src="https://giphy.com/embed/Lqf80ZDBNyhpe" width="480" height="323" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/technology-Lqf80ZDBNyhpe"></a></p>

Sadly, I realized I was not (yet) capable of creating those things, nor would they satisfy the project requirements, so I hunkered down for a “brainstorming session” (definitely NOT scrolling through my Facebook News Feed and Googling random things).  As it would happen, I came up with my idea while visiting one of my new favorite websites, [The Wirecutter](http://thewirecutter.com).  For the uninitiated, The Wirecutter is a subsidiary of The New York Times and provides arguably the most extensive and thorough product reviews available on the Internet…and unlike Consumer Reports, it’s totally free!  Looking for a new pair of headphones?  [They’ve got you!](https://thewirecutter.com/?s=headphones)  How about a Nespresso® machine?  [They’ve got you!](https://thewirecutter.com/reviews/best-nespresso-machine/)  Need a dog harness?  A knee brace?  A water gun?  A CAR?!  [THEY.](https://thewirecutter.com/reviews/best-dog-harness/)  [HAVE.](https://thewirecutter.com/reviews/best-knee-brace/)  [GOT.](https://thewirecutter.com/reviews/best-water-gun/)  [YOU.](https://thewirecutter.com/cars/passenger-cars/)  

But what they DON’T got…is an app!  

<iframe src="https://giphy.com/embed/xFmyBmvtETTwLWHAPW" width="480" height="480" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/latenightseth-seth-meyers-lnsm-xFmyBmvtETTwLWHAPW"></a></p>

I know, I was a little surprised, too!…but then I said to myself, “Maybe I could build that….”  I’m still nowhere near the level of programming ability to build the entire thing myself, but I COULD start with something relatively simple: scraping the data from the headline article and associated research and displaying it so I could read it in my Terminal. 

I’ll spare you the details of my work flow—which involves spurts of productivity punctuated by frequent breaks and numerous four-letter words—but I will say that I started by coding along with [this video](https://www.youtube.com/watch?v=_lDExWIhYKI) made by Flatiron School founder Avi Flombaum.  It was incredibly helpful at the very beginning of the building process, especially as far as creating the framework for the gem and understanding how my objects should work together to yield a working application.  Once I had my basic structure in place, it was fairly simple to plug in my own names and build out my Classes.  Scraping the website was by far the most tedious part of this project; omit one little selector in your Nokogiri CSS statement and you’ll either end up with a whole slew of information that you don’t want, or with absolutely no output at all!  All in all, I probably put a cumulative 6-8 hours of work (spread over three days) into the app, but at the end of it, I was amazed and proud to see that I had a working version of what I set out to create!

…and then everything broke.

<iframe src="https://giphy.com/embed/SqtUeHelzv0Pe" width="480" height="441" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/jessica-jones-SqtUeHelzv0Pe"></a></p>

I had inspected The Wirecutter’s HTML every day for a week before and while I built the app to confirm that it was consistent.  I had taken meticulous notes on which CSS selectors I should use to parse only the necessary data and nothing superfluous.  Everything had functioned exactly to my specifications for three days in a row.  And yet when I ran the program one morning, there was no website data output to my console; NONE of the scraping methods worked.  Obviously, I freaked out for a few minutes, pulling my hair out and frantically checking my code to see if I had accidentally changed something.  

<iframe src="https://giphy.com/embed/fQZX2aoRC1Tqw" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/fQZX2aoRC1Tqw"></a></p>

I hadn’t, but upon inspecting that specific article’s HTML, I realized that one of the programmers at The Wirecutter had: this article had entirely different code from its predecessors!  I decided on a fairly quick fix and created a new `alt_text` variable within my `#self.display` method that scraped the same content using this newly named set of tags without eliminating my original code that had worked up to this point.  My hope is that the good folks over at The Wirecutter won’t throw any more monkey wrenches into—aaaaaand speak of the devil, I just had to debug something else (this time, they decided to change a `<div>` to a `<section>`!), but I suppose this is just a part of the learning process.  Things will break, and it’ll be up to you to figure out how to fix them.  It’s initially frustrating, at least for a perfectionist like me who would prefer that everything go exactly as planned on the first run without a single hitch, but eventually, you catch a sort of stride: something doesn’t do what you’d like it to do, you diagnose the problem, and you (hopefully) solve the problem.

I’m glad that what started out as a fairly intimidating project assignment turned into a great learning experience and a finished product that is truly a source of pride to me.  This must be how a new parent feels when they look at their baby and think, “Whoa…I made that!”  And in a way, a new computer program is a lot like a baby: it needs to be fed (data), it needs to be taught how to do things (methods), and occasionally it cries (error messages) because it needs its diaper changed (debugged).  But it’s a beautiful little work in progress, and one day, the effort you put into it while it’s young will pay off when suddenly, it’s all grown up and has learned how to behave properly and has really blossomed into a fetching young program after that awful adolescent phase…maybe it’s even making millions of bucks and cutting you in like any good child would!  Early retirement…that’s the goal, right?

<iframe src="https://giphy.com/embed/yYXEQeTsoh2rS" width="480" height="400" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/rich-yYXEQeTsoh2rS"></a></p>

If you’d like to check out my project, feel free to do so [here](https://github.com/icvlahovic/wirecutter-daily-headline).  I’m going to continue to build it out in my free time, but I’m open to any and all suggestions.  Fork it, clone it, give it a whirl, and let me know what you think!



