January 5, 2018  
Brunswick, Maine

# What is Meteor Mogul?

Meteor Mogul is a hobby project for learning [Meteor][meteor], [VueJS][vue] and [Bootstrap](https://getbootstrap.com/) to create apps for friends and family.

The goal of the project (at this point) is just to make it easier for new developers to test out writing apps using VueJS with Meteor and Bootstrap.

There are four major front-end frameworks that can work with Meteor:

1. [Blaze](http://blazejs.org/)
2. [React](https://reactjs.org/)
3. [Angular](https://angular.io/)
4. [VueJS][vue]

VueJS is easy to learn and has momentum going for it.  Unfortunately, it can be a bit tricky to get working in Meteor since it is not part of the official build.  (At least, I found it tricky to get it working.)

That's where Meteor Mogul comes in.  You can clone our simple sample apps and quickly see how VueJS can work with Meteor.

I added Bootstrap to the mix to make my apps look a little nicer.

## Current Status of Meteor Mogul: Alpha

Four simple sample apps are working:

1. [Hello, world!](https://github.com/meteor-mogul/mogul-helloworld)
2. [Meteor Mogul Button Click](https://github.com/meteor-mogul/mogul-button)
3. [Meteor Mogul Meteor Vue To Do](https://github.com/meteor-mogul/mogul-meteor-vue-todo)
4. [Meteor Mogul Vue Intro](https://github.com/meteor-mogul/vue-intro)

I'm a neophyte at both VueJS and Meteor, so I'm just happy these apps are working.  I've already learned a lot writing them.

Once I have wrapped my mind around how other people are integrating VueJS with Meteor, and have some reasonable hope that I'm on the right track, I'll bump the status to beta, post an announcement somewhere, and invite random strangers to give me feedback and ideas.

## Getting Started

A preliminary note:  

> If you have Windows 10, you'll probably notice when you start playing
> with Meteor that everything comes to a grinding halt unless you turn off
> Windows Defender real-time scanning.  I don't want to recommend doing that,
> just putting it out there.
>
> If you can score a Mac or a linux machine to develop on, your time invested
> will be more rewarding.  The Meteor development toolchain is way better on
> MacOS or Linux than on Windows.

To start playing with Meteor Mogul, here's what you need:

1. Either MacOS or linux (easier and faster for developing with Meteor Mogul) or Windows 10 (harder and slower for developing with Meteor Mogul).
2. An [evergreen web browser](http://eisenbergeffect.bluespire.com/evergreen-browsers/). I recommend [Google Chrome](https://www.google.com/chrome/browser/).
3. A programming editor. I recommend [Atom](https://atom.io/).
4. [Meteor][meteor]
5. [git](https://git-scm.com/)

I also recommend that you try out [GitHub Desktop](https://desktop.github.com/). I find that it helps me manage commits without having to remember `git` shell commands.

Once you have all the above, you'll need to practice a little bit to know how to use them.  Then the following instructions will make sense.

Here's how to try out our simple sample apps.

First, from a shell, clone the app you want to try, e.g.

```
$ git clone https://github.com/meteor-mogul/mogul-meteor-vue-todo.git <target-dir>
```

Then do the following:

```
$ cd <target-dir>
$ meteor npm install
$ meteor
```

If you forget the `meteor npm install` you'll probably see error messages letting you know that you need to install the `babel-runtime` node package.  The `meteor npm install` just has to happen once, but it's okay to run it multiple times.

By default, `meteor` will launch a web application server listening to port 3000. You can play with your sample app by pointing a browser at [http://localhost:3000](http://localhost:3000).

## Under the Hood

The main thing Meteor Mogul does is provide the latest version of VueJS as a Meteor package (`meteormogul:vue-dist`) on [Atmosphere](https://atmospherejs.com/meteormogul) and removes the Blaze package.  So then when you write your `.html` files, vue.js takes over and deals with them instead.

There are [other projects](https://github.com/meteor-vue) which are aiming for a more robust integration of VueJS with Meteor.  Those other projects allow you to write both blaze and vue templates.

The ambition of Meteor Mogul is more modest: it's here just to help you quickly get writing apps that use VueJS as the front-end and can use MongoDB and the other things on the back end that Meteor provides.

In the future I may try the following:

1. Re-writing some of the most useful Meteor packages (such as the accounts system) to work with VueJS.
2. Helping other people (especially people new to coding) learn to write apps using Meteor and VueJS.

My main motivation is to learn by doing.  I have been toying with Meteor over the years and noticed that VueJS seems to be taking off, so I wanted to play around with it, too.

I hope Meteor Mogul saves you some time if you're interested in seeing what it's like to develop apps with VueJS and Meteor together.

Have fun!  

*\-Fred*

[vue]: https://vuejs.org/
[meteor]: https://www.meteor.com/
