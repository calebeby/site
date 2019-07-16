---
title: "Peregrine"
date: 2018-10-22T15:45:21-07:00
---

Peregrine is a scouting app I developed 2018-2019 with [Caleb
Eby](https://calebeby.ml/) and [Brendan
Burkhart](https://github.com/brendanburkhart). Brendan and Caleb kicked off the
project, choosing a stack of Go, SQLite, and React. When I joined the team,
about a week into development, I jumped straight into the project. I already
loved Go, and now there was a chance for me to create something useful with it,
with some awesome people! I started working on it the very night I was
introduced to it, without a solid grasp on what scouting even _was_, to be
honest. We worked tirelessly on the app for the next few months, and used it in
competitions that season. It proved much more effective than paper scouting,
allowing easier scouting, easier analysis, and an all around better experience.
We even experimented with gamification, which proved fairly effective.

## What's scouting, though?

> If you know the enemy and know yourself, you need not fear the result of a hundred battles.
>
> -- Sun Tzu, The Art of War.

In a FIRST Robotics match, there are 6 robots. Half on the blue alliance, and
half on the red alliance. In qualifications, these teams are picked at random.
After, however, the top 8 teams get to make their picks, and that's where it
gets interesting. At the 2018 Pacific Northwest District Championship, for
example, there were 64 teams, and with all these choices, making the best picks
gets really difficult. Your alliance partners often determine the fate of your
team in a competition, so it's crucial to choose wisely.

Most teams fill out paper forms about teams' performance during qualification
matches, _maybe_ enter them into a spreadsheet, and try to make decisions based
on those reports. It often leads to picks that have a history of being a good
team, or look pretty, but might actually perform well. Teams are forced to make
decisions based on qualitative observations, instead of looking at the hard
data.

## What makes peregrine better?

Peregrine provides scouts with an easier way to submit reports: an organized
system on their phones, rather than a disorganized mess of papers. In addition,
this takes stress off the scouting lead, allowing them to focus on analyzing
data rather than managing a mess of papers. As soon as a match ends and scouts
submit their reports, the scouting lead can access charts on how teams perform,
view qualitative observations about teams, and even a big-ol spreadsheet if
they're so inclined.

This allows our team to make more informed, bias-free decisions. We can say
with confidence that team x is _the best_ team at a competition at doing y. We
can analyze teams performance throughout a competition to see if they're
regressing or improving. We can tell our drive team what their alliance
partners are best at, and what their enemies' weaknesses are.

## What's next?

We're working on a rewrite of the app this year that will allow other teams to
use our app without hosting their own instance. It'll also have an improved UX
for both scouts and scouting leads. I've learned a lot from my job at
Billups, and Caleb Eby (the main frontend developer) has learned a lot from his
internship at Cloud4, so get excited about the new app; we sure are.

## Links

- [FIRST Faire Slides](/peregrine-slides.pdf)
- [Peregrine](https://pigmice.ga/)
  - Frontend Source: https://github.com/Pigmice2733/scouting-frontend
  - Backend Source: https://github.com/Pigmice2733/scouting-backend
- [Peregrine Rewrite (WIP)](https://peregrine.ga/)
  - Frontend Source: https://github.com/Pigmice2733/peregrine-frontend
  - Backend Source: https://github.com/Pigmice2733/peregrine-backend
