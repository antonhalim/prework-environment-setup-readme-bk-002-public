# Setup

## Welcome to Ironboard

You'll be using Ironboard (the site you're on right now), to go through the prework. You'll be also using this software while at school too. Ironboard works to deliver content to our students sequentially, and give instructions on how to complete assignments. It's also a communication tool: if you're ever seriously stuck and need help, or want to report something broken (a bug), click the "Need Help" button on the right hand side of any page, and it will get sent to us.

You'll find a few different types of assignments here in Ironboard in the prework track: readmes, assessments, and links to outside resources. When you're finished with an assignment, whether it's something here or linked externally, or a challenge that requires you to submit a pull request on Github (more on that later), click "Next Lesson" at the bottom to move to the next one. Also you can always toggle the left menu bar to see all of the topics, units, and lessons for the Prework Track.

### Accounts

To complete some of these lessons, primarily bonus resources, you will need [Treehouse](http://teamtreehouse.com/) and [CodeSchool](http://www.codeschool.com/) accounts. Both have free trials. 

At this point, you'll have already signed up for [Github](https://github.com/). However, to make our lives easier, be sure to have your name on your account. Go to Settings, and in your Public Profile, add your name. Go ahead and add a picture too; that helps!

## Basic Environment Setup

We're going to spend more time on this and in more depth when the semester begins, but in order to complete certain assignments here on Ironboard, you need do some very basic environment setup on your computer.

**Go through each of these sections carefully and in order and make sure you read all of the instructions.**

**Note:** this environment setup is all you need to do. If you come across any other configuration setup in any of the outside resources (like on Code School or Treehouse), don't do it.

### Operating System

Make sure you are using OSX 10.10 Yosemite. To check, click on the  in the menu bar and select "About This Mac" The version should be 10.10 or greater. If your version of OSX is below 10.10, update your Mac through the Mac App Store.

### Xcode / Command Line Tools / GCC

Download Xcode from the Mac App Store. If you already have Xcode installed, make sure there are no updates available in the Mac App Store. Once XCode is downloaded and up to date, open it and follow any instructions. You should now have the apple commandline tools installed. **Make sure you open Xcode. You need to accept Apple's terms and conditions before doing anytihng else.**

Most OS level programs are written in C or C++. These programs must be compiled and interpreted by a C-level compiler. The most common compiler for [POSIX](http://en.wikipedia.org/wiki/POSIX) systems is [GCC](http://en.wikipedia.org/wiki/GNU_Compiler_Collection), or the GNU Compiler Collection.

To test and see if you installed command line tools correctly, type `gcc` into terminal.

If you see output like this: 

```bash
clang: error: no input files
```
you installed it correctly.

If you see output like this:
```bash
Agreeing to the Xcode/iOS licence requires admin privileges, please re-run as root via sudo.
```
You probably need to open Xcode and accept the licence terms from Apple. 

### Homebrew

[Homebrew](http://brew.sh/.) is an awesome package manager, and makes downloading lots of software really easy. Download Homebrew by entering:

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Once downloading is complete, you'll want to enter `brew doctor` to make sure you don't have any conflicts. If there are some warnings, that's okay.

### Git

We're going to be going over git in way more depth later, but for now, know that git is a free and open source distributed version control system. Version control systems are used to manage saving colaborating on software. 

Your computer should ship with an earlier version of git.

Open up Terminal, and type:

`git version`

You should see an output like this:

`git version 1.9.3`

To update the version, enter `brew install git`.

Once the download is complete, you'll want to open a new terminal tab, and reenter `git version` to compare and see if we have a new version number.

### RVM

Next comes setting up our ruby version manager, which will handle ruby versions and gems, which are packages of code we can use in our programs. OS X ships with an old version of ruby so we want a more recent one. Install [RVM](http://rvm.io/) by typing this into your Terminal:

`\curl -L https://get.rvm.io | bash -s stable --ruby=2.1.4`

That will install the latest stable version of RVM along with the latest stable version of ruby 2.1.4. Then type `rvm use 2.1.4 --default` to make that your default ruby. Open a new tab and `try ruby -v` and see if it matches the installed version of ruby. You can install another version of ruby with `rvm install 2.1.3` and see all installable rubies with `rvm list known`.

### The Ironboard Gem

Now that we have RVM and XCode installed, let's install our first gem.

This gem isn't open-sourced, so we won't be downloading it from [RubyGems.org](https://rubygems.org/), which is where most gems are hosted. Before we download it, we will need to specify where it's coming from, which is a private server at Flatiron. Type this into your command line;

`gem sources -a http://flatiron:33west26@gems.flatironschool.com/`

Next, download the gem:

`gem install ironboard`

The ironboard gem will allow us to run the tests for challenges and labs. It's based off of [RSpec](https://www.relishapp.com/rspec), a popular testing framework in Ruby, but it does a bit more like help track your progress on labs.

Go ahead and install RSpec too: `gem install rspec`

Normally when we run our tests, we would type `rspec`, but to run the tests for challenges and labs, you'll type `ironboard` into your command line instead, within the root directory of the challenge/lab.

### Sublime Text

Sublime Text 3 is our favorite text editor for writing code. You can download it [here](http://www.sublimetext.com/3). You want to make sure you select the OSX version. You'll want to make sure that Sublime Text 3 is in the Applications directory on your computer.

One thing you should think about adding to your Sublime is [Package Control](https://sublime.wbond.net/installation). Follow the instructions in the link to install the Package Control. You can then download packages like [HTML snippets](https://sublime.wbond.net/packages/HTML%20Snippets), which allows you to autocomplete HTML tags as you type them. Follow [these instructions](http://www.granneman.com/webdev/editors/sublime-text/packages/how-to-install-and-use-package-control/) on how to install sublime packages.
