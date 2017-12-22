December 22, 2017  
Brunswick, Maine

# Meteor Mogul

Meteor Mogul is a hobby project for learning [Meteor][meteor], [VueJS][vue] and [Bootstrap](https://getbootstrap.com/) to create apps for friends and family.

The goal of the project (at this point) is just to make it easier for new developers to test out writing apps using VueJS with Meteor.

There are four major front-end frameworks that can work with Meteor:

1. [Blaze](http://blazejs.org/)
2. [React](https://reactjs.org/)
3. [Angular](https://angular.io/)
4. [VueJS][vue]

VueJS is easy to learn and has momentum going for it among hobbyists.  Unfortunately, it can be a bit tricky to get working in Meteor since it is not part of the official build.

That's where Meteor Mogul comes in.  You can clone our simple sample apps and quickly see what it's like to develop an app using VueJS with Meteor.

## Current Status of Meteor Mogul: Alpha

Two simple sample apps are working:

1. [https://github.com/meteor-mogul/mogul-helloworld](https://github.com/meteor-mogul/mogul-helloworld)
2. [https://github.com/meteor-mogul/mogul-meteor-vue-todo](https://github.com/meteor-mogul/mogul-meteor-vue-todo)

## Getting Started

A preliminary note:  

> If you have Windows 10, you'll probably notice when you start playing
> with Meteor that everything comes to a grinding halt unless you turn off
> Windows Defender real-time scanning.  I don't want to recommend doing that,
> just putting it out there.

If you can score a Mac or a linux machine to develop on, your time invested will be more rewarding.  The Meteor development toolchain is way better on MacOS or Linux than on Windows. Once you've developed an app, you can run it from a browser on any system.

To start playing with Meteor Mogul, here's what you need:

1. Either MacOS or linux (easier and faster for developing with Meteor Mogul) or Windows 10 (harder and slower for developing with Meteor Mogul).
2. An evergreen web browser. I recommend Google Chrome.
3. A programming editor. I recommend [Atom](https://atom.io/).
4. [Meteor][meteor]
5. [GitHub Desktop](https://desktop.github.com/) or `git`.

Once you have all the above, you'll need to practice a little bit to know how to use them.  Then the following instructions will make sense.

Here's how to try out our simple sample apps.

First, clone the app you want to try, e.g.
```
$ git clone https://github.com/meteor-mogul/mogul-meteor-vue-todo.git target-dir
```

Then do the following:

```
$ cd target-dir
$ meteor npm install
$ meteor
```

If you forget the `meteor npm install` you'll probably see error messages letting you know that you need to install the `babel-runtime` node package.  The `meteor npm install` just has to happen once, but it's okay to run it multiple times.

## Under the Hood

The main thing meteor-mogul does is provide the latest version of VueJS as a Meteor package and removes the Blaze package.  So then when you write your `.html` files, vue.js takes over and deals with them instead.

There are other projects which are aiming for a more robust integration of VueJS with Meteor.  Those other projects allow you to write both blaze and vue templates.

The ambition of `meteor-mogul` is more modest: it's here just to help you quickly get writing apps that use VueJS as the front-end and can use MongoDB and the other things on the back end that Meteor provides.

Any Meteor package that needs Blaze to run (and that's most of them that have a client interface) won't work with `meteor-mogul`.

In the future I may try re-writing some of the most useful Meteor packages (such as the accounts system) to work with VueJS.

Have fun! I hope this saves you some time if you're interested in seeing what it's like to develop apps with VueJS and Meteor together.

*\-Fred*

[vue]: https://vuejs.org/
[meteor]: https://www.meteor.com/
