Matias Hernandez (00:07):
I'm Matias Hernandez, and this is Café Con Tech.
Matias Hernandez (00:21):
My name is Matias Hernandez. I'm a Chilean software engineer currently working with Clevertech. I'm also an egghead.io instructor and a technical writer. Now, without further ado, let's start with the show.
Matias Hernandez (00:38):
And thanks to the sponsors of this show, Auth0 and Cloudinary Media Developer Expert Program. Auth0 provides an out-of-the-box authentication and authorization platform for any application with just a few lines of code. Check the incredible documentation and examples on auth0.com.
Matias Hernandez (00:57):
And Cloudinary MDE Program is a community of developers to share insight, expertise, and best practices of using media technology in web and mobile applications. Check it out on cloudinary.com.
Matias Hernandez (01:09):
Welcome to the second episode of this special season of Café con Tech. Today I have Sam Julien that's joining as  guest. Sam is actually the Developer Relations Manager at Auth0, but also an author, a self-published author, and author of a very good newsletter that I hope all of you follow it. Welcome to this show, Sam. Happy to have you here.
Sam Julien (01:49):
Yeah. Thanks Matias. Thanks for having me. I've had other podcast interviews get mad at me for not saying this earlier, but my name is actually pronounced Juleen. So this time around, I'm going to say it ahead of time, because I've had a few podcasts where I casually mentioned it later and the hosts are like, "Why didn't you tell me that ahead of time?"
Matias Hernandez (02:10):
Yeah. It's a good point. As far as I can tell, I hear a few podcasts and conference talk, and most of the people said Julien. And it's Juleen?
Sam Julien (02:24):
Yeah, it's very common. I got it my whole life growing up and everything. And sometimes I just don't even notice it. I am so used to it that I don't notice it, and I'm trying to get better about noticing it and letting people know.
Matias Hernandez (02:38):
That's a good one. It's actually Juleen. That's you. The other one is someone else.
Sam Julien (02:44):
Exactly.
Matias Hernandez (02:46):
Okay, Sam. Thank you for coming by. As I already mentioned this, I'm really happy to have you here in this spinoff of Café Con Tech show. We will talk during this conversation about microskills. That is the thing that I guess people could be more interested, but also about dev role and whatnot in the conversation, whatever it comes out.
Matias Hernandez (03:09):
So to start, I did a really poor work on presentations. so can you introduce yourself a little bit? A little bio?
Sam Julien (03:19):
Yeah, sure. Yeah. No, you did great. You did great. Basically, my day job is I'm the manager of the Developer Relations Team at Auth0. I have seven people on the team under me. And that's a lot of fun. It's a really fantastic group of people.
Sam Julien (03:38):
And then, on the side, I do books and courses and things like that. My main ones are a book called Getting Started in Developer Relations and another one called Guide To Tiny Experiments. I also make lessons and courses on egghead.
Sam Julien (03:55):
And then I have a newsletter called Developer Microskills where each week I send out a practical and actionable way to improve as a developer and developer advocate. So that's the nutshell. And I live in the Pacific Northwest of America. Yeah, I think that's everything.
Matias Hernandez (04:13):
I could say that you're also a prominent Twitter thread creator, something like that. People kind of follow your lead and answer your questions on Twitter. That is amazing.
Matias Hernandez (04:25):
Okay. So can you tell us a little bit, what is a developer microskills? I mean, I'm subscribed to the newsletter from start, and it's actually really good content in terms of little things that can actually really improve your life. And maybe it's some kind of a... Sam, you're becoming the self improvement developer area angel, whatever. Because the content is actually not really technical, but helps you with the technical side. Can you describe a little bit what are you writing there?
Sam Julien (05:03):
Right? Yeah. Yeah. You really nailed it. Basically where it came from was over... From about 2013 to 2017, I went through this big period of transformation in my life. I had just gone through this really painful divorce, and so I was kind of restarting my life from scratch. And so I did a bunch of stuff with my physical health and my mental health and my career and all of that.
Sam Julien (05:33):
And at first, right around like 2016, 2017, I was sort of thinking, "Oh, I made all these huge changes and look how great I am." It was kind of insufferable. And then as I got a little bit older and wiser and looked back and kind of read through my journal entries and things like that, I realized it was actually these tiny decisions that I made or these little skills that I picked up about how I interacted with the world, and how I treated my self-care, and how I looked at work, and all of those things that actually compounded over the course of a few years to build these big changes in my life. And so that's where the newsletter came from.
Sam Julien (06:13):
And a lot of my writing is trying to share that often when we think about achieving big goals around our health or our careers or things like that, it feels like this huge overwhelming effort, and there's actually these little things that you can do, these little skills you can learn, that I've coined microskills, that will add up over time. So that's sort of the general philosophy of it.
Matias Hernandez (06:37):
I really like the idea that first you're sharing your kind of process, your learnings, learning in public, this topic that is becoming wider and wider. And also I really like that you went to the path about talking to the developers, but not in the technical side. And that is something that now I think that it's more common than even a year ago that people tend to start thinking in developers like human beings that needs to improve different other aspects of their life to actually level up their careers.
Matias Hernandez (07:16):
Talking about level up their careers and the content you share in your newsletter, can you tell us a bit about what is the newsletter issue that maybe you enjoys the most writing it?
Sam Julien (07:29):
So probably the biggest one was I wrote this one called How To Finish What You Start. And that one turned into a whole bunch of things. The response to it was really, really good, so I turned it into a blog post and then that's what ended up actually becoming the book Guide To Tiny Experiments.
Sam Julien (07:49):
And that one was just a process. We all kind of struggle with finishing all of those side projects we want to do, and so I wrote this article about this process that I use to actually finish things. And I tried to do it in a really practical and step-by-step way, and that got a really good response. And so that one was a good one.
Sam Julien (08:12):
Another one from just a couple of weeks ago, I wrote this one called Embrace Your 1% Days that was all about: to make progress on something, it doesn't have to be all or nothing. You're better off making a 1% effort on a goal you have, like maybe working out or something like that, then doing nothing, and that you should be happy about that and do that.
Sam Julien (08:38):
So if you, for example, if your goal is to work out more and you work out a couple of days in a row and then you don't feel like it, you're better off even just putting on your gym clothes and walking to wherever you're going to do your workout, or driving to wherever you're going to go, and turning around and going home than you are just skipping it altogether, because you're still creating this pattern in your brain and building these neurochemical pathways that are basically telling your brain, "Hey, when I am done with work, I do this exercise." So that one also got a really good response. So I'll probably turn that into a blog post too.
Matias Hernandez (09:15):
I think that your content in the newsletter ties really nicely with the concept of content creation aspect of developer lives. If you was part of the cash note booth come three, talking in particular about content creation and how to write, and you have a few numbers of the newsletter about technical writing. I think that was the ones that hooked me up onto the newsletter because I was really interested in that.
Matias Hernandez (09:48):
So can you describe a little bit... People go and check the talk on the hash node, but can you describe a little bit what was the content about that and what people are interested on your knowledge there?
Sam Julien (10:06):
Yeah, for sure. So the talk for hash node was called The Counterintuitive Secret To Shipping Better Articles Faster, and it was really all about consistency. And I'd written some of that in the newsletter. I had written an article or an issue called The 90 Day Rule, which is all about some tips and tricks for getting consistent results on things.
Sam Julien (10:34):
And so I wrote this talk for the hash node bootcamp that I'm going to use other places too, but basically it's sort of all about how a lot of people, when they start blogging... I did this too. If you go back and look at my blog, you'll see how you get started and you write this big article and then you go silent for months or even years at a time. And sometimes that works and sometimes it doesn't, but most people generally don't like this about when they're trying to write.
Sam Julien (11:10):
And so I've kind of discovered some tricks to figure out that you're better off writing smaller articles more consistently and building the habit of doing the technical writing, because you can always build on that over time. You can always make bigger articles, longer articles.
Sam Julien (11:30):
But there's this kind of process that every article is going to require of editing it and promoting it and optimizing it for search traffic and that kind of thing, and so building the habit of doing that with little articles is going to help you run through that process over and over again, and you're going to see a lot better results than just sort of sporadically writing every so often.
Matias Hernandez (11:57):
What is the most complex thing about technical writing in particular for you or for your experience?
Sam Julien (12:04):
I think the biggest challenge of creating content of any kind, I think, is scoping it down to the right amount of content for the medium that you're working on. So the amount of stuff you can teach in a screencast is different than the amount of stuff you can teach in an article, because people's attention spans are different and they're going to come back to an article multiple times probably, they're probably going to do a lot of copying and pasting and that kind of thing.
Sam Julien (12:40):
So I think that's always the hardest part is figuring out: what is it that I'm going to cover in this article or video or whatever else that's enough for it to feel like a useful and valuable piece of content, but not so much that... What you want to avoid is people clicking on an article and seeing that it's this 6,000 word masterpiece or something and being like, "That's cool. I'll read that later, because this is way too long. I'm never going to..." And they save it to wherever they save it and then they move on with their life.
Sam Julien (13:15):
So you always have to have this balance of being substantial enough to be like, "Oh yeah, this is a legit article," but useful and practical enough, right from the start to where people will actually read it and get value out of it and use it, and not just save it to pocket and never come back to it.
Matias Hernandez (13:33):
Do you use some kind of technique or trick to write your content? Like, I don't know, your sit every day at same hour and you write a few words and then you come back? Or do you use this click baity or click worthy titles and some tools to help you with that? Or do you just have this natural talent of writing?
Sam Julien (13:58):
Well, I mean, for me, I've been working on writing for many years now. I was interested in writing when I was in high school and elementary school and all that. I did a lot of writing contests. And so writing is a big part of my life, so I probably have an unfair edge of experience there. But from the technical writing standpoint, it has been a series of things that I've practiced over time.
Sam Julien (14:25):
I think one of the biggest things for me is, with any type of content that I'm creating, I try to think of it very conversationally. I think of it in terms of... Like with an egghead video, it's a few minutes that I have to talk to somebody, whereas an article I tend to think of it in terms of like 10 or 15 minutes. That seems to be the upper limit of where people can pay attention. Unless I'm making a really big reference guide.
Sam Julien (14:50):
And so I think about in terms of: What could I teach someone in 10 or 15 minutes? What could I explore? What's outside of the scope, and what's inside the scope of just this kind of conversation? If somebody were to say to me, "Hey, how do you implement authentication in a graph QL backend?" Then I want to scope that down to what I could cover with them in like 15, 20 minutes or something. And I start from there and kind of outline it and then flush it out.
Sam Julien (15:22):
And some of it is just practice over time. You start to get an intuition about that. But that's not really a natural thing, it just comes from doing it over and over and over again.
Matias Hernandez (15:35):
And how this process of writing articles became a source of your book writing process? You wrote two books, two eBooks, that are not too long but also are not short in any way. So it's around 70 page still. That is a lot. So how you start with your first one? The Developer Relation Introduction? Yeah.
Sam Julien (15:59):
So that one, some of it I had already written in articles, either that I had published or hadn't published. That was a book that was sort of one of my back burner projects. I knew that there was something I wanted to do around an introduction to Dev Rel and just hadn't ever gotten around to do it. And then some people got together and were doing a two-week challenge to ship a product, and so I joined in on that. And that was my kind of motivator to get me to finish the book and everything.
Sam Julien (16:37):
But that book largely came out of the experiences I had with the Auth0 Ambassadors Program, because I was finding myself having a lot of conversations with ambassadors about what Dev Rel is, and how to become a developer advocate, and all of those things. And so I kind of had... I was seeing this trend both in the program and on Twitter and that kind of thing, where there's a lot of interest around Dev Rel and what it is and how to do it and that kind of thing, and so that's really my motivation for writing that one.
Matias Hernandez (17:11):
Well, actually Dev Rel is becoming a buzzword right now. It's used everywhere. I really have to say... I'm old enough to say that I love it, the old word for that, evangelist. I really love it. Evangelist.
Matias Hernandez (17:29):
But now that you're using developer advocate, developer relations and developer anything, what is... I had to do it. What is developer relations role? What are you doing?
Sam Julien (17:41):
Yeah, I feel like that's a required followup question. So developer relations is, basically, you're a developer who works for a software company that has a SAS product, software as a service, and the developer relations... Which sometimes they're called developer advocates, sometimes they're called developer evangelists, it sort of depends on the company. It seems like evangelists has sort of fallen out of vogue lately.
Sam Julien (18:10):
But the idea is that you're sort of the mediator between the users or potential users, which are developers, of the SAS product and the rest of the company, which would include the engineering teams or the marketing teams or the docs teams or anything like that. Basically, your job is to help developers using the product through education, through letting them know about new features that are happening, through product feedback. If they say, "Hey, this doesn't work over here," or, "This SDK has problems," you take that feedback back to the rest of the company and they adjust course accordingly. That's sort of the nutshell of what developer relations is.
Matias Hernandez (18:56):
Does it mean that developer relations is part of what department? Marketing? Development? Engineering? What is your role there? I mean, I imagine that every company has different visions there, but your experience.
Sam Julien (19:12):
Yeah. This is an ongoing debate in Developer Relations. So my company, Auth0, Developer Relations is under Marketing. Other companies like Okta, which just acquired Auth0, their Developer Relations is actually under Product and goes straight to Product. And then you have companies like Netlify where Developer Relations is actually its own organization. They call it Developer Experience, which means something different in my company, but they have a separate organization that just reports straight to the C-level teams.
Sam Julien (19:57):
So there's a lot of kind of pros and cons to all of these different approaches. It's hard. So much of that depends on the people involved and what the company mission is and stuff like that. Because at first glance you might say, "Well, if it's under Marketing, that detracts from the value of it." But actually it doesn't really, in the sense that Marketing is still a core function of any sort of SAS, so there's no conflict of interest or anything just by having Developer Relations under Marketing.
Sam Julien (20:36):
So there's a lot of different philosophies on this. And some of the more ideal solutions don't actually pan out that way, just because of the way that the company works. And Developer Relations is very cross-functional, so kind of where it originates is mostly affected by, or mostly affects, what kind of metrics and stuff are used to evaluate it. That's kind of a long-winded explanation, but that's sort of how it goes.
Matias Hernandez (21:04):
Yeah. I think that's a common question now about, basically, under what department will you work in. And the next question, also related, is: does this means that you are not coding? I'm a developer, but I will not be coding every day. What is?
Sam Julien (21:26):
So that's definitely a common fear. And you definitely change the way that you are coding. If you're working on a regular engineering job, you're probably working on some sort of product that you're... Whether it's an internal application or an external one, you're working on the same application or set of applications every day, fixing bugs or adding features, that kind of thing. Whereas in Dev Rel, you're doing much more educational work.
Sam Julien (21:57):
So our coding on the team generally falls into a few different categories. We have, basically, code for tutorials and talks, that kind of thing. So we're doing X technology plus Auth0 or whatever. But then we also have some open source libraries that we're responsible for. And this also is one of those things that it really depends on the company, but we have a few different what are called micro sites like jwt.io and a couple of others, as well as some open source libraries, and those are maintained by our team. In particular, Sam Bellin in Europe is sort of responsible for all of those things and does a bunch of work on those. So shout out to Sam Bellin for that.
Sam Julien (22:38):
But then there's also if we ever want to build something on the team, like a tool or an external site or something like that, we can also do that kind of coding. So it's definitely a different... It's more of a kind of you're sort of learning and coding and teaching all at the same time, so it has a lot of variety. But that there is that trade off of you're not going to have one or two production applications that you're working on day after day that you own and watch grow and that kind of thing.
Matias Hernandez (23:14):
I think, to me, the followup question is: does that mean that you are context-switching all day? Am I right?
Sam Julien (23:24):
It does mean you're...
Matias Hernandez (23:25):
Writing, then recording, then writing again?
Sam Julien (23:27):
Yeah. Every time I interview someone for a Dev Rel job, I always ask that: how they feel about constantly multitasking and switching from skill to skill, because that is one of the most bewildering parts of moving from a developer job to developer advocacy or developer relations is on any given day, you might be writing an article, building a sample application, doing an interview, writing, doing some work on a program, and switching back and forth between those two.
Sam Julien (24:04):
I mean, over time you can kind of get better at how you schedule things so you're not running around all the time like a wild person, but still, it does take a little bit of work. And the other side of that too is that, in theory, you can also code whatever you want or learn whatever you want, you don't necessarily have to stick to the same language or the same technology. You don't have to make React stuff all day long or even JavaScripts all day long, which also is real fun. It's kind of the dream, right?
Sam Julien (24:39):
But then you also kind of quickly find out when you get into it that you only have so much time and attention. And so if you're bouncing around from language to language and framework to framework and stuff like that, it actually tends to be even harder. So most of us get into it and we start by going all over the place and trying to do things in a bunch of different languages or frameworks or things, and then we realize that we don't don't really have the brain power for that and we end up kind of specializing and niching down. But you do always have the option to learn something new in a different language or something, and that part is really fun.
Matias Hernandez (25:14):
This brought me back to developer microskill in terms of time management. What are your thoughts and your content, that you already shared that, about time management and how to deal with context switching?
Sam Julien (25:31):
Yeah. It's so funny, right around the end of last year, I felt like I was finally starting to get the hang of managing time as a developer advocate. And then in January, my boss told me that it was time to move me to management and it totally uprooted everything that I was doing. But I did manage to write an article about time management as a developer advocate, and I found that stuff still holds true.
Sam Julien (25:59):
Basically, what I say in there is, first, you kind of learn how to prioritize things, like, for example, things that are dependent on other people, like if you're working with other teams. We do a lot of... One big part of Dev Rel, that I don't think people realize this much, is we do a lot of work with product launches. So anytime there's a new feature or a new cool thing, Dev Rel usually makes an article or a video or something and launches it on the same day as the feature that comes out. So that kind of thing is really high priority, because a bunch of people are dependent on you and it has a deadline. So that kind of helps shape your time, in a way.
Sam Julien (26:41):
I've also found that, for me, it really helps to block off time blocks. I kind of figured out that I work best in sort of a few different time chunks. There's the 30 minute kind of maintenance tasks of like, "Oh, I need to just kind of like..." It's like watering your garden. You just need to do a couple things on this application or these docs or this program or whatever, just half an hour here or there that I need to do regularly.And then sometimes I need to just sit down and figure something out, and it takes maybe an hour or so, maybe 90 minutes.
Sam Julien (27:20):
And so just being proactive about kind of setting aside the time that you need. It's hard because you have to do that. You have to be on top of it because it's easy for people to schedule meetings on your calendar, and you've got to kind of manage it. It's kind of an ongoing battle where every week you've got to kind of set up your time blocks for the next week and do your best to anticipate what things might come up.
Sam Julien (27:48):
So it's definitely a lot more kind of proactive time management, but it does pay off when you start building that time in to where you can focus on what you can actually ship, and building in time every week to do that.
Matias Hernandez (28:05):
I'm really into the context switching, I'm a disorganized organized person, so I basically use my disorganization to organize myself. And what works for me was time-blocking, as you mentioned, but also Pomodoro into the time blocking, so I can do a lot of things in the same time just to be able to switch.
Sam Julien (28:29):
Yeah. Yeah. I find a lot of people find Pomodoro really helpful. For me, for whatever reason, it hasn't really stuck for me, but I always bring that up because yeah, for a lot of people it really helps.
Sam Julien (28:41):
One thing that did help me, even though Pomodoro itself didn't really help me was I found that it only... You know when you get distracted by Slack and Discord and Twitter and all of those things, I found out that it really only takes me about 10 minutes of discipline to get in the zone. And so what I started doing was I would quit all that stuff.
Sam Julien (29:06):
There's an app on the Mac called Focused, or Focus or something like that, that can block some of those things. And I would set a timer for 10 minutes and block all those things or quit them or whatever else, and that was about all it took for my brain to switch over and get into the right context to work on whatever project I needed to work on without constantly checking Slack or Twitter or whatever else. So that's another big one.
Matias Hernandez (29:32):
It's like you just said, it's a proactive way of keeping focused that you need to be on top of everything and don't wait for the inspiration and motivation to come to be on the flow. It's like you need to put yourself into it, trick your brain to do hard things.
Sam Julien (29:52):
Yeah. Yeah. Yeah. I mean, that is one thing I find much more challenging about Dev Rel than doing a normal developer job because it's so much easier for... For whatever reason, when you have a bunch of development tasks, like tickets to close out or whatever, it's so much easier to get in the zone. You can put your headphones on and put some music on and quit Slack or whatever and just write code for hours and hours. And sometimes I look back fondly on those days. But yeah, on the Dev Rel side, you definitely have to be much more proactive with that: of making yourself block out time and that kind of thing.
Matias Hernandez (30:34):
And all of these tricks or techniques is part of what it comes into The Guide To Tiny Experiments, right? Improving yourself a little bit to be able to accomplish your goals. Can you describe us a bit of the framework so people go and read your book?
Sam Julien (30:56):
Yeah, for sure. So the idea is... This sort of came from... Looking back, this really did kind of come out of the fact that Dev Rel has just so many things going on all at once, and I found that it was very hard for me to move the needle on a project all at once. I had to do it in small iterations to get it done.
Sam Julien (31:21):
And so I kind of remixed all this stuff about habits and that kind of thing into this concept of the tiny experiment framework where, first, what you have to do is... Let's say you have this list of 10 different ideas you've had about articles or projects or whatever. And usually what that looks like for people is they've got something like, "I want to write..." Or, "I want to make the ultimate guide to React video course." But they haven't ever done anything else before that. And so it becomes this really big, overwhelming thing that they have to work on.
Sam Julien (31:57):
And so I have this framework where, basically, first, you just write down all of your ideas in one place. It doesn't really matter. You can set a timer for a few minutes or something and write them all down. And then you just need to go through and kind of do some triaging. You can drop some of them, or defer some of them, or decide that, "Okay, this is something that I want to do."
Sam Julien (32:22):
And usually, not all of your ideas are good ideas. Some of them are. And then some of them are good ideas but they're not realistic for your timeframe. They may be great six months from now, but they're just not right for you right now. I want to really learn Go, so it would really be silly for me to say that I'm going to make some big course on Go when I still haven't learned Go in the first place. So that kind of thing I would defer for later.
Sam Julien (32:47):
But then there's other things that are a good mix of your current amount of time and your current interests and that kind of thing, or maybe they just sound really fun. So then you narrow it down to that list of things, and maybe that's like three to five ideas, and then you pick one of those things to work on. And this is always the hardest part for people is actually just picking one thing, because most people want to do everything all at once.
Sam Julien (33:15):
But we're just not capable of doing everything all at once, and there's more value in getting something... Getting something shipped or out the door is a really gratifying feeling, and so the more you can give your brain those happy chemicals of, "I accomplished something," the easier it'll be. So the next step is just to pick something. And I always tell people, "If you can't decide on something, literally just pick anything. Pick one of those items."
Sam Julien (33:45):
Because there's basically three possible outcomes whenever you pick something. Either you're going to absolutely love it, and it's going to become this passion project, and you're going to... It's going to become a huge success or something. Or you're going to absolutely hate it, it's going to turn out to be not at all what you thought it was going to be, and it's just you don't want to do it. Or the most common one, the most likely one, is that you don't really love it or hate it, it's just sort of a thing that you do, and you're kind of neutral about it, but you learn a bunch of skills in the process. You learn more about video editing or writing or whatever else.
Sam Julien (34:25):
So that's sort of the first part. That's taken longer than I thought it would. But the idea is then that once you have the trick then is to scope that down into something that you can ship right away and get feedback on. And that's what I go into in the book about exactly how to scope a project like that to where you can ship it quickly and then get feedback on it and improve it over time. And that'll ultimately pay more dividends in the long run for you than trying to wait and ship something perfect that's large.
Matias Hernandez (34:58):
I really like how all of your content ties up together in a nice circle, because we were start talking about... Start with developer microskill, we went to the Dev Rel, content creation, and now microskill that will help you with content creation that can help you with Dev Rel if you are into that.
Matias Hernandez (35:19):
I have a few questions more. So one is: what are you learning now? One thing is create content but another thing is keep on top of what's happening around us in tech. That is a lot of things. And what have you?
Sam Julien (35:36):
Yeah. So right now, a large chunk of my brain space is going towards learning a lot of management skills, as this is my first foray into management, starting in January. So I'm thinking a lot about that kind of thing. But then, I have this ongoing project of learning AWS skills. I'm still working on my Cloud Practitioner certification. I've rescheduled it again. I just had so many things come up in my life that have prevented me from studying for it, but I think I'm pretty close to actually getting it done.
Sam Julien (36:17):
My goal is to do the Solutions Architect one, partially just because we use AWS a lot at Auth0, for internal projects and for Dev Rel projects and stuff like that, so it's mutually beneficial for me to learn that stuff, as a way to level up my career but also become more valuable at work. So-
Matias Hernandez (36:40):
You can argue that all of us are using AWS somehow. Every service out there is under AWS. And it's hard.
Sam Julien (36:49):
Yeah, it's true.
Matias Hernandez (36:50):
It's hard to understand all of that.
Sam Julien (36:51):
Yeah. It's really hard. I mean, I'm very much just scratching the surface so far. The one thing that's nice is that most of those Cloud concepts will carry over to the other providers like Azure and Google Cloud and stuff. They just have different names and different kind of organizational things, but picking AWS and running with it seems to be working okay for me so far.
Sam Julien (37:17):
So those are sort of the big ones. I have this ongoing goal of learning Go that I mentioned, and I just still haven't done it. I've started a little bit, but it's... I just always feel like there's so many other things for me to do in the day and it always ends up getting crossed off.
Matias Hernandez (37:36):
Yeah. I took the idea of learning Go from a Tweet of you, I think. And I took a look and, actually, there is a particular AWS service that have a Go API. and I wanted to do it so badly, but it's three or four months ago and I'm still here [inaudible 00:37:56]. So kind of so much happens in life.
Matias Hernandez (38:01):
Next question is: you recently released, at the day of this recording, recently released a course on egghead, not that recently, but maybe a couple of weeks ago, about Ghost. Are you using Ghost for your content?
Sam Julien (38:18):
I'm not using Ghost right now. That course is really more about deploying on AWS. It's sort of the most common skills that you need to deploy a full stack application. It's just that Ghost was a really convenient existing full stack application. It needs a server, it needs a database, that kind of thing, so Ghost was sort of a natural thing.
Sam Julien (38:44):
And also, it is a cool software platform. It's sort of like a open... Well, I don't know if it's open source anymore, but it was open source. But it was sort of the indie version of WordPress. And I did use Ghost a long time ago. My site was Ghost before I switched it over to Gatsby. And now Ghost has a lot of cool features. And if you're looking to start a new blog plus newsletter, it's a really good option for you.
Sam Julien (39:11):
But yeah, that course is about... It's called Deploying Ghost to AWS With ECTU and RDS, and it's basically... It walks through how to set up the server, and how to set up the database, and then how to get them to talk to each other. There's a little bit of networking in there. And it just turned out to be like a really good, complete, realistic project to do as an egghead course.
Sam Julien (39:36):
I had kind of tweeted about that... I was just doing it as a way to learn AWS, and I tweeted about it, and then Joel Hooks saw the tweet and was like, "Dude, you should turn this into an egghead course. This would be a great egghead course." And so that's what happened.
Matias Hernandez (39:51):
It used to happen that he see something and immediately think about the success of the content. Is really good to follow his advice, anyways.
Sam Julien (40:01):
Yeah.
Matias Hernandez (40:02):
I want to ask you about recommendations. Recommend something that you like, whatever it is, to the audience. Something from Sam to the audience.
Sam Julien (40:15):
Well, probably the biggest thing right now that is positively impacting my computing life is the application Obsidian, which is a note taking application. It's kind of part of the personal knowledge management system movement that seems to be happening right now with applications like Notion and Rome and Kraft and things like that.
Sam Julien (40:41):
Obsidian is one of those applications for taking notes, and the magic is that you can link notes together by just using double square brackets and magically linking things together. The thing that makes Obsidian so nice... There's a couple things, but one of the things that's so nice about it is that it's just a folder full of Markdown files that has magic over top of it in the application.
Sam Julien (41:08):
And so the biggest hangup I've had with a lot of these note-taking applications is they're usually a SAS or a private application. When you put things in Notion, it lives in Notion, and so if Notion ever goes down or it goes away, just like if Rome goes down or goes away, then all of my stuff is gone. And that's not to say there's not export options or backup options or anything like that. But Markdown has been around for forever and will continue to be around for forever, and so even if Obsidian goes away, then all of my raw Markdown files are just living on my computer and right there. And so Obsidian has been amazing for that.
Sam Julien (41:54):
It's also written by developers. I mean, it's maintained by developers, and it really feels like an IDE for thinking, and it's just been awesome. And I've been basically unofficially doing Dev Rel for Obsidian by promoting it to everyone I know. And so I've sort of become an Obsidian seller.
Matias Hernandez (42:15):
Tend to happen, so yeah. Actually, it's the same tool that I'm using right now. I was using Emacs or Chrome. That is basically the same idea. And it's amazing. It's amazing how you can just liberate by word of the tool to come up with ideas, because you have contender. So Obsidian, that's the recommendation. Check Obsidian, people. Obsidian.md I think is the URL. It will be in the show notes.
Sam Julien (42:43):
Yeah, I think so.
Matias Hernandez (42:43):
But just be aware, don't follow the rabbit hole of BKM. It's a big one.
Sam Julien (42:51):
Yeah, you can go really deep in the BKM stuff. We can add to the show notes, I wrote an article that's an intro to Obsidian for developers, so we'll add that there to, because that'll give you a good starting point. It goes over some of the core concepts and the top plugins and that kind of thing.
Matias Hernandez (43:08):
Yeah. Yeah. Great. And lastly, anything you want to plug? Like the content you create or something else or whatever?
Sam Julien (43:17):
Yeah. I would say the biggest thing for me these days is Developer Microskills, the newsletter. I mean, that's sort of the entryway to most of what I'm doing. And I use the newsletter as... It makes me happy because it's really just like a form of self-expression for me.
Sam Julien (43:34):
A lot of times, writing for a blog or other things, you have to think really hard about SEO optimization and getting traffic to it and that kind of thing. And the newsletter, I just write about whatever I want to write about, whatever's on my mind, and then I worry about... Later, if I want to port that content somewhere else, then I worry about the SEO stuff and all of that stuff.
Sam Julien (43:58):
So I've been having a really good time, and the response has been really good to it. And so that's the best way to get to know me is just sign up for the newsletter. And let me know... If you find things helpful or if there's anything you want to hear my thoughts on or get my advice on, let me know, because a lot of the inspiration for the issues actually comes from people writing in and asking me questions about things.
Matias Hernandez (44:24):
Where people can ask you?
Sam Julien (44:25):
Yeah, so if you go to developermicroskills.com, that's how you can sign up for the newsletter. It's also at the bottom of website, samjulien.com, and then my Twitter, I'm very active on Twitter, that's just @samjulien. That's been a real fun experiment too.
Matias Hernandez (44:43):
That's great. That's great. So Twitter, you'll always find Sam there. And Developer Microskill is really good content, so go ahead and subscribe.
Matias Hernandez (44:54):
Do you think in somebody that should be in the show?
Sam Julien (44:58):
Somebody that should be in this show?
Matias Hernandez (45:00):
Yeah. Someone that you want to hear.
Sam Julien (45:02):
Yeah. I think it'd be cool to hear Angie Jones come on this show. She'd be a really good person to talk to about Dev Rel and testing and things like that.
Matias Hernandez (45:17):
Let's-
Sam Julien (45:18):
See if she's available.
Matias Hernandez (45:20):
Yeah.
Sam Julien (45:20):
Hey, if you can get Kent Dodds...
Matias Hernandez (45:22):
Well, that was kind of awesome. He's actually really kind and open and he said yes immediately, like now. So yeah. And you too, and James Quick is coming to the show too. Coley Fyatt is also coming to the show. And wait for more because the list grows and grows. So yeah.
Sam Julien (45:44):
Yeah. Yeah. I would also make... Of course, I'm biased, but I would make a plug for any of the people on my team. Those are all good people to talk to.
Matias Hernandez (45:53):
Yeah. Auth0 Developer Relation Teams have a new Dev Rel from Brazil?
Sam Julien (45:59):
Yeah. Yeah. Jess Temporal. She's a Python developer and has a data science background, so she's a really interesting... She's got a lot of cool interests. She just launched a video on making interactive maps with Python. So she's been a really fun addition to the team, for sure.
Matias Hernandez (46:20):
There we have. So I will send some message. Call or message her. Thank you, Sam. Thank you for coming by. Was so nice talking. Really fun. And I hope you the best of the rest of your days.
Sam Julien (46:33):
Yeah. Thank you so much, Matias. Bye!
Matias Hernandez (46:37):
Head over to Café Com Tech to check the show's complete archive and read the transcripts in English and Spanish. Thanks to Clevertech for the support with transcriptions and translations. Clevertech: code the life you want with remote done right. Check out our website, clevertech.biz, for more information. Don't forget to subscribe to the show in your favorite podcast application and leave a review if you liked the show. I catch you the next week. And, as always, keep coding.

