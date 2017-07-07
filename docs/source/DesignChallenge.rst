Planning and Designing for the UAV Challenge
---------------------------------------------

**The anatomy of a Mozzie.**

As a part of the design process, one of the first steps we took was to identify the core goals of the project before we started.
We found that how teams set goals also ultimately defined how successful they were in the event.

In our experience, the primary principles for developing a UAV Challenge project are:

 * Ensure that all activities are safe
 * Understand and interpret the competition rules correctly
 * Create a list of development priorities that need to be achieved first
 * Leverage the best capabilities of the team and understand and manage the capabilities that need to be learnt
 * Allow time for things that will go wrong and don't leave them to the last minute to rectify and test

The result of applying those principles was a development priority to create a system that can complete the mission.

Broadly, the mission can be defined as:

  - Create an airborne system that can autonomously find and navigate to Joe, before returning to base with a blood sample.

The required payload is limited to the blood sample. All the aircraft systems are only required to achieve the single task of picking up and delivering that sample.
So the question became: If a 25gram payload is all that is required to be delivered, how small a system could be made to achieve that task reliably and safely?

(We didn't want to collect a big blood sample using the props!)

The resulting development priority became:

1) An electric 2kg VTOL aircraft with enough range, which it can transverse in the time allowed by the challenge
2) An autopilot that can reliably operate autonomously with the required functionality for the challenge (failsafe, geofence, VTOL, etc)
3) A communication package that can ensure continuous data to and from the aircraft with at least one redundancy
4) An imaging solution that can identify Joe and a nearby landing area from altitude in a flying (moving) aircraft
5) An overall package that was cost effective, easily built and rebuilt, and prioritised leveraging as many existing components and systems as possible

It might not be obvious from the first impression how the principles apply to the development. The key factors are size and availability.

By making a small platform, we effectively reduce the risk of damage to people and property,
we reduce all the overheads for purchasing and testing various solutions, we also reduce the costs for repeating "tests" (failures and crashes),
the costs for having multiple airframes that can be used at different times by different people and, most importantly, the precious time that is consumed by singular failures and issues because only one airframe was available for testing.

The availability and access to common systems and products also reduces the time consumed to develop them, by leveraging what was already available and adapting them to suit,
rather than developing them from scratch.
Many teams fail to even get to the event because they cannot achieve their goals in time.
Creating brand new systems typically requires lots of time, so trying to avoid them should, in theory, give you more time to achieve your priorities.
Any plan only works if there is enough time to complete it, so having a plan with strict milestones increases the teams' chances of getting to the event, and winning.

A real Mosquito can carry up to 3 times it's own weight in blood and travel up to 50km away, and still land so softly on Joe that he would not even notice.
Since training a real mosquito to hunt for Joe in the challenge is a bit tedious and difficult, the "Mozzie" is our attempt to replicate this feat as closely as we can! ;-)
