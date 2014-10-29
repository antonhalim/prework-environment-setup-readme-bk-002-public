# Setup

## Welcome to Ironboard

You'll be using Ironboard (the site you're on right now), to go through the prework. You'll be also using this software while at school too. Ironboard works to deliver content to our students sequentially, and give instructions on how to complete assignments. It's also a communication tool: if you're ever seriously stuck and need help, or want to report something broken (a bug), click the "Need Help" button on the right hand side of any page, and it will get sent to us.

You'll find a few different types of assignments here in Ironboard in the prework track: readmes, assessments, and links to outside resources. When you're finished with an assignment, whether it's something here or linked externally, or a challenge that requires you to submit a pull request on Github (more on that later), click "Next Lesson" at the bottom to move to the next one. Also you can always toggle the left menu bar to see all of the topics, units, and lessons for the Prework Track.

### Accounts

To complete these lessons, you will need [Treehouse](http://teamtreehouse.com/)
and [CodeSchool](http://www.codeschool.com/enrollments/dnFtaXFMbXROSVVqT3N1bngwWnBRUjhGc2k1Z1dEOW52cFJvZEMzRUZvRT0tLWpvUElMODBvdFhiZlA4MjE2Mlc2c1E9PQ==)
accounts. 

We will provide you with an account to treehouse and codeschool, feel free to use your own to get started, but we cover those costs for the duration of the prework and semester.

Sign up for [Github](https://github.com/) as well, which is free. To make our lives easier, be sure to have your name on your account. Go to Settings, and in your Public Profile, add your name.

## Basic Environment Setup

We're going to spend more time on this and in more depth when the semester begins, but in order to complete certain assignments here on Ironboard, you need do some very basic environment setup on your computer.

**Go through each of these sections carefully and in order and make sure you read all of the instructions.**

**Note:** this environment setup is all you need to do. If you come across any other configuration setup in any of the outside resources (like on Code School or Treehouse), don't do it.

### Operating System

Make sure you are using OSX 10.9 Mavericks. To check, click on the  in the menu bar and select "About This Mac" The version should be 10.9.5 or greater. If your version of OSX is below 10.9.5, update your Mac through the Mac App Store.

### XCode / Command Line Tools / GCC

Download the Command Line Tools from Apple's developer website, or if you don't have an Apple developer account, you can download the command line tools [here](http://flatiron-school.s3.amazonaws.com/software/command_line_tools_os_x_mavericks_for_xcode__late_october_2013.dmg).

Most OS level programs are written in C or C++. These programs must be compiled and interpreted by a C-level compiler. The most common compiler for POSIX systems is GCC, or the GNU Compiler Collection. On OS 10.8 and below (anything before Mavericks), GCC is part of the command line tools.

To test and see if you installed command line tools correctly, type `gcc` into terminal.

If you see output like this you installed it correctly.

 ```
clang: error: no input files
```

### Homebrew

[Homebrew](http://brew.sh/.) is an awesome package manager, and makes downloading lots of software really easy. Download Homebrew by entering:

```
ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
```

Once downloading is complete, you'll want to enter `brew doctor` to make sure you don't have any conflicts. If there are some warnings, that's okay.

### Git

We're going to be going over git in way more depth later, but for now know that git is a free and open source distributed version control system.

Your computer should ship with an earlier version of git.

Open up Terminal, and type:

`git version`

You should see an output like this:

`git version 1.9.1`

To update the version, enter `brew install git`.

Once the download is complete, you'll want to open a new terminal tab, and reenter `git version` to compare and see if we have a new version number.

### RVM

Next comes setting up our ruby version manager, which will handle ruby versions and gems, which are packages of code we can use in our programs. OS X ships with an old version of ruby so we want a more recent one. Read about RVM and then install [RVM](http://rvm.io/) by typing this into your Terminal:

`\curl -L https://get.rvm.io | bash -s stable --ruby=2.1.2`

That will install the latest stable version of RVM along with the latest stable version of ruby 2.1.2. Then type `rvm use 2.1.2 --default` to make that your default ruby. Open a new tab and `try ruby -v` and see if it matches the installed version of ruby. You can install another version of ruby with `rvm install 2.1.1` and see all installable rubies with `rvm list known`.

### Ironboard Gem

Now that we have RVM installed, let's install our first gem.

`gem install ironboard`

The ironboard gem will allow us to run the tests for challenges and labs. It's based off of [RSpec](https://www.relishapp.com/rspec), a popular testing framework in Ruby, but it does a bit more like help track your progress on labs.

Go ahead and install RSpec too: `gem install rspec`

To run the tests for challenges and labs, you'll type `ironboard` into your command line within the root directory of the challenge/lab.

### Sublime Text

Sublime Text 2 is our favorite text editor for writing code. You can download it [here](http://www.sublimetext.com/2). You want to make sure you select the OSX version. You'll want to make sure that Sublime Text 2 is in the Applications directory on your computer.
