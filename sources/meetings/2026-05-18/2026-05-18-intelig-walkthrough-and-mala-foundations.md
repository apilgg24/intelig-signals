Levi <>Apil - May 18
VIEW RECORDING - 112 mins (No highlights): https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3

---

0:02 - Levi Garner ( amaracore)
  I mean, because a lot of what I'm going to teach you, man, like what I was kind of thinking through these sessions, like I'll share stuff with you.  Yeah. Right.

0:09 - Apil Gurung (intelig.ai)
  It'll help you out.

0:11 - Levi Garner ( amaracore)
  And then that way you can sort of apply, like really push yourself. I think you've got something with that application you're building, right?  Like push that thing to like super high quality, you know, super high quality. And what I'll do too, man, post this call, I'll invite you or maybe to what I'll do is I'll give you access.  I'll get you access logged in because basically what I have is a couple of dev accounts. have a builder at IntelliG.ai, then like a dev at IntelliG.ai.  That way you can have access to my repos. And then a lot of what I show you today, can, I'm telling you, man, like even with what I built, how I built tree inventory, AI, a lot of what I did was a clone off of what I did with IntelliG.  Even though it was a completely different stack. I built Intelligies back in with Java, but I stole the design system, I stole the reasoning engine, and then I refactored the reasoning engine of Cognos, and then now I'm refactoring the reasoning engine of Arboros, which is a tree inventory one.

1:24 - Apil Gurung (intelig.ai)
  You know what mean?

1:25 - Levi Garner ( amaracore)
  But a couple things off the Batman that I'll show you, I think, would be very, very beneficial, is number one, I originally didn't set this up, okay?  I intentionally didn't set it up. But obviously, one of the most important things that we do whenever we build these systems, right, is the planning portion, right, in the agentic era.  We're planning, right? Okay, yeah, you've got to come up with, you know, your spec, your architecture, so on and so forth.  So I was originally doing... Doing that out of just a docs folder. originally it was way worse than this.  just had, you know, when I started off this project, I just had tons of markdown files for planning. And then I was like, let me evolve it.  I want to have an architecture, you know, a proper plans, what's active, what's shipped. And then, because I was trying to, I was trying to fight against myself from what I already did, that works with, with IntelliJ.  And that's what I want to show you, man. I'm telling you, this is, this is going to be very valuable for you.  But what I would do if I were you, and you probably got a mono repo set up, and that's absolutely fine.  The way I structured IntelliJ, and I don't know, I think there's pros and cons of both, honestly. I think there's pros and cons of both.  With IntelliJ, there's basically separate repositories, right? You know, like I have IntelliJ AI. AmaraCore, which is basically dealing with all of the AI integration, IntelliG back-end, IntelliG front-end, infrastructure, knowledge, marketing, continue, right?
  ACTION ITEM: Add product/knowledge folders; create backend/frontend standards - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=191.9999  And I think there's value to that and a lot of benefit to that. Honestly, I actually prefer it, but I get it.  Mono repos are very, very popular, and that's what I did with Tree Inventory AI. So what I would do with that, man, is create yourself a product folder, okay, in your Mono Repo.  Very similar to what I technically did with IntelliG. If you go under IntelliG knowledge, IntelliG knowledge is basically, and I refer, you could create something like this.  I'll honestly probably do something like this within Tree Inventory. But knowledge holds everything that's critical, right? Like, for example, I have like an audit where I run these audits against the application.  I have my domain specification. I have engineering standards, right? And this is one thing you can just steal directly from my app, like back-end patterns, rules, database.  These are just  money. That'll make your app super, super clean. And then what you can do is you can reference these standards from your Claude.md, right?  So every single time you spin up a new session, it goes and injects those. It will inject those standards for any development that you do.  But this is why I wanted to start with. If you just take away our call with this, it's going to help you a ton, man.  Because this is how, like, I keep  super organized. So basically, I have under my features folder, I have, like, you would have one under your features folder for identity, right?  That's very, very critical for what you're building right now. You know, or possibly organization, so on and so forth.  But anyways, like, I have a folder for Cognos, right?

4:53 - Apil Gurung (intelig.ai)
  Yeah.

4:53 - Levi Garner ( amaracore)
  Because Cognos is so valuable to my. application. I do this for a lot of different feature folders. I actually have architecture specifications right there, and I constantly keep these updated, right?

5:08 - Apil Gurung (intelig.ai)
  current state, future state, etc. I have one question regarding Cogniz. Is this your AI agent, the Cogniz? Yeah, let me explain it real quick, dude.

5:18 - Levi Garner ( amaracore)
  Let me explain that real quick, because that's going to help out real quick. I'm actually getting ready to... You can see my screen, right?  Yes.

5:27 - Apil Gurung (intelig.ai)
  All right, cool, man.

5:28 - Levi Garner ( amaracore)
  So, and dude, I'm telling you, man, like I actually want to get you hooked up. Post this call. We'll get you set up with your repos with this, because I've done some really, really cool things to even help startups, okay, gain value.  And I'm going to take you through that. So, what Cogniz basically is, man, it's basically the reasoning engine on top of the strategy, the code, the knowledge, the finance, right?  All these different pillars, essentially. So you can come in here and ask any question related to, like, I could say, what has the org worked on this week?  And this is what I technically, completely, and let me pull this open real quick. I did a podcast last week.  I want to show you this because it's really, really important, man. I think that there's basically going to be two different types of, there's going be two different types of apps that are built in the future.  One will be these reasoning apps, you know, intelligence apps, which is basically, man, this is not much different than what, what I'm building with this is not much different than what Palantir is trying to do for government, et cetera, right?  Like, where you basically suck in all these knowledge sources, and then you build an intelligence layer on... On of it.  Right? On top of it. So this is what happened this week for my work. Yeah. 298 commits, seven repos, up 140% versus the prior period.  Makes sense because the week before that, I was doing a lot of tree inventory  and then I got a cell from this healthcare client and I was like, , I got to, I got to, and I'm going to take you through some of the features I added.  Yeah. Because I really want to take the app to the next level on a few different pieces that I saw missing.  So this is, that's basically what Cogniz is. Right. And it can cross synthesize. So something I did that's really cool with this, man, and is I was, whenever you build these reasoning systems, there's basically layers it has to go through.  Right. And that's basically what, and let me pull this open real quick. Let me see if I have it.

8:00 - Apil Gurung (intelig.ai)
  Nice. Do you switch to Mac as well? Oh, yeah, dude. I  love it.

8:04 - Levi Garner ( amaracore)
  My Mac is just juiced up, dude. This thing's like a , this thing's like a , like, on some serious juice, man.  Like, you know that dude you see in the gym, he's just taking too much  steroids?

8:17 - Apil Gurung (intelig.ai)
  That's what this  computer is.

8:20 - Levi Garner ( amaracore)
  It's saucy, man. It's saucy, for real.

8:26 - Apil Gurung (intelig.ai)
  Looks good. Yeah, man.

8:30 - Levi Garner ( amaracore)
  Yeah, and plus, too, I got an Asus ProArt monitor as well. I mean, you get ripped off in Nepal on them, but  it.  Where did you get the Mac, though?

8:42 - Apil Gurung (intelig.ai)
  I got the Mac in the U.S.

8:44 - Levi Garner ( amaracore)
  Okay. Which one did you get?

8:46 - Apil Gurung (intelig.ai)
  The M4, M5? Yeah, so it's, let's check out these specs, man.

8:51 - Levi Garner ( amaracore)
  I think it's about this Mac. It's a M4 Mac, 64D.

8:58 - Apil Gurung (intelig.ai)
  That is. That is, like, still, like, years ahead of any competitor. Oh, dude. Yeah, it's amazing.

9:07 - Levi Garner ( amaracore)
  It's not even close, man. Like, compared to, like, I bought the most souped-up Lenovo I could possibly buy, and the  thing was heavy.  I sent that back. I'm like, you know, Macs are smooth, man. Macs are smooth. Yeah. Yeah, sorry. I still don't feel like it's, like, where...  I think something better can be built, though.

9:34 - Apil Gurung (intelig.ai)
  Yeah. You know? Yeah. For sure.

9:37 - Levi Garner ( amaracore)
  But, yeah, the hardware itself is solid. Yeah. One second, let me open that up real quick. I just want to show you this.

9:47 - Apil Gurung (intelig.ai)
  Yeah.

9:48 - Levi Garner ( amaracore)
  I don't even know where the  I stored it. Let me just tell the show for it. One time. Yeah, I'll pull that open.  Yeah, but something I did with this, I'm going show to you, man, it's like, the way I built it originally, and I'm telling you, I've been working with these coding agents, like Quad and Codex, eight hours a day plus, every day since like October, right?  Eight hours a day plus. And, I mean, they've come so far, man.

10:35 - Apil Gurung (intelig.ai)
  They've come so far.

10:37 - Levi Garner ( amaracore)
  And when I originally built this, I built, and that's where, let me pull this open, I'll explain this real quick.

10:45 - Apil Gurung (intelig.ai)
  Yeah.

10:45 - Levi Garner ( amaracore)
  So if you think about it, man, all apps today essentially are working around the LLM, right? Yeah. Which is basically, I like to think of the LLM as the brain, right?  But if the brain's not connected, If to the rest of the body, it's  useless, right? And that's essentially what large language models are.  I mean, they're super intelligent, but you have to connect it to something, right? And that's basically what a harness essentially is.  You deal with the harness every single day, which is a coding agent by Claude, right? Wherever that be, the user interface could be terminal, it could be, you know, co-work.  That's just basically a harness, everything around the LLM. And that's essentially what Cogniz is, right?

11:32 - Apil Gurung (intelig.ai)
  For IntelliJ.

11:33 - Levi Garner ( amaracore)
  It's just a harness. I like to think it was a harness. It's the operating system. And then I like to compare it, right?  Like if you think about it, the data is kind of like, in a way, the memory. Memory is interesting.  The data is kind of like the history, right? Then you have, you know, persistent short-term memory, et cetera. And that's what's really cool with how I built, built, I basically, I read Vance.  Cogniz entirely. Man, with better persistent and short-term, persistent memory, long-term memory. then also, basically, there's something that in these reasoning systems that you build, right?  Basically, one of the biggest issues, man, is understanding user intent, okay? So, like, if you open up a chat with ChatGPT, right, you'll notice, man, like, its intent is not as strong as Claude because of context, right?  It knowing, like, what it wants to know about you or what you want it to do, unless you feed it lots of context, right?  You can do that with ChatGPT, but, like, Claude, like, you could hardly give it any context at all, but it's, like, in terms of the prompt, sorry, you can give it a  prompt, but its context is pretty aware.  So, it's going to... Pick up and do what, it's going to execute what you want pretty well, right? And that's a lot of, that you're going to see when I set you up with a Cogniz, that it's memory, man, like you can see down here.  So basically, you asked the agent, yeah. So this is the main reasoning agent. But then I also set up all of these, I call them, they're basically called standing agents or observational agents.  And basically, if you think about it, man, in the age of AI, especially if you build intelligence systems, the reasoning is as good as the  data, right?  The reasoning is as good as the data. And that's why I created all of these standing agents to basically make sure the data is super, super clean, right?  So like, for example, you and I are having a conversation right now. Let's say it was a sprint planning call.

13:58 - Apil Gurung (intelig.ai)
  We come up with all these actions.

14:00 - Levi Garner ( amaracore)
  Those action items automatically get associated with sprints, right, here, automatically, right? Now, we've got to make sure those action items automatically close out, right, based off of the code.  So that's basically kind of what these standing agents do, kind of like workflow agents, but a little bit more intelligent, right?  They'll basically run, they run based off of events, and then they also run based off of cron jobs, essentially.  So I have different types of agents, but Cogniz is the main agent. Like, you can come in here in agent mode and then ask, you know, generate a release.  I'll just help me generate a release. I can say, help me generate a release, and then it will prompt me, right?  Like, all right, well, here are the repos available, right? Okay, I want to generate one off, IntelliJ front. Front-end, IntelliJ, back-end.  I want to make it customer-facing and last six days. So then it will generate that formal, right? Now, what's cool with this, man, is that the way you build these, again, you've got to keep the code super, super clean.  So behind the scenes, man, of IntelliJ, it's still very, very clean command handlers, etc. So basically what these, the way you build this harness, right?  I have these different tools, basically.

15:44 - Apil Gurung (intelig.ai)
  That's part of the harness.

15:45 - Levi Garner ( amaracore)
  then these tools, the LLM actually now decides. I had built this  6,000 line complicated intent classification. So whenever the user types something in, it tries to determine what the intent is.  And I just scratched all that . And now the entire intent classification is based off of the LLM. So I basically built this tool registry.  What are all of the tools that Cogniz has access to? What is the user typing in? How should I route this request?  What can I use? And that makes it much, much better because you could ask like, what were the commits pushed this week?  Right? And then they're like, okay, well, what was the most significant commit? Okay. And then go in detail on that commit.  Before it would, it had a very hard time basically doing these sub processes.

16:40 - Apil Gurung (intelig.ai)
  Right?

16:41 - Levi Garner ( amaracore)
  Because the intent classification was just not there. right. So your release notes are ready for draft. Bam. We can open it up.  It generated it for us. So that's kind of the purpose. It's got multiple purposes. But yeah, man, any comments, questions?  Wow. Now, the interesting thing is, I mean, a lot of this stuff, I just want to be completely clear, right?  I can come into Cloud Code today and I can say generate, I can do something very similar to this, go through all my commits and generate me a release summary.  The real value of IntelliG, man, is it's crossing all of these pillars, right? It's accumulating the data, the brain, right?  That technically, Cloud doesn't have access to. Cloud has access to my code, which is great, right? It doesn't necessarily have access to my strategy or my meetings, you know, so on and so forth, especially at like an institutional level, right?  But the way I built this, man, too, is like... The setup is completely agentic as well. You can come in here to Playbooks, or you can come in, you can generate an API key and set up the entire system, even your initiatives, et cetera, with Quad.  That's the future of systems.

18:19 - Apil Gurung (intelig.ai)
  But anyways, dude, what I understand so far is like, yeah, the Cogniz, IntelliJ, has like the whole context of your whole company, not just your code base, right?

18:32 - Levi Garner ( amaracore)
  You're  nailing it, dude. And that's where like, technically, what I see long term is building these kind of intelligence layers, like, exactly, man, it's the brain.  If you think about it, like, I could plug in this system to really any, what's going to stay the same, right?  Basically, code is kind of domain specific. And technically, too, I need to also tie into account like input. Infrastructure, intelligence as well.

19:02 - Apil Gurung (intelig.ai)
  That's kind of domain-specific.

19:04 - Levi Garner ( amaracore)
  Knowledge is basically your meetings, right? Like your artifacts, right? Like all of the artifacts that like, imagine all the sprint planings, et cetera.

19:15 - Apil Gurung (intelig.ai)
  And if you just want take care of that as well, like sprint planning tickets, will this like automatically pick up on that and like create those tickets or action items, all that stuff?  Absolutely.

19:27 - Levi Garner ( amaracore)
  So like, let's say, for example, I had this, um, I had a sales call. Yeah. I'll show you right here.  All right. With this, this dude from Sigmatic. Okay. I had the sales call, right? It automatically extracted from the sales call, the action items, right?

19:49 - Apil Gurung (intelig.ai)
  It extract the action items.

19:50 - Levi Garner ( amaracore)
  So it actually created those action items here, right?

19:54 - Apil Gurung (intelig.ai)
  As well.

19:55 - Levi Garner ( amaracore)
  Then what it does on top of that, right? Now let's say more. Importantly, man, those are kind of basic.  Did I actually do that action item, right? Did I actually do that action item? You can imagine it being tied into your Gmail, right?  And then being able to tell you, did you actually send it or not, right? And then it closes the action item out.  Now, it doesn't do that because it's not connected to your Gmail yet, but from a code perspective, it is, right?  So I have a feature in here from a sprint perspective or your action items. These action items will automatically, number one, will automatically associate that action item based off to the initiative using AI, right?  Then what it will do based off commit, right? It'll automatically close those action items out, right? So you can see here, let me switch to actually Meridian because I've got good data seated there.  So if I come down to sprints, you can see for... I need to reseed this, but it'll automatically complete these out.  The users never do these things. That's what I kind of saw going on with, it's like we have all of this talk, right, in tech.  We jump on these stand-ups every day.

21:23 - Apil Gurung (intelig.ai)
  You talk about it.

21:25 - Levi Garner ( amaracore)
  And that's where, dude, I'm getting to that level of intelligence now. Okay, I'm not  joking. It could sit on your sprint planning calls, your daily stand-ups, and let's say you said that you did something, right?  You said that you completed this feature. You could then ask Cogniz, what went on and what meetings occurred this week?  Ask what happened in the meetings, right? And then I can link, Apil said that he completed X. Did he complete it or not?  You see what I mean? That's the level of list the action items by develop by person in the meetings from the meeting.  And if you think about it too, man, it's like, you're right. Like in a way though, when we, if we look at it from a harness perspective, it's debatable.  And it's interesting from an academic perspective that if you think about it, it's like Cogniz is the operating system in a way, but it is also kind of the brain.  You know what I mean? But it gets its intelligence right from obviously. The large language model integration. And I'll tell you something that I've learned building these intelligence systems.  Now, I'm using Claude Sonnet, you can see asking this question, but I've improved the harness so much. Like I said, the tool registry, eliminating the intent classification.  We would get pretty much the same  results with Claude Sonnet 4.6 from 4.7 to Gemini Flash 2.5, which is basically free.

23:30 - Apil Gurung (intelig.ai)
  You know what I mean?

23:31 - Levi Garner ( amaracore)
  You're not going to see that big of it. Now, if it's a very deep question, of course, right? Okay, so let's say, okay, can you reference and see if Alex completed or any code related to his action items?  You get what I'm getting at. Yeah. Right.

24:04 - Apil Gurung (intelig.ai)
  You get what I'm getting at. Yeah.

24:06 - Levi Garner ( amaracore)
  And the way this is working as well, you can see it cross-referencing the action items there.

24:21 - Apil Gurung (intelig.ai)
  Yeah. Basically, you know all the data, what the developers are doing. I mean, from your first video that you posted out in LinkedIn, like you've been marketing it as like the AI CTO, right?  Like we can see all your, what your devs are doing. Yeah. This is basically it. Yeah, man.

24:42 - Levi Garner ( amaracore)
  And if you think about it, it's like, I like the term AI CTO and then also execution intelligence, right?  Like if you think about it today, we're having, teams are using things like JIRA, right? They're having to manually create these artifacts, update these artifacts so that you can actually able to, really, it's think you're There's  Understand who's doing what, right? What's pushing the business forward? Where I basically took the inverse of that. And a perfect example is this feature I'm launching today.  I'm getting this rolled out, which is this discovery feature. I'm not  kidding, dude. What I realized about myself is that I'm moving way too fast, and so are you, right?  Like, the code can, what if, because what's, how it's always been, Apil, is that we've, we've have, we have executives, we have business people that tell engineers, this is our business priority, right?  Well, what if the code actually told us what the business priority is, right? It's one thing to say we're working on these initiatives, right, that the business is getting.  So we create the initiative in JIRA, we create all the tasks. I created the inverse of that through this discovery feature.  So basically it works like this. You run a discovery, okay, and yeah, just added one in there, and I already ran it, I can clear and run it again.  But basically what it does is it goes through all of your commits. You can see here, latest run, I just ran it, that's why it wipes out.  But I ran it earlier, it had 582 commits from me, tons of PRs, et cetera, and it basically said, here are what your initiatives are based off of your code.  All right, Microsoft Teams integration, that's 100% accurate. It's got an 83% overlap because I actually already had an initiative for that right here, Teams integration, as you can see.  I'm basically landing this healthcare client, so I had to build a Teams integration. I had to do a bunch of SOC 2  that's boring as hell.  I'm improving Cogniz, right, the harness, we've been talking about that. And I built this agent intelligence platform because I realized, and a lot of these, dude, I just want you to know, we're already...  I command handlers. So I had command handlers pushing to events like commit intelligence. I already had to clean commit handlers to handle all of these things based off web hooks that came in.  But then I'm like, I want to build an agent on top of it that can run autonomously and learn from its runs.  That's all the agents basically were. So that was the agent intelligence platform. So if I go down here again to Discovery, let's see how well it did.  Microsoft,  nailed that. SOC 2 Readiness, nailed that. So it's recommending this. It's saying, hey, let me go ahead and I could enrich that as well.  It's saying, let's see here, and enrich this one. Let me run that real quick. I'm in the middle of finishing, but you get the idea.  Yeah. So Cogniz engine rebuild. Okay, Cogniz harness. So basically already it's recommending me. And dude, what I did too, I'll just give you a hint on how I built this.  So what I basically, I said with Quad, I said, look, I thought of this feature. And we'll run it on yours as well after I deploy it here today.  I said, I'm moving so  fast. I'm thinking about it, dude, I shipped 600 commits in the past week. Okay.  What the  have I been working on? I get overwhelmed, I get overwhelmed. I've got, look how many agents I'm running right now.  I have to name them like this, initiative linking, know, fixing Cogniz release. I've got so many agents. That's why I use these little icons as well, because it just helps me kind of identify, okay, brain is Cogniz for this session.  This is agent. You know what I mean? Yeah. And I'm like, what the  have I been working on? Because if I haven't.  I just go  build it. I'm not waiting for .

29:03 - Apil Gurung (intelig.ai)
  And that's where I came up with that feature, initiative discovery.

29:07 - Levi Garner ( amaracore)
  I noticed it too because I got a couple of AI startups. And those dudes are , they're just moving too fast.  They don't give a  about creating initiatives. Even if I built it in such a way that's like this, you can go to agent here and go to playbooks and just copy the strategy setup.  So I created a prompt that literally, you can just open this up with Claude and it'll basically just create all the initiatives for you, right?

29:36 - Apil Gurung (intelig.ai)
  Based off of your code base, right? Kind of same thing.

29:41 - Levi Garner ( amaracore)
  But they just move too fast, know, kind of like me. And that's where I see this being the future, dude.  I see this being the future because this could plug in with a chief executive officer agent, right?

29:53 - Apil Gurung (intelig.ai)
  You know what I mean?

29:54 - Levi Garner ( amaracore)
  And you can kind of get it, man. I think you kind of get it. It's the future. It's the future of, and I think it's even, it's even surpassing like linear, dude, because linear, what teams are doing now, like if you go listen to podcasts on how like the Codex harness team builds, basically what they do is they front load their sprints.  So they basically add in linear detailed tickets, right? They build these detailed tickets, then they have agents that suck in that ticket information.  Which I can see that, but like, I see it moving more towards like, it listening to our conversation right now, right?  Building out the action items based off of that, under our sprint, these are all automatically created. The user doesn't come in here and create anything, right?  It's all automatically, it just knows, okay, you're working on these initiatives, how much work has gone through. There, you're working on these action items, closing them out, right?  And then two, pushing these all down to the repo. So after we have this conversation, this conversation will automatically get pushed down to the repo for the agent to kick off the sprint.  You know what I mean?

31:17 - Apil Gurung (intelig.ai)
  That's how I see.

31:18 - Levi Garner ( amaracore)
  That's the future I see.

31:21 - Apil Gurung (intelig.ai)
  That is quite autonomous. It's like we're just like, let's say, speaking, having this meeting, and then based off of our discussion, the AI picks up what our action item is, and then commands to the agent to do the coding stuff, and then executes on that.

31:42 - Levi Garner ( amaracore)
  A thousand percent. A thousand percent.

31:45 - Apil Gurung (intelig.ai)
  Here's my question, like, on this, like, would you want it to be, like, fully autonomous on that, or would you want to have, like, something, some kind of an option, like, okay, here's this, what you discuss in this meeting.  Do you want to accept this? then they kick off? without that, let's say, option, they just do it autonomously, automatically?

32:11 - Levi Garner ( amaracore)
  Yeah, that's a great question, man. I think so. Because even right now, there's still a human in the loop.  You know what I mean?

32:18 - Apil Gurung (intelig.ai)
  There's still a human in the loop.

32:19 - Levi Garner ( amaracore)
  And I'm that human, right?

32:21 - Apil Gurung (intelig.ai)
  Essentially.

32:22 - Levi Garner ( amaracore)
  I'm still doing a lot of the facilitation. What this system's basically doing is, right now, it's just replacing the reporting piece to the business, right?  You just connect it, and it reports exactly what you actually did. That's the execution intelligence. You see what I mean?  Teams execute. Where does intelligence come from? And this is a whole new field, dude, just so you know. It's going to be a $10 billion  industry.  The issue that I'm having right now, dude, is when I talk to CTOs, CTOs, mostly VPs of engineering. I talk to a lot of VPs of engineering because CTOs are basically, you only really get a CTO title if you're a founder, just so you know.  Otherwise, you're a VP, essentially. I mean, Bobby shouldn't even have had a title of CTO. I mean, he's so far from that, but he's so far from that.  But CTOs are really founders. And I talk to a lot of VPs, and it's like, they get this after like an hour of me selling, you know, explaining it to them and taking them through.  They're like, okay, but their brains are like still in the human loop, dude. Well, my PMs aren't in the repos yet.  I'm like, they're like, our PMs are creating, we're using Confluence. And I'm like, dude, don't, your PMs don't create PRDs, right, in Confluence, using ChatGPT and then copying and pasting.  It's a  way. You want to create your PRDs in the code base, right? Because the code is the source of truth, right?  It can validate the legitimacy of the PRD based off of the code base, based off what it currently does, right?  And like I said, execution intelligence, it's a new field, man. It's a completely new field. That's where it's like I'm selling something that's like six months, 12 months in the future, in the future.  Like no one's, the only people that are really doing execution intelligence right now is Palantir, right? I'm doing it for engineering, something specific.  But basically what Palantir does is they connect to every system that a business works with. So you can imagine like Microsoft Dynamics, it connects to your Intact, your accounting.  And it sucks all of this in and it creates an ontological model and then it reasons on top of.  This, right? But I mean, dude, to be honest, I've studied Palantir, and I'm going even more in-depth, like, I'm really obsessed with that concept of, like, what are people actually doing?  You know what I mean? Like, what are people, because I used to go into these different engineering works, and even my own, and I'm like, what are these engineers actually doing, right?  I mean, I think a perfect example is the firings that happened at Team Brand. Like, look at it. That's a perfect reason of Bobby's incompetence.  He fired, for example, obviously, let's just take Arpit for an example. Yeah. Okay. Arpit as a contributor, right? If I mapped Arpit out as a contributor, let's just go to my budgets.  This is how I would have made that decision, okay, objectively. I would have plugged Arpit in here as a full-time employee, Arpit making, you know, less than you.  mean, he was making, like, probably maybe $7. And then what I would have done is I would have looked at RPIT's output, right?  So then I would have plugged that in, okay? Then I would have went to contributors, and I would have saw what his ROI actually is, right?  I would have saw his ROI. And then I would have compared that against a full-time FTE like Oliver, who's not really delivered  that's costing X amount of dollars.  Do you see what mean?

36:30 - Apil Gurung (intelig.ai)
  I had the same conversation with Nathan.

36:31 - Levi Garner ( amaracore)
  He's like, 100%, dude. RPIT was one of our highest performers, right?

36:36 - Apil Gurung (intelig.ai)
  A perfect example of this.

36:37 - Levi Garner ( amaracore)
  actually have this kind of baked into the Meridian example. Like this Ravi Krishna guy, making 38K a year, right?  I mean, you could have really good contributors like this that are full-time, but they're making 136,000 a year. So what's your actual ROI on them based off of their...  Their commits, their quality, how they're using AI, what they're pushing. And  doesn't really change. Like, I've had a lot of VPs come to me and they're like, oh, well, commits don't really matter as much anymore.  Well, , yeah, they do. Are you committing? How much is your developers committing? Like, it took Peter Steinberger, you know, I think 10,000 commits to build OpenClaw.  It took me 3,000 commits to build IntelliJ. What the  do you mean commits don't matter? Like, they 100% matter.  We should be pushing more commits, facilitating more agents. You know what I mean? That's all that really matters. Now, in the future, this will completely change, this contributor costs, it'll completely change to bots, right?  But it doesn't matter whether it's is your actual client, right?

37:46 - Apil Gurung (intelig.ai)
  The Meridian is an actual company that is like Meridian's a fictitious company I created and seeded to represent.

37:53 - Levi Garner ( amaracore)
  You see what I mean?

37:55 - Apil Gurung (intelig.ai)
  Yeah, exactly.

37:56 - Levi Garner ( amaracore)
  But it's like a fintech company that, you know, but I do have- Pro-Clients on the product. But this is just one that I've created, the data I can show.

38:09 - Apil Gurung (intelig.ai)
  Gotcha. Yeah, man.

38:11 - Levi Garner ( amaracore)
  But you get what I'm getting at there. Yeah, it's interesting, man, because we've used all of these systems. And I think everyone right now, Apil, is racing towards, if you go look at all of the  YC startups right now, they're all racing to build coding agents.

38:31 - Apil Gurung (intelig.ai)
  Right? No one's building the intelligence layers. Yeah.

38:35 - Levi Garner ( amaracore)
  No one's building the intelligence layers. And that's what I'm focused on. Whether it's, and too, but I think it's interesting.  I you, like, I launched this tree inventory app, you know, and I got, I'll show you my users. I got 25 users.  I mean, like,  that. Like, I created an, I took a completely different approach. I think you learn things when you.  You do, like, you learn so much more running, start, like, doing a  startup than you do working for a corporation.  I mean, it's just, it's astronomical. But, and even though I have money, I've got a lot of money, I still, like, it bothers me not having lots of money coming in.  And that's when I was like, that's when I, that's why I kicked off the consulting  that I'm going to bring you in on.  And it motivated me to build this because I just, I wanted to test something out. Because I have a theory, people buy products, right?  People are more entitled to buy products that they, that are usage-based, right? Or improve, improve productivity, right? And that's why I built Free Inventory AI, just to prove that, because that's what it does, right?  Like, someone uses Free Inventory AI in their daily life. Yeah. They, IntelliJ, plus it was part of the market, dude.  Like, I'm working these large deals with IntelliJ right now, these VCs, you know, private equity. They're just, CTOs are different, because it's got the biggest TAM, you know, total available market, IntelliJ, but one of the hardest  buyers.  Like, CTOs and VPs, like, once I get them on the call, they're sold. But getting them on the  call is a challenge, because if you think about it, dude, I get swarmed myself with 10,000 new tech companies wanting me to use their product, because it's the total addressable market's huge.  But you can see where it premiered, these are legitimate users I've got on Tree Inventory AI, 27 users, but I took a completely different approach to it.  And that's what I want to tell you, is just, like, go free, dude. Like, I was all worried about, like, with IntelliJ, making everything perfect before I launched it.  I launched it in three months, which is not bad. It was a good MVP.

41:00 - Apil Gurung (intelig.ai)
  People got value from it.

41:02 - Levi Garner ( amaracore)
  But was so concerned about being a perfect product. And I think that's common for people that come from academia or have worked in the corporate world.  You think about perfect. It makes something just minimum viable to  use. And then I went to Instagram. I created an Instagram account.  I started following tons of tree companies. And I got 300 followers and I followed 1,000. Not bad. It's like 300 to like 950.  Not bad at all.

41:33 - Apil Gurung (intelig.ai)
  . You know what I mean?

41:35 - Levi Garner ( amaracore)
  And you get users. And that's a great way. Let me just see what this dude's been up to. Someone just signed up today.  I created this. And that's something you should also do. It's very, very easy. I created basically an admin dashboard that allows me to see my key stats because I want to see how people are.  We're using the app. Like I said, dude, I've not even really pushed this app that much. I created the Instagram account.  I started following people. But yeah, man, we got to question it.

42:14 - Apil Gurung (intelig.ai)
  So Arborist, is that the harness for tree inventory or is that just... Arborist, exactly, dude.

42:20 - Levi Garner ( amaracore)
  And I'm revamping Arborist. Now, what I'm going to come in here and do technically, man, I'm going to show you how I would build that out.  We can go through that example together. Yeah. So what I basically built with this is, yeah, Arborist is basically the intelligence layer, 100%.  So you can come in here and be like, communicate, email a client, a link to their property, and Arborist will analyze that request.  Yeah. And that's what I'm actually running a sprint right now where I'm completely revamping. Yeah. So they can generate this link and then you could, bam, click that.  Oh, okay. And they'll open up the email to the link.

43:08 - Apil Gurung (intelig.ai)
  Nice. You see that?

43:11 - Levi Garner ( amaracore)
  So, yeah, man, it's got the same kind of... Now, I got to come back on this app and do some kind of cleanups and policy.  Honestly, dude, building the mobile... Because most people don't even use the web version, right? They're using it from the mobile phone.  That's where the app, the heart of it is really at. It's just a pain in the apps, dude. That's where I came up with all these other...  Now, I have all these Claude commands like slash build, deploy. I don't know about you, too. I've been using these browser agents.  Yeah, yeah, I've killer, dude. Because I'll have to go set up a stupid- profile, give Google, go set up something in Google, set up these creds to give to the place.  It's just all this . I'm just like, I work with Claude. like, generate me the prompt to give to the browser agent.  You know, same with IntelliJ, dude. Like, testing all of these different, all of the different ask modes, etc. I just have browser agents test all this for me.  I don't even, I don't even come in here and  manually ask, like, okay, initiative portfolio, what is our progress for initiatives this quarter, and then test it.  Now, I will, at the very end, right? But honestly, dude, Quad's gotten so, so, so capable now, Apil. I make, I make it actually test it live.  Here, so I'm working on a Cogniz tool refactor. Yeah. Right now. And I make it actually test itself from here.  Like, write all the integration tests, write all the unit tests, then actually physically call it, generate an API token, or sorry, a JWT token, and call it itself and check the responses before I even pass it to the browser agent.  Right. That's another trick to do as well. Yeah. So, yeah, man. All right. Yeah. So back to it. Exactly.  We went on a long tangent there. That's what I'm saying. Set this up. Product, HabClaw generate what your features are.

45:16 - Apil Gurung (intelig.ai)
  Yeah. Right.

45:17 - Levi Garner ( amaracore)
  And then what you can set up too, man, is this is how you structure. If it's a very complicated feature, you can have architecture.  Don't overcomplicate it. The most important thing within the features, product features folder is the work items, which is basically just a folder, subfolder structure to encompass whatever you want to build out as a feature.  Right. So, for example, I'm working on Cogniz external connectors. Okay. So I'm going build an MCP. So instead of me having to physically build all these integrations, I can use MCP to go fetch for the client all of their infrastructure costs.  And then bring that into Intelli. So you can see what I set up there. I have architecture, PRD, sprint plan, tracker, what's my vision?  Those are kind of the markdown files I like to generate for every single feature I create. That's a big one, dude.  And then another one I'm going to, I'm going to, I'll give you as a takeaway is work trees.

46:26 - Apil Gurung (intelig.ai)
  Okay.

46:27 - Levi Garner ( amaracore)
  So you can see I've got multiple and I honestly just started. Yes. I used to just build out of Maine, everything and out of Maine.  And then what ended up happening is like, I wanted to review what's going on. Right. But it's  one agents working, breaking the backend.  So I can't compile. Yeah. Have you done it? Have you done work trees? No, I haven't.

46:48 - Apil Gurung (intelig.ai)
  No. All right, dude.

46:49 - Levi Garner ( amaracore)
  Claude will take care of it for you. basically what you want to do when you're working on multiple features at once is you want to create work trees.  Okay. So you'll say, create a work. WorkTree for me to work on this feature. So basically it creates a local checkout.  basically clones your entire repo and works out of it as a WorkTree. And then it can actually push to a, it can create a PR and push to your GitHub.

47:14 - Apil Gurung (intelig.ai)
  Okay.

47:15 - Levi Garner ( amaracore)
  And then later you can merge it back in, but that way, and that's all these, a bunch of these startups are creating like this, this one I checked out, it's called Conductor.  It's just a , dude, all it is, and this company got acquired for 22, or they got funding for 22 million.  And all it  is, is exactly that. It's literally, dude, all you have to do is tell Claude, generate a WorkTree, okay, for me for this feature.  And we're going to push a PR to this, you know, or create a branch for it in GitHub. And we'll, we'll raise PRs to that as we, as we complete our work.

47:54 - Apil Gurung (intelig.ai)
  That's all it is.

47:55 - Levi Garner ( amaracore)
  And that they're basically that conductor startup is they're just solving. The which is what I just mentioned that I ran into, which is basically  work trees.  So what I like to do, dude, I actually do like to open up Cursor.

48:08 - Apil Gurung (intelig.ai)
  Yeah.

48:09 - Levi Garner ( amaracore)
  And then, oh, no, today I'm going to actually switch it up. Once I close these out, I like to also start new sessions daily because the context, the agent starts to get inefficient after 70% context.  know, the window fills up about 70%.

48:22 - Apil Gurung (intelig.ai)
  But I've noticed Codex.

48:25 - Levi Garner ( amaracore)
  I use both Codex and Quad.

48:27 - Apil Gurung (intelig.ai)
  Yeah.

48:27 - Levi Garner ( amaracore)
  So I'm running major debts with my AI, dude, just so you know. I mean,  IntelliJ. I mean, I'm just like, I've got, I'm spending, I spend 300 bucks a month minimum on building infrastructure.  And that's what I'm telling you, suit-based is way better. It's way better. It's way cheaper. Yeah. Because my AWS bill for IntelliJ right now is like, is a, is a thousand a month, sometimes upwards to a thousand a month.

48:56 - Apil Gurung (intelig.ai)
  And I've even had to scale back on some savings. Yeah. That's just a waste of  time.

49:01 - Levi Garner ( amaracore)
  And then on top of that, all the models. That's where I got smarter, dude. When you build in, you got to start to build in like AI integrations into your app, et cetera.
  ACTION ITEM: Import Levi–Apil transcript into IntelliJ; prompt Claude to generate vision/initiatives/action items - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=2949.9999  You got to be smart. When you're doing your testing and , use like, and you want to set this up again, dude.  This is where design patterns become extremely critical. And that's what I'm saying. You're going to take this transcript, take this transcript, pull it into your repo so your agent can reference it.

49:28 - Apil Gurung (intelig.ai)
  Dude, I just talked to this dude.

49:30 - Levi Garner ( amaracore)
  He's like this tech guy. He's  crazy mad. You take everything he mentioned that's very important, and let's come up with some action items to implement this.  What your agent also needs to do, you've got to create your back-end standards, your front-end standards, et cetera. Your app needs to be CQRS.  It needs to be domain-driven design. It needs to be event-driven. Everything needs to persist to event stores. It needs to be functional.  That's another thing. Even though it will do CQRS CQRS CQRS and 10-15 It will follow it. You'll have long run-on methods and .  I like my  to be extremely functional. Small functions within each. It's very, very important. then another thing your agent needs to do is it needs to understand design patterns.  So for example, see how you can swap out any of these providers?

50:23 - Apil Gurung (intelig.ai)
  It doesn't matter.

50:25 - Levi Garner ( amaracore)
  So that's where you need to create an abstraction with your AI integration. I have my AI core, and it can just swap the model.  It falls back. Let's say, for example, I switched to Sonnet 4.6 as my default was Claude Office 4.7. Let's say Claude Sonnet fails.  Okay, I use adapter port pattern for this and integration segregation. That's all your model needs to know. It will then fall back to GPT, 5.5, right?  That should be 5.5. Yeah, GPT. 5.5 or GPT 5.4. Next up, Haku. then in the harness, behind the scenes, even though you're using 4.6, let's say I have an LLM call to just try to understand user intent.  I would just use Haku 4.5 or Gemini 2.5 Flash. But when I'm doing my testing, I'm just using 2.5 Flash.  Because I was spending thousands of dollars a month on  Claude before, just from API calls.  the subscriptions.

51:31 - Apil Gurung (intelig.ai)
  Cheap as hell, dude.

51:32 - Levi Garner ( amaracore)
  What costs money is when I let users take pictures using Claude Office 4.7 to identify tree species. You know what mean?  That's what runs your  bill up.

51:43 - Apil Gurung (intelig.ai)
  That's what I'm saying. But that's what I'm saying.

51:46 - Levi Garner ( amaracore)
   the cost, dude. When I get acquired, I don't give a  about revenue.

51:53 - Apil Gurung (intelig.ai)
  Revenue doesn't  matter, dude.

51:55 - Levi Garner ( amaracore)
  All that matters is users. That's all that matters is users. That's it.

52:01 - Apil Gurung (intelig.ai)
  know what mean?

52:02 - Levi Garner ( amaracore)
  But that's another trick with these. Because you've got to build AI into your app. It's very, very important. You know what I mean?  You could even build into your app when they take the pictures. Steal that  from me, dude. I don't give a .  I'll give you access to Trematory AI. You can look at my photo feature. When they take a picture, automatically identify what the species is for them.
  ACTION ITEM: Add Apil to Tree Inventory AI; grant repo access - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=3146.9999
  ACTION ITEM: Implement multi-org RLS; add org_id to tables; auto-create org on signup - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=3146.9999  So they don't even have to type it in and . You know what mean? You've got to have those AI features for people.  And then, this is another big takeaway. We talked about this. dude, role-level security is very, very important. On all of your tables, okay?  You've got to have organization ID. When someone signs up, automatically, don't just create them as a user. You need to create them as an organization, right?  And people can have multiple organizations, right? You'll see how I structured that inside tree inventory. AI. See, it's all multi-org, right?  That's like something like, for example, Arboggle just never  could figure out. So every app I build now, it's all always multi-org.  Like I can switch from this company to this company. That's very common. You just want to build these kind of things as the basis of your application, right?  Because it's very, very important, dude. And build fast, dude. That's why I'm just trying to motivate you a little bit here.  It's  possible, dude. It is 100% possible to build a full-scale nursery management system. Give it a cool  name, too.  Like a nursery management system that you can scale across Nepal and India.

53:44 - Apil Gurung (intelig.ai)
  You know what I mean?

53:45 - Levi Garner ( amaracore)
  You could do it for both. It's all AI-driven first. You know what I mean? And then really think through the user's experiences you were going through things.  That's also very, very important.

54:00 - Apil Gurung (intelig.ai)
  You know what I mean?

54:00 - Levi Garner ( amaracore)
  But build it fast, dude. Build it fast and give it away. Just give it away to people. You know what I mean?  Any other comments, questions, anything? Man, there was a lot to take in.

54:14 - Apil Gurung (intelig.ai)
  I have to, yeah, look back at this and, you know, make some notes and then as well. Yeah, do this, dude.

54:21 - Levi Garner ( amaracore)
  So use that, like, do this. Like, from this, I'll send you the meeting. Suck in the transcript. Like, create a folder within your project called, like, meetings, right?  Suck in that. Transcript. And just prompt Claude to go through it with you to create the action items and then also action items for your code base.  And that's what I'm saying, dude. That's why IntelliJ, check this out. Post all my meetings. If you look at this knowledge, technically, we set up IntelliJ for you.  It'll do that. Oh, yeah. By the way, dude, show your screen real quick. Show me your, let's just set that up, actually, right now.

55:00 - Apil Gurung (intelig.ai)
  Yeah, share your screen real quick. Yeah, do have the...

55:06 - Levi Garner ( amaracore)
  Let's just do it.

55:12 - Apil Gurung (intelig.ai)
  Let me see. I have the IntelliG for my repo, or it was already onboarded. I was already onboarded. Perfect.  Yeah, let's sign in.

55:31 - Levi Garner ( amaracore)
  I came up with some new features, too. The way I set it up, was originally set up... Well, you should just be able to log in, but it should just take you to jump back there real quick, hit cancel.  So this is the same... If you jump back... You already signed up, right? Yeah. I'll log in with GitHub.  Let's see. All right, let's just see.

55:59 - Apil Gurung (intelig.ai)
  Okay, yeah. Maybe sign up.

56:08 - Levi Garner ( amaracore)
  Okay, cool. So let's do unlock intelligence. Let me give you a code real quick, man. Sure.

56:18 - Apil Gurung (intelig.ai)
  I remember it was already working. Did you have a code?

56:24 - Levi Garner ( amaracore)
  I, let me see, let me check.

56:27 - Apil Gurung (intelig.ai)
  It let you come to this screen. Yeah. What'd you do? It said, I just clicked the unlock intelligence. Oh, I should click activation code, right?

56:42 - Levi Garner ( amaracore)
  Yeah, yeah, yeah. That way you don't have pay for it. One second. Let me. I think I have it.

56:47 - Apil Gurung (intelig.ai)
  Hold on one second. Yeah, maybe, maybe you're in a different browser that doesn't have that GitHub.

56:54 - Levi Garner ( amaracore)
  Thanks for that. You think that's it?

57:04 - Apil Gurung (intelig.ai)
  No, I was logged in before. It was set up already. Let me check. What am I going check to?  Yeah. Sorry. My network is acting up. You're good, man. Let me prompt it real quick.

57:56 - Levi Garner ( amaracore)
  I'm going to check. Okay, so I'm on call with Appeal right now. You can check his email. It's AppealGuru93 at gmail.com.  Can you check to see if that user, and you can check AWS, I'll send you the path, was already registered or not?  Because it prompted him on sign-in that he didn't exist. So just check the user that just signed up versus the appeal that we have in our system.  Check the logs and see what could have caused that or what's going on there.

58:41 - Apil Gurung (intelig.ai)
  Because I remember I forwarded you the welcome email as well. Yeah. Must have been, this was March 10th, so let's see if I can.  Let me see if I can log in with email. Did that go to your spam? Yeah. Hit the drop.

1:00:41 - Levi Garner ( amaracore)
  And is that connected to if you go to your code intelligence?

1:00:49 - Apil Gurung (intelig.ai)
  All right. Okay, let me see. Go to integrations real quick. Where is that?

1:00:57 - Levi Garner ( amaracore)
  click the integrations at the very bottom there.

1:01:03 - Apil Gurung (intelig.ai)
  Okay, I need to change this because I changed my GitHub from this account to apilgg24.

1:01:20 - Levi Garner ( amaracore)
  Oh, perfect. So we can just sign up with your new account then, right? Yeah. Now, which one are you logged into, technically?  Funny, this one, the apilgg24.

1:01:34 - Apil Gurung (intelig.ai)
  Because previously, I moved my, this one, this email GitHub to my now main account because I'm not working.

1:01:43 - Levi Garner ( amaracore)
  Okay, so it's the same GitHub account, you just changed the email? Yeah. Then it should be the same. Let me see, it's telling me everything that's going on here.  I'm just investigating. Because it says you're connected, right? If you go to repositories, maybe. It just didn't import. Oh, I know what I can do here.  Okay. Go to integrations real quick because I fixed this a few months ago. Click that real quick. Just click to manage.  Okay. Do a clean and re-import. Yep. I understand. Clean and select repos. So now it will take you here one second.  Let's let that load. It'll load all your, which ones are, okay. It's loading those. Click that. Don't see a repo.  Manage GitHub app access.

1:02:43 - Apil Gurung (intelig.ai)
  Yeah. So this, this is the one. One second.

1:03:00 - Levi Garner ( amaracore)
  Let's back to IntelliJ real quick. Because I think these are the ones that you were granted originally, right? Yeah, I think so.  So go ahead and jump back to IntelliJ, the other up in the URL. This one?

1:03:19 - Apil Gurung (intelig.ai)
  No, sorry.

1:03:20 - Levi Garner ( amaracore)
  Just go back from that one. If go back, I think I'm just going to do this. One second. Yeah, it says you have two GitHub accounts.  Yeah. And try to sign in with the wrong one.

1:03:53 - Apil Gurung (intelig.ai)
  Oh, that's right. Actually, Levi, I'm wrong because I moved all of this. A POGD 99 to a POGD 24.  I moved all the repositories from here to this one. I do have two GitHub accounts. I moved all of that, all of my stuff from this, the Gmail account to this 24 account.  Okay, and which one are you logged in?

1:04:20 - Levi Garner ( amaracore)
  You're logged into the old one right now, right?

1:04:22 - Apil Gurung (intelig.ai)
  Yeah, so this one is basically this, the one that I was logged into in IntelliJ, this repository, this GitHub doesn't have any more repositories.  Okay, so let's do this and log out of this one.

1:04:36 - Levi Garner ( amaracore)
  Yeah. And then let's, did you just try to sign up with the new one? Then like, which one are you authenticated to GitHub right now?  Because it's going to take whatever that one is in the browser. So let's make sure you're logged into the correct GitHub here.  All right.

1:04:56 - Apil Gurung (intelig.ai)
  All right, cool.

1:04:57 - Levi Garner ( amaracore)
  So try to sign in with GitHub. Sign up again. It's Appeal. Okay. I'm going to tell it. All right.  So we're trying to sign up now with AppealGG24. That's the correct account. What are you getting in the logs right now?  Because it's just showing connecting. Okay. It does look like it's authenticating. All right. Cool. I think we may be good.  All right. Hold off right here. Yeah. I'm going to give you a token. All right, so you just copy this into that, I'm going to send you on WhatsApp, into the coupon code for intelligence layer there, actually two, yeah, that's fine, just use that one.  Okay, and now we'll do install. Do you have that? Yeah, click that one. All repositories, install. Yeah, one sec.  we go. One sec.

1:07:51 - Apil Gurung (intelig.ai)
  The VPN here is not as strong as it used to be before. I don't know why. All right, well, it did look like Silly Connected.

1:07:58 - Levi Garner ( amaracore)
  Cool, you're good.

1:07:59 - Apil Gurung (intelig.ai)
  All right, now, which one?

1:08:00 - Levi Garner ( amaracore)
  Which repos do we actually want to select here? Like which ones are we going to actually, like which one is like the ones we're actually working on and want to track productivity on?

1:08:13 - Apil Gurung (intelig.ai)
  Let's say these five, because yeah, one, two, three, four, five, yeah, five. All right, cool.

1:08:24 - Levi Garner ( amaracore)
  Yeah, now it will analyze that commit volume in just one second on that. All right, cool. So let's just go all the way back.  So you just have 67 commits. That's going to be easy. That's fine. 67, last six months. Yeah, it's fine.  Continue.

1:08:49 - Apil Gurung (intelig.ai)
  This will be fun too, because like I'll finish up the discovery feature.

1:08:53 - Levi Garner ( amaracore)
  Yeah. And then we'll go through and attempt to. Cool. Yeah, it's syncing all of those. This was honestly, dude, as hard as building Cogniz.  The import from GitHub was like, that initial sync process. Because you think about it, dude. I mean, I basically eliminated what a data import person has to do, right?  Like, Accelerate's got these people that do those data  imports. That's what this basically does, just automatically as a backend.  All right, so we're done there. That's clean. So now if you go to Code Intelligence, let's just see commits.  Perfect. So let's go to Cogniz real quick. Now, this is what's cool, man. Just ask, like, what commits have I worked on the past week?
  ACTION ITEM: Finish Discovery feature; run on Apil's repos - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=4202.9999  Very cool. All right, cool. So now what we'll do, okay, let's do this, man. Let me finish up my discovery.  We'll jump back on because basically what the process would have been, okay, the first step that you would have had to do is you would have to go to strategy.  Oh, actually, let's do this real quick, dude. This is  perfect. Perfect. We're going to do this because you and I are going to start to have these meetings, okay?  And what we're going to do is all these conversations that we have, exactly that flow I mentioned where it's got to pull down into your repo, that's now eliminated with this.  Open up Fathom real quick. It's absolutely free for this. Fathom. Using your Gmail. Yeah, see that Fathom right there, AI Notetaker.  It's the best, honestly. We give Bobby a little bit of credit for picking Fathom. I've... I'm writing right now an integration with Teams, dude.  I finished it in two days, but Teams. Can you imagine people wanting to use Teams to record Microsoft Teams?  It's like, dude, right.

1:11:15 - Apil Gurung (intelig.ai)
  Fathom's nice.

1:11:15 - Levi Garner ( amaracore)
  Their APIs are a bit . Their webhooks do not work, but it's a nice recording. All right, so we'll sign up for free there.
  ACTION ITEM: Create Mala Plants branding/website initiative; build site w/ Claude - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=4295.9999  I think what you should do, honestly, man, I'm telling you, this is, I'm telling you, a smart move, appeal.

1:11:45 - Apil Gurung (intelig.ai)
  Yeah.

1:11:46 - Levi Garner ( amaracore)
  Post this call. I actually think we should have an initiative that we set up for you to build out the full branding of this application you want to build.   the product off for now.

1:11:58 - Apil Gurung (intelig.ai)
  Okay, hear me out on this. Build out the brand for it.

1:12:01 - Levi Garner ( amaracore)
  Build a super professional website with Claude, okay? And I'll show you the tree inventory structure. I actually, in my mono repo, have the website as part of it, okay?  IntelliJ doesn't care whether it's a mono repo to report on your initiatives, but start building out the brand for this.  We're going to make this  look super big, okay? And super professional, okay? Like, what names are you thinking for this?  For this?

1:12:29 - Apil Gurung (intelig.ai)
  Yeah, this nursery app. I don't know. I picked this name up just because of my parents. plants? It's cool.  I like it. What's mala mean? Mala means like a garland of flowers. Okay, cool. In Nepali. Mala plants. Yeah, but I don't know.  I don't know. I haven't really gotten into the naming and branding stuff. I just wanted to build the stuff first, and I hadn't given much thought on the branding or naming.  know. don't know. No, I like Mala. fine. It does not matter.
  ACTION ITEM: Create identity/security hardening initiative; implement RLS + org management - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=4381.9999

1:13:02 - Levi Garner ( amaracore)
  So we'll build out the Mala, the website, okay, as one initiative. You need to do that as part of your initiative, your branding.

1:13:09 - Apil Gurung (intelig.ai)
  Yeah.

1:13:09 - Levi Garner ( amaracore)
  The branding is actually not bad itself. Another initiative you're going to have is the identity security hardening, right? Like we've got to get that super, super tight with your RLS.  And I'm telling you, everything I'm saying right now,  co-op is going to pick up on it. It's going to know what to do with your organization, management, et cetera.  Okay. I am going, I'll give you access to like Tree Inventory AI because I'll have you help me some on Tree Inventory AI and you can also rip from some of the code there.

1:13:39 - Apil Gurung (intelig.ai)
  Do not care. Okay.

1:13:41 - Levi Garner ( amaracore)
  And part of that, you can reference it. Okay. For how I did RLS, et cetera. You'll probably find some bugs in it.  Yeah. That's what I found with Tree Inventory AI. Like I'll use Tree Inventory AI because I'm rebuilding something from IntelliJ and I'm doing deep research on IntelliJ to pull into Tree Inventory AI.  Yeah. And then Tree Retrieval-Augmented. Oh, by the way, you need to fix this thing. You know what I mean?  You'll find similar stuff. Just clean that up when you see it for me. But yeah, make it a very cool login, etc.  Should I just use the personal email on this one?

1:14:19 - Apil Gurung (intelig.ai)
  Yeah, continue with personal. You were saying, sorry. No, yeah, I was just saying that.

1:14:28 - Levi Garner ( amaracore)
  So that would be another initiative, the website, branding. Another piece will be the security hardening, the org management, etc.  Because you've got to make this like that. That main page has got to go. Unless you're thinking this mall of plants is going to be for...  That is kind of cool, actually. If you're kind of building a marketplace. Is it a marketplace, technically? Yeah. What you're building for Nepal.

1:14:53 - Apil Gurung (intelig.ai)
  That's  cool, dude.

1:14:55 - Levi Garner ( amaracore)
  Then it can be kind of like you're listing those plants. But you see what I'm saying? See how buy local...  That's got to be, and you've got to add from this main page here, man, you've got to add the areas, right?  You know what I mean? It's like a Google search, basically, where they can filter by like, you know, I'm in Jollicale right now.  You know, I only want vendors around me. I can't travel far. Or,  it, dude. You know, it'd be super cool with this appeal.

1:15:29 - Apil Gurung (intelig.ai)
  That's what I'm saying.

1:15:30 - Levi Garner ( amaracore)
  They upload it from, and then the delivery comes in to play.

1:15:34 - Apil Gurung (intelig.ai)
  Right? You plug in with the delivery.

1:15:37 - Levi Garner ( amaracore)
  Like, are you thinking potentially, yeah, I mean, they could just self-manage it with , you know, delivering pants is a little bit more difficult, but yeah, go ahead, man.

1:15:51 - Apil Gurung (intelig.ai)
  They, it's like, what I was thinking was like, okay, if it's within, let's say, five kilometers, six kilometers, blah, blah, blah, and  And then if you pay above, like, let's say, 1,500 rupees or 1,000 rupees, delivery will be free, blah, blah, blah.  Or, like, you – I mean, there are delivery apps. Like, you know Denim, right? He's, like – he and his – another friend of his who both went to Lincoln, they have, like, a delivery company that they – that it's quite popular in Nepal, Tudel.  And then Tudel – Denim built this?

1:16:29 - Levi Garner ( amaracore)
  No, they did not build, but they acquired it.

1:16:34 - Apil Gurung (intelig.ai)
  Oh, okay.

1:16:36 - Levi Garner ( amaracore)
  And then the other one is Patel.

1:16:38 - Apil Gurung (intelig.ai)
  I'm pretty sure – Yeah, Patel. I used that one. Yeah, but Patel is from Bangladesh. Tudel is from Nepal.  then Click Tudel real quick.

1:16:46 - Levi Garner ( amaracore)
  I just want to see that app real quick. Yeah.

1:16:49 - Apil Gurung (intelig.ai)
  And Tudel was actually done by Nepali developers. And then Denim and his good friend who both went to Lincoln, they acquired it.  Oh.

1:17:00 - Levi Garner ( amaracore)
  How long ago did they acquire?

1:17:04 - Apil Gurung (intelig.ai)
  2023, I think. Dude, I need to message him right now.

1:17:10 - Levi Garner ( amaracore)
  So how many developers do think they have? I have no idea, dude.

1:17:15 - Apil Gurung (intelig.ai)
  I haven't been in touch with them in a long time, but yeah. No, dude, I know him well. Yeah, because they used to have this app called Zap, which they did delivery.  The Zap services, right? This guy, the other guy's name is Shreyash and Denim. So they're two good buddies. They made Zap.  who owns Toodle, you said, right? Sorry? Denim, you said, owns Toodle?

1:17:45 - Levi Garner ( amaracore)
  Yeah. Now they own Toodle as well.

1:17:48 - Apil Gurung (intelig.ai)
  They first created Zap, which was another delivery service. And then later on, they acquired Toodle. Got it.

1:18:00 - Levi Garner ( amaracore)
  Zapp they own as well. Yeah.

1:18:03 - Apil Gurung (intelig.ai)
  Open that one up real quick.

1:18:06 - Levi Garner ( amaracore)
  I don't know how active they are today.

1:18:09 - Apil Gurung (intelig.ai)
  I used to follow them on Instagram, like sending packages on Scooter, especially within Kathmandu. This is cool, dude. Yeah, it's like, yeah, they did this during COVID.  That's what I remember. Because I met Denim and the other guy during COVID time. And, you know, they were like, oh, you need to get this app of ours.  Like, you know, so that you can use delivery for stuff.

1:18:57 - Levi Garner ( amaracore)
  don't know why he's never  told me one time about this. Like, I've never once, one time been like, oh yeah, dude, like I tell him all the time I'm in tech, like we talk about, and he always talks about his  like bread business or some .  Lame. I don't know why he ain't talking about this, you know?

1:19:14 - Apil Gurung (intelig.ai)
  I think this is just like his side hustle because their family is like, they're quite rich. Maybe he just invests in it, dude, but has nothing to  do with it, possibly.

1:19:23 - Levi Garner ( amaracore)
  Could be. I don't know, I messaged him, I'll see, I'm curious.

1:19:26 - Apil Gurung (intelig.ai)
  Yeah, yeah, they do this. Yeah, that's what I was thinking, like either, let's say, because what my idea with this was like, okay, I want to build a marketplace because there's so many nurseries, so many local growers in Nepal or in Kathmandu, right?  I just want to start out with my parents first and then slowly give access to other, you know, like applications for nurseries, like who are qualified.
  ACTION ITEM: Create Go-to-Market initiative; build beta vendor list; contact Kathmandu nurseries - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=4793.9999  But I just want to, yeah, I mean... mean... But now you said, oh, just give it. Yeah, and now if you're like, yeah, just let it out.  give it away, dude.

1:20:04 - Levi Garner ( amaracore)
  So what you should really start to do now, Apil, I'm telling you, dude, is like, before you ever build this thing, go get the clients.  That's where I've also made major mistakes. Like, we think we're going to build something and people are just going to  start using it.  It's not a bad idea, but like what you should do right now is like go on Google search, search for all of the nurseries in Kathmandu and be like, hey, I'm building this app.  But first, make your app look a little bit more, you know, like I said, like a super cool landing page and she'll be like, I'm building this.  Dude, it's so  easy. If you just give it away to them, be like, look, you can take pictures of your plants.  You use the app, come to Kathmandu, use the app and take pictures of it, automatically identifies what the plant is, you know, and creates the name of the plant, et cetera.  know, creates their catalog for them, basically. And then all they have to do is, you know, make it really easy for them to create their vendor profile.  That's what I'm saying. The multi-org identity is extremely important in this app. Let them create their vendor profile and then let them start uploading their products or link to their Google profile.  But you could do some cool stuff, man. That's where AI comes in. Apil, you need to link to their website or whatever, their Google, to pull all their information automatically for them to just fill it out.  That'll also be helpful.

1:21:36 - Apil Gurung (intelig.ai)
  Yeah. So yeah, they can, yeah. Perfect.

1:21:42 - Levi Garner ( amaracore)
  So you've got some of this in there. Did you add in the ability, is it handling the multi-org? Right now, in the back end, at all?

1:21:56 - Apil Gurung (intelig.ai)
  Not yet. Not yet. Not yet. right, right. That's my next problem. I just finished. So yesterday after the talk with you, I did this.  So if I'm not assigned end user, and when I press add to cart, it just this signals you to add.  so that's for the end user, but what about for the vendor?

1:22:17 - Levi Garner ( amaracore)
  So you have to have both those pieces, right? The vendor has to be able to manage as well, right?  Yeah.

1:22:25 - Apil Gurung (intelig.ai)
  Yeah. Yeah. haven't got to that part yet. So next session after our call, that's what I'm working on. Cool.

1:22:37 - Levi Garner ( amaracore)
  No, dude, I want you to be a use case for IntelliJ for this whole project. Okay. 100%.

1:22:43 - Apil Gurung (intelig.ai)
  And that's what I'm saying. You won't have to do anything, but you have, you see what I mean? You have to get a little bit organized when you run these businesses.

1:22:49 - Levi Garner ( amaracore)
  Yeah. Like even as a tech startup, like you have this idea, but how do you really take it to market?  We have to identify what your initiatives are, what you're going to do from a code perspective. And that's what this app is going to give you.
  ACTION ITEM: Schedule follow-up w/ Apil; add Fathom to invite - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=4986.9999  This will all automatically be created for you.

1:23:15 - Apil Gurung (intelig.ai)
  Yeah, let's talk about it a little bit more.

1:23:17 - Levi Garner ( amaracore)
  I actually have a really cool idea. Did you sign up for Fathom? Yeah. We'll end this call, then we'll jump right back on call, and then we'll go through what your initiatives are, and then we'll create those automatically from the recording, and then we'll sync this.  We'll import this as a historical meeting, okay, because it won't catch it in the webhook. We'll just use import historical meeting, and it'll pull down into your code base.  It'll actually pull down. If you go to your repositories right now.

1:24:11 - Apil Gurung (intelig.ai)
  You see what I mean? That's another thing, dude.

1:24:13 - Levi Garner ( amaracore)
  You can help me. I'll help you with this. I mean, what other apps? Because that's what I'm going to say, dude.  I'm going to teach you how to use IntelliJ. Yeah. Because there's a ton of these tech companies that could use  IntelliJ in Nepal.
  ACTION ITEM: Clone IntelliJ repo locally next to project repos - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=5067.9999  I just need users, more users. I don't necessarily care about if they're going to... I don't need to charge them.  I've got some paying customers. That doesn't really concern me.

1:24:35 - Apil Gurung (intelig.ai)
  I see that IntelliJ signals right there.

1:24:38 - Levi Garner ( amaracore)
  It's going to automatically push all your meetings into that. Okay. So you want to open up in your workspace, clone this locally, right next to your repos.

1:24:48 - Apil Gurung (intelig.ai)
  Okay.

1:24:49 - Levi Garner ( amaracore)
  And it's going to pull... Don't even... Wait, wait, wait. I'm going to show you something real quick. Have you set up a key yet to give to Claude?  Show me your Claude workspace real quick, what that looks like. Claude space, this one? Well, what are you using?  Cursor? VSCode.

1:25:08 - Apil Gurung (intelig.ai)
  All right, that's also fine.

1:25:09 - Levi Garner ( amaracore)
  And you use Terminal? Yeah. All right, that's good. Did you give Claude a client secret or token, classic token, so it can automatically commit and push for you?

1:25:24 - Apil Gurung (intelig.ai)
  No, I haven't.

1:25:26 - Levi Garner ( amaracore)
  All right, let's do that real quick, dude, because that's going to save you so much time, because you could just ask Claude right now.  You could say, go commit and push all my changes. You see what I mean? Can you do that now?  Or do you have to manually commit and push them?

1:25:40 - Apil Gurung (intelig.ai)
  I mean, I think I can push them. I did that with... Hold on. Yeah, just check it real quick.

1:25:46 - Levi Garner ( amaracore)
  I'm curious. Here, let me go here.

1:25:49 - Apil Gurung (intelig.ai)
  I think I pushed it with Claude earlier. Let me go back here. In the resume website, I think I...  I pushed it with Claude. Where is it? Right, this one? Is this what you mean?

1:26:23 - Levi Garner ( amaracore)
  Denim said he's out of those companies, I guess. Oh. All right. Is this what you mean? Yeah, yeah, I think you're committing it with Claude.  You're not manually going to GitHub and saying, typing in a commit message, are you? No, no, no.

1:26:46 - Apil Gurung (intelig.ai)
  All right, cool, cool, cool.

1:26:47 - Levi Garner ( amaracore)
  All right, yeah, I think you've got it set up then.

1:26:50 - Apil Gurung (intelig.ai)
  Yeah.

1:26:51 - Levi Garner ( amaracore)
  All right, jump back to IntelliJ, or, yeah, jump back to IntelliJ real quick. All right, so go to Knowledge.  Then go to integrations, then go to connect Fathom. So yeah, just open up, open API settings, and then it'll prompt you.  You don't have to do, you could, you know, whatever. Did you, maybe, I think that was another tab or something.  Jump back to IntelliJ, I don't even need that. If you jump, just click open Fathom API settings. I should open the, yeah.  Oh, you've not finished the setup. That's why it's making you, yeah, finish the setup real quick. Yeah, sorry, it took a while for the.

1:28:01 - Apil Gurung (intelig.ai)
  All granting access thing, right? Applications.

1:28:18 - Levi Garner ( amaracore)
  Yeah, I saw that one company you saw that said that was kind of big, that Frogger company, or what's the name of it in Nepal?  Something like Frogger, right? Or LeapFrog or some ?

1:28:29 - Apil Gurung (intelig.ai)
  LeapFrog.

1:28:30 - Levi Garner ( amaracore)
  Dude, those kind of companies are just going to get wiped out. You know what I mean? Those service development companies are  done, dude.

1:28:37 - Apil Gurung (intelig.ai)
  Yeah. Done. And they're based out of Seattle, and then they, yeah, they're partnering here in Nepal. And, yeah, they've been quite popular.  Like, a lot of the top developers in Nepal have been, like, trying to get into that company. But in the future, I think they don't have a future, unless they change, like, their directions drastically.  Yeah. All right, let me see, what is, all right, yeah.

1:30:00 - Levi Garner ( amaracore)
  I'll be right back, man. want to say I'm just going to take a break. Sure. Can you hear me, man?  Yeah, just one second, Fathom.

1:32:00 - Apil Gurung (intelig.ai)
  This being a little bit annoying, it's not letting me enable this, I don't why.

1:32:09 - Levi Garner ( amaracore)
  And that's no worries, just enough to get it set up, because we'll just sync it in from my call anyway.

1:32:15 - Apil Gurung (intelig.ai)
  And screen and system audio, no screen.

1:33:07 - Levi Garner ( amaracore)
  What the hell?

1:33:15 - Apil Gurung (intelig.ai)
  There we go.

1:33:39 - Levi Garner ( amaracore)
  I love this guy just there. Yeah. Who's making it very longer for her? Yeah, she'll just want to keep bringing it harder without her.

1:33:50 - Apil Gurung (intelig.ai)
  Somehow I'm not able to get this Fathom set up. Do we need that? Maybe if I can. No, this is good enough, dude.

1:33:59 - Levi Garner ( amaracore)
  So now... All you have to do is open up the browser, account link, perfect. So now just go back to Intelligent, click Open API Settings, because when we talk, it'll be fine.  We'll be able to import even this conversation, I believe, from yours.

1:34:20 - Apil Gurung (intelig.ai)
  See, I'm trying to enable this, and it's not letting me enable.

1:34:30 - Levi Garner ( amaracore)
  Just close that, click X, go to Settings real quick, in Fathom. Let's do a Command R on this, let's refresh this.  Yeah. Maybe they changed some  in their stuff. Like, you have to do all this from the desktop app? I don't know.  That's weird. Yeah.

1:35:15 - Apil Gurung (intelig.ai)
  I'm trying to click it, it doesn't open, which is so weird. Just maybe log out of here and log back in.  Yeah, just quit that. Yeah.

1:35:28 - Levi Garner ( amaracore)
  Quit that, and then just log out of Fathom there, and then sign back in on the web. Yeah.

1:35:35 - Apil Gurung (intelig.ai)
  And then now just continue with Google. All right, let's see if it works this time.

1:35:50 - Levi Garner ( amaracore)
  Yeah, open it up down there. still nothing. think you have to do it from settings, you know, like enable Fathom.  Yeah, that's what I'm trying to look, find.

1:36:10 - Apil Gurung (intelig.ai)
  Go to sound.

1:36:12 - Levi Garner ( amaracore)
  Yeah, click sound there. It should open up like permissions. Yeah. I mean, I don't know. Fathom's like new UX is like here.

1:36:40 - Apil Gurung (intelig.ai)
  This is kind of annoying. Let me just ask Claude. Privacy and Security, Screen and System, there we go. You're all set.  It said you're all set. Yeah, so now refresh this maybe.

1:39:00 - Levi Garner ( amaracore)
  Now, IntelliJ just makes it easy to jump to that. So if you go back to IntelliJ, it'll just automatically take you to the API settings.  If you click that link now, it should allow you to go there. Okay, just close that. All right, cool.  You're good. So see that API access? And that's what I'm setting up next, that  MCP server. That's going to be cool.  But anyway, click Add on API access.

1:39:30 - Apil Gurung (intelig.ai)
  Yeah. All right.

1:39:32 - Levi Garner ( amaracore)
  Generate an API key. Then just call it IntelliJ. Yep. Create API client. Copy that key there. Jump back there.  Plug that in. No, got to, yeah, paste that in there. And then hit Connect Fathom. And then... Now, IntelliJ just makes it easy to jump to that.  So if you go back to IntelliJ, it'll just automatically take you to the API settings. If you click that link now, it should allow you to go there.  Okay, just close that. All right, cool. You're good. So see that API access? And that's what I'm setting up next, that  MCP server.  That's going to be cool. But anyway, click Add on API access. Yeah. All right. Generate an API key. Then just call it IntelliJ.

1:40:40 - Apil Gurung (intelig.ai)
  Yep.

1:40:40 - Levi Garner ( amaracore)
  Create API client. Copy that key there.

1:40:46 - Apil Gurung (intelig.ai)
  Jump back there.

1:40:48 - Levi Garner ( amaracore)
  Plug that in. No, got to, yeah, paste that in there. And then hit Connect Fathom. And then... And you won't have any meetings, so you can just skip this.  Cool. So now on our next one, you'll just add that to the call. And once the call finishes, it's going to take our meeting and automatically push it into IntelliG signals.  Okay. So if you go to signal there, it should be connected automatically for you. Yeah. Direct commit, auto-sync enabled.  All right. So let me do this, dude. I'm going to hang up this call real quick. And then we'll...  Actually, let's see. Can you add it to the meeting right now? Let's fathom what, yeah? Let me see. Or go to Google Meet real quick and try to...  Oh, yeah. It says, I think it's in the meeting right now. I see two appeals. Oh, no, no. I'm sorry.  Yeah. So click add to meeting right there. See that? Yeah. Start meeting. It'll prompt me to, yeah, switch here.  Well, does it let you add it to that meeting? If you click, oh, yeah, I got it. I got it.  You're good. All right, perfect, dude. So we're now officially in. All right, so you'll have the beginning of my transcript I'll send you, which you can just paste into IntelliG meetings, the beginning one, and then we'll have this one.  All right, so plain English appeal, jump into Mala, the application. Let's talk about the vision of that application, what it is, okay?  Let's talk about a vision of it. Let's talk about your roadmap, okay? Yeah. Just open up IntelliG real quick.  I just want to show you what we're going to do. So in plain English, okay, what's essentially going to happen if you open up IntelliG?  Yeah. I can't see your screen, maybe. I'll stop presenting. Oh, sorry. Entire screen. All right. All right. So open up strategy real quick, Apil.  I just want to explain kind of what we're going to do as an experiment here. Yeah. See how we have your vision and roadmap?  Yeah. We're going to talk in plain English, okay? And essentially, Claude, okay, our good friend Claude, what we're going to do is we're going to talk in plain English about kind of what the vision and roadmap is for this app.  Then we're going to use one of IntelliJ's agent playbooks. We're going to paste that off to Claude. We'll give it an API key.  And then we're going to feed Claude as well, the transcript you and I talk about right now. And it's going to automatically appeal, create your vision, create your initiatives, so on and so forth.  You get what I'm getting at there. And then all your commits are automatically going to be linked. Well, the initiative linking is one other piece, but that's easy.  There'll be linked to these initiatives. So even. For example, maybe one of your initiatives is probably going to be your website, right?
  ACTION ITEM: Leave LinkedIn review for Apil; ask Nathan to do same - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=6245.9999  Like your public branding. You've got to do some other stuff we talked about on LinkedIn, know, getting your profile kind of updated with the Accelerate, you know, that's one action item there.
  ACTION ITEM: Draft SOW to bring Apil under AmaraCore for consulting - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=6252.9999  And then another action item is for me to leave you a review, and then I'll get Nathan to leave you a review.

1:44:23 - Apil Gurung (intelig.ai)
  Why? Because in the near future, right, I'm going to be leading, I'm working as a private AI, you know, consultant for this big U.S.  company, right? So I'm going to execute on this project for it, finish it, then I'm going to promote, you know, and I'll create an SOW to bring you in under me, under AmeriFore, okay, as a consultant.  Yeah. So you can still get paid. That would be, so that's kind of part of your appeal website, making yourself look super, as an initiative, right?

1:44:58 - Levi Garner ( amaracore)
  So appeal, that would. Repository, yeah, that repo will be linked under that. So any commit, you'll see that. Any commit linked to that repo will go under that initiative.

1:45:09 - Apil Gurung (intelig.ai)
  The other one is just mala plants.

1:45:15 - Levi Garner ( amaracore)
  Talk to me about the vision of that application. So I basically want it to be like a marketplace for local homegrown gardeners that want to sell their plants or even nurseries around, let's say, let's begin with the city of Kathmandu, and then we can slowly expand it towards all of Nepal and maybe even spread it to India so that these local gardeners and nurseries can sell their plants to, you know, customers across Nepal or India.  So, yeah. Yeah, and kind of like a use case, right, man, would be like, and this is what I was talking about.  We need another initiative for like GoToMarket. Hold on. think we're cut off. Are you able to hear me, man?  One second. Yeah. Can you hear me all right? Yeah, now I can hear you. Are able to hear me now, man?  Yeah. All right, cool, dude. So kind of another initiative we have. So that's kind of the vision. One kind of initiative I see with this is the GoToMarket strategy, which is obviously kind of like the public facing.  But what's kind of cool with this, man, it's a marketplace. Yeah. Right? So the website itself kind of is the marketplace itself is kind of the website.  Yeah. Right? Because like the first page, someone. When lands will be like here. Yeah. They can probably select, we need to prompt Claude with that, like some serious, like next level UX.  That's why you had Amazon open, right? Because it's kind of similar.

1:47:12 - Apil Gurung (intelig.ai)
  Yeah. But dude, I'm telling you, that's another thing with Claude, dude. It's like, let it control more of the UI UX.  So a prompt I always use is like, or you can use the agent mode for it as well.

1:47:23 - Levi Garner ( amaracore)
  Yeah. Designer, like, and that's what I'm saying, giving it this vision. Because it'll come up with a better UI UX than you and I could even, right?  For like the main landing page. Yeah. Right? All right. So that's one piece there on the, a go-to market will be kind of a theme.  Yeah. Right. Then under the go-to market, we're going to have like public facing materials and initiatives. So like one of the initiatives you'll have, man, is like getting these beta customers, probably like contacting every single one of these vendors in Nepal.  Yeah. Right. In Kothmandu, just looking up nurseries. Those are. They're going to be your customers to get on the app, right?  Essentially. Yeah. All right. Cool. I was just thinking, because this is just a web app right now, or just a website right now, should I take an initiative to build a mobile app as well, or just leave it?
  ACTION ITEM: Implement MVP: vendor profiles (Google link), manual uploads, location filters; launch in 15–30 days - WATCH: https://fathom.video/share/_VsKdn45KUeMKjNKWmqF7yTyWLJwFxK3?timestamp=6493.9999  Separate, dude. Separate. So, like, I'm telling you, man, like, you should be completely, you should be live, I'm not joking, dude, 100% with this kind of app, you should be live with it in 15 days from now.  There's absolutely no reason. We couldn't be live with this 30 days maximum, dude. 30 days maximum, 100%. Vendors should be able to, so basically the main kind of use case is, right?  Vendors can take the pictures, upload the pictures, you know what I mean? And then it basically shows in this marketplace.  each one of the vendors, that's where, like... I would put that in your MVP, allow them to like copy in their Google profile link, and then you automatically extract that and categorize them in terms of locations, right?  Because people are going to want to be able to fill, when they come here, like different areas within Kathmandu, right?  But that's also what's cool with this app is that you'll actually be able to sell these plants. People can buy them anywhere.  doesn't matter because it gets delivered, right? This is a use case like I've even fell into. Like I want to buy plants, but , dude, I don't want to have to go to the nursery.  And that's your main, that's your main selling point. It's like when you go to these vendors, it's going to be like, dude, we can sell your plants across Kathmandu, right?  Like you're now, this is, you're now not just selling to people in Dobigat, right?

1:49:58 - Apil Gurung (intelig.ai)
  You're selling to. To everyone in Kathmandu.

1:50:02 - Levi Garner ( amaracore)
  It's a  cool concept. This app will take off. This app will take off. Also, another thing, we're not concerned about pricing.  It's going to be absolutely free for people to use. And where you're going to make your money, dude, is in the transactions.  You can later make your money in the transactions, like a small transaction fee. You can take money off the top.  So, like, let's say it sells for 500 rupees, right? You take 10 rupees or whatever. I don't know. Claude will help come up with the proper pricing structure.  You see what I mean? That's where you can make your money down the line. But don't even  worry about taking anything off the top for now.  Because also what people will, yeah, I think that's smart. Same thing as Patel, right? Patel delivery just adds in a fee for you.  Yeah, they charge 20% to each rider for their, each rider. Which is quite high. Yeah, exactly. Now, another big one we already touched in.  I'm not going to touch on that too much, but I'm telling you, dude, walking down this app for the RLS, the org identity, et cetera.  And I'll add you as a member on my tree inventory AI so you can have Claude reference my repo to kind of see how.  And don't even  the AI features for now, dude.  all that off. Just let people upload and give the name of their plants manually.  Okay, I'm telling you, dude, I've wasted way too much time.

1:51:29 - Apil Gurung (intelig.ai)
  I'm trying to build fancy-dancy features. Like, even in my app, I shouldn't even have built  arborists in MVP.  that off.  Just build. That should have been my MVP. You know, and I went and added arborists. And all these fancy things that people don't really give that much of a  about.  You know? Yeah. All right, cool, dude. That's perfect. perfect. That's perfect. So... Wow. Yeah, so, and two, I think what's going to be cool with this, too, man, we're going to, let's end this call.  Yeah. Then, because once you end it, then we'll jump right back on call. We'll pull those transcripts into Claude, and then I'll show you the next stages within IntelliJ and Claude kicking off this.  Because do you have, like, a vision? Yeah, anyways, you'll see, dude. You'll see. All right. We'll hang up this, and then I'll create another meeting right away, and we'll stuck in the news.  All right, go on. All right.