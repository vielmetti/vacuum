---
title: What is your superpower?
date: 2021-03-14
draft: true
author: Ed Vielmetti
---
What's your superpower, and what routine do you do to invoke it?

I am convinced that everyone has a superpower, a special
set of talents and experiences that they are especially
well placed to get exceptional outcomes. You might not
know yet what that superpower is, but once you discover
it there's an opportunity to build on top of it.

In the past I've picked up some of my own little habits
that accumulated over time that look like superpowers, in their
own way.

## Postcards

I like writing postcards to people who send me postcards in return.
This is a fun way to have slow-motion correspondence as well
as to keep a stream of pictures to put up on the fridge.

I learned this habit from [my grandfather], who would send hastily scrawled
cards to his grandchildren when he was on geological expeditions.
Grandpa Kay's cards usually had rock outcroppings on them. Now my kids
send cards to their grandmothers.

[my grandfather]:https://www.geosociety.org/documents/gsa/memorials/v07/Kay-M.pdf

When I was travelling a lot in the 1990's, there was a
genre of "airport postcards", sold only in airport gift
shops and featuring aerial photos of those airports. In
the pre-Internet of airplanes there was a lot of time to
write in the air.

## Paper rolodexes

I keep a few paper Rolodexes to go with my electronic directories.
Even the best of the contact management tools can't beat the
tactile discovery of hand-written notes about your friends,
acquaintances, and colleagues - little cards to jog your memory.

Online contact management tools have not gotten better over time.
The "CRM" systems that proclaim that they do contact management
got turned into sales funnel and forecasting systems, and they
do a lousy job of actually helping you do anything except
sell things to people. All of the "personal CRM" stuff I've
seen to date is pitched squarely at 20-somethings who are dating
in Silicon Valley. LinkedIn ate your carefully constructed list
of professional colleagues, and sold it back to you.

Paper rolodexes are awkward, bulky, hard to find and easy to
get out of date. They will never be as shiny as LinkedIn.
That said they are great and I highly recommend the next time
you find yourself in a thrift store to see if you can score one.

## Organizing lunch

I organize [a lunch group] that's been meeting for a dozen years.
This group has stuck it out through a year of pandemic so far,
and still has a regular Zoom call - though I can't always make
it, there's a steady pace of friends keeping in touch until
they can meet again in person.

[a lunch group]:https://groups.io/g/a2b3

At first the lunch group was very small, and we could meet anywhere.
The great idea was to do a tour of all of the Korean restaurants
in Ann Arbor, which easily had multiple months of a new bowl
of bi bim bap every week. As the group grew I started a mailing
list (see a pattern here?). When the Great Recession hit, everyone
suddenly had time for lunch, and one week we had 35 people show up.
Fortunately the restaurant (Eastern Accents in Ann Arbor) was
very accomodating.

The economy got better, and the restaurant closed, and the lunch
group got a lot smaller - mostly people who were either working
independently or who are retired. The pandemic stopped our in-person
meetings but we carry on with Zoom. I can't always make lunch
because of my current jobby-job but I try, and I look forward
to seeing folks again.

## Writing for publication

At one time, I regularly met a daily 500 word noon deadline. I'm not
sure yet how I'd do that again, but I'd love to try.

There was a time that I could reasonably sit down in a cafe,
order a fine cup of coffee, and produce publishable work at
about the cost of a penny of coffee per word. Fancy coffee
and the warm ambiance of a cafe both helped this effort. I
haven't yet determined how to replace the cafe in my own
house.

There's a lot to be said for the German word "sitzfleisch",
the ability to sit still for a long time and focus on one
task. Writing takes focus and stamina and that's very hard
to find in a world of continuous interruption and
[continuous partial attention].

[continuous partial attention]:https://lindastone.net/2009/11/30/beyond-simple-multi-tasking-continuous-partial-attention/

## Bug finding and fixing

Filing and fixing bugs - that's more for another story, since it's a
technological superpower. There were a whole lot of bugs and requests for
help that happened during the course of my last big project. Understanding
how to gain the interest and trust of an open source project to recruit
people to test and patch and test again is a fine art that can be learned.

My favorite kinds of bugs have to do with the things you discover
when taking old code and making it run on a new system, or taking
new code and making it run somewhere the inventors haven't thought
of going yet. The sort of bugs you find are often tiny configuration
issues, where the code works easily as soon as you teach it just a
little bit about a new machine.

More rare are the mysterious bugs, where the behavior looks
flaky rather than predictable, and the underlying cause is
far, far away from the observed behavior. My favorite was
the [go pagesize bug on arm64]. The observation was that Docker
was mysteriously crashing in CI/CD environments. The code revealed
eventually that Go was picking a fixed page size, and while that
constant was correct in RHEL and CentOS, it was wrong on Ubuntu.
The fix involved writing the necessary tests to make the crashes
repeatable and not mysterious.

[go pagesize bug on arm64]:https://github.com/vielmetti/go-pagesize-test
