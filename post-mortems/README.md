# Post Mortems Process

## Postmortems 101

So, what is a postmortem?

A postmortem is a written record of an incident. Among other things, it documents the incident’s impact, what caused it, the actions taken to mitigate or fix it, and how to prevent it from happening again.

I will tell you more about the ingredients of a good postmortem later in this document. For now, I want you to understand that fixing the underlying issue(s) of an incident is important — but not enough. We also need a formalized process to learn from these incidents.

That’s what postmortems are for. Postmortems help us understand why incidents happen and how we might better prepare our systems for the future. 

[Active Issue List](https://github.com/ghostinthewires/Post-Mortems-Template/issues)

## Failure isn’t a disaster, it’s a learning opportunity.

We need to embrace failure for postmortems to work. This includes having blameless postmortems and no finger-pointing when looking for root causes. 

(By the way, human error is **_never_** a root cause, but more on that later in the document.)

## Postmortem Template

We raise an `issue` against this [repo](https://github.com/ghostinthewires/Post-Mortems-Template/issues) with a brief title and a description explaining the issue. It is also required to use the appropriate labels.

Once the investigation into the `issue` has been completed you use this [Postmortem Template](https://github.com/ghostinthewires/Post-Mortems-Template/issues/tree/master/post-mortems/postmortemtemplate.md) to update the description of the `issue`.

The Postmortem template was created for two reasons: First, I wanted to share our postmortems as part of our standard documentation, so that anyone can easily find them. Second, all of our work is based on Gitlab and we’re used to writing and reviewing Markdown files. In other words, my goal was to reduce barriers to reading, writing, and publishing our postmortems.

Publishing more postmortems ultimately means being more transparent about failures, which in turn builds trust in our team and makes our platform more reliable.

## Your first Postmortem

Now I encourage you to use the [Postmortem Template](https://github.com/ghostinthewires/Post-Mortems-Template/issues/tree/master/post-mortems/postmortemtemplate.md) as a foundation for your next — or perhaps first — postmortem. Give it a read. If there wasn’t an incident in last few days (I hope so!), think of the last time you had to deal with an outage. Then go through the different sections and try to fill in the blanks. Be consistent. Use the [active voice](https://plainlanguage.gov/resources/articles/dash-writing-tips/) throughout the document.

Postmortems are a collaborative effort thriving on feedback. Make sure to share first drafts internally with our team (Comments can be made on the [issues](https://github.com/ghostinthewires/Post-Mortems-Template/issues) page)

Always keep in mind: **Failure isn’t a disaster, it’s a learning opportunity for the whole company.**

## On Finding Root Causes

One of the big questions a postmortem has to address is: What has caused the incident? — What’s the reason the system failed the way it did?

At first glance, finding the root cause — the initiating cause that led to an outage or degradation in performance — seems to be the rational thing to do. For system owners, knowing who or what is responsible for an incident appears to be a desirable goal. Otherwise, how else should they implement appropriate countermeasures?

**In reality, however, trying to attribute an incident to a root cause in hindsight is not only impossible — it is fundamentally wrong.**

## There is no single root cause

In complex systems, such as web systems, there is no root cause. Single point failures alone are not enough to trigger an incident. Instead, incidents require multiple contributors, each necessary but only jointly sufficient. It is the combination of these causes — often small and innocuous failures — that is the prerequisite for an incident.

**As a consequence, we can’t isolate a single root cause.**

One reason we tend to look for a single, simple cause of an outcome is because the failure is too complex to keep it in our head. Thus we oversimplify without really understanding the failure’s nature and then blame particular, local forces or events for outcomes.

One of the things I like about the [Postmortem Template](https://github.com/ghostinthewires/Post-Mortems-Template/issues/tree/master/post-mortems/postmortemtemplate.md) is that it says “Root Causes”, not “Root Cause”. For me, that’s a testament to the fact that you need to look deeper if you only have a single root cause.

## Human error is never a root cause

It’s the easiest thing in the world to point the finger at others when things go wrong. And unfortunately, many companies still blame people for mistakes when they should really blame — and fix — their broken processes.

Blameless postmortems only work if we assume that everyone involved in an incident had good intentions. This ties in with the [Retrospective Prime Directive](http://retrospectivewiki.org/index.php?title=The_Prime_Directive) (a postmortem is a special form of a retrospective), which says:

_Regardless of what we discover, we understand and truly believe that everyone did the best job they could, given what they knew at the time, their skills and abilities, the resources available, and the situation at hand._

**Human error is NOT a root cause.**

We should rather look for flaws in systems and processes — the causes contributing to failure — and implement measures so that the same issues don’t happen again. It requires systems thinking, which focuses on cyclical rather than linear cause and effect, to view the system as a whole in order to find out how it drifted into failure — both at a technical and organizational level.

Here’s one of my favorite passages on the topic, taken from the [SRE book](https://landing.google.com/sre/book.html):

_When postmortems shift from allocating blame to investigating the systematic reasons why an individual or team had incomplete or incorrect information, effective prevention plans can be put in place. You can’t “fix” people, but you can fix systems and processes to better support people making the right choices when designing and maintaining complex systems._

**Does this mean that Engineers are off the hook?** 

No, not at all. They’re the ones with the most knowledge surrounding the incident. For example, they know first-hand how the system failed in surprising ways. Hence, they’re responsible for finding ways to make the system more resilient — including writing a postmortem.

One more time: **You can’t fix people, but you can fix systems and processes to better support them.**

Keep this in mind when you write your next postmortem.