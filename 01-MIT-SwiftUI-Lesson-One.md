# 01 - MIT SwiftUI Lesson One
(upbeat music)

Stanford University.

## 课程介绍
Hello everyone and welcome to Stanford University's CS193p
This is a course about developing applications
for iOS devices like iPhones and iPads
using the development environment called SwiftUI.
This is a replay. This course was originally offered to my students at Stanford back in spring quarter of 2021.

My name is Paul Hegarty.

I've been teaching this course in one form or another at Stanford for about 10 years.

And I know that all of you are coming to this with a very wide variety of backgrounds and experience and expectations for what you might get out of a course like this.

So this time I decided to do this little intro for non-Stanford students to try and give you an idea of what to expect in this course before you dive in.

This quarter was another pandemic quarter,only offered remote, so you're going to be consuming this course in the same way as my students were, on video,and there's definitely disadvantages to doing that.

I love live lecture, can't do that, but there are advantages
to watching on video as well.

For example, you've got pause and rewind.That's a great feature to have when you're consuming very highly technical
course content like you're going to find in this course.

Of course, my students also had highly interactive class forums and the TA, and you're not going to have that,but there are a ton of really great resources out there on the internet.

There's a very vibrant SwiftUI community.

And this is not the only place to go out and learn iOS programming.So you'll definitely want to seek out all of those resources as you watch these videos if you haven't already.

Now, this course plays out in kind of a narrative format which works well for the students because they're interweaving it amongst all their other courses.
现在，这门课程以一种叙事的形式进行，对学生来说效果很好，因为他们把它交织在所有其他课程中。

And so, we work together, the students and I to build the couple of good size applications, a card game, and a drawing application.

So I'm telling part of the story when I'm lecturing and demoing and they're participating in the storytelling too though via their homework assignments.

Their homework assignments are always building on the stuff that I'm doing in lecture.

And so we post all the homework write-ups and all the demo code at cs193p.stanford.edu.
因此，我们在cs193p.stanford.edu上发布所有的作业写法和所有的演示代码。

So be sure to go look for those.

They are absolutely essential to getting the most out of this course.

This course is also intended, not just to be a, a how-to course in iOS programming but it's also a little bit of a
how-things-work course.
这门课程不仅仅是一个iOS编程的方法课程，也是一个有关如何工作的课程。

### 本课程适合的学生对象
Systems design is really important for our CS students to learn and so, we try to spend some of our time in the lectures in this course talking a little bit about how SwiftUI is doing what it's doing, not just how to turn the knobs to make it go.So you'll see that flavor kind of sprinkled all throughout the lectures.
系统设计对我们的CS学生来说真的很重要，所以，我们试图在这门课程的讲座中花一些时间来讨论 SwiftUI 较为本质的东西，而不仅仅是知道如何控制一个按钮、一个拨盘。

A little bit about the prerequisites in this course.For the students here at Stanford, they have the prerequisite to take at least three, and recommended four, intro CS courses.
这门课并不是针对零基础的学生，对于斯坦福大学的学生来说，他们至少要学习三门，建议四门CS入门课程，才建议学习本课程。


So, they're relatively experienced programmers.

### 关于面向对象编程
One of the things in particular that students all know by the time they're taking CS193p is object-oriented programming.

So even though we don't actually use much object-oriented programming doing SwiftUI, the concept that you learn in object-oriented programming, like instances of data structures and encapsulation, these are really good things to know when you're trying to understand how SwiftUI works.
学生们都认为 CS193p 时都认为它的主要是面向对象编程的课程。

尽管我们在做SwiftUI时实际上并没有使用很多面向对象的编程，但你在面向对象编程中所学到的概念，如数据结构的实例和封装，当你试图理解SwiftUI如何工作时，这些都是非常好的知识。

Also, SwiftUI requires you to learn a new language called Swift.

And for all of my students,you know, they'll have learned a new language three or four times before coming in here, so it was kind of old hat for them to learn a new language.

So if for you Swift is going to be your second language ever or you're a first time coder and it's your first language, that is going to add a significant extra challenge to absorbing all the material in this course.

So as you can probably gather from all that, this course is not aimed at the first time programmer. I will say though, that if you are just starting out coding or even if you're not even a coder at all, maybe yet, you might still find the first couple of weeks of this course very interesting to watch just to see what it's like to develop an application for iOS, because we dive right in.

Students at Stanford, haven't learned Swift yet so we don't really assume that they know anything at the start. We're going to go step by step.

### 要做家庭作业
We encourage the students to follow along. The homework really requires them to follow along. And so you should be able to do the same thing really, no matter what your level of programming experience is, at least for that first few lectures.

And then you can decide kind of where you want to go from there. So hopefully that gives you all the information you need to know to get started.

So, off we go.

## 进入课程

### 本学期要做的App一览
Let's start by looking at what we're going to build and we're going to do that in these iPhone simulators.

These two things you see on screen are simulating an iPhone 11 on the left right here, and an iPhone 8 on the right.

When we run our application to see if it's doing what we want, of course we could plug our iOS device, our iPhone or iPad, into our Mac and run it on there.But, a lot of times it's nicer to be able to just
simulate a device and see it right on our screen.

That's what these simulators allow.

They simulate not just our application running on an iPhone, but most of the iPhone environment as well, like the settings app.

We can go to the settings app and set things that might affect the way our app runs, or contacts where you need to access the address book, calendar, et cetera. All these things that our application might want to interact with are also simulated on the iPhone.

Here's our app that we're going to build this quarter.It's called Memorize.It has no app icon yet.
这是我们本季度要建立的应用程序。它叫Memorize，还没有应用程序图标。

Hopefully we'll get to that during the quarter.
希望我们能在本季度内完成这个工作。

I'm just going to tap on it to run it. Here it is, and it's a game. I'm going to click here on this Halloween version of it. It's a card matching game. Some people would call this game concentration, perhaps, or memory it's sometimes called.

We're going to call ours Memorize.

That's going to be the name of our app. It's a very simple card matching game.

You click on cards and they flip over and you're just trying to match them. These cards have emoji on them. Our Halloween has a nice orange theme to it.

Those two cards don't match so I have to keep searching around. Oh, I think that was this one, right? So now I could find a match.

There it is. You get a little spinning animation there. Notice also that there's this timer ticking down in the background. That timer is essentially saying how long this card has ever been face up.

We clearly want to reduce that as much as possible and match these cards as quickly as we can. Now, notice there's no score on the screen
because I'm leaving that to you on your homework assignments to decide how to allocate points based on this timer ticking down and how quickly matches are made, or maybe penalize when you could have made a match, but you didn't. There were two cards that match and you're like,

"Oh, I didn't - Oops, I didn't match that one. Oh no, that was the same as that one."

So you might be losing a lot of points here, clicking around, trying to find matches or you might be gaining points because you're so good at memorizing and so you're like, 

"Oh yeah, I know exactly where this thing was. It was right there and I'm going to click and match, and the timer doesn't tick down, et cetera."

So I'm gonna leave that all to you.

I don't want to bias you with any particular canonical implementation of the scoring. So that's totally up to you.

This UI can do other things. We can create a new game. We'll restart with all the cards face down, and re-shuffle everything all around.

You see there's a lot of animation in this game. Animation is very easy to do in SwiftUI. Back here, this part of the UI that we saw over here lets us choose a different theme.

We had Halloween. Let's pick Vehicles.Now we're matching vehicle emojis. That one had a match there. There's another match.

But, it also let's you edit these themes. I can go here and hit edit and then I can click on these and it brings up this nice UI for adding emojis to my theme, changing the theme's color, maybe changing how many pairs of matching cards, what is theme's name.

You're going to be doing all of this UI, a hundred percent of it, in your homework. By the time we're done with this just a few weeks from now, you're going to have the skill to be able to build UIs even as complicated as all this.

Now this is obviously a fair amount of UI to build. We're not going to build this all just this week in the lecture time we have left.

We're going to get ourselves started by just building some of it, a little bit of it. In this simulator, I have a version of Memorize right here that is going to be what we're going to build in this week's lectures.

You can see it has the cards and I can tap on them and they do flip over, although they don't animate.

Obviously there's no timer there. Also, if I flip over all the cards, you'll notice that no two cards are the same. These are all 12 completely different cards. So, we can't play the matching game because we have no matching cards. In general, the whole logic of playing the matching game, we're going to do that next week.

What we're doing this week is just trying to start building our UI and have it look like this. Obviously we're not doing any of this sophisticated UI over there, we're just trying to get our cards up here. We are going to put a couple of things down here that aren't in our final version like this plus button, which adds a card. Add more cards.

Also, our UI is going to scroll because we can hit so many pluses here
that the cards don't fit anymore. Whereas over here that's not true.

By the way, that's really noticeable if we take this and rotate it. This button here will rotate to landscape mode and the cards resize themselves a little bit so that they fit the space more perfectly.

In our version when we rotate, it still works, but we have to be scrolling because we can't fit all the cards.

Our cards are a fixed size right here. I was originally going to have you do a shuffle button down here in your homework, that would shuffle the cards around. But I actually decided to have you do something a little more ambitious which is to shuffle the cards but also provide a very, very simple theme chooser.

Nothing like the theme chooser we saw on the left here, but just something that lets you use what we're learning this week. Also, you probably noticed that that shuffle is doing a little bit of animation but I decided to put that off for now as well, so you won't have to do animation for the shuffle buttons in your homework and we're going to talk all about animation in a couple of weeks.

### Xcode 
The tool we use to build all this is called Xcode. It is one-stop shopping for doing all of this stuff, whether it's editing your code, running it, seeing the UI as you build it, debugging it, et cetera.

All in one place.

Let's talk briefly here about how we get a hold of Xcode. We need Xcode. And since it's a Mac app, of course, we can go to the Mac App Store. If you go to the Mac App Store and go to the search bar and just type in Xcode, then you'll get the top match which will be Xcode.

If you click on it, this is going to say, download. Just click on that and you're up and running. It's a free app, costs nothing, and you can join a developer program with Apple for $99 a year. I'll talk about in a moment what you get for that, but it's not required. Not required for this class, nothing that you do in this class, this app that we're building over here, none of that requires joining the developer program at Apple.

So it's free. So everything's free.

Now, if you're a little bit bold(大胆的) and adventuresome and you want to try the beta version of Xcode, which of course they're always coming out with betas every few weeks, you're certainly welcome to do that.

I'll show you briefly how to do that. Just bring up your Safari, go to developer.apple.com. In fact, we can go directly to developer.apple.com/downloads, probably the fastest way to get there.

You can see there are beta software downloads, both of Mac OS and iOS. But also, under applications here, you're going to see Xcode 12.5 beta 3. This is again going to update over time.You just click download and you can run it. Nothing I do in this course is gonna require this beta, so you're perfectly fine if you just want to use the version off the app store.

Maybe start off with that one, then as you get more confident and you want to be on the bleeding edge of things, feel free to switch over to the beta if you want.
也许从那个开始，然后随着你越来越有信心，你想站在事物的最前沿，如果你愿意的话，可以随时切换到测试版。

Once we get Xcode on our machine, we launch it by clicking on it.

I happen to be running the beta version here. When we do and we get this splash screen. Beta or normal, you're always going to get this splash screen. A very simple starting point in Xcode: on the right over here we have all of our recent projects.

Things we've been working on will be stored here. Then on the left, we just have three options for starting a new project or finding an existing project that's not in this list, which is pretty rare.

All of the projects we work on are kept in here reliably(可靠地), so this is usually how we open that. There are two ways really to create a brand new project.

One is to create it here. That's what this first one is. The second one is to clone a project that is in a source code repository somewhere.

I am going to talk a little bit about source code control and repositories later in the quarter, but for now, we're just going to obviously be creating our very first project ever by clicking this "Create a new Xcode project". This "Open a project or file" down here, not going to really have to do that. Those things will all be over here.

### 新建一个项目

Click "Create a new Xcode project".

It immediately says, what kind of project do you want to create?

Because Xcode can build not only iOS apps, which is what we're clearly building here, but also Mac OS apps, Apple Watch apps, Apple TV apps, even multi platform apps that run both on Mac OS and on iOS.

We will be doing that for the second big app that we build later in the quarter. But, today we're going to do iOS apps. Even within iOS, there are different kinds of apps here. Most of the time we're going to do this just basic "App".

But, later in the quarter we're going to make a "Document App", and there are other kinds here. You might explore some of these for your final project. But we're going to do iOS app. Just click here and here and make sure you do that when you're building your app.

Here's where you might want to pause and go get Xcode if you want to follow along. If you do, be sure to click 'iOS' and then 'App' before you click 'Next'. When you do that, it's going to ask you some questions about this iOS app you want to build.

First question: what do you want to call this thing?

We know that we're calling our app **Memorize**. The second thing here is the team. This is the development team working on this.

Well, that's going to be you. When you run this, unless you've used Xcode before, this probably says something like 'create a team' or something. You're going to click on that to create a development team.

It's really easy to create a development team, you just need an Apple ID. That's just your normal iCloud login. Again, it's not going to cost any money.

You're just going to go and register this development team with that iCloud Apple ID and that's it. Then you'll be off and running. Next, you're going to have a string, this organization identifier. You are the organization.

Basically, it's the organization you work for, but you're a student.

If you're not a Stanford student, this might be the company you're working for. This has to identify your organization that you're working for on this.

If you're an individual, I really recommend using what is called reverse DNS notation right here. Maybe your email address, or if you're a Stanford student,edu.stanford.cs193p.[your SUNetID] instead of instructor.
如果你是一个人，我真的建议在这里使用所谓的反向DNS符号。也许你的电子邮件地址，或者如果你是斯坦福大学的学生，用edu.stanford.cs193p.[你的SUNetID]而不是教员。

Maybe you could even skip the CS193p if you want. But, you just want to pick something here that no one else is going to pick.

If you work for a company, this might be your company's website name backwards, or even your company's website name backwards and then the group you're in at the company.

This just has to be a unique thing that identifies the group that's working on this app. Xcode quickly combines the name with that to create this bundle identifier that's a unique ID for this app.

Makes perfect sense.

These last three little choice boxes here are letting you choose between the new way, SwiftUI, of developing iOS apps, and the old way, which is called storyboard. I only have 10 weeks to show you this stuff so I can't show you both.The new way, it's very new only introduced about two years ago, but it's very powerful and it's also benefited from all the learning that the old way had.

When you're creating an app, you're always going to have these three buttons be on. SwiftUI, the new way, SwiftUI App, that's the new way Also, you can mix the new way with the old way of creating an app.

It's kind of odd, but you can do it, We're not going to.

We're always going to do SwiftUI App. Since we picked these, for the language, there's only one choice which is Swift. SwiftUI is totally dependent on the Swift language, which is a new programming language that I'm going to not assume that you know.

I'll be showing you that language from scratch the entire quarter. If we had picked the old way up here, then we would have another language choice here called Objective-C that was the language that the old way was originally written in. But again, it's all Swift all the time in this course, so we're always going to have these buttons in these Swift settings here.

Last thing: regarding these switches down here, make sure they're all off for this first app, but we are later going to look at this core data thing. That's an object-oriented database. I probably am not going to have time to show you the testing framework in SwiftUI, but it's pretty darn amazing. It lets you test not just the backend code but also your UI to make sure that your UI is looking like it's supposed to.

But again, please, all of these off for the first version here, Memorize. When we hit next, now it just wants to know where are you going to put this thing in your file system?

### 建议项目存放位置
I strongly recommend putting it in your home directory in a folder called Developer. So all of your projects should be collecting over here in your home directory Developer.

This is the canonical(典型的) place to put it. You can see that Finder even puts a hammer icon on there. It recognizes this as a standard kind of folder.

Down here, we have the source control that I was talking about at the beginning where you're storing this stuff in repositories, and this is something we will talk about later in the quarter briefly.

Source control is good as an individual for versioning your app as you work on it but it's really valuable for teams.

When you're working on a project with teams, five programmers or something working on one app or even a hundred programmers working on one app, how do you not step on each other?

This whole source control thing provides a mechanism(机制) for checking out your code, making changes, checking it back in, making sure it doesn't conflict with what other programmers on your team have done, et cetera.

Again, we'll briefly talk about this later in the quarter but we definitely want this off to start. I say definitely, but I'm going to do it with it off.

So if you're following along, you might think that yours looks slightly different if you have it on. So let's leave that off and hit create and voila, it created our app for us.

### 进入 Xcode 界面
This is our first iOS app. Congratulations, you've built your first iOS app. This is the main screen of Xcode. You're going to spend all quarter long living here, so I'm going to spend some time talking about all the parts of this.

I'm going to start right up here at the top with this fun little combo of buttons. This is how you run your application.

#### 有关模拟器
So the first thing you do is pick where you want to run your application. That's this. Right now, it says iPad touch (7th generation). That's where it would run it if I ran it but I'm going to click on that, and you can see that I can choose to run it on an iOS device connected to my Mac (I don't have any connected right now) or I can run it in one of those great simulators that we saw. There's the iPhone 8 simulator, iPhone 11. We're going to run our app on the iPhone 12 mini, my favorite iPhone.

You just select where you want to run it and you just press this play button, and then when you're done, you press stop.

So play and stop. So let's go ahead and play.

It's going to launch this iPhone 12 mini simulator. There it is. Then it's going to install our app on it and it's going to run the app. There it is. It just says "Hello, world!". Now, those of you who were looking back here at our code probably saw that "Hello, world!" right there, and you were like "Hm, I bet this app says 'Hello, world!'"

And in fact it does say "Hello, world!".

That's what this app says. Otherwise, it's just big blank space. That's cool, we can do that and we can do things like rotate and it's nice. It keeps it automatically centered.

We're going to find that this thing where we rotate and our UI changes, we have to do very little code for that.

SwiftUI pretty much handles that for us,centering things properly and all that. Then when we're done simulating our app running right here, and again this is a full iPhone simulator. I can switch over and run settings over here and go back, switch back to my app, full simulation there.So when we're done, we press stop. It stops running.I have the menus hidden just to give us more space but obviously there's a lot of menus up here in Xcode and we will be using them.

Obviously as the quarter goes along you'll be learning them as we go.

It can be intimidating to see so many menu items with so many things, but again, we'll slowly unveil them.

It won't be quite too intimidating(令人生畏的) as all that. There's a little status wonder here that just tells you what's going on.Here, we just finished running Memorize.It'll say when it's compiling and all those things. 

#### 界面导航 Navigate 
Let's take a look at this blue area here on the left. This is called the navigator and it does what it says: it lets you navigate your application. It lets you navigate it in lots of different ways.

These little icons up here are letting you choose those different ways to navigate it and the default here is to navigate it by file. These are all the files that are in our application. These four files were created for us by Xcode, to get us started, and I'm going to actually look at all four of those in a moment.

But we can also navigate other ways by searching throughout our project or if we're debugging, we can look at all of our break points, et cetera.

We'll see these different ways of navigating as we go. All of the parts here can be resized. Just grab this with your mouse and you can make things bigger or smaller to allocate the space as you want.

You can also hide and show with this little button. A lot of times, once you're deep into doing some editing, you really don't need to switch back and forth between files here, especially because you're going to see tabs developing along the top here, like this thing that says ContentView.swift, where the files that you recently edited in are in tabs. So then you really don't need this as much, unless you're going to search or something like that.

#### 属性设置界面 Inspector
Now on the right, this area here, this gray thing is called the **Inspector**(检查员,督查).

I'm going to show you that a little bit later. In the center, this two paned thing here is the main editing window.

Usually you're going to have your code here on the left and you're going to have one or even more of these other ancillary(辅助的, 附属的) windows.

#### 预览界面 Previewer
This particular little space right here is very cool. This is the previewer. The previewer previews your UI. It actually shows you what your UI looks like without having to run it on the simulator, and it shows it to you, mostly, in real time.

It does pause occasionally. It says right here "Automatic preview updating paused" That's why we're not seeing our "Hello, world!" code over here show up.

But, we can resume it at any time with "Resume". When we resume, it essentially is like launching a little simulator in place right here.

We can zoom out a little bit and we see our UI. There's our little "Hello, world!" UI. We can divide the space up better if we want.

We're going to see this preview used as we're doing development.

#### 顶部导航栏
It's just always going to be previewing for us. It's a really powerful, really awesome system. Up here at the top, we also see there's a little line that's just saying where we are, specifically where our cursor is. If I click down here, it's actually saying we're in this body thing. If I click down here, it's saying we're in this ContentView_Previews thing.

You can even click on this and navigate around, jump your cursor around, jump it down to the bottom, jump it back up to the top, et cetera.

This is kind of where our cursor is up here.

#### 界面同步 preview-code editing-inspector
One thing that's cool about these three things here, the preview, our main code editing and this inspector, is they'll stay in sync. If I click on this line of code right here, it not only selects this thing that says Text("Hello, world!"), but it's selected that "Hello, world!" text thing with a blue line here and it made an inspector, some kind of UI over here, for inspecting or editing the attributes of this thing I have selected.

If I click away, then it stops selecting it here. Nothing has to be inspected. Click back. It's doing it.If I click away, I can also double clickin here and it'll select it here.Show me here and select it over here.

These things are linked.

They're always showing you, unless this thing is paused, they're always showing you what's in the other three panes. We can edit things or change things in any of these panes.

For example, we have "Hello, world!" here, what if we said "Hello, CS193p!" Look at that, it changed here and it changed up here. We could change it up here. We could say "Hello there, CS193p!"

Changed it here, changed it here. What was really cool is as I was editing it here, it was changing in here in real time and it will always do that as long as it's not paused.

If it gets paused then you're just going to say, resume, and it will continue.

This inspector over here is pretty powerful. It's not just changing the text. You can also change the font, font color, et cetera.

Here I even have some padding. You see this little blue dot says that my padding is on. Sure enough, you see this says padding right here, we're going to look at all this code in a bit here, but this little padding in here, if I turn this off, it takes that out of there.

Or if I turn it back on but only for vertical padding, then I get padding vertical.

Again, we're not worried about what all this means, but the point is that as we can change things over here, it's changing them over there.

That is your tour of Xcode. There is the debugger which comes up from the bottom. We'll see that in a little bit when we start doing some debugging.

You won't need to be using the debugger during this first week's lectures. The stuff I'm going to be asking you to do on the homework is very straightforward and will not require debugging.

### 项目初始文件介绍
Let's go back and do what I said and look at these four files that Xcode created for us when we created this project.

#### Assets.xcassets
We'll start with this one: Assets.xcassets When it says assets it means things like images, sounds, and videos, those kinds of assets.

What we do for that when we're building an iOS app is we drag the assets into here and we give them names.

In the white column here is going to be the names of the assets and then here is going to be the actual assets themselves. You will see the images showing up right here.

Some assets are more complicated than the others, like your app icon is quite a complicated asset because it has lots of different resolutions. These resolutions here are dependent on the environment, whether it's on an iPad or an iPhone or you are in the spotlight area, is it said a notification that just came in on your iPhone for that app, etc.

If you have an app, especially an app that you're shipping to the app store, you're probably going to have an artist or somebody make some perfect nice icons that look good at all of these resolutions.

We're not going to look at the assets more than this, but we will be using it later when we want to add images to our application.

#### Info.plist(在13版本的Xcode已经没有显示这个文件了)
What about this thing, Info.plist? This is essentially the settings of your app, but this is a pretty raw way to edit it and we usually don't edit this Info.plist directly. Instead, if we go up to our project and click on the project itself, we get a nice UI for editing these same settings right here.

And what kind of settings are we talking about? Well, does this app run on the iPhone? Yes. The iPad? Yes. Does it run on the Mac? No.

We're not building this Memorize app to run on the Mac. The next app that we do, we will have it run on the Mac. Also, are we deploying to iOS 14, iOS 13, iOS 11?

The farther back we tried to deploy(施展；部署), the fewer new features we get to use. All of this stuff, when you change them here in this nice UI switches and all that, it changes it in this list over here as well. We don't really look at our Info.plist hardly at all. We're almost always clicking up here if we want to change project settings and 99% of the time, you don't need to change any of these settings. They just default to the right thing. 

That leaves us with these two files right here. They're both .swift files, Swift language files. Swift is a new language that I'm going to be showing you from scratch.

#### MemorizeApp.swift
This one right here, MemorizeApp.swift, I'm not going to look too closely at that one. It really doesn't matter too much. Couple of things to note about it, it's our main program. In C, you have main.c which is the main C module where your app, when it runs, starts executing.

We have the same thing in Swift and this is it. Because we put this @main in here, this becomes our main program. We don't worry too much about all this. The main thing to note here is that this ContentView() that's in the middle is basically saying that this other Swift file, ContentView.swift, is the thing that describes what our app looks like.

#### ContentView.swift
When we go to our simulator over here and see our app, this whole area right here no matter which app we're talking about, is our ContentView.swift.

That's really all the main program is saying is what is the name of that main area? And that's this, ContentView.swift, so this code is the entirety of the code that makes this.

In fact, it's a little bit more than the entirety of the code. It's also got this little thing at the bottom ContentView_Previews.

This is the code that glues this previewer to our ContentView.

So really only this is the entirety of the code that draws our "Hello, world!" And this glue code, we hardly ever even touch this.

I'll show you a little bit later in this week's lecture, how we could modify this a little bit but most of the time we don't pay any attention. In fact, I usually like to just get it out of my way, so I don't even see it.

It's down there. It's doing the glue but I don't even look at it.

#### 关于 Preview 的使用
Notice, by the way, that when I made a big change like that, our previewer paused so I can hit resume and it'll continue.

Okay, that is it. That is your tour of Xcode.

Now we're going to focus in on these lines of code and understand what every line of code in here does.

I'm going to reset this "Hello, cs193p!" to "Hello, world!"

### ContentView.swift 代码讲解
Let's hide that and focus in on that ContentView right there, with that little bit out of the way.

#### import SwiftUI
Let's just go through this line by line. This top line: import SwiftUI.

This one's an easy one.

This is like include or import that's in other languages. We're basically just saying that this file is going to use the package Swift code called SwiftUI.

That's made by Apple and it ships with all iOS devices and on Mac OS and Apple Watch and all these things.

It's here because we're doing UI in this file, but not every file that we create is going to have UI.

For example, the files that we create that do the logic of our game, that actually match cards and keep score, that is not UI. That is logic and that will not be importing SwiftUI.

One of the great things about SwiftUI is how it clearly separates that logic from the UI.

But here, we're working on UI. We're not even going to start doing our game logic till next week, so this is all UI, so of course we want to import SwiftUI here.

#### 关于结构体
This is the entirety of our code that generates the UI and it's creating a data structure here. 

So **struct** is short for data structure, and most languages have structs. Structs are essentially collections of variables and C has this and pretty much all languages, they may not at call it struct, but they have some sort of collections of variables.
**结构体** 在其他编程语言中也有，它的本质是一堆变量的集合，其他语言中不一定也叫做「结构体」，但是一定会有类似变量集合的数据结构类型。

Swift's collection of variables is pretty powerful because not only can we have variables in our struct right here, in fact, here's a variable we're going to look at later, but we can also have functions. So, func foo, have some code in there, this is perfectly legal.

We will be looking at functions especially next week, but we actually don't need much in the way of functions to build this UI it turns out, but structs can have functions on them.

#### 面向对象编程 vs. 函数式编程
That might feel to a lot of you like object-oriented programming because object-oriented programming is some data variables encapsulated(装入胶囊 总结；扼要概括；囊括) together with the functionality on it. What we call methods in object-oriented programming.

And Swift does actually support object-oriented programming and we will even be using object-oriented programming especially to connect our logic to our UI. You'll see that next week.
Swift 支持面向对象编程，当我们在给我们的 UI 加逻辑的时候，总会用到面向对象编程。

However, nothing that you see this week is object-oriented programming.
然而，本周你看到的都不是面向对象的编程。

Structs in particular, even though they can have variables and functions on them, are not object-oriented things. They're not classes.

There's no inheritance or anything like that and structs have different things, that I'm just about to talk about, that lead to a kind of programming that we call functional programming.
结构体没有继承属性而有其他的一些特性，我们称之为函数式编程。

Swift supports both object-oriented programming and functional programming.

And we use the functional programming design model in the UI code that we built. We use the object-oriented design model to hook up our model, our kind of logic, to our UI.
我们在构建 UI 的时候，使用的是函数式编程，在把逻辑和 UI 关联在一起的时候，使用的是面向对象编程。

Today all the things we're talking about are functional programming. All right, we clearly don't need this function foo, not doing anything anyway.

#### ContentView: View
What's the next thing after struct?

Struct is a keyword. All our keywords, of course, in magenta here, easy to understand them.

Next word is ContentView. That is just the name of this data structure and this can be any name we want. This is our app we just created, it says, "Hello, world!"

It didn't really know we were going to build a Memorize app so it called this thing ContentView because it's essentially the contents of our entire app.

I'm going to leave it to that but down the road, we're probably going to rename this to something like MemorizeView or something a little more specific to what we do, but it's just a name of this structure, nothing special about it.

This is very special. This little :View, when you're defining a struct, means that this struct that we're creating behaves like a View.

I told you, this is functional programming and in functional programming the behavior of things, how things behave, is crucial.

Most of how a thing behaves is the functions that you can call on it that defines how it behaves. But even the storage, the data storage, functional programming says nothing about how data is actually stored. It can talk a little bit about what data there is and what data should be in this struct but it doesn't say how it should be stored, er it's stored in memory or calculated.
==疑惑点==


In that way it's very different from object-oriented programming because you're not encapsulating the storage with the methods on that storage, the functionality.

You're just talking about the functionality and describing the storage that might exist. You're not actually implementing it.


#### View 是什么？
When you say that you have a data structure that behaves like something, in this case behaves like a View, and we'll talk about what a View is in a minute here, that's really a double-edged sword(双刃剑).

One side of the sword is really great, which is that a View has a lot of functionality that's built into the SwiftUI library. As soon as you say, you behave like a View, you get all that functionality because Views do all those things and you behave like one so that's great.

The other side, the other edge of the sword is that you might have some responsibilities if you want to behave like a View. You can't just walk down the street and say, yeah, I behave like a View. Sometimes behaving like a View means you got to do some stuff too.

In fact, behaving like a View, even though it's hugely powerful, really only requires you to do one thing, which is to have this variable.

We're going to look at that variable and what that means in just a moment.

But first let's talk about what a View is. When we say that this data structure we're creating behaves like a View, what does that mean?Well, a View is just a rectangular area on screen.

This struct ContentView is this rectangular area. The corners are rounded here just because the device is rounding them off.

This large rectangle area is this View, ContentView, and a View has the capability to display things inside. Here we see it displaying some texts. That's good. It also can receive input from the user in the form of multi-touch events.

Taps, swipe, pinch, things like that. That's all a View is, really. It's just a way input and output in a rectangular area on screen.

Now that's simple in concept, but in implementation it's super powerful because we want to build very beautiful rectangular areas on screen.

Like for example, this where things are flipping over.

In this sort of View right here, we have this ContentView or this top level View, but there's also a View here, which is this text. This card is a View that's got multiple things on it. It's got this emoji. It's got this kind of rounded rectangle drawing around it. 

If we go look at a complicated thing here, we got all kinds of Views in here. That text, this smaller text, this little arrow right here, the whole thing where we can click on something and it goes to another View.

Those are all Views. Everything here, everything on screen, every rectangular area is a View.

You can see that some Views like these cards are embedded in larger views.

Views inside Views. This is kind of obvious, almost every UI system has this idea that there's rectangular areas on screen and you combine them to make your UI.

But in Swift we do it with this functional programming model and we say that we're building this ContentView that behaves like a View.

#### View 可以做什么？

What can a View do?

A ton of things.

We actually earlier saw something a View can do, which is it can be padded. We had this text here before. It had this little padding turned on and it got a little bigger, a little space around it. That's just one tiny thing. Look at all these other things up here.

Those are all things that views can do: set their color and all these things. We're going to see all of this and how we leverage(促使…改变) the power of the behavior of a View a little bit later.

But first I'm going to look at the flip side of View, which is this requirement that if we want to behave like a View, we have to implement this variable.

This is a great opportunity to talk about variables inside of a struct, inside of a data structure in Swift.

#### View 结构体里嵌套 body View 类型？

This is what it looks like to declare a variable, super simple.

Keyword var for variable, **body** is just the name of that variable.

**Then :some View, that's different than this one up here. :some View is the type of that variable.**
> 上面：是继承，这里的: 是数据类型说明

Now, this is a pretty complicated, not necessarily complicated, but an important kind of type. Tt's a little bit odd.

Normally the types will be very straightforward. Like var i is an Int. Or var s is a String. That's what most variables look like in Swift.

This one has this weird, some keyword in there, this some magenta keyword. Also, it's got this View thing which we know that a View is a behavioral thing.

So why is the type of this body variable, some View behavioral thing?

Well, it's kind of exactly how it reads. The type of this body is something that behaves like a View. That's what the type of this var body is.

Let's think about that.

That's kind of strange.

To create a data structure that behaves like a View, you are required to provide a variable whose type is some other thing that behaves like a View.

That's kind of strange. Here's an analogy that might make it make sense.

Why the requirement to behave like a View is that you have to have a variable that provides some other thing that behaves like a View.

#### 用LEGO类比View

That analogy is Lego. Hopefully, all of you have had the joy of playing with Legos in your life.

Legos are little blocks, little building blocks you use to build really cool things from a little tiny house, Lego house.

You can build the Lego Star Wars Super Star Destroyer and everywhere in between. So Legos are very powerful little building tools.

If you think of Views as being kind of like Lego, the analogy, it's not perfect, but it kind of works.

Let's think about a Lego. Let's say I wanted to build a Lego house. Okay, a Lego house has got all the rooms in it. It's got a kitchen. It's got the bedrooms. It's got bathrooms.

Let's say it's got a dining room. In each one of those, there's a
lot of other little sub-Legos in there. Like, the kitchen's got a bunch of kitchen cabinets and table and appliances.

The dining room has a dining room table and dining room chairs. You can see that the Lego house, we're actually building out of other Lego.

We can think of that Lego house as just a thousand pieces of Lego. But actually when we really build something like a Lego house, when we're building let's say the dining room, we build the little dining room table out of some Lego and then we built one dining room chair out of the Lego.

Then we are going to build another dining room chair and another dinning room chair exactly the same.

We might have, I don't know, eight dining room chairs around our dining room table and they're all exactly the same those dining room chairs.

So if we think of the dining room chair itself as a Lego, yes it's a Lego that we built out of other Legos by stacking them on top of each other and connecting them up, but once we've done that, it essentially become a dining room chair Lego.

Then we can take eight of those and combine them with a dining room table Lego and now we essentially have a dining room set Lego.

Then maybe we combine that with the rest of the furniture in the dining room, we have a dining room Lego. Then we put the dining room Lego together with the kitchen Lego and the bedroom Lego and the bathroom Lego, we put them all together, now we have a house Lego.

We can put that whole huge house Lego together with other house Legos to make a Lego neighborhood and Lego planet, the Lego universe.

We could build an entire universe out of Lego. If you think of it that way, you make the simple leap to say that a Lego dining room chair is itself a Lego, built out of other Lego, then that's how Views are created.

That's why it makes perfect sense that if you're going to behave like a View that you have to provide this body variable that is some other View.

Because we're going to be building Legos out of Legos. It's as simple as that.

To understand our analogy a little bit better, let's talk a little bit about the kinds of Views that you're going to find in SwiftUI.

Of course, you're going to find this kind of View: Text, which is like a Lego brick, a basic building block, stands on its own.

If we look in our UI, they are everywhere. Here and here and here. On the card, this emoji is just a string, a little Text.

So that's one clear kind of View. Similarly, we have these shapes like
rounded rectangle and circle and oval, and things like that, these basic shapes, those are Lego bricks as well.

But the real powerful Views that we're going to find in SwiftUI are the combiners, the Lego combiners. They're the things that take these other Views and combine them on screen.

Either arrange them in a grid, like this perhaps, or maybe in just a line across, stack them on top of each other, things like that.

Those kinds of combiner Views are probably the most important thing to making complicated user interfaces in this Lego model of piecing things together.

There is one other kind of View that I'm going to talk about, which is like if you want to use our Lego analogy, it's a bag of Lego. If you buy a very large Lego set that has thousands of pieces, let's say, Star Wars Millennium Falcon or something.

When you open the box, the people at Lego have very kindly grouped a lot of those thousands of pieces into little clear plastic bags, so that when you get to the part of the Millennium Falcon, let's say, the gun turret on the bottom or something, you don't have to search through thousands of pieces to find the pieces to build that.

There's a bag. There's the gun turret bag and you open it up and there's only a couple of hundred pieces in there to build that part.

So you don't build your Lego Millennium Falcon by just throwing the bag on top of it or sticking the bag in there somewhere. You open the bag and combine the Legos.

So, those last two kinds of Views I talked about, the combiners and the bag of Lego, they go together.

A combiner is obviously going to take a bag of Lego and open up and put it together.

Armed with that knowledge of the different kinds of Views, you're going to see that this var body is almost always going to be a combiner View.

In our case, right now, it's just a single Lego brick, this Text, but this some View is going to be a View that is a combiner View most of the time, the vast majority of the time. We'll get back to this some View syntax and what that really means in a second.

But first I want to talk about this little piece of code right here.
What is this? It's just kind of plopped in here right after this var body: some View.

This is actually a function and I told you that Swift is a functional programming language.

And in functional programming languages, functions are really, really important.In fact, functions are first class citizens and we can drop functions anywhere we want.

This is something that for some of you, maybe even programming Java or languages like that, having functions be things that are just plopped
right in the middle of your code might be slightly jarring but you're going to want to get used to it because in a functional programming language functions are everywhere.

They are just absolutely everywhere. This function happens to take no arguments right here and it has no name. It doesn't need a name because I just plopped it right in the code here.

This function actually returns something. It returns a Text, this Text. You might say, "well, where's the return statement?" There really is a return statement right there. It's kind of a hidden return statement right there. I'm going to leave it in there if I build under Command-B to build by the way, it says "Build succeeded". That return does belong there, it's just being hidden by Swift just to make the world look a little nicer.

We're going to see a lot of examples of Swift hiding extraneous keywords and things when it's kind of obvious what's going on there. It does that all the time to make our code look a little bit nicer.

This is a function with no name, takes no arguments. It returns in this case, a Text.

So what's it doing there? What is this function plopped right in the middle of the code, right after this var body? This var body is not actually stored in memory. It's not a variable stored in memory. It's actually a variable that's calculated by executing this function.

Every time someone asks this ContentView struct, "Hey, what's the value of your variable called body?" It executes this function and returns whatever it returns.

In this case, it's going to return this Lego brick, this text. A text, what is a text? A text is another struct that behaves like a View, the Lego brick I said, so it has to be that.

In other words, somewhere in SwiftUI there's something that says struct Text. It behaves like a View and it's probably got a var body. It's some View and inside there there's some code right there.

There's probably some code something like this, somewhere in Swift. Maybe not exactly like that, but something like that.

So, this is itself just something that behaves like a View. You've got a function here that returned something that behaves like a View and that's good because this var body is supposed to be a type that is some kind of View, something that behaves like a View.

So these match up. This function is returning something that matches the type of this variable.Of course, if you're going to have the value of a variable be set by plopping a function right in there and have it be executed, the types better match up, whatever this returns, better match up to this.

And it does in this case. It's great. In fact, this is going to help us understand what some View really turns into when our compiler is compiling this code. some View, it's not in and of itself a type.

It's more like some advice to the compiler saying, "Hey this variable's type is going to be some View. Please go figure out what it actually is and replace it with that when you compile it."

In this case, the compiler is going to look at this function, see that it returned a Text and it's going to essentially replace this with Text because that is its type.

And again, if I compile, succeeds!

Because this var body's type is Text. It's got a function, returns a Text.

#### 为什么使用 :some View(两个原因)

> 第一个原因没搞懂，和第二个原因不是一个意思么？不是说的因为ContentView 会越来越复杂，所以才是 some View

Why didn't we just say, var body: Text from the first place? Why did we do this weird some View? There's really two reasons for that. 

One, when we're trying to behave like a View, this View thing has to say what you have to do to behave like a View.

So it's not going to say, "Oh, you've got to provide a var body that's a Text." Because of course you could behave like a View and your var body could be some combiner view that's doing this whole UI over here. This entire UI in this is returned by the ContentView of this version of the app. Part of is just the declaration, just declaring that that's going on.

But another part of it is, we're going to make this code in here more and more complicated. It starts out as a single Lego brick, ends up being an entire game playing app. And then as it gets more and more complicated, the type of the thing that this returns is obviously going to get much more complicated and we don't want to have to figure out what it is exactly, or type it. We want the compiler to figure that out for us.

That's what compilers are good at looking at the code and bringing out what the types of things are. It's very, very good at that.

I can show you that very, very vividly by talking about something we already saw, which is padding. I clicked on my Text right here. That has brought back up and we can resume our preview here, brought back up, it's showing in the preview and also it brought this inspector back for us.

If you remember when we originally started this whole thing with this Text we went over here to this padding and we turned it off. It used to be a little blue dot there and we turned it off. I'm going to turn it back on. So, it's back on now with all the sides, see padding all right there.

Let's talk a little bit about what happened here when we turn this on and off. What is this line of code that got plopped in when we turned that back on? This is probably a little more understandable, if I move this onto the same line and you look at it like this.

First, let me explain that this padding is just a function that exists in all structs that behave like a View. So any struct like ContentView or like Text, anything that behaves like a View, it has a function on it called padding. This is how you call a function in Swift.

You just find the struct that you want to call the function on. If you're doing object-oriented programming in Swift then it's the object, an instance of the class.

Then you just say '.' and the name again. Hopefully very familiar to you, Java and other languages do this exactly the same way, and then if there are arguments then you just provide them here.

Swift arguments to functions, you're going to find to be very, very, very flexible. They can default. You can have different arguments that mean different things. For example, here, we have this .all and I will explain what things like that are later, but that means all of these here.

We saw that if I click some of these off now it's .horizontal, but it even has other things too. I can type a number here like padding(20). That means put 20 points of padding on every side or padding(100), put 100 on every side. **Or no arguments, which means just use default padding, which is a really good one to have because the default padding might be a little different on an Apple Watch vs. Apple TV vs. MacOS vs. iPad. So a lot of times we'd like to use the defaults of things because they're platform specific.**

But the point is we can put a lot of different things here in the arguments and it's the same function, padding, does the same thing.

It's just that you're providing different information to tell it to do what it does. This function, padding, returned something.

**This is really, really important to understand that this padding function returns something. What it returns is something that behaves like a View.**

**It's a different thing than this. This padding does not return a Text. It returns a padded, modified other View which happens to be a Text in this case.**

The actual type if I wanted to type it here, I could go to try and look it up and documentation, it's probably something like ModifiedContent, something, I don't know. Something complicated, but it's definitely not Text.

In fact, if I put Text here and hit build it says "Build Failed". Cannot convert this expression to type Text.

#### view modifier
Because this expression is not a Text, it's whatever kind of View .padding returns. It's really important to understand what's going on here, because we are going to be doing a lot of these kind of little functions that return a new View, a View that's different than another View. **They're called view modifiers, because they obviously modify some other View.**

In the Lego world, you can think of it as, we took this brick and we sent it back to the factory and said, "Send us a new one, please, that's padded a little bit around the sides of it."

That's essentially what happened and the factory quickly sent us back a new one and that is now the brick that we are using here.

So it is a modified Text.

**Every time we do a modifier here, it's going to essentially create a new View. That's why having this be some View, especially as this gets more and more complicated, is really valuable to us.**

We can see that even more if we add more modifiers because we can of course take these Views and modify them and modify them again.

Let's take our Text right here and change its color, for example. I'm going to have my Text selected here and over in my inspector, I'm just going to change, let's say, the color of the font to orange. It added another modifier here between that and the padding.

Let's see if it worked. It sure did. Now, we actually have three Views going on here. We've got this original View. We've got the View returned from this function, which is a Text modified to have its color be different, and then we have a View that's returned by taking that colored text thing and padding it.

It's this View that is returned as some View right there. You can see there's a lot of power here, creating exactly the kind of View we want with these modifiers, but really we're only still talking about taking a brick and modifying it.

A single Lego brick modified certainly is nice, but we need to be able to combine bricks. When we build something like this card right here, this is a combination of this rounded rectangle and a little emoji string right there on top of it.

Combining these, and then combining those into this grid and then combining it all into a big app, that's we want to do.

Let's focus here on making just a single card and using a combiner View to combine a rounded rectangle with the text on top of it, this emoji text on top.

#### 添加注释
To do that, I'm going to comment out my Text here for the moment. So I type Command-/ there. It's a great way to quickly comment things in and out, by the way.

You'll notice I got all kinds of errors: my preview can't biuld and all this. That's because I commented out the only thing in this function that returned some kind of View.

#### var body 返回值
This var body, this function that provides this value, has to return some kind of View.

Let's do that.

Let's have it return a RoundedRectangle. RoundedRectangle, another thing built into SwiftUI, it is a Lego brick. Notice that as you type, Xcode is always jumping in there trying to help you out. Here, it's helping me out with all the different ways that I can create a RoundedRectangle.

I can do it by specifying the corner radius or even the exact size, the width and height of the corners. I want this with corner radius, so I'm going to click here and sure enough, it filled out some default corner radius here, 25. There is a rectangle with corner radius. I'll click away so we can see it. There it is, looking nice, looking good.

Looks like a rounded rectangle to me.

#### 属性标签
But, a somewhat strange thing happened on the way to creating this rectangle that you haven't seen before. Here's my creation of a rectangle. Look at the arguments to create it, very different than what we had with Text or even the function calls we had like color.orange, this argument has a label.

Arguments with labels is very common in Swift. It might even be more common than not having argument labels. This Text doesn't have something like String because it's kind of like its argument is some text, so it's a little redundant(不需要的; 多余的).

Same thing here. Saying foreground color is color: orange, that's the word color too many times. By the way, you don't even need this Color because Swift is smart enough to know that you're passing a color, and so you can leave that Color out as well.

Swift doesn't like you typing the same thing over and over, color, color, color. But here, with RoundedRectangle, since I can create one by specifying the corner radius or by specifying the size, if I were just to say RoundedRectangle(25.0), it's just not clear enough what that 25.0 is.

So whenever you define your own function and the arguments, and it's not obvious what an argument would be, you want to define it with a label.

We're going to talk all about functions next week and how we declare them, how we make arguments, how we make them optional, all that business. And one of the things that we're going to see is we almost always put a label on our arguments. Really makes the code easier to read.

One of the best things that Swift inherited from its predecessor, Objective-C, is these nice labels. Of course I can change this to anything I want, I can also change it over here in the inspector.

We've got the RoundedRectangle over there. A RoundedRectangle is just a View. It behaves like a View. It's a Lego brick. So I could do things like padding and put some padding on it. Maybe I only want horizontal padding and it's going to do what I want. Make it match up in the inspector. It's all great there.

**RoundedRectangle is also a Shape. I told you that Lego bricks are Shapes, Circles and Rectangles, RoundedRectangles, Ovals, they're all Shapes. A Shape has one extra thing that it can do, which is that in addition to the Shape being filled in like this, you can just outline the Shape and you do that by saying .stroke** 

So if we put stroke on the end of something that is a Shape, then it will just do the outside edge. See the outside, only the outside edge right there which is what we want it to look like, when the cards face up anyway.

We want it filled when it's face down and stroked when it's face up. You can also do fill, that fills it in, but this is the default, so that's why we originally had this and it wasn't there at all.

Stroke is just a function that things that are a Shape understand.

So I can't stroke a Text. It's because a Text, while it's a View, is not a Shape, so it can't be stroked. But all things that are Shapes also are Views and that's why we can pad them.

The stroke also can have arguments that are optional. lineWidth: 3 makes this line a little bit thicker.

Notice this also has a label. **So these labels are not just in the creation of structs, they're also when you call functions.** Not all of them have it. Padding doesn't use a label and as we saw foregroundColor doesn't use a label, but some of them do.
属性标签不仅仅结构体有，函数的参数也会有标签。这里讲到这个地方是因为前面创建的矩形是一个结构体，而后面在这个结构体上使用了 stroke 函数。 

So we'll leave that in there just to remind you that that can happen. We could also do color. Maybe I want this RoundedRectangle to be some color, like maybe the red that we have over here, this red going on.

#### 搜索 modifier
So how do I make it red? Well, I'll just go over to my inspector, Oh no. In my inspector, there's no color. When I inspected a Text, it had the color there and I just picked the orange and I got this orange text right here. But that doesn't exist here.

So what am I going to do?

Well, what appears here is the most common things that people want to put in here. But everything that a View can do is available via this search field right here.

See where is says "Add Modifier", it's going to let you add any of the modifiers that don't appear here that you want.

If I click in here, you'll see that there are an awful lot of modifiers that Views know how to do. We are amazingly going to cover most of these by the end of the quarter.

But, right now, it looks kind of daunting, such a long list. How would you find what you want? Well, you can search in here by just typing for example, 'color', and this will show you the, looks like the seven things that a View can be modified to do related to color.

Like Color Invert would invert this probably turn this from black to white. But we know that we want this one, Foreground Color. When you select it, it actually did add it then as one of the sections here, Foreground Color. We don't want blue. We want it to be, let's say, red. So now we have the red border that we want there.

#### 规整代码
This is getting a little bit messy over here in that our code is wrapping, and it's like wrapping in the middle of a function call here.

This is why you're going to see a lot of times, these things put on their own line. So I'm going to put that on its own line, that on its own line, that on its own line, very common to do that.

We've gotten really good now at taking a basic Lego brick, like the RoundedRectangle or a Text, and modifying it to make it look the way that we want.

#### 关于 ZStack
If we look at these cards, it's just a combination of a RoundedRectangle and some Text. These emoji are just little Text strings.

So how do we combine these things? Well, we want to return some kind of View, which is a combiner, a View combiner like the Lego combine we were talking about before.

So, that's exactly what we're going to do. We're going to return a different kind of View called a ZStack.

I'm going to talk about in a moment here what a ZStack is all about. Let's get rid of our RoundedRectangle.

When we try to create a ZStack, do our little open parentheses, Xcode suggests two different versions.

One, which has some alignment argument and then content and another one that is just the content.

We'll talk about this alignment in a second, but the key argument to a ZStack is content.

So let's type this content argument. This is the label of this argument. And what kind of thing is it? Well, it turns out to be a function. Yes, functional programming strikes again.

#### View builder
This is a function and this function is actually going to return a bag of Lego. Remember the bag of Lego in our analogy, when we're building the Millennium Falcon, that's what we have to give the ZStack is this bag of Lego.

Swift knows that you're going to want to make these bags of Lego a lot and so it makes it really easy for you to do. It's really enhanced the concept of a function to be able to create a bag of Lego.

This kind of function that you pass to a Lego combiner view is called a **View builder**.

Essentially, it lets you list other Views in here and then it bags them up into a bag using this function right here and returns it so that the ZStack will have a bag of Lego to work on.

All we need to do is take these things that we've already built down here and just put them in here. We don't need return statements in here. We can just list them.

This is very strange function like syntax because there's no return statement involved here. This mechanism, this view builder mechanism, knows how to take this list of Views and actually combine them into another View which is a bag of Lego View.

The type of that other View, you don't really need to know what it is, but it's called TupleView. You're never going to be typing that in your code because you don't care. This happens for you automatically, this view building mechanism that creates bag of Lego, and you're gonna use it all the time.

You're going to be listing Views like this all the time. This bag of Lego is even more powerful than just listing the Views. You can also put if-then's in here. These bags of Lego can have conditional statements in them. You can even define variables in here. But there's really not much else you can do.

It's basically, list Views, use if then's to pick Which views you want to have in the bag of Lego, and then if you need to do some variables you can do that as well.

Notice that I've been arranging this in the background here. I had the texts have its things on separate lines as well, but I used indentation(缩进) so that when I look in this bag of Lego right here, that I'm giving to the Zstack, that the leftmost edge is lining up the actual Views and the modifiers are indented a little bit.

What is this ZStack thing going to do with this bag of Lego that we passed it? Well, a ZStack stacks these views on top of each other from the device out towards the user.

Exactly what we want, right? When we're building this card, there's this kind of background of the card and then on top of it is this nice string right here, which is the emoji. So it's stacking them towards us.

There are other combiners that stack things horizontally and other ones that stack them vertically and other ones that stack them in a grid like this.

So we're just starting with the first one which is building the card but when we want to have multiple cards we're going to start using some of those other Lego combiners to combine them in different way.

You can see it actually already worked, background card and then here is our "Hello, world!". What we've built here is actually going to be a sum View which is a ZStack that contains a RoundedRectangle and a Text.

This is not simply ZStack because the type of the ZStack includes the type of the things that are included in it.

So that doesn't really work to say ZStack. We'll let it build. You'll see that won't allow that to happen.

That's again, why we need some View. We build this complicated collection of Views that are combined with the ZStack, we want to let the compiler figure out the complicated type that's involved here.

So we never type the type with some View we always just let some View get calculated for us. 

#### 再谈 modifier
I want to talk a little bit about these modifiers that we have on these.

Right now, we have the modifiers on here, each as we want it, but let's talk about what it means to put a modifier on one of these view combiners.

It's really kind of two different categories of things that you want to put on a ZStack.

One of them might be padding. Currently we have padding on this rectangle, we also have padding on the Text. You can see there's padding around the Text. We currently don't actually need padding around the Text. There's no reason to have this padding around the Text.

So if we take it off and we resume, it doesn't really change the way things work. We also have padding on the RoundedRectangle, which we kind of want because we don't want it to be over near the edge right here. But we could put this padding on the ZStack itself.

So if I take this padding off of here and put it down here, I'm now doing this padding function on this ZStack that I created. And remember ZStack is just a View, it behaves like a View, therefore it has that function padding, it can be padded as well, and it looks like nothing has changed.

By putting that padding on here everything looks the same, but there is a subtle difference. Watch this. If I click on the rectangle, you see the blue line that defined where the rectangle is, it's no longer padded.

So there's no padding on the rectangle. If I click on the Zstack, that's where you can see the padding. The blue line goes all the way to the edge right there.

View modifiers like padding work perfectly fine on something like a ZStack. There's no difference really between a ZStack and a RoundedRectangle and a Text, in the sense that they're all just Views, so they can all of course be padded.

#### 关于覆盖 view 的属性
But there are other kinds of modifiers that are a little interesting when it comes to a view combiner. Let's take for example, foregroundColor.

Let's take the foregroundColor off of each of our Lego bricks in her and put it on the ZStack instead.

Look what happened over there. I put this on here and everything inside the ZStack turned red. The text turned red and the rectangles turned red.

So what does it mean to say the foreground color of a combiner is red?

The combiner itself doesn't actually draw anything. It combines other things that draw, namely the Rectangle and the Text. So this kind of modifier gets passed on to all the things inside. Putting .foregroundColor(.red) on the ZStack is exactly the same as putting it here and putting it here separately.

This is only though the default color, if you put it out here on the ZStack. If I still wanted my text to be orange I could still say .foregroundColor(.orange) and my text would turn orange.

So that is allowed. This is going to be a foreground color of it. This is the default that it's inheriting from its container. And remember, we're eventually going to have containers inside containers, inside containers as we build these complicated views and the awesome thing is they'll pass their colors down the chain to each of the levels.

So, if this whole grid of cards is red, we're probably going to set the foregroundColor to red at the very top level.

At the grid, we're going to set that to be the foregroundColor of the grid and all the things inside, including all these cards, are going to inherit that color. Unless they want to override it, they get that color.

Before we move along here, I actually want to clean up my code a little bit. Remember we talked about how Swift doesn't like you to have a lot of extraneous stuff.

For example, foregroundColor(Color.orange), we could leave this Color off because Swift can figure out what's going on there. We also know that this return up here, not needed. This is a function, we know it returns some sort of View.

The compiler can look in here and see that there's only really this one line of code. This looks like multiple lines of code but really it's one thing.

It's a modified Zstack. It's the only thing that's in this function so it knows to return this one thing, especially since it matches some View right there. So we don't need that.

But there's some other stuff we don't need here as well.

This argument to Zstack, ZStack only takes one argument. It could take another argument by the way.

Let's put it in here, alignment. For example, top. That's still stacking these two things on top of each other, the "Hello, world!" and the RoundedRectangle around it, but it's aligning them so they're stuck up at the top instead of the default alignment, which is center.

Let's get rid of our orange texts, we want it to all be red.

This argument right here, content, its value is a function, one of these special **view builder** functions right here that wraps this up into a bag of Lego but is still a function.

#### 关于最后一个参数是函数的省略写法
Any time you have a creation of a struct or even calling a function and you're passing an argument whose value is a function, then as long as it's one of the last arguments, it can be removed from being inside the parentheses We have this (alignment: .center) and now I've got this function just kind of hanging out on the edge. It's very similar to this function, hanging out on the edge and this body thing right here.

We can just leave this like this. Why do we do that? Why does Swift allow you to just have this last argument? And you can also do the last couple arguments if they're both functions. Why do we have it hanging out outside of the list of parameters?

It's purely for looks. It's purely because it looks nice and it's even nicer if you don't have another argument or you're just not going to use that argument.

In this case, you can get rid of the parentheses as well. Now you have this beautiful little code here that says, Oh, I got a ZStack on these two things. We're always going to do this. No one ever types, content: this thing. They will all just leave that off. If we want to put the alignment in there, that's fine. We can go back and put alignment in, but if we're not doing that, we just always do this.

A lot of people dive right into SwiftUI and they start with this and they don't really even understand what's going on here, but **this is just a function that's an argument to ZStack, is the content argument to ZStack, and it's a special function because it's a view builder where you can just list views and it packages them up for you.**

But it's still nothing more than that. We're going to stick to our pre-pandemic lecture schedule which is to have two 80-minute lectures.

So I'm going to stop here and we'll start off next time by continuing this demo and creating multiple cards and making them look a little better, make them scroll around a little bit, adding some buttons, etc.

For more, please visit us@stanford.edu.