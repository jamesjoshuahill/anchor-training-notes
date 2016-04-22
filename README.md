# Anchor training notes

These are my notes from a training session given by Colin Humphreys, CEO of CloudCredo in August 2015.
All typos and undecipherable non-sequiturs are my own.

-----

## eXtreme Programming

Batch size vs latency: large batches are faster when there is no deviation, small batches are faster when each batch will have lots of deviation.

Spectrum from NO IDEA
- XP: small features, fast feedback, just enough to get feedback
- Scrum: contract, longer sprints
- Lean: eliminating waste
- Six sigma: precise copy of existing product, mass production, eliminate deviation

to CERTAIN

## Goal

Deliver value to the customer. Our process is only useful if it continues to help us deliver value.

## Role in the team

Product owner: what is going to happen

Anchor: how it's going to happen

## Responsibilities

### Flow

Ensure stories make their way from backlog, to work in progress, to done.

#### Metrics

- no. of started stories == number of pairs
- story cycle time

Want: lots of small stories flowing through

Anchor is not responsible for architecture etc.

Technologists usually not best to be team anchor.

Lead technologist will push for architecture. Anchor will push for flow.

### Team

Anchor should take care of team admin. So Product Owner is free to be demanding.

Anchor should take part in interviewing, identifying skill gaps etc.

Ideal team might be two senior, two middleweight, two junior. Balance avoids arguments.

Seniors should pair on big/tricky tasks to achieve consensus. Otherwise seniors diverge and juniors probably won't stop, or identify it.

### Pair rotation

Novice + expert. Daily rotation by default. Always someone new on a story. Entire team will get context on long running stories.

#### Pairing basics

- Be sympathetic
- Have courage to say if your pair is dominating: verbally, physically
- Use a mutex, or unplug the keyboard!
- Pilot + navigator

Interruptible pair: live bugs, ci failure, production environment issues. Publicise interruptible pair on Slack and in the room, e.g. Build Tzar crown and sceptre

When odd, one person is flying solo. They should be interruptible and only work on chores. All production code should be pair programmed.

### Meetings

Product Owner facilitates the Inception

Anchor facilitates the IPM, Standups + Retros

Anchor and Product Owner: pre-IPM, approx. 1 hour, groom backlog, add chores after retro, to avoid discussion during the IPM.

Goal of IPM: consensus on about 2 iterations of work, (n.b. update the team strength)

#### Pointing game

- Powers of 2
- Must give own opinion without bias. Can use poker cards.
- Then highest and lowest should discuss. The discussion and knowledge sharing is valuable.
- Anchor should mediate different opinions, e.g. 'get on with it'

Ideal backlog: all 1 point stories prioritised by value to the customer

Better to build slightly the wrong thing and get it done. It's not the Anchor's role to build the perfect thing.

Ensuring meetings are focused and short.

Retro should focus on flow and delivering better. Anchor encourages everyone to come up with ideas. Especially consider changing the XP defaults (except retro otherwise you can't change back).

Anchor ensures people voice their opinions. And write actions points that are actionable. And adds all action points to Tracker as chores.

### Tracker

Is it a bug, or refinement of feature? A bug is a defect in a story that has been accepted. A refinement of a feature is a new story.

You can enable pointing for bugs and chores is Tracker, but DO NOT.

Chores and bugs do not get the team closer to its goal. Features do.

#### Chore patterns

- Interleaving: feature, chore, feature, chore etc
- Every engineer picks a favourite chore in IPM

Start every feature with a refactor. Progressive change over large-scale refactoring.

Release markers: morale by marking accomplishment.

Epics: label stories to group them together into a strand, or by customer

Anchor's responsibility to keep Tracker up to date and minimise work in progress.

## Technical practices

### Refactoring

- Renaming is remarkably important for refactoring
- Refactor, Red, Green

Refactor first then it will happen regularly and lower the cost of the change.

Targets refactoring on the code that is changing.

### Test first

Listing class behaviours makes single responsibility principle violations obvious.

Dependency injection for free

Regression tests for free

Living documentation of behaviour

Book: 'Growing object oriented code guided by tests' aka GOOST

### Continuous integration + Continuous delivery

Need good test suite to deliver continuously with low risk.

Maintaining CI + CD are Anchor responsibilities.

### Value stream mapping

From Lean. Post-it all the things that happens to deliver value and how long they take. Move them around. See what could be faster.
