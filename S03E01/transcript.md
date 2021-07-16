
Matias: [00:00:00]
Welcome to this first episode of Cafe con Tech in English. Today, I'm with the one and only Kent C Dodds. Kent, thank you for coming by.  Thank you for accepting to be my guest in this particular episode that is starting the first season.



Kent: [00:00:14]
Yeah, I'm honored to be invited. It's really cool and cool of you to have a podcast in Spanish and, and nice of you to invite me to do one in English. Cause I, , don't comprende comprendo much español. 



Matias: [00:00:33]
That's usual. Also, I think that every Latin American developer should learn English anyway. If you want to get more doors open and to level up your career, but, to start , Kent, can you kind of introduce yourself? I don’t know. Should anyone else need an introduction from you, but let's do it.



Kent: [00:00:56]
 I'm sure there are plenty of people who don't know me, but,  yeah, my name is Kent C. Dodds, and I live in Utah in the United States. I'm the father of four beautiful children, a husband, I have a dog, and I teach people how to write quality software. In particular, I focus a lot on React, but I do plenty of Node as well. So pretty much all just JavaScript for me.  I've been doing that for just over two years. Before that was PayPal and then a couple of other companies. I've worked on really large codebases, and so I know the pain and the struggle. I try to take that experience that I've had to help other people relieve some of that pain and make the world a better place with what they're doing.



Matias: [00:01:44]
 I really liked that quote, ”Make the world a better place with code.” In general, people tend to think that we just write code, but in fact, we solve problems. So that is what I liked. I have a question. At some point you  were known as the testing guy, uh now you are more a React guy in terms of testing. And since you mentioned, that you have experience with a large codebase, how can you Sell testing to your bosses? Testing is kind of this gray area that no one wants you to do because it takes time, but it's always desirable to have because it will improve your process, but how do you sell it?



Kent: [00:02:26]
 Yeah. So actually, I have a blog post titled “Business and Engineering Alignment,” which is where I talk about how you get the business folks to do whatever you want. The trick is the part of changing what you want, to be in line with what the business people want you to do. What it really comes down to is identifying the mission of the company and making the assumption that everybody is motivated to push that mission forward. And so if you have people who aren't motivated to push the mission forward, then you're kind of in a bad place anyway. And so, we have to make that assumption that people are motivated to push the mission forward.



Kent: [00:03:24] 
So you identify the mission, and then you find out how you can explain to the business folks that the thing you want to do is going to push that mission forward better. It's going to help you in your goals.  And to be able to do that, you have to convince yourself first that this is really going to be a valuable return on your investment of time.



Kent: [00:03:40]
 And if you can't convince yourself, if you really, after analyzing it and thinking about it, you're like, oh, I don't know, we’re only in the prototyping stage, and I can't really convince myself that testing is really super valuable right now at this stage, then that's easy. You don't even need to have the conversation. But for most of us, we're not working in a situation where testing is unnecessary. Most of us are working in a situation where we need to write tests. Your job is to be able to have as strong a link as possible between testing and the mission of the company. So you can say if we don't test or because we don't test, we are having all of these bugs that we're shipping, and because of those bugs, we're not able to push the mission forward as much as we would like to.



Kent: [00:04:41] 
So we can solve this pretty easily by writing tests. It may not be easy depending on where you're at,  but the answer is pretty simple. , you know, you get tests, automated tests running,  so that you don't have to manually test everything. That's where it comes down to just making or communicating effectively with the people who make these decisions, the managers or whatever, that this is an important part of your return on your investment of time and not doing this is worse than doing it. 



Matias: [00:04:56]
Yeah, I like it. I like the idea of lining up with the mission and selling the technical need of this with more like the product need. We actually are solving problems and delivering products. So we should be sure that we are doing a good job there, but leaving testing aside, like always and everyone, you have a talk that is always interesting to me. And I think I already watched it like twice or more times,  in different places. And the one that you mentioned that React is actually a state management tool, not just a UI tool. , can you kind of summarize the concept you want to deliver to us?



Kent: [00:05:38]
 Yeah, sure. Uh, I remember when I got started with React, one of the first questions that I had was what's the difference between props and state? I think a lot of people ask that as you get started. And I remember coming across this flow chart that Ryan Florence had made that describes kind of those differences. Ever since the very beginning React has always been able to manage the state. Before I really got into React, I thought a big part of it was that React encourages you to be stateless.



Kent: [00:06:37]
 And so you have your state that lives outside of React, and then you just pass that on to React, and then, it renders your thing based on the external state. And while you can do that, you can make all of your components stateless and then just pass it on through, that's possible. And this kind of embodies the, you know, UI as a function of state, a thing that a lot of people talk about. That's actually not what react is really, not practical react. Uh, it's really about statelessness. It's more about giving you a deterministic way to manage your state and a declarative way to interact with the things that change over time so that you don't have to think about them.



Kent: [00:07:21]
And you just think about it based on the current state. Here's my current UI. And when this happens, I will update the state, but I'm not going to worry about what happens to my UI at that point. That will be a completely different render and everything. So for as long as React has been around, it's always been a state manager. From the very beginning, people tried to add things to React to enhance its capabilities there for various reasons that you run into when you're trying to build an application at scale, like a really sizable application, a common term is prop drilling. And that basically means that you are managing a, well, let me take a step back.



Let’s say you have this one little component, and it’s small. Then you’re building this application out. You realize you need to break things up into multiple components. Then two sibling components need to access the same state. So you just move that state up to the least common parent, and that’s what we call lifting state.



Over time, as you continue to slowly lift to state, eventually you're probably going to have some state that comes from the very top like everything needs to access this state. So when you’re doing it, you have all of these different layers of components. You have to pass the props down to the components that need them.



The real frustration is when you have a component that's pretty far down in the react component tree that needs to state that it's very high up in the component tree, but none of the components between those two need it. And so, all of the other components between these are just passing props along that they don't even need themselves.



It's just that there's this relationship between the great grandparents and the great-grandchild. That can be frustrating. This is what we call prop chilling, and you not only need to pass the state, but also the mechanism for updating the state. Yeah, that makes it kind of annoying to have to thread those things through.



I think this was probably the biggest challenge that led people to start exploring things outside of React for managing the state. We can talk about that a little bit more, but then, the other thing that I think motivated people reaching outside of react was when Facebook came out with their idea behind flux, which is a way of managing a state where you have this mechanism to dispatch an event that you handle an event that dispatches, at some other event with some payload and then that gets set into some state, and then that propagates through the whole app. And, and there are various benefits to this approach and various trade-offs that this approach makes, which we only discovered after we all clambered onto this, flex that raft, going down the river, we didn't realize somebody forgot the order or something.



Everybody decided that this is the only way. And then this is the react way when it really isn't. The react way has always been, you, you manage state inside of a component. If a sibling needs it, then you lift the state, and if no siblings need it and only one child needs it, then push that state into the child.



There's no reason for it to exist outside in that situation. React has always been a state management library. But because of these problems, we reached for other things, and that's where Redux came in because it solved both, both of those things. It was a flex implementation or a flux-like implementation and it used the unofficial context API.



Uh, which in the react docs, it was documented, but it had this big warning that was scary that said, you know, don't use this, it's going to change everything. So people didn't want to, but literally, everybody was because we were using react-router and that was using it. We were probably using a CSS and JS theme provider that was using it.



And then Redux was using it. And so, we are all actually using this API to solve the prep drilling problem. And, and there were actually some other much simpler implementations of the context API that I used. There was one called react broadcast by Michael Jackson that I really liked.



It was awesome. Just to make it easier to get your state from one from the top of the tree down, But, yeah, so I, I did use Redux for a while and, for long enough for me to realize I wasn't super happy with it. I ended up opening like 30 files to make a single change. Uh, I did not enjoy that at all.

I only used it for one project. I didn't choose it for that project either. I came into the project that had it already, and then any other projects after that. That was the only project I ever used a Redux with just because I saw that it was solving a lot of problems. But if I change my approach, I don't have those problems.

I didn't need to worry about it. So anyway, that's, that's a long way to say yes, react is a state manager.



Matias: [00:12:15]
 You mentioned two things that I want to kind of shout out, this idea of, you don't need to solve the problem that you just don't have, or you just don't declare it that you have, and people tend to, or used to think that prop drilling is a problem. So we have to solve it even before we have it, and we use redux and any other, a lot of possibilities there. , but actually, there is another concept that is native to react that is composition. And I feel that, yeah, learners and beginners don't actually use composition at all. It's like just children under the children, but there is no other idea there, their composition. Can you, kind of, talk about that.



Kent: [00:12:59]
 Yeah, yeah, absolutely. So, and I'm pretty sure I mentioned this in the blog post. I didn't originally, and I added it later cause it was a glaring, missing part of that blog post. So composition is like, let's say that you're building some chat-based UI and you want to have, I dunno, you're managing some state at the top level that says what users are currently logged in. And then you have this sidebar over here that lists those users, and it needs to be at the top level because you also have another thing that indicates the total count of people who are currently logged in or something. And so that does need to be up higher in the tree. But, but you have two things, two components that are lower in the tree that need to access this data. , well, so a pretty natural thing for people to do when they're writing react is they have one component that renders this stuff, and then those, those components render this stuff and, and those components render this, these things.



And so when you do stuff like that, you naturally have to prop drill. So you have to pass this value down to that one. Then down to that one and down to that all the way until you get to where you are. However, what if instead of, and, and often these other components are kind of like rappers, and often they're like layout components. Uh, so it's like, okay, well, I've got my, my sidebar, but what's inside of my main nav for something like that. And then, , and so they make the main responsible for rendering the sidebar, , where there's actually no state being managed by main. There's nothing like in there that says that it needs to be the one to render the sidebar. And so if, instead, you say, Hey, I'm going to render the main and that's responsible for the layout. And then, I'm going to pass you what I want you to put into it like the children for that layout. So I'm going to be responsible for saying what you render in the different parts of what you're laying out.



, that means that the top level component gets to render the sidebar by itself. And so there's no prop drilling, , of any kind, because the top level component can just pass those prompts directly to the component that needs it. Uh, it's a little bit hard to describe this audibly. So, , the blogpost has an example, and, and actually there's a video by Michael Jackson where he explains this very well.



, and, and actually Michael Jackson made that video because, he was making the suggestion that, , most applications don't need context at all. , which I think. You might be able to get away with, , maybe, but I don't. I think that most applications probably have at least one or two, useful use cases for context, but in spirit he's correct.



, he and his assertion is, , context is mostly useful for libraries, which I believe is, is the case. , but, anyway, if like, like you said, also, , if you change your approach from the, just the way that you're writing your components, then you can just eliminate the problem of propelling altogether and you don't have to reach for context.



And, and the other thing that, that reacted to help eliminate the problem of prompt drilling, or at least, reduce the impact of, of prop drooling is by making context official and making it a pretty straightforward API to use relative to what it used to be, , before hooks and stuff. 



Matias: [00:16:33] 
That was really helpful.

And at  the same time, I think that was kind of damaging the composition concept in terms of like a so easy to use context that you just use it and people will start falling in the same patterns that with redux, like, it was so easy to push everything there that you do just using it. But for some reason, composition is not even taught by instructors around the world, like using this render prop like pattern, because it's kind of similar where you pass the component as a prop, not the data. And why do you think that it is so hard to teach or learn composition and really use it? And because I've been in a lot of React projects and yeah, this is not the pattern. This is, you can find it, but it's not the usual 



Kent: [00:17:28]
You know, you're right. And actually, , I don't think that I had talked about it directly even in my own stuff. I do use it just naturally in the way that I build stuff, but I don't actually teach it specifically. And that will change in an upcoming version of epic react. I'm going to include a section on leveraging competition. Cause that's one of the cool things about react. So that's like one of the primary key features



I think I see react components as functions, which they are of course, but, even the JSX I see is as functions that you're passing these arguments to these functions and we don't really often leverage composition, even in our functions. Not as heavily as you see it when you're leveraging composition with react where you just pass this function and pass this call to this function, to this other function and things like that. I think there's something just in our brains, it feels more natural to say, well, here's this block of stuff.



I'm going to put this in a function. And now this function is responsible for this block of stuff where actually that function really is only in charge of what a portion of that and the rest of it can be passed as an argument. I think that's the big challenge there is we fail to parameterize enough when it comes to our component, 

Matias: [00:19:00] It's kind of the mental model that you come with an imperative, mental model, like most of us. And then you need to change a little bit, like in the path of functional programming, like declarative, more where composition is kind of the king, but we are kind of falling in the middle with JavaScript and react itself. 



Kent: [00:19:24]
Yeah, I would say that, that one of the coolest things about JavaScript is its flexibility to, , cater to people's different use cases for the way that they like to write their code, , whether it's functional or, , object oriented or, or whatever they want to.



And so, , Because JavaScript is so flexible that way, but also, because it is so ubiquitous for better or worse, it's the language of the web. And it's the most popular language in the world and people kind of have to use it whether they want to or not. , for many instances you get a lot of people with different backgrounds and preferences, , than you would in, in a different, , a language in a different platform.



, because not only are they in different backgrounds, but they're also deploying to different targets and they have different use cases and, and all sorts of things. So none of them are necessarily wrong. , they're just, it's just different use cases and different preferences. And so I think because of that, we get a very wide variety of, , of, just the way that people write their code.

, when they're running javascript 



Matias: [00:20:33]
Makes sense. Moving forward with this part of the state thing, topic, in the talk and, and other places you are kind of supporting really hard on react query and saying basically the same as Tanner's said or Tanner said the same thing you did, I don't know - that state is actually two different natures.

One is UI and react is a tool and one is a server state that or cache that is react  query tool. So I understand that your reac-query is your jam here. And, but can you little describe this difference between the state's nature? 



Kent: [00:21:10]
Absolutely. I found out or kind of started thinking about this , maybe two years ago when I realized that we could drastically simplify our UI state if we don't try to treat the server state like its UI state.



And embrace the fact that the server state is a cash. , and so Tanner and I , Tanner lives pretty close to me actually. And so we were having lunch and he was talking about this before he created react query. And he's saying I've been building some really interesting utilities for, for my app at work.



, and so we talked about it quite a bit, and then he came out with react query and it was a game changer for me. Yeah, just when you separate your, what, so first, when you embrace the fact that your server state is a cache, , rather than, it's just some state you need to keep updated, you do a couple of things differently.



So one thing that I did a lot before was, , when I would make a update to, so let me take a step back when, when you are building some app state, some UI stuff, forgetting about the server,  when there's an update, you update that value in memory. So you're saying set state or set, , modal status or whatever it is that you're, you're updating.



 And that's just how we operate in that way when we're. , so when we bring in the server and we're starting to talk about server state, it just kind of feels natural to go ahead and update that state and then maybe have a useEffect  or something that we'll update on the backend.



, and more often what we end up doing is to say, no, I don't want to have an inconsistency here. So  I'll say,  go do this fetch request to go update this. And then it'll give me back the new state and I'll update my local state to be what that new state is. And , actually Apollo does this a lot, not, not to rag on Apollo or anything.



They're solving big problems, but they try to mutate their cache to match what they get back from, from the backend.  And react query kind of takes a different approach.  I think that like, you should be able to, to make that work, but react query just says, oh, you made a mutation. Let me just go get it again.



, because you embrace the fact that it's a cache and, and when you do that, you have to say, as soon as I get this data, it is stale. It's wrong. Uh, you just, you embrace that fact. And so I'm making an extra request to go say, okay, I made a mutation, let me go get what the current state is and putting all of that inside of react query as a package means that you don't have to worry about keeping that state up to date yourself.



And so it drastically simplifies the management of your stuff. I used to have, like these really big, context providers that had all of these different methods or  it was in a reducer, all of these different ,you know, switch statement reducers stuff  to manage like, oh, I added it to do so I've got to push that onto the, the array list or whatever, but with react query, now I just say go ahead and add it to the backend API and then react query takes care of getting the fresh state back for me. There are trade-offs with this approach, but there are ways to work around some of those trade-offs too, but I like the default that react query gives me, which makes me more correct.



And, , because I've moved all of the server state into this cache. Now what I have left for context or composition or whatever is very simple. And if I'm co-locating my state, I often don't even need some of that stuff in a context provider, I just put it in the area of the app that cares about that state.

And so, yeah, the, , react query has just been phenomenal for my client side applications. I don't really use it a whole lot for stuff like remix, , because remix eliminates the problems that react query solves. And we can talk about that if you want to. But, , for, if I'm doing a client side application, , a hundred percent, I'm going to be using react query. It just saves me so much time. 



Matias: [00:25:11] 
Yeah. One of the things that resonated with me was this difference that basically a UI state is synchronous and server or cache state is asynchronous, and you have all of the package into a really cool and clever solution. So you don't have to worry about the synchronicity of that data.



And then you just worry about your own logic basically because the server states not your logic, it belongs to somewhere else. So that kind of resonates a lot with me. Uh, yeah. I want to ask about  remix too, but I'm really curious, but I have another little question there and I'm sure that you receive this question a lot, so many, so many times that you already have a post about it.



Uh, but anyways, well you have a post for almost everything along with a gif. UseEffect is so complex for people to just drop the dependencies into the useeffect and just follow the rules. Like, eh, like you have another talk. I think it's called, “common react pitfalls” where you joke around like LinkedIn rules is Diana Vermont saying, use these things critically.



Eh, I know, eh, Why, why people just, why would you, whether you think that is so hard to follow these effects, synchronicity or staying synchronized by mobile, that use effect need. 



Kent: [00:26:46]
I think there are various reasons that people struggle to follow the linting rule. If you have experienced react already, then your challenge is unlearning. By that I mean if you have experience with react class components, you're thinking about react components in an old way. The way we used to think about them was life cycles. And so you think, okay, when the component mounts, and then when the component updates, then when the component mounts, I want these things to happen.



, and with use effect. Because it doesn't really operate that way. , we try to make it operate that way, , because we're thinking about, the way that, we used to, we think about components and life cycles, but that's not the way to think about those things. So I, I think that's one of the, the major ones for people who have had experience with react already, , is they're trying to bend use effect to operate in life cycles, , rather than synchronizing the state of the world with the state of the app.

, so another reason is that. , sometimes we don't understand or people don't understand what, how the dependency array works. , so the, the fact is that you have an array that you provide to use effect and, , anytime any of those elements changes, even if it's the exact same shape of an object, , if it's a brand new object, it's going to trigger a rerun of your use effect.



And if you don't understand that and you see that your use effect is running over and over again, you're going to just say, well, okay, nevermind. I'll just, , I'll turn off the rule and then your, when you turn off the rule, you are turning on a bug. That's, that's really what it is. , it's like switching on bug mode, I guess, if you want to think about it that way.



, but, But your people are doing this because they're ending up with an infinite loop because they're used effect called set state or something. , and, or even worse that it's calling an API and then calling set state. And so if you have, an ever-changing dependency, you're just forever calling this API and then you get rate limited or something.



I wish I could say I've never done that before. Oh yeah. We've all done it. Yeah. , so yeah, we like, we removed dependencies out of desperation, , for that. And it's because we don't understand that, you know, , when you create a new object, you're creating, even if all the properties are the same, you're creating a new reference to, an entirely different thing.



, and so it is, honestly, it is fairly tricky. , and you have to have a good understanding and like, For one, if you don't have a good understanding of the way JavaScript works and closures and, you know, , JavaScript passes by value and stuff like that, then, , , then it's just a thing that's in your way, and you don't understand why it's causing you so much trouble and that's, that's frustrating.



Uh, so I don't, really blame people for wanting to turn it off and just move on with life. , but like I said, they are turning on, on hard mode, black mode. , but, yeah, the, the other. , point to all of this is I think that use of fact is a pretty low level primitive. , and what's really awesome about hooks in general is that it gives us the ability to abstract things really nicely in a way that we never could with class components.



We tried with, with render props and higher order components and stuff, but, and, and that actually worked out pretty well. I was pretty happy with render props. Uh, generally there were, there were different problems with it, but when hooks came around, , so many problems were just eliminated because we can now share code the same way, share react code and react logic in the same way that we share any other code and that's by making a function and we call it a custom hook, but it's just a function that uses other hooks.

That's all that a custom hook is. And so, , I, I'm finding myself using use effects less and less as I'm using other, libraries. And so what's cool about that? I'm a library author, so it's good for me to understand how all of this works, but the more, , good abstractions that we build, the less people actually have to use, use affect themselves.



And, and a lot of the times that I'm seeing in my discord community or online is, people are using use effect to do lots of the same things for which there are libraries developed that, , I suggest people use, , react query is a perfect example of this. , so many people are using react query or use, , making fetch calls themselves and stuff.



When I just say, why don't you just use react query? Uh, and then you don't have to bother worrying about the dependencies. , oh, and one other thing about use effect that makes it a little tricky is that as soon as you abstract something, , out of a component. So you're trying to make your own custom hook or something.



If that logic is using use effect, then some other things become tricky too, because you no longer have direct access to the variables that, that inmate might be using, especially if, , you were, if you want it to abstract, like what happens in the use of facts with some sort of callback or something?

Uh, because now, you can't just put the callback directly in the use of fact, do you want to genericize that? And so now you have to accept that as a parameter. , and now, as things rerender, that callback could get changed, you could wind up with a stale closer kosher. So you either have to memorize that or, or you have to use this later latest ref pattern.



So abstracting use effect is I think another thing that, , makes the dependency array, and it's not just use effect, it's also used memo and you just call back, but it makes that dependency array a little tricky, , because. You can't just inline things. These hooks are, work a lot easier if you just inline everything, stick everything that it needs directly into that callback.



, but, yeah, it's, it's cool because when you have, when you understand those things, you can build some really awesome abstractions that you can never do before. , and, that's why I say that use effect is a pretty low level primitive upon which you can build other cool abstractions so that most people don't and including yourself, that you don't have to worry about using use effects in your regular application code.



Matias: [00:33:25]
Yeah. Two questions. Uh, do you have any particular resource with tips and tricks to get around with use effect, like using a conditional insight of the fact just to avoid, to shake that particular value or whatever. And second, do you think that use effect is somehow a shotgun. Shoot guns. Shoot. 

Kent: [00:33:44]
Yeah, yeah.

Foot gun. Yeah. , so first I do have some really good articles on epic react. If you go to epic react.dev/articles, , as well as on my own blog, Kent C dodds.com/blog, , where I talked about use effects and also use memo and, and, use callback, as well. Those are, similar because of the dependency your'e situation.



, so yeah, those are some really good resources. , one of one in particular is the, well, now I should, I should look it up. So I give you the right title. , it is how react uses closures. Yeah. How react uses closures to avoid bugs. And that kind of describes the, , the primary difference between react, class components and, and hooks and how react just kind of changed the default.



, it might seem like it's harder, but it ends up saving us a lot of pain, in the long run. Uh, and then I also have another blog post on there tied to the latest ref pattern in react, which solves a lot of the problems that people would find, when they're actually trying to do something similar to what we used to have in, , in class components.



Uh, it's actually a really simple pattern. , but it's pretty powerful when you're building abstractions. , but, yeah. So your, your second question about why is a use effective foot gun?



Matias: [00:35:17]
if you think that it's  because yeah, API lower level API is really hard to use it, but at the same time it's lower, but it's is, is describe it as one of the basic ones that you need to learn to actually develop an aggregation.

So is what, 



Kent: [00:35:32]
yeah. Yeah, that's true. I would say that use effect is, It's relatively advanced, but the fact is that it's very simple. Like I could, I could explain to you what use effect is in two or three sentences and cover everything. , because it is a relatively simple thing. The challenge is that, , in practical application, it can be hard to get right.



Uh, and, and it's not easy. It relies on, , several concepts that people don't have super, , nailed down when they're working with JavaScript. , and because, or, sorry, let me say that differently. It relies on, , or being able to use it effectively. Depends on how well you understand these fundamental JavaScript concepts.



And so if you don't understand, the fact that render actually recalls your function and what that implies about the, functions that you're creating within your components, as well as the variables you're creating within your component. , yeah. If you don't have that understanding, then it can absolutely be a hard thing to get right.

, so is it a foot gun? Yeah, maybe, , potentially, but I think it still is the right approach. Just because something is hard doesn't mean it's wrong, , that you can find the right thing by finding the thing that is simple because you can't build a simple application with really complex abstractions.



It's just that that's not a thing you can do. However, you can build a simple application with simple abstractions and, , and you can also build a complex application with simple abstractions. It's not like a silver bullet or anything, but, yeah, if you have simple, , primitives, then you can build a simple application out of that and you can build simple abstractions on top of it.



That's what I think use effect is, is intended for. Let's provide something that is simple. The whole idea is to synchronize what happened outside of Ray or let's synchronize what happens inside of react with things that are outside of react. That's the whole objective of use effect.



And,  and then people can build on top of that, to, to make nice abstractions so that most people don't have to work with the low level perimeter. 



Matias: [00:37:54]
makes sense. , I want to jump to another topic before the time goes and you are actually diving deep into TypeScript. I you're been a JavaScript developer for a long time, but now you're moving to, eh, what the wave is given us.



That is TypeScript. Everyone is writing TypeScript right now. So the question is really simple. Why type TypeScript? Why TypeScript? 



Kent: [00:38:19]
Yeah. Yeah. So I have actually been using TypeScript for, , Three or four years. , but I, I decided for a long time, a long time ago, and actually before that it was flow. , I use flow type at PayPal for a long time.

, but, yeah. , I think react is still written in flow and stuff, but yeah, that was the only ones. Yeah. Yeah, for real. , so yeah, I decided to not add typings to my open source stuff and my educational material, because I didn't want that to be a barrier for people getting into it. , especially for open source.

I just felt like I don't, I don't want to limit the people who can, participate in my open source stuff to those who know TypeScript, because there are fewer people that know TypeScript. The thing is that. And people who know TypeScript also know JavaScript, but the people who know JavaScript don't necessarily know TypeScript.



So if I just kind of go with the least common denominator, I can reach more people in both my open source, as well as my educational material. , but a few months ago I changed my thinking around that actually after talking with Ryan Florence, cause he told me that they were starting to move their material over to TypeScript.

And I said, well, what about this? And he said, why. , we found that as we were going to give these workshops, we'd say who here uses TypeScript and literally everybody would raise their hand. And, , and on top of that, as we were helping people work through the exercises and stuff, we saw that, they were really confused when they didn't get autocomplete for different, basic things.



And it was really frustrating for them. , and if you do it right. , for the educational stuff, you can make it so that, , for the learners, TypeScript is mostly opt-in. , so you configure TypeScript to not have to type everything, you know, any is fine, whatever. And so if, if I'm just a regular JavaScript developer, the only difference for me is that the file ends in dot TSX.

Uh, everything else is the same. I don't have to worry about it. Uh, and then on top of that, if there are, , utilities that are provided by, the, as part of the material that I'm just calling into this function, I'm getting auto-complete, which is really helpful. Uh, even if I'm just a regular JavaScript developer and I don't care about TypeScript.



And so if you configure things, right, , even the learners don't have to know TypeScript to be able to use a workshop that's primarily in TypeScript. , And, on the open side, I I'd been telling myself this for a long time that, my concern about, TypeScript being a barrier to entry, was just fake, because I expect people to write tests, in addition to implementing whatever they're doing and touch script is just tests.



, at the end of the day, that's, that's all that it is. , and so I was already expecting people, like I already had a barrier to entry on the test side of things, , learning how to add some parameters and stuff. , you know, perimeter types and stuff is a, it's not that much of a bigger ask. , Granted library, TypeScript is a lot harder than app type script.



So, we'll see how this all plays out, but, and maybe there are some people already who have tried to contribute to my open source stuff and decided not to, because it was TypeScript and I feel bad about that, but at the end of the day, the, the end product is way better for people. And so I'm okay with the trade-off because the cool thing about TypeScript is that yes, it is tests, but it's also tests that you can hand off to the consumers as well.



, because the type definitions there too, so, , yeah, so that's yeah. Yeah, it's fantastic. I love being a consumer of my own stuff now that it's all really nicely typed. , so yeah, that's kind of where the turnaround publicly has been. , but yeah, I've been using typed JavaScript for a long time and, and, it just seems obvious to me, really like it's.

, I never really enjoyed working in just JavaScript after I started using, Flo and TypeScript at PayPal several years ago. , but I did it for those reasons and I'm not doing it now for those other reasons. 



Matias: [00:42:35] 
Yeah. Your computer writing TypeScript and then going back to playing JavaScript.



It's kind of, moving back to the nineties. Yeah, no, never again. , one more question with TypeScript. Eh, now you are creating material blog posts, mostly with TypeScript. Do you think that you will move epic react to that too?



Kent: [00:42:54]
Absolutely. Everything that I'm doing is moving to TypeScript.

So, , testing javascript.com will also be all TypeScript when I'm done. Uh, and epic reacts will all be TypeScript. Uh, Before I update either one of those though, I am working on a couple TypeScript workshops, , because I want to, for people who just aren't experienced with TypeScript or who want to level up their TypeScript, I want to give them a place to go before they go through epic react and, and testing JavaScript.



So I can, so if they say, Hey, I can't go through epic react. I don't know a TypeScript. I can say, well, no, go through this first. And then you can go through epic reacting. Won't be a problem. So, , well, what I'm doing right now is I'm updating all of the material and then I'm going to just take a, a kind of little survey over my material and see which features of TypeScript I'm using.

And I'll make sure to include all of those in, these types gripped workshops that people can go through first. 



Matias: [00:43:52]
Nice, nice. That will be really good. , to finish, I think that this shoot to remix.



Kent: [00:43:59]
Yeah. I'd love to talk about remix. What do you want to know? 



Matias: [00:44:03]
Uh, but basically all I wasn't able to, sorry, my call, sorry, Ryan. I wasn't able to finally buy my own lessons at that point. , but you do so can, you can kind of summarize again and it's short in, it's just LD, but why remix have you so excited, like, to me, it's kind of similar at some point we just spoke it as far as I know, but yeah, I'm all ears here.



Kent: [00:44:31]
So I have zero experience with felt kit. , and I actually have pretty limited experience with next JS, which a lot of people compare remix to. , but from the experience that I have, it's not really like next JS a lot. I like it. There's a lot of overlap on use cases that they can, handle, but, they're pretty different in a lot of ways.



The thing that, the elephant in the room, so I'll address that quickly is, remix is licensed, , software where you have to purchase a license to use the software. , this is going to eventually they plan on, , having a trial period for that. , I know a lot of people are really frustrated that there's no way to, to just test it out and see if they, if you like it.



Uh, so they are planning on having a trial period eventually. , but right now they're, they're still . , and so they're there. Uh, focusing on people who, , are willing to pay them to, , to work on it so they can feed their families and stuff.



Matias: [00:45:35]
I think that it's pretty awesome open source for model.



Kent: [00:45:40]
I totally agree. A lot of people feel like you offended their mother when you suggest that software like this should be paid, which I don't understand at all, but, , yeah. Some people feel that way. , but, yeah, so remix, why is it so awesome? I love remix because I feel like it embraces the fundamentals of the web in the way that, , that we always should have been embracing those fundamentals.



, so it, it, we spend so much time, , solving problems with JavaScript. That's what we do as humans. We solve problems. , and because we are such good problem solvers, or at least we enjoy it so much, , And we tend to like, kind of seek problems too. , and, and so when, when we started needing to do more in the browser with JavaScript, we built entire frameworks that all ran in the browser.



And, ,and so, because we were running in the browser, that was, that was the programming area that we, we owned and, the team structures kind of changed. And so, you had the front end team and the backend team. And so if you needed to solve a problem in that environment, you didn't go to the backend team.



You said, how can I solve this without talking to the backend team? , and so we would solve all sorts of these problems, like with caching. So we don't call the backend if we don't need to or whatever, , with, like so many different things that that's, That we do as problem solvers. And especially when, like so much of our stuff with client side now, things are moving more toward a kind of a hybrid approach with hydrating and server side rendering and stuff.



, but still we are in JavaScript and we want to use our JavaScript to solve our problems. And we come up with these very, very complicated solutions to, to these things. So, for example, let's say that we're using our own Webpack thing, everything's client, and we say, oh, you know what, there's an SEO problem here.

We need to pre-render this stuff, but I don't want to manage a server. I've been really enjoying just sending these JavaScript and HTML files up to AWS S3 buckets. And I don't want to lose that. So what if instead we pre, we, because react can run a node. I can run this little. Uh, script that will generate all the HTML files for all the pages.



And then I send that to S3 and, and now I still get the nice deployment experience that I've had without having to talk to the backend engineers or without having to manage a server. And, , And so then I, and we just rehydrate everything on, , you know, on start-up and, and that's what Gatsby is or react static.



Uh, it's this static site generator. And, it works, it's a solution to the problem of SEO issues and, and, and various other things. It improves perceived performance as well. , but it comes with a whole host of other problems that an entire company has been working to solve for years. And, a big one of those problems is what if I have a store with many products or when I was a PayPal, I worked on paypal.me and everybody has their own link. And so we evaluated Gatsby and it was very quickly obvious that this would not work because we have millions of users. And so like you, you can't do that. 



It would take weeks to build everything, , to build all those, those HTML pages and people will say well, but the cool thing is that you can cash it and stuff, but literally every time you redeploy, you are blowing away all of your cash.



And in fact, Netlify is built expressly to blow away your cash on every deploy. , and this isn't necessarily a terrible thing because Netlify is a CDN. , but the fact is that it's, it's built with that in mind, , where if you change the approach, you can just eliminate all of these problems in the first place.



And I feel like that's what remix does is it changes the approach in such a way that it eliminates a lot of the problems we created for ourselves by doing everything in JavaScript. , now we're trading off problems, right? It's not like we eliminate all problems and that's all we do. We're also trading, , for different problems because now we do need to manage a server.



Now, I'll say before anything else that remix is planning or it's, , not exactly a rocket science to make remix support, static site generation, or completely client side rendering. And in fact, I believe they plan on supporting that with service workers. So you run remix on the server, so you can have a totally offline app with remix.



So. Remix will be able to do these things, but the default is what's better for you and better for the user. Uh, even though you do have to now manage a server, the cool thing is that nowadays we have services that allow us to handle thousands of requests a second for like 10 cents a day. It's like, it's ridiculous how cheap and easy it is to manage these, , deployment targets.



It's I would say it's not quite as easy as just sending up a couple of files to an S3 bucket, but it's getting there and it's , you S and then you also still have to worry about like, so the only reason I'm mentioning this is because people always bring this up when I say this. , but they say, well, , What about like the, one of the nice things about just sending up, , a JavaScript files and HTML files to S3 is now I don't have to worry about like the server crashing and runtime problems and like, no, no, you absolutely have to worry about runtime problems because like, eventually that your code is going to run.



It's going to run, whether it runs on the server or the client makes no difference, you have runtime problems. And so, , You that is no different with this. The only real difference is now you have a server, which if you're using any of these services, which you probably should be, then, , then it's basically a non issue.

, and so yeah, remix is embracing all of the really cool things of, the, , fundamentals of the web, the foundations of the web, with browser caching and, history. And, and then they add some of the really cool things like, , nested routing and, , Like actual single file, components where you have, here's how I get my data right here.



And this runs on the server. Here's what happens when the user posts some form or does some mutation? That's my action. And then here's what's going to render for the UI. And then they have like Arab boundaries, things for your, each module. You can specify what happens when there's an error. , and then you also even have a pending UI, so they can, this is so crazy, but, but they can, they can render your application.



And if you have a pending UI for a particular, , component, then they'll just say, okay, I'll just render the pending UI. And we'll fill that in on the client when that request finishes. So if you have something that's expensive, you just slap a pending UI in there and it's done. And it, it, it works even.

Even if that pending UI is like a parent, and then it has children that aren't pending. It will just, , you can render the children who aren't pending and then that, that parent can just have the part of its UI. It's outrageously cool. , and the, just the API, , and non API for remix is really cool.



So they give you access to the HTML document. You're the one responding to the request. And so you're the one calling react to render, to, render to stream if you want to, or render to string. Uh, you're the one calling react on hydrate. , and so, because you're responsible for all of these things, you have, an enormous amount of control with zero API, re remix.



Doesn't need to, to give you a special API for overriding the document or, or anything. And because it's nested, , , A nested router. You don't have to worry about rendering your layout component for every single page, which you do with, with Gatsby and next, , which is a point of frustration for people who have experienced this.



, and, yeah, so there, there are a lot of really cool things about remix, but foundationally for me, it is all about giving me a really nice mechanism for using the cool things of the web fundamentals with the really awesome advances that we've had in the innovations in the JavaScript front end side, too.



Matias: [00:54:18]
I have the feeling that they take real ownership about that sentence of, “use the platform.” Yeah. I think that's coming along, but this is actually real. They're all there. The ATD, because the video that Ryan recorded on YouTube, is actually awesome. Yes. I compare it with Belkin because this is the end product that you can deliver an application without any JavaScript at all, because it's just not required as I think it's pretty amazing.



Kent: [00:54:49]
Well, with remix you, because you're responsible for rendering the HTML element. So the root element, , it's very trivial to, , to not render the script tags. Uh, and so you can, , do your whole application and, because of the way that they do mutations. , your whole thing can work without, , without JavaScript.



And, and what's really cool about this actually is, , you can build your, your application to work really nicely. Client side. It shows error messages and stuff, , for all of you mutations and whatever. And then if for some reason, the JavaScript fails to load. This has happened to all of us where the JavaScript fails to load for some reason, , with remix because of the way that they structure their API APIs.



, and, and the way that is the idiomatic way to do this, your application will work exactly the same. Uh, even if there's no JavaScript on the page. So people will be able to submit their forms. They may get a full page refresh, , you know, cause it's a form that's posting, , but error messages will still re render and everything.



Uh, and uh, like if, if there is an error in the form, everything will, will still work. And so. Uh, yeah. If you have a use case where you're like, Ooh, I really don't want to have, any JavaScript on the login page because I want that login page to just load like lightning then, , it's trivial to, to add that there's no API for it.




Matias: [00:56:22]
It's just obvious because of the way that it's built. It feels to me, two things, it feels to me that they kind of reinvent the idea of framework because currently JavaScript frameworks are things that you ship with your obligation. And this is something that is just chip delegation, not the framework itself.



Uh, and the other thing is like remix, , a bit as a tooling, mechanism, spill, kit, and other are kind of opening the door to what can be called the third era of JavaScript. Like we are moving past of the client frameworks to something else. Awesome. 



Kent: [00:56:56] 
Yeah. And this, and it comes with builds that take 50 milliseconds.



Well, yeah, it's pretty great. I'm a really big fan of that. 



Matias: [00:57:08]
 Okay. So we are, almost at the end of this amazing conversation on Kent. Thank you for coming by. Uh don't. I'm not sure. Do you want to obviously look at something and recommend something to the audience?

 

Kent: [00:57:22]
Ooh, , yeah, so I, I don't know, like, a recommendation just in general.



, I think that you can be really, really awesome. Solid developer and really good at coding and stuff. , but no matter how good you are at coding, if you aren't nice, you won't find satisfaction in life. , you will always be chasing something, to make you happy. , and I think that finding happiness in life has a great deal to do with the amount of happiness that you work to bring in other people's lives.



And, , and kindness has a lot to do with that. So, yeah, I guess if there was anything I would recommend to the audience it's, , to evaluate how kind you are, , or how kind you were in your last interaction and work on improving that every day. 



Matias: [00:58:16]
I love it because we are humans and we are not just technical skills collection.



We are human and we work with other humans. So be kind, be happy is part of our goal somehow.



Kent: [00:58:29] I don't know what you're doing if you don't want to be happy. 



Matias: [00:58:33]
Yeah. Yeah. , obviously as a plug, I will do it, eh, epic reactor dev go to material react on the web. So all of these things that Ray can mention through his talk will be in the show notes as always, and, hopefully transcriptions also.



So thank you for being here. Uh, can again, I'm not sure. Oh, one last question. Who else should come to this show? 



Kent: [00:59:03] 
Ooh, that's a good one. , I, I've got a number of, of people in my discord community that are just awesome. , that I could mention to you and maybe I'll, I'll shoot you an email or something, but, , I.



Anybody that's been on one of my podcasts, would be awesome. So go check out Kent C dodds.com/podcast. We have three seasons, season four is coming soon. , and yeah, like the people that I want to hear on a podcast are, are the ones that I invite to mine. So there's also epic react has a, a kind of a podcast sort of thing in it as well.



So you can go take a look at, at the people that I had on, on that. And they're all like react focused, obviously. , so yeah, it's the epic react to expert interviews. , and they're all fantastic people. I'd love to see you on this podcast.



Matias: [00:59:53] 
Really awesome content there too. So yeah. Thank you, Kent. This was awesome.



Kent: [00:59:58] 
Thank you. It's been a pleasure 



Matias: [01:00:01]
and we hear us, in the next week.


