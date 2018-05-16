---
layout: page
title: Projects
permalink: /projects/
---

## [Reactathon] 2018
---
#### **React Native, AWS, GraphQL** | *24 - 25 March 2018* |  Github HQ, San Francisco, CA
[NoTow] is the result of the remarkable effort of [Chris McDermut], [Maria Nguyen], [Taylor Harwood]
, [Mariia Rudenko], [Gabe Levasseur], with a sprinkling of assistance from yours truly. The app,
written in [React Native], prompts the user to take a picture of a street sign, and will tell them
whether or not one can park there worry-free!

How does it work, you ask? It's pretty straightforward!

The user's GPS coordinates, along with a timestamp, are stored with [GraphQL], which was a dream to
set up using an amazing new service, [Hasura]. This information is captured in our MVP with the
intent to eventually build out a feature which alerts the user when they should head back to their
vehicle so they don't get a ticket.

Next, the image is sent to a text-parsing [lambda], which communicates the image to Amazon's
[Rekognition] API, does a bit of data massaging/sanitization, and forwards some of the
freshly-parsed image text along to another lambda, which serves as a "rules engine." Separating
this first step from the "rules engine" gave us the opportunity to tell the user that we were
unable to parse text from the image before we even attempt to process anything, shortening the wait
time for users, and preventing us from running data through our second lambda unnecessarily.

Finally, assuming we were able to get text from the user's image, our "rules engine" lambda parses
through the sign's text, and pretty much just spits out two pieces of information:

1. a boolean representing whether or not the user is able to park there right now, and
2. a string stating approximately how much time they are able to park there before they might get a
ticket.

This information is passed back to the original lambda, which then responds to the front end of our
application with the information it needs to help the user make the right choice.

Ultimately, we placed second among a total of 21 submissions, something I am immensely proud of,
especially considering it was the first competitive hackathon in which my work played a nontrivial
part (I wrote that rules engine I mentioned earlier.) I am also extremely proud of my team; for
many of them, this was their first hackathon experience, and despite it they all made significant
contributions to the project.

![](/assets/notow-team-interview.jpg "Congrats, team! 😁 You earned it!")


## Adventure Assistant
---

#### **ES6 with React, Node, Karma, others** | *February 2016 - Present*

Adventure Assistant is an ongoing, multipurpose personal project. One goal of this
currently-web-based tool is, for tabletop RPGs such as Dungeons & Dragons, to reduce the amount of
time spent pausing gameplay to handle necessary bookkeeping with pencil and paper. Based on my
experience and expectations of these kinds of games, I feel that a primary objective is immersive
storytelling. I plan to eventually add a section of my website dedicated to explaining Adventure
Assistant in greater detail.

In the meantime, check out [Adventure Assistant on Gtihub]


<!-- Turn into a Post at a later date
I began a campaign with some friends relatively recently (just shy of a year before beginning work
on Adventure Assistant) and found that I mostly enjoyed the storytelling aspect of the game.
Silly as it might sound for a fantasy world, I have found a certain degree of realism is fairly
crucial for my personal immersion. Hauling around thousands of coins of varying metal without
consequence, while convenient, made very little sense to me, for example.
-->

## An Hour of Code
---

#### **Scratch, Python** | *December 2015* | Apple Store, Berkeley, CA

An Hour of Code is an annual worldwide event encouraging young people to dive into the world of
coding. Promoted by many companies and individuals in the tech industry, the event's origins lie in
a relatively new organzation, [Code.org]. In 2013 I was inspired enough to host my own hour of code
via YouTube streaming, but shortly after posting the video to my channel I removed it, realizing
only afterward that I had not downloaded a copy of the video.

Luckily, I got another shot, as I had the opportunity in the 2015 Hour of Code
to teach kids the fundamentals of programming on behalf of Apple! It was an
incredibly fulfilling experience. Children as young as three (with surprisingly
minimal guidance from their nearby parents/guardians) seemed not only to
understand the concepts in the carefully crafted form in which the information
was presented, but also deeply enjoy the activities provided by Code.org.

Some of the older children had participated in similar events in the past, and with them my
co-instructors and I were able to dive a little deeper, breaking down more complex analytical
problems while learning the fundamentals of Python.


## BattleHack Los Angeles
---

#### **HTML5, JavaScript, JSON** | *28 February 2015 - 1 March 2015* | Santa Monica, CA

This event, organized by [Braintree], was a blast. Going into the hackathon without a team, I knew
that I would face challenges. After forming a team with some colleagues from school (who I was not
expecting to be there) we got to work hashing out ideas. Eventually, we decided on building a web
platform designed to assist non-profits in connecting with their target audience.

Despite deciding to axe our project at the very end of the competition, I had a great time and
learned tons. Ultimately, this project was a great learning experience, and I came away from the
event with an idea I hope to pursue and build upon in the future.


## Conway's Game of Life
---

#### **Java** | *10 January 2015 - 14 January 2015*

The Game of Life is one I had been meaning to get around to for a while. Naturally I decided my
birthday would be a great day to start a new project. Day one included very little productivity,
however by day two I had a functioning game which relied on the command line to convey game data,
with a poorly-constructed ASCII universe. Day three brought a GUI into the mix, and day four brought
significant optimization to the game. Conway's Game of Life, while relatively simple, was a fun
problem to solve!

## Introduction to Computer Science
---

#### **Swift** | *4 January 2015* | Apple Store, Berkeley, CA

A lecture taught by yours truly, to a few dozen Apple employees! My primary goal was to provide both
a deeper understanding of computer hardware and software, and give an overview of the programming
process, with a brief live demonstration of some simple scripting in Swift. Overall an awesome
experience, this opportunity strengthened my own existing knowledge of the topics discussed,
and helped to improve my public speaking skills. Despite having two years of experience with improv,
from a club in high school, and despite spending the second year as president of said group, I don't
consider public speaking one of my strong suits.

Feel free to [download the slides] from my personal Dropbox!

## Ludum Dare 30
---

#### **C#** | *22 August 2014 - 25 August 2014*

My first experience with a game jam, Ludum Dare was an awesome adventure. A 48-hour (competitive,
solo) or 72-hour (relaxed, group) game development hackathon, I viewed Ludum Dare as a great way to
put my rapid development skills to the test.

Teaming up with the invaluable Anthony Becker ([@b_cker]) and the
indispensable Bethany Barker ([@BethhhJB]), Earth<->Krethys was born. A 2-D platformer with a
twist; as Kale you have the ability to traverse between two parallel but vastly differing worlds,
and use this unique skill to complete each level.

I learned tons, had a blast, and did so with great company. I can't wait to do this again.

Check out [Earth<->Krethys on Gtihub]!

## Machine Learning Research Project
---

#### **Python, C++, MatLab, Java** | *April 2014 - March 2015*

With oversight and mentoring from Dr. Ehsan Kamalinejad, Professor of Mathematics at CSU East Bay,
and alongside Anthony Becker ([@b_cker]), the purpose of this research work is to explore the realm
of Artificial Intelligence and Machine Learning, and their real-world applications.

I worked primarily with Dr. Kamalinejad on a utility which gathers data from [Rate My Professors]
and tries to predict whether or not you will enjoy taking a course with a professor. The
technologies utilized include Python, [Beautiful Soup], and [SQLite] for data collection and
storage.

## GameGame, the Game
---

#### **C++** | *August 2013 - December 2013*

One of my first large-scale* personal projects, my objective with this oh-so-creatively-named
text-based adventure game was to familiarize myself with the language. Having moved from Southern
California, and a community college which favored Java, to Northern California and CSU East Bay
(which favors C++) I deemed it necessary to give myself a self-driven primer of the latter of the
languages. This project was a valuable introduction to both the importance of personal projects, and
the C++ language.

###### *large-scale, at the time, meant over 2000 lines of handwritten code

Check out [GameGame, the Game on Github]!

## Hack for Change 2012
---

#### Tiny amounts of **Objective-C** | *July 2012* | San Francisco, California

As a programming newbie, with more textbook knowledge than practical knowledge or experience, I dove
into this headfirst knowing all too well that I would probably be completely overwhelmed. All the
same, I decided rather on a whim that this was going to be my first hackathon. I was hungry for
experience, and figured that it would be an amazing opportunity, even if it meant just watching over
the shoulders of the experts I was certain would be present for such an event.

[Hack for Change], hosted by [Change.org] did not disappoint, and thanks to the endless patience of
Frederic Jacobs ([@FredericJacobs]), I didn't feel *completely* useless. Working with a team of a
little over [half a dozen extremely talented people], we managed to put together a mobile
application called LivePort, an instant, live reporting tool designed to help people in conflict
areas stay safe.

Our submission took home an API award from [tokbox], for best use of their OpenTok API!

Check out [LivePort on Gtihub]!

---

##### Last updated June 2016

[//]: # (People!)
[@b_cker]: https://twitter.com/b_cker
[@BethhhJB]: https://twitter.com/BethhhJB
[@FredericJacobs]: https://twitter.com/FredericJacobs
[Chris McDermut]:
[Maria Nguyen]:
[Taylor Harwood]:
[Mariia Rudenko]:
[Gabe Levasseur]:

[//]: # (Websites / Project links!)

[//]: # (Reactathon 2018)
[Reactathon]:https://www.reactathon.com/hackathon
[NoTow]: https://www.pleasenotow.com
[React Native]: https://facebook.github.io/react-native/
[GraphQL]: http://graphql.org
[Hasura]: https://hasura.io
[lambda]: https://aws.amazon.com/lambda/
[Rekognition]: https://aws.amazon.com/rekognition/

[//]: # (Adventure Assistant)
[Adventure Assistant on Gtihub]: https://github.com/nrebhun/AdventureAssistant

[//]: # (Hour of Code 2015)
[Code.org]: https://www.code.org

[//]: # (BattleHack Los Angeles 2015)
[Braintree]: https://www.braintreepayments.com
[charitable.com on Gtihub]: https://github.com/nrebhun/charitable.com

[//]: # (Apple Lecture)
[download the slides]: https://www.dropbox.com/sh/qxalap2n5j07vgn/AAAMjSHV83sr5Xy2gdD_9j16a?dl=1

[//]: # (LD30)
[Earth<->Krethys on Gtihub]: https://github.com/nrebhun/Earth-Krethys

[//]: # (Research Project)
[Rate My Professors]: http://www.ratemyprofessors.com
[Beautiful Soup]: http://www.crummy.com/software/BeautifulSoup/
[SQLite]: https://sqlite.org

[//]: # (GameGame the Game)
[GameGame, the Game on Github]: https://github.com/nrebhun/Gamegame

[//]: # (Hack for Change 2012)
[Hack for Change]: https://hackforchange.org/
[Change.org]: https://change.org/
[half a dozen extremely talented people]: https://twitter.com/liveporting/status/229735173120458752
[LivePort on Gtihub]: https://github.com/FredericJacobs/LivePort-iOS
[tokbox]: https://tokbox.com
