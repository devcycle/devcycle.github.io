---
title: "Levers of change"
excerpt: "Evolutionary architecture is the art of self organisation of both the human subsystems that produce software
and the automated systems that form the environment and building materials for that software."
layout: single
comments: true
read_time: true
share: true
related: true
tags:
  - architecture
  - systems thinking
  - methodologies
header:
  overlay_image: /assets/images/difference_engine.jpg
  overlay_filter: 0.25 # same as adding an opacity of 0.5 to a black background
  caption: "Levers for change"
  teaser: /assets/images/difference_engine.jpg
---

# A Confession

I'm old.

No, really, relative to most software developers I'm really old!

I've been a professional software developer for over 30 years and I've designed software systems for over 29 years.

This means I've seen software trends come and go, and then return again in a different guise.... multiple times.
During that time I've had to forget many tools, techniques and languages and learn new ones. Recently this has lead me
to thinking about what knowledge has endured over that time.

I can only think of a few subjects that I studied at degree level or below that are still highly relevant today. Setting
aside basic mathematics and underlying computer science concepts, like logic, there is one field that I think not only
holds relevant but has become even more relevant - Systems Theory.

# What is Systems Theory?

People have literally written whole books on this so I can't explain this in any depth in a blog but here's _a_
definition:

> Systems Theory is the interdisciplinary study of systems, where a System is:
>
> A set of elements or parts that is coherently organised and inter-connected in a pattern or structure that produces a
> characteristic set of behaviours, often classified as it's "function" or "purpose".

Obviously in software development we often think about systems. However, we often lose sight of a number of truisms.

* Our software is a representation of an incomplete, inaccurate model of the system.
* We, the people designing and building the software, are a part of that system and therefore we exert influence over
  it's behaviours.

Systems are dynamic. They consist of stocks ('reservoirs' of information), flows (of information) and feedback loops
(with delays).

# Mapping systems theory to software

If we are trying to solve a problem using software one of the first things we need to do is draw a boundary around what
it is that we are trying to solve: What is inside our problem and what is external?

In Domain-Driven Design this boundary is called 'bounded context'.

Defining a bounded context is both critical to success and really hard. I've never worked on a software system where we
got this context 'right' first time with the exception of a system re-write two years after the first system was
written. Even if, as in that case, the bounded context reasonably contains the problem, the world moves on and the
problem space changes.

This is the fundamental driver for 'agile' methods. The acceptance that things will change and our software needs to
adapt to this change. As a result, we accept that we, the development team, are an integral part of the system over
time. Our bounded context is an imperfect model of the problem our software is representing. The runtime environment,
the development team, the organisation we work in and the market that organisation is operating in all have an effect on
that model and are potentially affected by the models dynamics.

# What levers do we have for changing systems?

So if we accept that the team, department, organisation and the market we operate in all influence our software how do
we make changes to that larger system if we want to transform it? This is often the question organisations ask when
starting a transformative journey.

Examples of these transformative journeys are often expressed in trite marketing phrases like; 'Agile Transformation',
'Digital First Strategy', 'Customer-centric approach'. However, I would add 'Evolutionary Software Architecture' to that
list.

So what are the levers we can use to affect change in whole systems?

In increasing order of effectiveness:

<ol reversed>
    <li><strong>Numbers:</strong> Constants and parameters such as thresholds, targets and standards.</li>
    <li><strong>Buffers:</strong> The sizes of stabilising stocks relative to their flows e.g. Work in progress limits, team size, number
    of specialists, datastores, etc.</li>
    <li><strong>Stock-and-Flow Structures:</strong> Physical systems and their nodes of intersection e.g. Departments in an
    organisation, responsibilities across teams, services, etc.</li>
    <li><strong>Delays:</strong> The length of time relative to the rates of system changes e.g. milliseconds in runtime
    environment, days and weeks in teams changing software, months/quarters in organisations, quarter and years in
    markets. Shortening these delays has an effect on the system overall (sometimes in the wrong direction if not careful).</li>
    <li><strong>Balancing feedback loops:</strong> The strength of the feedbacks relative to the impacts they are trying
    to correct e.g. Rate limiting APIs, Circuit breakers, Fixing forward or rollback, Customer complaints feeding backlogs.</li>
    <li><strong>Reinforcing feedback loops:</strong> The strength of the gain of driving loops e.g. adding more
    developers adds more code with more complexity, more code needs more developers to change it...</li>
    <li><strong>Information Flows:</strong> The structure of who does and does not have access to the information.
    Missing information flows is one of the most common causes of system malfunction. For example: not measuring the
    impact of code quality can lead to seeing the code rot, thus slowing delivery this leads to adding more developers to
    increase delivery, focusing on new features and not improving code quality, which results in more code rot and slower
    delivery.</li>
    <li><strong>Rules:</strong> Incentives, punishments, constraints. For example: rewarding 'hero' behaviour over
    collaboration leads to individuals hoarding knowledge and becoming both a bottleneck and a single point of failure.</li>
    <li><strong>Self organisation:</strong> The power to add, change, or evolve system structure. Here's where
    evolutionary architecture sits. The ability to self organise is a key lever to responding to change. In this
    context, self organising means changing any aspect of a system already mentioned in this list. Enabling self
    organisation means inherently giving up some 'control' to allow for experimentation and diversity, the trick is to
    recognise when you are pulling the lever in the desired direction.</li>
    <li><strong>Goals:</strong> The purpose or function of the system. The goal of a system is what drives all the
    things already mentioned. Changing the fundamental purpose of a system by definition will remake the system to chase
    that new goal. The goal chosen has a huge impact. Most corporations would state their primary goal as "To make
    profits" but this is just a necessary condition. How different are two corporations that chose goals of "Increase
    the wealth of our shareholders" and "Improve the health, happiness and well-being of our customers and employees"?</li>
    <li><strong>Paradigms:</strong> The mind-set out of which the system - its goals, structure, rules, delays
    parameters - arises. Paradigms are the sources of systems. The ancient Egyptians built pyramids because they believed
    in a specific material afterlife. Paradigms can be both incredibly difficult to change and also changed in an
    instant. A change of leader of an organisation can start to impact the direction of that organisation
    overnight.</li>
    <li><strong>Transcending paradigms:</strong> If you keep yourself unattached in the arena of paradigms, stay
    flexible, realise that <em>no</em> paradigm is "true", this allows you to choose the paradigm that helps achieve
    your purpose or even defines your purpose.</li>
</ol>

So some of the levers in that list may appear to be beyond the scope of a development team or a software architect but
it's important to understand where pressure to resist change comes from and where we can use these same levers to affect
change.

# Scope of change

The order of effectiveness of the levers shown above is somewhat fluid. Depending on the context you may find some
movement in the order but it's generally limited to the swapping of the order of two 'levers' next to each other.

If we assume the ascending order of effectiveness shown we can use this to understand whether we are likely to be
effective in driving change using one of these levers.

Assume that we are trying to change an organisation to react more quickly to change from the market it operates in, what
is typically referred to as an 'agile' transformation.

Adding visibility on 'stories' delivered by a single development team through some kind of information radiator like a
'sprint' or 'kanban' board (information flows) is not likely to make a drastic change in the organisations
responsiveness. We haven't incentivized team members to collaborate (rules) and given the team the authority over their
own tools & work (self organisation) and therefore the current hierarchy of communication and management structures will
apply pressure to resist responsiveness to change.

In fact, the reason most 'agile' transformations fail, or at least only partially succeed, is that the lever you
actually need to 'pull' to make the whole organisation more responsive is at least at the level of 'goals' for the
entire organisation but more often that of a complete 'paradigm' shift for the entire organisation.

Note that not only is the lever further down the list but that the scope of the focus of the lever is much broader.
Introducing agile information radiators to development teams is not going to address the way the work flows to the
teams from other parts of the organisation, how the work is delivered or measured.

True agile transformations are a complete mind shift in the whole organisation, driving fundamental restructuring of all
the systematic structures in the organisation.

# Evolutionary architecture

As, by definition, evolutionary architecture is the concept of software design and implementation being responsive to
change it is predicated on the goal of the organisation responding rapidly and effectively to change.

Evolutionary architecture is the art of self organisation of both the human subsystems that produce software and the
automated systems that form the environment and materials for that software.

Therefore to be successful in producing architecture capable of evolution, which is predominantly at the level of 'self
organisation', we need to already be in an organisation that embraces a paradigm of change.

For a more detailed discussion of the various potential tools and techniques of evolutionary architecture I suggest
reading my blog post on [Prerequisites for evolutionary
architectures](https://circleci.com/blog/prerequisites-for-evolutionary-architectures/) and/or read [Building
evolutionary architectures](https://www.thoughtworks.com/books/building-evolutionary-architectures) by Neal Ford,
Rebecca Parsons & Patrick Kua.
