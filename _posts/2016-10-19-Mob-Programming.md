#Mob programming – an obvious use case:

I attended a talk by Woody Zuil on Mob Programming at Agile NE a few weeks back, and I thought he made a fairly compelling argument for why it could help, as well as clear instructions on how to set up a session. There was also a partially written book available on discount (which I bought) and I thought I’d give it a go at the next opportunity at the UK public body where I ply my trade. I don't talk about them, but you can think of them as the 'Department for Necessary Evil' if that helps.

The opportunity arrived fairly swiftly. I’m a member of a team that has been producing a substantial body of code using ‘traditional’ techniques; that is, not TDD. The test coverage is not great and much of the code has become encumbered with a lot of tech debt.

One large class in particular was the focus of the last sprint. Three separate teams worked on it and because git does not handle Scala test files particularly well the merge was painful. The current sprint is focused on extending the functionality of the class even further and it seemed like an opportunity for a well thought out refactor.

I talked to each of the other devs individually and discovered that all of us agreed that a refactor could be helpful. So on a recent Friday we were able to carve out enough time for an hour long architectural discussion on how we might approach it. Towards the end of the time I floated the Mob approach and since nearly everyone would be sitting around waiting for the refactor to complete before we could move on, it was pretty easy to get most of the devs on board. We time boxed it for Friday afternoon.

We ended up with five people fully participating and two others dropping in to listen. I went through the basic instructions and we kicked off for a three hour session with one short break. There was a clear goal and we had an approach outlined. By the end of the session there was obvious progress although not as much as I would have liked to see given the time spent. Despite this, it was successful enough that we decided to extend the time box through to Monday lunchtime. Monday had four people participating by which point there was enough working, tested code that we could easily split into pairs to finish the work.

How did it work out? Inevitably the are pros and cons to this way of working. The biggest negative in my opinion was that our initial (first hour and a half) productivity was quite low in terms of code production. I’d put this down to three factors:

1. Unfamiliarity with Mob Programming as a technique.
2. Blank sheet of paper syndrome that TDD always seems to bring on.
3. An initial period of group discussion while we try to get our bearings.

I think I could argue that issue 1 is temporary, issue 2 is more about TDD than Mob, and issue three is possibly a good thing, so none of these seem to be a major stumbling block. Things moved faster on Friday afternoon’s second half, and faster still on Monday morning. So, at this point I think it’s possible to draw some positive conclusions as well.

There have been three primary benefits from the experience:

1. We ended up with a usefully refactored class.
2. All the devs involved agree with the code and have a thorough understanding it.
3. Team morale.

I suppose point one goes without saying – it was our primary purpose after all. The other two were slightly unexpected.

Because a large number of people were heavily involved in putting together the refactored class, we all walked away with an intimate understanding of it. I’d contrast that with the typical pairing experience where it is agreed that a class will be refactored and a pair goes off and deals with it. Ideally they will come back with improved code – at least code that the pair believes is better – but they are still faced with the prospect of justifying it, and explaining precisely how the new code works to everyone else. Mob allows a consensus on what is to be done to be easily arrived at, and completely removes the need to explain it to the participants. This is a big gain.

Finally the impact on team morale can not be underestimated. I personally found that the two blocks of time passed rapidly and enjoyably. I also noticed that some individuals who have been generally at odds in the past were at least cordial with each other. In general I’d have to say that this is probably where a substantial payoff is likely to arise.

At the moment, it’s very hard for me to claim that on the basis of this one experience that Mob Programming as a technique is suitable for a very wide range of situations. However, I am going to keep an eye open for other opportunities. So far I’d say it’s been a win.
