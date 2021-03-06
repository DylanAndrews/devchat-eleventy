---
layout: layouts/post.njk
title: >
  096 AiA Angular 2 and TypeScript with Dan Wahlin
date: 2016-06-09 07:00:16
episode_number: 096
duration: 01:03:04
audio_url: https://media.devchat.tv/adventures-in-angular/AiA096DanWahlin.mp3
podcast: adv-in-angular
tags:
  - adv_in_angular
  - podcast
---

01:59 - Dan Wahlin Introduction

- [Twitter](https://twitter.com/DanWahlin)
- [GitHub](https://github.com/DanWahlin)
- [Blog](https://weblogs.asp.net/dwahlin)
  03:24 - [Dan Wahlin: Typescript: Angular 2's Secret Weapon @ ng-conf 2016](https://www.youtube.com/watch?v=e3djIqAGqZo&index=3&list=PLOETEcp3DkCq788xapkP_OU-78jhTf68j)04:44 - [ng-conf](https://www.ng-conf.org/) Fair Day Workshops
- TypeScript 2 in 60ish Minutes
- Angular 2 in 60ish Minutes
  05:45 - Pre-Conference Workshop06:32 - [AngularJS Fundamentals In 60-ish Minutes](https://www.youtube.com/watch?v=i9MHigUZKEM) =\> Angular 213:49 - Responses to Angular 2 and TypeScript18:22 - Learning TypeScript; ES5/ES625:25 - Interfaces29:33 - Aha Moments
- Databinding Syntax
- The Module Concept
  34:07 - Edgecases and Struggles
- Providers
- Grabbing Elements
- The Build Chain
- Pipes
- Observables
- [Pluralsight: Modern, Modular JavaScript with SystemJS and jspm](https://www.pluralsight.com/courses/javascript-systemjs-jspm)
  51:41 - Flexibility of Providers &nbsp;Picks
- [John Papa: Angular 2 Workshop in Barcelona](https://johnpapa.net/angular-2-workshop-in-barcelona/) (John)
- [Ghost](https://ghost.org) (John)
- [CloudFlare](https://www.cloudflare.com) (John)
- [Angular 2 Style Guide for TypeScript](https://jpapa.me/ng2style) (Lukas)
- [Deskbound: Standing Up to a Sitting World by Kelly Starrett](https://www.amazon.com/Deskbound-Standing-Up-Sitting-World/dp/1628600586) (Lukas)
- [iPhone](https://www.apple.com/iphone/) (Ward)
- [ng-conf 2016 Starcraft Tournament](https://www.youtube.com/watch?v=J5Dj7rINOK4) (Joe)
- [Duet](https://www.duetdisplay.com/) (Dan)

### Transcript

**DAN:** &nbsp; You don't care.

**WARD:&nbsp;** No, when you've got a horrible [tooth], you've got to embrace it.

**_[This episode is sponsored by Hired.com. Every week on Hired, they run an auction where over a thousand tech companies in San Francisco, New York, and L.A. bid on JavaScript developers, providing them with salary and equity upfront. The average JavaScript developer gets an average of 5 to 15 introductory offers and an average salary offer of $130,000 a year. Users can either accept an offer and go right into interviewing with the company or deny them without any continuing obligations. It’s totally free for users. And when you’re hired, they also give you a $1,000 bonus as a thank you for using them. But if you use the Adventures in Angular link, you’ll get a $2,000 bonus instead. Finally, if you’re not looking for a job but know someone who is, you can refer them to Hired and get a $1,337 bonus if they accept a job. Go sign up at Hired.com/AdventuresInAngular.]_**

**_[Ready to master Angular? Oasis Digital offers Angular Boot Camp, a three-day, in-person workshop class for individuals or teams. Bring us to your site or send developers to ours classes in St. Louis or San Francisco – AngularBootCamp.com.]_**

**_[This episode is sponsored by Telerik, the makers of Kendo UI. Kendo UI integrates seamlessly with both AngularJS 1.x and 2.0. It provides everything you need to integrate with AngularJS out-of-the-box bindings, component configuration, directives, template directives, form validation, event handlers and much more and yet Kendo UI tooling does not depend on AngularJS. So, if you want to use it with Angular or not that’s totally up to you. You can check it out at KendoUI.com]_**

**JOE:&nbsp;** Hello everybody and welcome to Adventures in Angular episode 96. Today on our panel we have Ward Bell.

**WARD:&nbsp;** Hello.

**JOE:&nbsp;** Lukas Reubbelke.

**LUKAS:&nbsp;** You mad, bro?

**JOE:&nbsp;** [Laughs] And John Papa.

**JOHN:&nbsp;** Hello.

**JOE:&nbsp;** And I'm Joe Eames, your host. And today we have a very special guest, Dan Wahlin.

**DAN:&nbsp;** I'm feeling special, Joe. Thanks.

[Chuckles]

**JOE:&nbsp;** Dan, do you…

**JOHN:&nbsp;** Special Dan. Special Dan's [voice].

**JOE:&nbsp;** Right. There's got to be somewhere between three and four listeners who may not know who you are. So is it possible you could take a minute and introduce yourself?

**DAN:&nbsp;** Sure. Well, based on the junk mail I was telling you guys I just got, I'm actually switching careers.

**JOE:&nbsp;** [Laughs]

**DAN:&nbsp;** So, I'm going to start maybe a pet or dog-walking company or something like that.

**LUKAS:&nbsp;** 60 minutes or less.

**DAN:&nbsp;** Yeah.

**JOE:&nbsp;** Oh my gosh, dog walking in 60 minutes or less. I love it.

**DAN:&nbsp;** [Laughs]

**JOE:&nbsp;** [Inaudible] work.

**DAN:&nbsp;** Yeah, so I live out in Arizona. I'm actually next door with Lukas.

**LUKAS:&nbsp;** [Inaudible]

**DAN:&nbsp;** So, we get to have, I'm waving to you Lukas. Can you see me? You got to get on top of your roof though, maybe. But [inaudible]

**LUKAS:&nbsp;** I'm staring at you.

**DAN:&nbsp;** [Chuckles] We do lunch from time to time, so it's cool. But yeah, I run a consulting company called Wahlin Consulting. We do a lot of work with various clients around the world as far as consulting goes and I do a lot of training as well on a lot of different topics, JavaScript, Node, C#, all kinds of good stuff.

**JOE:&nbsp;** Awesome. You were also an incredibly featured speaker over at ng-conf this year. You gave a total of…

**DAN:&nbsp;** [Chuckles]

**JOE:&nbsp;** Three different presentations, right?

**DAN:&nbsp;** Yeah, we did a few. Yeah, it was fun. That was a great conference.

**JOE:&nbsp;** Yeah, yeah. It was really fun. So, let's take a quick minute and just go over the stuff that you talked about and just talk about each of the three pieces that you did and what they were about and maybe give us the CliffsNotes version of them.

**DAN:&nbsp;** Yeah, sure. So, the 20-minute version which is always fun giving a 20-minute talk because you sit there and stare, people don't realize it when they're down in the audience. But I think all of us do it. We have that nice timer going and you're like, “Son of a… I've got five minutes left. I haven't even gone through half of the talk.”

[Chuckles]

**DAN:&nbsp;** This time it was timed pretty well. But yeah, the first one was 'TypeScript: Angular 2's Secret Weapon'. And the idea there was to introduce people to some really cool features of TypeScript that especially if you come from a JavaScript world you may not have ever even dealt with maybe ever in your career. But I covered things like interfaces, generics, some of the type support and custom type support. What I call future-proofing your app today, which is a pretty awesome way to take advantage of the future features in JavaScript but leverage a lot of those today based on what we're seeing with ES 2016 and all that fun stuff coming out. So yeah, that was that talk and that was a lot of fun. I don't remember what there was, weren’t there about 1500 people or something like that there?

**JOE:&nbsp;** Yup.

**DAN:&nbsp;** So, it was a big, big room actually. Great conference. Highly recommend it for those next year that might be interested. But the Fair Day was awesome. So, ng-conf in the past has always had two days of the everybody's in the big room and they have the 20-minute type talks that follow each other. And this year they did the same two days but then in the middle they had this Fair Day where there are a lot of different workshops and Ask the Experts rooms and all kinds of cool stuff. It was great, I thought. So yeah, I did two there. I did a TypeScript in 60-ish minutes. And then Angular 2 in 60-ish minutes. John actually was able to join me for that one so that was a lot of fun. And great turnout to both. So, it was a lot of fun.

**JOE:&nbsp;** Awesome. You and John do a fair amount of work together, don't you?

**DAN:&nbsp;** Well, he's muted right now probably. So, he won't be able to hear me, right? No.

[Laughter]

**DAN:&nbsp;** Wrong mute. Yeah, we do a lot of workshops and stuff together. So, we have a lot of fun. I don't know how long we've been doing it, John. At least 10 years.

**JOHN:&nbsp;** Yeah, about 10 years.

**DAN:&nbsp;** We team up on workshops several times a year. So yeah, it's been a while. So, a lot of fun and we're pretty good now. When I do a horrible joke which I'm pretty good at, he's able to follow it up with even more horrible comedy. So, we're like the dual tag-team horrible comedy group. But it's fun.

**JOE:&nbsp;** So, I mentioned three specific things but there's actually a fourth thing that wasn't necessarily… it was part of ng-conf but not part of it proper. It was the pre-conference workshop day. You and John taught a workshop, right?

**DAN:&nbsp;** Yeah, yeah. That's right. Jeesh. It's all a blur.

**JOE:&nbsp;** [Chuckles]

**DAN:&nbsp;** Yeah, so we did a full day workshop on Angular 2 there. And yeah, that was a lot of fun because the audience we had, we had a couple of people we knew and that always helps a little bit to get questions going. And once the questions got rolling, it was very interactive the whole, pretty much the whole day. So yeah, we enjoy that a lot more than when we're just talking to people for eight hours, six hours, whatever it is, and you don't hear any feedback. But we usually try to make it pretty interactive and fun. And we got some other stuff planned actually, coming up a little later down the road here, workshop-wise. So, it's going to be fun.

**JOE:&nbsp;** So, you did this Angular 1 in 60-ish minutes thing. Of course it wasn't titled Angular 1 at the time. [Laughs]

**DAN:&nbsp;** Yeah. [Laughs]

**JOE:&nbsp;** But you did that and you kind of became I would assume the most recognized third-party for an introduction just to get your feet wet in Angular. You've taught a lot of workshops and introductory type workshops in Angular 2 as well. You're a well-recognized expert in TypeScript. But this whole introductory getting into Angular 2, you did it in Angular 1 and now you've established the same thing in Angular 2. So, you've probably seen a lot of people coming around to Angular 2. And Lukas, I think you had a specific question. I don't remember exactly how you phrased it. If you could ask that.

**LUKAS:&nbsp;** Well, I don't remember how I phrased it either. But…

**DAN:&nbsp;** [Laughs] Make something up.

**LUKAS:&nbsp;** [Inaudible] is quite the eloquent master of laying things out. And I think that everybody would like to hear when he approaches Angular 2 specifically, maybe to somebody who's never seen it or heard it or heard of it or just completely new and uninitiated, what is generally the narrative arc that you take Dan, for explaining this new version of Angular? And depending on the audience, how will you modify that narrative?

**DAN:&nbsp;** Yeah, yeah. That's a great question because you get all the people that, a lot of them are, they've been doing Angular 1. So, they know those concepts. And then you have a lot of new people. I just had a group, did a four-day class last week, our first one actually in Florida. I'd say maybe, probably less than 50%, maybe 50% had actually done Angular 1 and the rest of them were pretty new to everything. So, I'll address the Angular 1 folks first and then the never seen any of it, maybe they're just doing React and they're interested in hearing what's new and stuff like that.

But yeah, so for the Angular 1 folks I think everybody assumes that those of us that do speak on it and do these different code samples out there on GitHub and all that, that we just I don't know, wave the magic wand and went “Poof. We got it.” And for me, Lukas for you, that might be how it is. But for me, that's not how it is. I got to put a lot of time into it. So, for those that are moving from Angular 1 to 2, it is a bit of a jump. But it's totally worth it in my opinion. I always joke that had the Angular team stayed exactly with what they had with Angular 1, I guarantee in less than a year people would be like, “Oh, that's such a caveman framework. Why didn't they move to the modern stuff? Look what all these other frameworks are doing.” And they in my opinion had no choice but to start embracing the ES 6 concepts and all this cool new stuff you can do with modules and things like that. So, long story short, for those that are moving to Angular 2, don't let the newness be like, “Oh my gosh. I'm not going to do this. It's too involved.” And I think we've all felt that way. I felt that with Angular 1 very much so. But the good news is due to how nicely laid out the docs are if you go to Angular.io, due to all the samples out there, for instance I have one called Angular2-BareBones up on my GitHub site, it's a really simple starter one, it is pretty easy I think now to jump right in and be super productive.

I think if you're starting from total scratch, and when I say total scratch I mean you're trying to figure out SystemJS or Webpack or whatever it may be to get the modules loaded and all this fun stuff that you can do with Angular 2, that part I think can be actually very intimidating. But really, you don't need to start there, I don't think. I think your number one starting point's going to be, “Hey, I've done controllers before. And now we have these things called components.” Are they identical? No. do they have some similarities? Definitely. We had views before and template URLs and things in Angular 1. We still have those in Angular 2. We had data binding. We still have that. Is it different? Yeah, it's different in how it works. But we always, John and I in our workshop, a little one-hour workshop we did and the big one, we kept bringing up that, “Hey, there's 43 directives, and I think Brad brought this up in his keynote talk that there's 43 directives that we used to have to worry about in Angular 1 that are just gone in Angular 2,” because there's just a better way to do it. It's way better I think for maintenance, consistency, all that stuff, as you build your app. So the bottom line for me, if you go to Angular.io Deborah Kurata did a real nice write-up. I think, Ward, isn't it in the cook books section or something like that? Where I think there's a comparison between Angular 1 and Angular 2.

**WARD:&nbsp;** That's right. She did write the cook book for… it's a nice chart of here's what you know in ng1. Here it is over here over here in ng2.

**DAN:&nbsp;** Yeah, and it's really good I thought because it's super quick to read. You don't have to spend a lot of time and you can jump right in and get some nice parallels between the two. And going back to your question at least on the Angular 1 people Lukas, for me I learn the best when you say, “Okay, here's how you used to do it. Here's how it is now.” Because syntax, eh, I get over syntax. And that's our job. Syntax should not be a big deal in my opinion. A lot of us can do multiple languages and do all those fun stuff because it's just what we do for a living. What I think is important is the concepts. And once the concepts click and you understand how, “Okay, here's how we did it in Angular 1. Here's how now it works in Angular 2,” I actually think it's a pretty, well I want to say pretty easy, but a much easier jump between the two.

Now, if you get the people, I'm going to address the second group here which I had last week when I was out in Florida for this class we did, I'd say, I don't know. I'd have to count them up. But probably 50% of them, maybe a little more, had never done Angular 1 at all. So, they're brand new to all this. A lot of them were server-side people that had done other languages on the server. In a way, I almost think it's sort of almost easier to pick up. [Chuckles] Because when you know Angular 1 it's almost like you know too much. You're so used to worrying about when do I have to call \$apply and do I have to do controller as and all this fun stuff in Angular 1. Whereas Angular 2 we don't need that anymore. It just goes away. So, for the folks that are brand new to Angular 2, if you're looking to get into what I call true framework, Angular 1 was a framework but Angular 2 is definitely what I'd argue as more a framework that's more consistent is probably the best way to put it. Then I think you'll actually find it's really easy to get started with as soon as you understand the role of components and how they all work.

And so, for me it all really boils down to when we do classes and workshops, what do you already know? And if you already know Angular 1 then I try to bring in the analogies between the two, the parallels. If you don't know Angular 2 at all then we can just jump into why are we doing this in the first place and here's how Angular 2 can make your life hopefully happy. So, anyway that's my little spiel there. Hopefully that answers some of your question.

**LUKAS:&nbsp;** So, what has been your experience when you're dealing with people that have a classical background such as .NET or Java and then you show them what was traditionally, at least from their vantage point been weird? I hear that a lot of, “Oh, JavaScript. It looks like Java but man, it does not behave like Java at all.”

**DAN:&nbsp;** No. [Chuckles]

**LUKAS:&nbsp;** When you start to show them Angular 2 with the TypeScript, what is traditionally or generally what is their response to that versus if you were showing them a jQuery “application”?

**DAN:&nbsp;** Yeah, no. Great question. So, I can definitely address this because I just had this like I said last week come up. So, in this class I was doing, the second chapter is just an intro to TypeScript. And nobody in there had done TypeScript. Well, I think two of them had maybe played with it barely. But really, nobody had one it. And a lot of these folks had done Java or .NET. So, pretty much what you just asked about. That's their background, either Java on the server or .NET on the server. And so, we got through that chapter and we went to the TypeScriptLang.org and I like to play with the playground that they have there because it's a great way to do live demos and have everybody do it with you and all that fun stuff. And we got done with the chapter and we went on break right after that. And the response was like, “Oh my gosh. This is so much better than what I thought we had to do,” because a lot of these folks had not done… some of them had because there were some Angular 1 folks as I mentioned. But a lot of them had not done much with JavaScript per se other than maybe copying and pasting some function from something they found on the internet, which I guess that means you know JavaScript.

So, with TypeScript being in the mix, or even if you just went with ES 6, even if you didn't want all the cool stuff TypeScript has the structure that ES 6 and TypeScript can give you if you want to take advantage of it is actually pretty awesome. And the response when we got done was, “Wow,” like I said, “This is amazing. I actually want to do this.” And so, I think if you're coming from a background where you're used to classes, you're used to properties and methods and things like that in your classes, then what I love about TypeScript is it doesn't force you down either road. If you're a functional programmer it will support that. If you want to jump into the new class support and do all of that, it supports that great. And so, you can have your cake and eat it, too. And for this crowd a lot of them did have that kind of classical object-oriented background. So, going with classes which is obviously what Angular 2 does if you're using TypeScript or ES 6, that's pretty much right up their alley. And so, that was an easy sell I guess you could say to that crowd.

And so, the other thing I would as is when you throw into the mix that TypeScript supports interfaces and generics and types and all these other feedback you can get when you transpile from TypeScript to say ES 5, that was also very compelling to this group. Because they're used to having a compiler that gives them instant feedback when they screw up. And I used one of John's quotes. I'll have to summarize it here. But basically it was something along the lines, in my ng-conf talk I mentioned a quick little quote he had and it basically tells you when you screwed up. [Chuckles] Something like that. But that's really a cool thing that I think people underestimate when they haven't worked with a language that has a compiler.

I hear a lot of people say, “Oh, I don't need that. I don't need this feature of a compiled language. I can just do it with JavaScript.” And yeah, you can. I've done it for years and years. And you guys all have and probably everybody listening has. But I'll tell you, getting on, especially on large-scale enterprise apps, when you get the ability to get instant feedback on when you screwed up how you pass something or how you defined a variable or whatever it may be, that's pretty compelling once you get into some of these bigger enterprises. And this company was a bigger kind of enterprise development shop.

**JOHN:&nbsp;** You know, and some of those things you're pointing out Dan, you wouldn't even find those kinds of issues until you went live in production. So, I think that's one of the big advantages there of TypeScript.

**DAN:&nbsp;** For sure. A particular friend who might be on this call right now, I'll just leave it as they ran some code through the TypeScript compiler. Apparently the code already had a lot of unit testing things and they were able to catch issues right off the bat that just wouldn't have been caught otherwise, to back up what John was just saying.

**JOE:&nbsp;** That's interesting.

**WARD:&nbsp;** That could have been any of us. [Laughs]

**JOE:&nbsp;** Yeah, yeah.

**LUKAS:&nbsp;** I'm just like, “Was it me?” I don't remember but it might have been.

**DAN:&nbsp;** [Laughs]

**JOE:&nbsp;** So, what if I happen to not really like… I'm a JavaScript developer. I don't like types. I don't like TypeScript. First question is, why is my opinion wrong and what do I do about it?

**DAN:&nbsp;** [Laughs] I don't know if you're setting me up Joe, or…

**JOE:&nbsp;** [Laughs] No, I'm…

**DAN:&nbsp;** [Chuckles]

**JOE:&nbsp;** No, seriously. If you are…

**DAN:&nbsp;** Except for I know you so I don't think you are. No, it's another…

**JOE:&nbsp;** Right. But seriously, you're a JS dev and you're not really a big fan of TypeScript. What do you do about that?

**DAN:&nbsp;** Yeah. And there are plenty of people out there. Now this particular company I was at last week, they were all find with it. But I did a user group talk. There's a new meetup here in my area in Phoenix. In fact, Lukas I think you're talking soon if I remember right, at it. And we had a pretty good turnout. And I did have several people come up and say, “You know, I just can't buy into the TypeScript thing. I don't see why I need it.” And I really do think it goes back to sometimes they totally know exactly what they need about their projects. And what I mean by that is they know what they know and they know about the options and had actually taken time to research. And in that case I'd say go with whatever is going to work for your team. Because I'm not one of those that says, “Oh, if you don't do it this way it's wrong.” I hate those religious battles we get into.

**JOE:&nbsp;** Yeah, John. Your style guide.

**JOHN:&nbsp;** [Laughs]

**DAN:&nbsp;** He wasn't even on the call yet when we were talking about that.

**JOE:&nbsp;** [Laughs]

**DAN:** [Laughs] But anyway, when it comes to choosing am I going to go with ES 5, ES 6, or TypeScript? I'll have to admit I'm not a big fan of how ES 5 looks with Angular 2. It works. I'm not saying it's bad. I'm just saying me personally I don't really like it. It feels too much boilerplate code to me. Because I've seen a bunch of stuff out there with ES 5 and Angular 2. And it works. You can do it. So, if someone listening is like, “Hey, I'm sticking with ES 5. I don't care what these guys tell me. This is what I do,” then I'd say great. Go for it. You can still do it. It's not my favorite approach. But you can do it.

**JOE:&nbsp;** You're not saying it's bad. Just that it's the worst thing ever.

**DAN:&nbsp;** Well sort of, yeah.

[Laughter]

**LUKAS:&nbsp;** So, I think what he's trying to say… it's not half bad. It's all bad.

**JOE:&nbsp;** It's all bad.

**DAN:&nbsp;** Well, no. It's actually not that bad if you're an ES 5 person. But what you…

**JOHN:&nbsp;** Yes, it is.

**JOE:&nbsp;** I'm an ES 5 person. It's [horrible]. It's [inaudible]

**DAN:&nbsp;** Well, once you've tasted the fruit of ES 6, you know…

**JOE:&nbsp;** [Inaudible]

**DAN:** &nbsp; Once you're into ES 6 man, it's like there's no going back, I don't think. Because…

**JOHN:&nbsp;** And thank you folks. This is Dan Wahlin, the nicest man on the internet.

[Laughter]

**DAN:&nbsp;** Yeah, I remember. I think Joe's intro said that. But I think it was nicest man staring at you at Subway or something like that.

**JOE:&nbsp;** On the subway. Staring at you [inaudible]

**DAN:&nbsp;** Oh, on the subway. [Laughs]

**JOE:&nbsp;** Staring at you on the subway, yeah. That was [inaudible].

**WARD:&nbsp;** No, I like at Subway.

**JOE:&nbsp;** [Laughs]

**WARD:&nbsp;** I can see Dan there with plastic gloves on his hands.

**LUKAS:&nbsp;** [Laughs]

**JOE:&nbsp;** Would you like everything on that?

**DAN:&nbsp;** That's right. That's right. So anyway, I'm not a big fan of the ES 5 route. I won't lie to you. I just think it doesn't look at structured and as pretty I guess you could say. I don't want to maintain it is my bottom line. Now, if you…

**JOE:&nbsp;** You know what I think is interesting about that whole thing is that the reason to do Angular 2 in TypeScript and ES 6 is not so much that, “Hey, the coding is better.” It's because like, “Oh, you got all the things about ES 6 or about TypeScript that people will say are advantages.” Fat arrows and modules and types that catch things. The fact is that it just, without TypeScript and ES 6 it really stinks to do Angular 2. So, to do them you do less stuff. You do less work. There's less ceremony. There's less things. You're not saying, “Oh, my ES 5 code is fine.” It's just you're jumping through so many hoops to do Angular 2 in ES 5. And they take away the hoops, the fact that then you have the option to start using types and start using fat arrows and you have to be using at this point modules, right? Then you might start realizing the benefits of all those niceties.

**DAN:&nbsp;** Yeah.

**JOE:&nbsp;** But they actually, it's sort of weird. It's not like, “Hey, TypeScript and ES 6 are great so let's do it with TypeScript and ES 6 and hopefully you'll go there and say yeah, that's actually really cool so I'm going to do it in TypeScript and ES 6.” What they kind of did and it wasn't on purpose, it was just the way that things fell out, is they just made it really suck in ES 5. So you're like, “Ah, I'm trying to do it in ES 5 and it sucks so I'm just going to have to do it in TypeScript and ES 6.” And then you might get in there and say, “Oh, there's lots of other things in here I can benefit from as well.”

**DAN:&nbsp;** Yeah, and you know there's one particular guy who is out there that's pretty well known. And he just loves the ES 5 with Angular 2 and that's why I say, you know more power to you. If that's your thing and that's what you want to do, stick with what you're good at. But I'm telling you, you're missing out if you don't make the jump to ES 6. And if you're going to make the jump to ES 6 you might as well just jump right to TypeScript.

**JOE:&nbsp;** Yeah.

**DAN:** In my opinion. Because jumping from ES 5 to ES 6 is a pretty good jump. Number one you're going to be using a transpiler, probably Babel. And then if you're going to do that anyway, then in my opinion you might as well get these benefits that TypeScript offers that we can talk about as well. I've already mentioned a few of them. Interfaces, generics, the basic types, things like that. So for me, I've told this story I think even on here before. But what the selling point for me years ago was this group at Intel who I came in for some architecture stuff about almost three years ago now. They decided to go TypeScript with Angular 1. And that turned out to be, if you care about maintenance and you care about reuse and you care about that some team members leave and sometimes we have contractors and things like that, then structure matters. Having consistency matters across your codebases. Having&nbsp; led several teams over my career over the years, it's just I've always been a little bit of, I don't want to say dictator but [chuckles] a little bit picky on how team members write code. Which is why we need style guides and stuff like that for out teams, in my opinion.

So getting back to your question though, yes you do have a lot of choices. ES 5, ES 6, TypeScript. Definitely I would start at a minimum with ES 6, at a minimum. But given that Angular 2 and several other frameworks now out there are starting to be written in TypeScript and Angular 2 is written in TypeScript, given all the benefits it offers, given that it'll give you what ES 6 gives you, at least the core concepts you need for Angular 2 development it's a no-brainer in my opinion to say, “Hey, I want something that as John mentioned earlier is going to let me catch errors upfront.” And once you get into that kind of technique or way of developing for your team, even if you're a team of one I think it's super useful. Because you catch all these errors.

**LUKAS:&nbsp;** Well, I think it's interesting that when we talk about TypeScript we talk a lot about error catching and I think IDE tooling. And I think that's super awesome and I appreciate it especially when you can type something and then it auto-imports your module. It's pretty neat. But I think another thing that is really important I don't hear a lot of people talking about is when you are working on an application with more than one person TypeScript makes your code a lot more descriptive. It's really easy to convey intent when you say, “This property is of this object.”

And so for me, I think my favorite thing about TypeScript is actually interfaces and being able to program to interfaces and not concrete implementation of things. That opens up the door for all kinds of things, especially when you start to see different render targets. So, with Angular Universal, it's different things. The pattern is to abstract those out and then just basically program to an interface. And then at runtime pick the appropriate, concrete instantiation that you're going to use. And so, upfront there's a huge benefit of catching stuff at basically compile time. But I think over the long term, you cannot overstate the importance of writing really descriptive code that people can understand your conveying intent right up front.

**DAN:&nbsp;** Totally agree.

**JOHN:&nbsp;** I think one of the things you brought up Lukas is important, too. And I'll change what you said slightly different for my angle and that's not that the interface makes it important but the fact that you've got a type in some cases can be super valuable. And here's an example of that. In Angular 1 when we wanted to tell what types were the things you were injecting we had to use a stringed array, an array of strings basically to tell it “Hey, these are the types. Go look them up.” And what happens if you misspell that? Who catches that? That was a big mess that we had to deal with, with Angular 1 with the dependency injection because ES 6 solves a lot of this with TypeScript. But in ES 5 we had to do these strings. And in TypeScript with Angular 2 we just tell it, “Hey, that's of type data service or HTTP.” And it figures these things out for us. So, we have less opportunities to make these big screw-ups that we had with TypeScript. And it's super, much more readable. So, I totally agree with you there.

**DAN:&nbsp;** I think the biggest one, I mentioned this in one of the talks I did at ng-conf was how many times have you gotten data back from a promise and you're like, “Huh, I wonder what I'm getting back?” Maybe you know the API really well but even when I know the API I always forget the property names and things like that. And so, by… in Angular 2 it's an observable typically we're getting back. But whether it's a promise or an observable or whatever it may be, even just a regular function call that's synchronous, the ability to say, “Here's exactly what you're getting back,” and then yeah you get the tooling and support and all that is just a huge deal.

Or when I'm passing data into a function, especially the example I always give is a settings object. I remember back in the day with jQuery plugins you had to make sure that when you passed in your object literal for your settings to initialize the plugin when you called it, that you had the proper properties, you didn't have any typos in them and things like that. And with interfaces that you mentioned Lukas, you get all that. And so, if I have a typo in one of the properties, depending on your editor, if you have one of the editors that support this well then you're going to get a red squiggly or maybe something over the right or left of the code that tells you right away, “Hey, you screwed this up.” And that's just, I can't even say how important that is.

If you're on a small project, it probably doesn't matter as much. But having been on many projects over my career where many thousands of, even back in the 90s we had some apps that were many, many thousands of lines of JavaScript. I always joke, if you think IE 6 is bad you should have tried programming against IE 3. I had to do that. A lot of fun. But it really locks things down not in a restricting way. In more of a, “Hey, I'm going to protect you,” way. And so yeah, pretty awesome.

**WARD:&nbsp;** We are totally sold on TypeScript and we've been preaching it. And it's good to hear you confirming our perception. But swinging over to Angular 2 itself, what are the things that you find people who are hearing about it for the first time, well you know, [inaudible] some misconceptions about it. That would be interesting. And also what surprises them? What do you have to teach them to give them that 'Aha' moment? What are the big Aha's?

**DAN:&nbsp;** Probably the first big Aha is, especially if they've done Angular 1 is the new data binding syntax with the square brackets for properties or the parentheses for events and things. Because people go, “Aha! I used to have to write a custom directive for that or use an Angular directive for that. Now I just do it myself. So, my maintenance story is better. I'm more consistent. Everything is good about that.” I always like to say now that I wish they would have thought of this five years ago where I could just bind directly to a raw DOM property or a raw DOM event. Because that's pretty compelling once you get what it's doing. So, that's one of the Aha moments. Like last week everybody was like, “Oh, that's actually really super cool,” once they get over the syntax. [Chuckles] Right? You got to get over the syntax. But once you get over that hump you start to realize that, “Wow, this is really powerful because I don't have to write as much custom code to do what I used to have to do,” as an example.

I think probably the second biggest which I usually don't get into this right away because it gets a little more complex is the whole module concept. That's just huge because if you come from, Lukas you asked about some of the classical object-oriented developers and they’re all used to having some type of a naming container. And things don't link in the global scope in those worlds unless you're just meant to do it for some reason. And anyway, I won't go into the details there. But with JavaScript on the other hand we've always had to do if/e's or some other wrapper function of some type or another that allowed us to make sure that data was pulled out of the global scope.

And so, another Aha moment Ward going back to your question I think is once people understand how Angular 2 is based on the concept of ES 6, ES 2015, whatever you want to call it, modules, there's another, “Aha, this is really cool.” Because every file ultimately becomes its own module which basically means things in that file, variables, functions, whatever it may be, classes, they don't leak in the global scope. And that file is self-responsible. And if you haven't done it, this is a huge, huge Aha moment. In the past I've always had to rely on, Ward or Lukas or John or Joe or whatever, you guys know, you loaded the script in the wrong order in the page. And all of a sudden my code's not working because I thought your script was loaded and you thought my script was loaded. And anyway, everybody's done this.

The Aha moment with ES 6 modules and TypeScript of course supports this is the ability to say, “Hey, this file is totally in charge of itself. It doesn't rely on this or this or this.” It's going to import exactly what it needs right at the top of the file. So, you're going to be very clear on what this file is using. And then once those things are imported you can of course then use those however it may be. Maybe its dependency injection in Angular 2. Or maybe you're new-ing it up yourself if it's some custom object potentially I suppose. So, that'd be another Aha moment I think people have when they move.

And this is a great reason that you want to jump into modules and ES 6 and TypeScript, because if you've ever dealt with either A the global scope problem and if you haven't then you probably haven't written much JavaScript. Everybody's hit that. Or B, just the sheer size of an application and making sure that all of the scripts are in the right order and this script relies on this script which relies on this script. And it gets kind of painful in large apps. And that's why we had RequireJS back in the day. And some people still use it. I was never a huge fan. But it was one way of dealing with that problem. Whereas now it's just built into the core of ES 6. And so, I think that's another big Aha moment with Angular 2 is the self-responsibility I guess is the word I'll use, of these modules. So, that's kind of two things. I think the data binding is like, “Ah, that's really cool.” And I think the modules. And I can keep going more but I'll let you chime with a follow-up. [Chuckles]

**JOHN:&nbsp;** Well, let me ask you too, Dan. Let's look on the other angle. What parts of Angular 2 do you feel like people shouldn't focus on right away? Are there areas that are kind of edge cases? Because you look at the surface area and you say, “Yeah, you should definitely look at components and modules and data binding.” What parts of Angular 2 should people push aside for the short-term when they're starting to learn it?

**DAN:&nbsp;** As of today there are a few things that are still being worked on. [Chuckles] Today being May whatever it is. What are we, 17<sup>th</sup> or something like that today? 18<sup>th</sup>? 17<sup>th</sup> I think. So, one of the things that I think is not your first thing to dive into is something called providers as an example. This is how under the covers dependency injection works with Angular 2. It's way more flexible than with Angular 1. I remember Ward and I were having a discussion. We were at a different conference and we were outside in Vegas. And as we were talking he was actually, because he had done more at the time with these things called providers than I had and he was telling me about all these things you can do. And it was a great discussion but I'm like, “Man, this is getting pretty deep.” Now that I've had more time to dive in I get it and I get how it works. But anyway, that'd be one thing. You don't need to worry about that upfront.

Some of the stuff that as of the time we're recording that's going to be ready it looks like by the time [inaudible] you know, soon, is the new version of the router. But you really, that's not the first thing you should focus on. You should get a little, just load a root component and get a template and start playing around with just one component, one template. And start doing some data binding with that and get the hang of that first. Then maybe you say, “Okay, now I want to load a child component into that root component.” And then you start to add another TypeScript file and template. And you start doing some data binding there. But I definitely wouldn't jump into providers and routing and even HTTP, observables all that stuff upfront. That comes after you know the basics. Get good at the root component. Get good at the data binding and the templates. And then start expanding your knowledge from there. That's my opinion.

**WARD:&nbsp;** I think I really agree. I think you can make a pretty amazing app without knowing any of the other things that you describe there except possibly having to get some data with HTTP, which doesn't have to be a particularly complex task. There's a quick cover my eyes and go kind of approach to HTTP that gets you there, a cook book approach. And then you're back in business.

**DAN:&nbsp;** Yeah, I think for me, I'm going to ask you guys a question. So Ward, what was the first thing that you thought was the hardest when you learned Angular 2? We're reversing the interview panel here.

**WARD:&nbsp;** Oh, dude. [Chuckles] Of course there were all kinds of things that were hard because there was no documentation at all at the time

**DAN:&nbsp;** Okay. Well, forgetting that, just general [inaudible] concepts that are available today.

**WARD:&nbsp;** Well, I think that the thing that I stumbled on which you must see over and over again is having to repeat myself. I have to… especially with directives that are used within my component. And so, I have to first import it to get the symbol. And then I have to remember to put the directives property on there and list it there, or the providers thing and you put it there. And then I have to…

**DAN:&nbsp;** Yup.

**WARD:&nbsp;** You know, those are things that are easy to overlook. And then you're staring at the screen and wondering why nothing is happening.

**DAN:&nbsp;** Those are when you first start, I hit that. Lukas, you got a favorite that you started with initially?

**LUKAS:&nbsp;** So, I've found generally when I'm just talking about Angular 2 to someone who's knew, walking them through building just a really simple kind of website, so just start with a simple root component. Then you build out a couple of child components. You stack them in there. And then you show them how to split those out with the component router. And it's gotten a lot better. I will say that. But I think the first moment that I had where I wanted to throw a chair through a window was when I tried to do something non-trivial with the component router. I think I was expecting parity with UI router. And when I was, so trying to set up child routes and then trying to do a parallel [main] route which at the time was impossible, that just made me want to jump off a bridge.

**DAN:&nbsp;** [Laughs] I could sympathize there. John? What's your one? I got one. You guys haven't hit on mine yet but we'll get back to me in a sec.

**JOHN:&nbsp;** One of mine is, and I don't necessarily agree with this. I think it's why there's friction for me, is when I see people trying to grab elements out of the UI inside of a component. They're actually grabbing them by IDs or by selectors and whatnot trying to get handles on those elements and deal with those inside of a component and going down that road. I feel like the code that you have to write to do that isn't necessarily clean. And nor is the concept behind why you would do that in the first place. So, when we're mixing UI inside the component I still feel like that's a little messy. Although it's a little bit better than directives were. But that to me is still a pain.

And I'm going to cheat and add a second one. And that's before I even get to Angular I think it's really hard to teach somebody like you talked about from last week who isn't really a JavaScript expert, hasn't been in this world, how do I get Node installed? How do I use npm? How do I even get to the point where I can start doing Angular?

**DAN:&nbsp;** Yup.

**JOHN:&nbsp;** And that's really painful.

**DAN:&nbsp;** So last week, that's my base image that we always use. In this case it was on-site class at a company. So, they had to set up the machines and luckily they were set up properly. But I think probably 90% maybe of the people had never once run an npm install before. And that's just because they work in a different world. They worked in the server world and that was the whole point of this thing we did was to bring them into, “Hey, where are modern web apps going?” So yeah, I'm with you. I hadn't even thought of that one. But that's true. We all, those of us that do this a lot I think we get stuck in our own little bubble and we forget that we all, the first time we ran npm install, I still remember too, and something didn't work. And I was like, “Oh my gosh. What do I do? I have no idea.” So, cool.

Joe, you got a favorite that you stumbled on [inaudible]?

**WARD:&nbsp;** Can I jump back in with another one? Because the other one that gets people is the complete change in the tool chain that they're used to. And if you're a Visual Studio person and you think you're going to be coding Angular 2 and JavaScript and TypeScript in Visual Studio today, you're [chuckles] in for a rude awakening. And we're still trying to figure out something under 16 steps that make no sense to get there. So, you're facing… and none of these things have to do with Angular 2. They are… all of them are about getting, embracing this new world of this kind of modular JavaScript, TypeScript development.

**DAN:&nbsp;** Yeah. And since you talked out of turn Ward you're officially banned. Moving on, but Joe.

**JOE:&nbsp;** [Laughs]

**DAN:&nbsp;** [Laughs]

**JOE:&nbsp;** John a little bit stole mine. The build chain was just, the build for Angular 2 to get it running in a browser was just crazy. And it's definitely changed. It's gotten a lot better. But there are four or five scripts. You get one of those scripts out of order or forget one of them and you can actually… there's some that you don't necessarily need depending on what browser you're in. That could be crazy.

But since John took that one, I'm going to say pipes. Pipes are one of those black holes because you'll do a pipe and you'll think it's a fil-, if you come from Angular 1. You work with a pipe. You'll think it's a filter. You're going to try to do something you would do with a filter like sort or filter.

**DAN:&nbsp;** Yup or order by. [Chuckles]

**JOE:&nbsp;** Yeah, yeah. And then that's it. You're going to be in a world of hurt. And it's not clear enough. I don't know that there's a way to make it clear but it's just not obvious that that's not the place to do this in Angular 2.

**DAN:&nbsp;** Yeah.

**JOE:&nbsp;** Because we did it there in Angular 1 because we didn't worry about performance in Angular 1.

**DAN:&nbsp;** Yeah.

**JOE:&nbsp;** We care about performance in Angular 2.

**DAN:&nbsp;** Let me circle back. John, is that something that's already… I know the style guide is brand new for Angular 2. And because it's hard to be too detailed when it's not even officially released yet. But is there anything in there yet about how the role of pipes versus doing it in the component yet?

**JOHN:&nbsp;** No, not yet. I wanted to put it in there but Ward restrained me. Please don't ever use a pipe to create a custom loop through an array and a filter. But…

**DAN:&nbsp;** [Chuckles] Right.

**JOHN:&nbsp;** But he told me not to put that in there just yet.

**WARD:&nbsp;** Did I stop you?

**JOHN:&nbsp;** [Laughs]

**WARD:&nbsp;** Because I would rather just say don't use pipes.

**DAN:&nbsp;** [Laughs] Is this format in the [inaudible] component?

**WARD:&nbsp;** Well, okay. So, you got the one use case. But I wouldn't…

**DAN:&nbsp;** [Laughs]

**WARD:&nbsp;** Aside from using it as a formatter, I'm very reluctant to use pipes for any serious work with the…

**LUKAS:&nbsp;** Well, the…

**WARD:&nbsp;** Go ahead.

**LUKAS:&nbsp;** Sorry.

**JOHN:&nbsp;** That's a good qualification. A formatter. Yes.

**JOE:&nbsp;** You see them a lot or you see the advice. A lot places in the documentation don't use pipes to do order by and filtering. But not everybody's going to see it. And the pipe itself, especially if you came from Angular 1 which is funneling you down this road. And you'll implement a custom pipe. It will be working. And you'll think everything is okay. And then you've introduced a horrid performance problem. On the flip side of that is if you really know what you're doing you can actually do that functionality in a performant way in a pipe if you really understand the change detection schema and how it works in Angular 2. It's like one of those things that are so advanced you shouldn't do it. And so, I know that there are people…

**DAN:&nbsp;** Yeah.

**JOE:** Out there that are going to do it because they understand the ramifications. And then somebody who doesn't is going to come along and be like, “I'm going to do it too,” or, “I'm going to try to figure out. I'm going to make a change to this code that you already wrote” and it's going to be terrible.

**DAN:&nbsp;** Joe, can you explain a little bit too about some of the reservations you have, like the whole stateful/non-stateful pure or impure. Let's not get deep in it but kind of give people a synopsis of why there's a concern.

**JOE:&nbsp;** Yeah. And there's been a slight change in the last version that I'm not up to date but I don't think that it's meaningfully changed this. Pipes. Man, how to describe this in a simple way that works over a podcast? Like when you make a change to data you go and you have an array of data and you add a new element to the data you have just changed or mutated that array. You don't have a new array. You have the same exact array. And normally that works out great.

A pipe by default has no idea that you made that change. Because think about the code that you would have to write by hand to say, “I've got a handle to an array. Has this array changed on me? I can count the number of items but what if somebody removed an item and then added a different item? So, you can't just look at length. What if they changed one of the properties of one of the objects in that array but didn't actually remove or add an item?” There are so many things. And say that they re-sorted the array. The item that was the 10<sup>th</sup> item is now the second item and everything else has been pushed down one. Or items two and 10 just got swapped. Think of all the code you would have to write to check that. That code all exists in Angular 1. It was super non-performant.

So in Angular 2, in order to keep with the performance framework they said, “This is stupid. This is not the right way to do this. People should be doing this by hand in the components. So, the pipe, there's no built-in filter by or order by that will do this because of that. Now, if you instead of mutating that array, if whenever you make a change you create a brand new array and copy all the data from the original array into the new one which sounds like it's way [inaudible] performant but actually is much less of a performance problem than you'd think. It's actually done in a very performant manner. If you do that, then pipes are fine for that sort of thing. Because all they know is, “Oh, you're using a totally different array.” And so then they'll re-run the bindings and re-display the data.

So, once you start understanding how to do immutable operations with arrays or using a library like Immutable.js or Richard Feldman's new immutable library, you can do this sort of stuff. But man, you've really got to know what you're doing. And that means that all the places where you might mutate that array, you've got make sure you're producing a brand new array. And it's so easy for somebody to go in and say, “Oh, I need to make this one little change in this piece of data. I'll just mutate the array,” not realizing that its' supposed to be an immutable array. And so, it was just such a black hole.

**DAN:&nbsp;** Yeah.

**WARD:&nbsp;** Or you can just throw up your hands and flip the switch that says, “This pipe is impure” and it will get called a lot.

**JOE:&nbsp;** Oh my gosh, yeah. Yeah.

**WARD:&nbsp;** A lot.

**JOE:&nbsp;** Potentially every mouse, it could be every mouse movement depending on if you're looking at mouse moves.

**WARD:&nbsp;** Mm, absolutely.

**JOE:&nbsp;** Oh my god.

**WARD:&nbsp;** Absolutely.

**JOHN:&nbsp;** Yeah, to me this is one of those complicated… these are one of those edge cases. Like when Dan mentioned things you don't learn right away, this is one of those things in my mind. You don't learn how to do this right away. Because quite frankly I think you need to use a function half the time to solve the same problem.

**WARD:&nbsp;** [Exactly].

**JOHN:&nbsp;** And Dan, when you teach Angular 2 do you teach how to create custom pipes or do you teach just the, use the built-in formatting type pipes first?

**DAN:&nbsp;** Yeah. So, with this new thing we're doing yeah, we do. But I wouldn't call them, definitely wouldn't call them a filter. They're formatter. They're just taking data and literally dumping that. Adding the dollar sign for instance for the currency type thing. You know, that's built in. I'm not a big fan, in fact we pretty much explicitly cover that I don't like, for the reasons Joe has already outlined, pipes when you're doing anything more than just formatting the data output. In my opinion that's something that really needs to be moved either into a service layer, maybe the component. It depends on who's doing it, where it's being done. But yeah, I like to keep all that stuff separate from the UI. [Inaudible]

**WARD:&nbsp;** And may I just add one thing there, because I think it's really important. Because we're making it sound like, “Oh pipes are a disaster in Angular 2.

**DAN:&nbsp;** Oh, oh, [inaudible]

**WARD:&nbsp;** They are no worse in Angular 2 than they were in Angular 1. The exact same problems existed maybe even worse in Angular 1 because the digest cycle kept whipping around so often.

**DAN:&nbsp;** Yeah.

**JOHN:&nbsp;** And most of these problems really only apply to pipes or filters in Angular 1 over arrays or lists, right?

**DAN:&nbsp;** Yeah.

**JOHN:&nbsp;** You're using a scalar value like a single-value like Dan said. You're taking a name or a currency and you're formatting it. It's super simple and it's a great use case. [Inaudible] people [inaudible] use it.

**DAN:&nbsp;** Yeah, I do it as…

**JOE:&nbsp;** And just to [inaudible] in on with what Ward said.

**DAN:&nbsp;** Yeah, go.

**JOE:** Digests are actually worse because they ran a minimum of twice every time they ran.

**DAN:&nbsp;** Ah, yeah.

**JOE:&nbsp;** Got to remember that.

**DAN:&nbsp;** Yeah, and I always view pipes nowadays in Angular 2 as definitely part of the UI layer. Because they are. They're rendering in the UI, in the view. And so, what should you be doing in the UI? And I think the answer there is very little [chuckles]. And so yeah, I'm with you guys. I agree it should be simple. So, let me…

**WARD:&nbsp;** So, let's just all agree. Pipes are for smoking.

**DAN:&nbsp;** Oh, for sure.

**JOHN:&nbsp;** Okay there.

**WARD:&nbsp;** [Laughs]

**DAN:&nbsp;** [Inaudible]

**JOHN:&nbsp;** So, on that note Dan, what's your favorite feature of Angular 2? What do you just love using?

**DAN:&nbsp;** Yeah, hold on. I got to circle back to what I struggle with first now that we got around the round robin here.

**JOHN:&nbsp;** Oh. Wait, you struggle? You, Dan Wahlin, struggles with something?

[Laughter]

**JOE:&nbsp;** I don't believe it. Don't believe it.

**DAN:&nbsp;** Ah, yeah. It's why I don't… my glass on my window like Lukas was saying. I've already thrown the chair so my wife just said, “Oh, put up some tin foil.” No, just kidding. But…

**WARD:&nbsp;** You'd never know because Dan never sweats. This is one of the things that are really weird about him.

**DAN:&nbsp;** Yeah, yeah. Ward, you know me better than that, Ward. But so, my two things, SystemJS or Webpack, whatever one you're using, I really struggled with understanding what mapping really meant, how you set your defaults because some of that become deprecated in different ones. So, that's part of the stuff. Just go get the quick start from Angular.io or I have this BareBones one and there are a lot of them out there, seeders. Just go get one of those and start working with it. Don't jump into all that right away. And I think we've already kind of established that. Because that part, John and I, we always say, we were on a call once, just the ES 6 modules probably a year or so ago and I don't know how much time we wasted but it was a lot. Just trying to get a really simple, I think we were injecting an engine into a car or something like that, wasn't it John?

**JOHN:&nbsp;** Yeah. We were just trying to get ready for a keynote or something.

**DAN:&nbsp;** Yeah, I think that's what it was. [Laughs] We couldn't even get the stupid thing to work. And now, if we knew what we knew now it'd be like, “Oh, it's easy. You just do this, this, this.” But it's always, I would say it's advanced until you know how to do it. Then it ceases to be advanced, right?

But my biggest thing probably was I definitely was used to promises. So, I think my biggest struggle was I did kind of jump right into the HTTP thing because I wanted real data, was jumping into observables. And that's another one that people if you're new to this you just don't need to jump in right away. But once you get it, they're super cool, super powerful. But they're one of those things that I definitely kind of went “What? What do we need this for? We have promises. I'm fine. Leave me alone. Get off my lawn.” But that's something that is kind of a default now in Angular 2. And actually I like it now, now that I get what it's doing. So, the whole RxJS and Observables and all that stuff, that was definitely new to me. Because I hadn't done a lot. Well, I've seen it but I haven't really done much with it to be honest.

So, my favorite feature.

**JOE:&nbsp;** Dan?

**DAN:&nbsp;** Yeah.

**JOE:&nbsp;** Let me interject really quick. Just for those who may be suffering from some of the same struggles, Pluralsight has a really awesome course on SystemJS. We dig super deep into it.

**DAN:&nbsp;** Oh, nice.

**JOE:&nbsp;** So, if you do really care about SystemJS and you really want to understand it there's a really great course on it on Pluralsight. I watched it and it was really good.

**DAN:&nbsp;** Cool. I might just go watch that too. [Chuckles] But my favorite feature, probably the simplicity of the data binding now. But I really like the flexibility of providers now. In Angular 1 you can do dependency injection. But with Angular 2 it's just so cool to build, say “Hey, the app needs,” well my example as of today because it's something I had to write custom as of today was I needed a way to detect anytime HTTP triggered a request or response. So, you don't want to rewrite your whole codebase to say, “Use this custom thing,” every time. So, with providers and things you have the flexibility to say, “Hey, any time you see this substitute this or add this little custom little piece to it,” or you can do all these really, really cool things. That's one of those things that we already talked about, don't jump into first. But it's really powerful. So, that's another one of my favorite features.

**JOHN:&nbsp;** So Dan, you do quite a bit of traveling and course writing and speaking and you're also on Dancing with the Stars I think in the upcoming season.

**DAN:&nbsp;** [Laughs][inaudible] must have already been canceled.

**JOHN:&nbsp;** [Laughs]

**DAN:&nbsp;** [Laughs]

**JOHN:&nbsp;** Ward got me thinking about it for some reason, about not seeing you sweat. But [chuckles] with all your travels and all that and [inaudible] to talk to, how do you see the adoption or the interest in Angular 2 going right now?

**DAN:&nbsp;** You know actually it's kind of funny because for a while I didn't see any interest. I'd say even six months ago, very little. I shouldn't say any. You always have your people in certain companies that they're kind of the jump ahead people, bleeding edge people. Now it's crazy. Huge interest. We're seeing one of two things. We're seeing companies, one is a big credit card company we've been doing a lot with. They are kind of split. They're looking at React but now that they've seen what Angular 2 is doing, they were kind of looking at React for Angular 1 and debating. Because we did a ton of Angular 1 training with them and consulting type stuff. But now that they've seen, and I'm kind of trying to push them into “Here's why this is cool,” with Angular 2 they're starting to go, “Oh wow. This is actually really neat.” Because a lot of these folks at this one company have a Java background. And so, it's really attractive to them to have this really structured framework where the code is structured, the templates are clean. Everything's really structured, maintainable, reusable, consistent, those types of things.

So yeah, we're seeing a pretty massive amount of interest now over just the last I'd say the last couple of months actually. I don't think I had a single request for anything in Angular 2 two months ago. And now it's like, “Holy cow. We got to figure out our schedule here.” It's pretty busy. So, it's good. It's good for that. So yeah, it really depends. Those are the two things I'm hearing is either React or Angular 2, or React or Angular 2. Those are the two big ones I'm seeing people wanting to move into the dynamic web apps where we do push a lot down to the client.

**JOHN:&nbsp;** Cool. Is it time to do picks, folks?

**JOE:&nbsp;** I think so. John, why don't you start us off?

**JOHN:&nbsp;** Awesome. I'm actually prepared this time. So for picks, what I've got is two things. One is Dan and I are actually doing a workshop in Barcelona, Spain on July 31<sup>st</sup>. So, I' going to pick Dan as my co-presenter and partner. We're doing an Angular 2 workshop in Barcelona, Spain. If you're interested in checking that out we'll put a link in the show notes.

My second pick is recently I decided to stop dealing with creating my own blog and coding it myself and spending countless hours dealing with it going up and down and customizing and I'm writing it. And I finally just decided to pay somebody to host my blog so I could just do what I wanted to do which is write posts. And it's probably the best decision I've made all year. So, what I've done is JohnPapa.net, my blog is now running on Ghost Pro. It's a Node-based system that lets you blog. And I've decided to go with hosting as opposed to doing it myself which I could have hosted on Azure myself. But I decided to get a hosted model because they handle any outages or other issues that you have. And they do patches and security updates. It's really great.

And then on top of that I run CloudFlare in front of it which is free. And CloudFlare, you can put this in front of anything you do. It's a great way to take advantage of caching or streamlining your data. I've actually enabled it to only run SSL to my site now. So, you can only hit my site through HTTPS. If you don't come with HTTPS it actually redirects you to HTTPS. So, those are my picks. Definitely if you're looking into hosting a blog, check out Ghost and CloudFlare.

**JOE:&nbsp;** Awesome. Lukas, how about you?

**LUKAS:&nbsp;** I've got two picks. The first one is this new style guide that just went up. So, John I'm giving you a hug right now. Thanks. I appreciate it. I'm sure…

**JOHN:&nbsp;** Aw, I can feel the warmth.

**LUKAS:&nbsp;** That said…

**JOHN:** Over the intarwebs.

**LUKAS:&nbsp;** Yup. I'm telling you a lot of people have been looking for this and it is here. Christmas in, what is it, May? Yes. May.

My second pick is a book called 'Deskbound: Standing Up in a Sitting World' by one of my heroes, Kelly Starrett. He is really big into mobility and functional movement. And being that we spend hours and hours on a computer it really actually takes a huge toll on our bodies, sitting in this broken position as we program. And so, this entire book is about how to restore mobility and order your body to basically keep yourself from ending up in a wheelchair when you're 65 or 70. So, great book. Kelly Starrett is phenomenal.

**JOE:&nbsp;** Very cool. Ward, how about you?

**WARD:&nbsp;** I have something that is almost on the same order as acknowledging that I like Star Wars which will by the way never happen. And that is that I, those that know me know I carry a big Windows Phone with a giant crack in it. And I in the prodding of my wife bought an iPhone. Now, I know that most of you are already sold on that.

**DAN:&nbsp;** Oh, this is big news, Ward.

**JOE:&nbsp;** [Laughs]

**WARD:&nbsp;** This is just ridiculous news.

[Laughter]

**WARD:&nbsp;** Being the guy that [inaudible]

**JOHN:&nbsp;** Congratulations, Ward. The intervention worked.

**WARD:&nbsp;** [Laughs]

**LUKAS:** Oh my goodness. Pigs are flying right now. They're just flying around.

**WARD:&nbsp;** I'm just shocked to have to admit that it's better. [Laughs]

[Laughter]

**WARD:&nbsp;** I know you've all known that. But like I'm just coming out of the cave and I'm discovering that electricity exists. And I'm conceding that that might be better than cooking over an open flame. But you know, whatever.

**DAN:&nbsp;** Ward just got off satellite phone what, like a year ago or so.

**WARD:&nbsp;** [Laughs] My [inaudible]

**DAN:** He had his book case size phone he'd carry around.

**WARD:&nbsp;** My Get Smart shoe phone. I'm finally retiring it.

**DAN:&nbsp;** [Laughs]

**LUKAS:&nbsp;** In five years from now he'll finally admit that unidirectional data flow might actually be a good thing.

**JOE:&nbsp;** [Laughs]

**WARD:&nbsp;** Never happening, Lukas.

[Chuckles]

**JOE:&nbsp;** Okay. Awesome. For my pick I'm going to pick the StarCraft games that we played at ng-conf. There's video up on YouTube that we'll link to in the show notes or you can just google ng-conf StarCraft. We're trying to get to, trying to get some time to edit the video because the first hour and a half is just dead time. You have to skip forward. But it is the funniest damn thing. And even if you don't play Star Craft or know Star Craft it's just hilarious to watch, because it's people that are just average Joes and there's a very professional caster who's just extremely clever, extremely funny. It's kind of like if you invited Louis C.K. to watch a couple of scrubs playing basketball. And he was making some commentary on the basketball came. You can imagine that's what it's like. We had some very brave souls who volunteered, played some awesome games. But the commentary just makes the whole thing hilarious, Bernie Sanders jokes and all. So, that's going to be my pick is the StarCraft games that we played at ng-conf which you can watch if you want to watch something a little bit funny.

[Chuckles]

**JOE:&nbsp;** Eh. So last, Dan how about you?

**DAN:&nbsp;** I think my biggest pick lately, well I was going to do what John did about the Barcelona thing we're doing. We're super excited to head over there. But since he took that one, Duet. I don't know if you guys have heard of, if you have iPads and you travel at all which I do, there's a software out there called Duet. And I've always tried when I travel, I have, Ward has the same one, I have a monitor that's a USB3 and it works for a dual monitor. But it got a little bit of a hassle because you have to be careful when you shove it in the overhead bins and stuff like that. So, I tried all these other ones but they're always over Wi-Fi and they had lags. Well, this one actually uses your just direct connector into your iPad. So, it's wired. And you can see as a second screen or third or whatever you have your screen right on there. It works with Windows or with Mac. And I like this so much that I actually convinced my wife to get me an early father's day present which is the new big iPad Pros. I never wanted one but now I do because…

**JOHN:&nbsp;** Wait, let's be honest. Did you ask her permission for that?

**DAN:&nbsp;** I actually did.

**JOHN:&nbsp;** [Laughs]

**DAN:&nbsp;** She was with me. But there was a little bit of emotive, I sort of played up the fact that she wanted something else. [Chuckles] So, I kind of got approval because I said, “Well you know, you want this thing. How about, can I get this thing?” But anyway, awesome software. I'm super impressed with it. It's been rock solid and there's no delay at all. And now I have this perfect travel companion. I don't have to haul around a separate thing. So, there's mind.

**JOE:** &nbsp; Awesome. Well, thank for being on the show Dan. It was awesome to have you on. [Inaudible]

**DAN:&nbsp;** Well, thanks for having me. You guys are always great to talk with. Good discussions.

**JOE:&nbsp;** And for those who haven't already keyed on this, go watch Dan's talk from ng-conf. It was a great talk.

**DAN:&nbsp;** Oh, thank you. That was fun. It was a great conference. Highly recommend. If you haven't been, you need to go next year. Great conference.

**JOE:&nbsp;** Alright. And that'll be it. We'll be back next week. Thanks, everybody.

**_[Bandwidth for this segment is provided by CacheFly, the world’s fastest CDN. Deliver your content fast with CacheFly. Visit CacheFly.com to learn more.]_**

**_[Do you wanna have conversations with the Adventures in Angular crew and their guests? Do you want to support the show? Now you can. Go to AdventuresInAngular.com/forum and sign up today!]_**
