---
title: How to see the code for every stage of the compilation process?
subtitle:
date: 2018-08-07
bigimg: [{src: "/img/postimg/", desc: "Coding"}]
tags: ["programming"]
---
## The Compilation Process in C/C++

Knowing how your code compiles can be very helpful when writing and debugging it.

Compiling a C/C++ program is a multi-stage process.

The complete compilation process in C/C++ can be split into four separate stages:  

  1. Preprocessing
  2. Compilation
  3. Assembly
  4. Linking

![Entire Compilation Process](/img/compilation.png)

By using appropriate compiler options, we can stop this process at any stage. These options are passed as command line parameters.

In the following examples, I will be using the **C++ programming language** to write the code and **g++ compiler** to compile it. However, these commands can be easily implemented with a program written in the **C programming language** and compiled in **gcc compiler**.

As an example, the code below is apt for understanding this.

```
/*
Name : div.cc

Program to check divisibility by 2 */

#include<iostream>

using namespace std;

int main()
{
	int x;

	cin >> x;

	if (x % 2 == 0)
	{
		cout << "Divisible" << endl;
	}

	else
	{
		cout << "Not Divisible" << endl;
	}
}
```
It is a simple program that asks the user for an input and expects an integer (int) type constant. It prints _Divisible_ on the screen if the number is divisible by 2 and _Not Divisible_ otherwise.

## Preprocessing
The C++ preprocessor copies the contents of the included header files into the source code file (#include), expands macros, and replaces constants defined using #define with their values. It also removes comments from the main code.

A new source file is created that contains code from our program as well as the header files and this is what is used as input to the further stages for the compilation to be declared complete.

We can stop at this stage and see the output by using **“-E”** flag in gcc or g++.

In g++:
`g++ -E div.cc`

GitHub also provides further details like the number of repositories, frequency of contributions activities, starred repositories, and the number of followers/followings can also reflect how passionate the owner is about programming. Most famous programmers are quite active on GitHub. In the end, job candidates who take the time to develop their GitHub profile and participate actively in the community can be better evaluated than others.

## Get Started
0. Install Git-SCM (Recommended) or GitHub Desktop Client (Not Recommended).

1. Create a GitHub account and add some of your projects to it, don't worry if you do not have any, you can always go to other's project and **fork** theirs.

2. Once you have a repository in your GitHub profile, you can experiment with it, **clone** it to your local machine, make changes to it and **commit** those changes, and then **push** the changes you made. Then create a **Pull Request** to the original author and request a **merge**. Like this, you can easily get started with using Git and GitHub

3. All your repositories, contributions, and activities will be shown on the profile homepage on [www.github.com/your_username].

#### Resources for Learning Git -
- Git Hello World - [GitHub Guides](https://guides.github.com/activities/hello-world/)
- Resources to learn Git - [try.github.io](https://try.github.io/)
- A Beginner’s Git and GitHub Tutorial - [Udacity](https://blog.udacity.com/2015/06/a-beginners-git-github-tutorial.html)
- Basic Git Concepts - [Dy Classroom](https://www.dyclassroom.com/git/git-basic-concepts)
- Getting Git Right - [Atlassian](https://www.atlassian.com/git)
- Learn the workings of Git, not just the commands - [IBM](https://www.ibm.com/developerworks/library/d-learn-workings-git/index.html)

## Getting it Right
GitHub was never designed as a place where programmers primarily exhibit their code to impress potential employers. It’s always been mainly a software development platform, the purpose of which is to make software development more efficient. If you're mentioning it on your resume, be sure you get it right.


### 1. **How often do you code**
Your GitHub profile shows your coding consistency right at the profile page! (_see above images_)
New programmers have less commits and activities, in short, overall git **contributions**. A more experienced user has more contributions. The darker the green square is, the more they contributed that day. And it is _relative_, this means that initially even one contribution is shown as dark green square, but as you contribute more and more, even 20+ contributions might be shown as a light green square depending upon the frequency of your contributions.


![Git Contributions](/img/github-contri2.JPG)

![Git Details](/img/git-detail.JPG)


### 2. **Maintain your repositories**  
Whenever you are working on something interesting, you can just put it to GitHub. It can be an algorithm you are just practicing writing, a piece of code or even a logo design you are working on. It serves as a backup for your work and you can access it from anywhere using the internet. Also, you can collaborate with others.

If you don’t know what to put on your GitHub, here are some suggestions:

- **Side Projects** - Working on a hobby or personal side project? Let others see and review it.
- **Course Projects** - You can also put up your projects on GitHub and mention the link on your project report. Ex - **ByteCode** was a course project for Semester-4 Database Management Systems - Project Based Learning (PBL) Lab.
- **Open Source Projects** - Contribute to open source projects, **fork** them and they will show up as your repository, you can also **star** them for later review, or **watch** them for any changes.


### 3. **Keep your code clean**
Nobody tells you this because it is obvious. If you write bad code, it will not only waste other's time in understanding your code but it means that you are inexperienced and not capable of developing software in a team. If your code is dirty, chances are you yourself will be looking at it, having no idea what it does, after some time of writing it. Comment appropriately.

You can follow Google style guide for [Java](https://google.github.io/styleguide/javaguide.html), [C++](https://google.github.io/styleguide/cppguide.html) and [Python](https://github.com/google/styleguide/blob/gh-pages/pyguide.md), which are very popular amongst professional developers.

Follow the proper directory structure to ease the process of locating the required files. See Folder Structure Conventions [here](https://github.com/kriasoft/Folder-Structure-Conventions).

### 4. **Be Professional in communication**
Whether you are writing comments in your code or explaining the changes you made while making a Pull Request, you need to be clear and precise in what you want to convey to other developers and coders.

- **Write clear descriptions** - Everybody reads the description. No one will read your code to understand what you are working on. Something like this -

![GitHub Description](/img/github-desc.JPG)

- **Always include a well-formatted README file** - It’s highly recommended to have a README for every repository, it has detailed instructions in it on how to use the contents of your repository, resources, links and sometimes a list of contributors. Include screenshots in it. Nobody has the time to install the application just to see it. As an example, you can see [this](https://github.com/abhishekarya1/cluster-image-classifier-tensorflow/blob/master/README.md).

- **Use Issues to track bugs** - You can use **GitHub Issues** to keep track of all the bugs. It makes a catalog of all known features and organizes them in a very intuitive manner, which makes it easier for reference to others in the later stages of development. To give you an idea, Open and resolved/unresolved issues are displayed separately in a chronological fashion. Below is a screenshot of the issue page for [Vue.js](https://github.com/vuejs) -

![GitHub Comm1](/img/github-issues.JPG)

### 5. **Avoid too many forks**
Forking a repository and letting it sit unmodified is a big no-no. You can star the repository if you are just browsing its content. Even if you fork, make sure that the repository does not stay unmodified for a long period, if it does, just delete it. Every forked repository has a _"forked from"_ original source indicator link just below the repository name.

![GitHub Comm1](/img/github-fork.JPG)

### 6. **Have some finished projects**
They don't have to be something extravagant. Just build one from what you know, even a small app or a webpage is enough. It shows that you can ship code on time and you can explain your code in a nicely written README file.


### 7.**Pinned Repositories**
Pinned repositories which appear at the top of your profile are by default your most frequently accessed repositories. It should be a showcase for your most impressive ones. Use the **Pinned Repositories** feature to

![Pinned Repositories](/img/pinned-repos.JPG)


### 8. **Test Cases**
In 2018, if your project doesn't have unit tests you should hide it. It's a bad practice and it reflects poorly on you. It is a sign that everything works perfectly and nothing is hardcoded into the code.

How to Write Test Cases: Sample Template with Examples - [Guru99](https://www.guru99.com/test-case.html).


### 9. **Meaningful Commits**
Your commits should be meaningful. After all, they are there for keeping track of all _meaningful_ changes you made to your project. Commit after small incremental features or fixes with a clear description of what was changed.


### 10. **Keep Contributing and Exploring**
Explore popular repositories on [Explore · GitHub](https://www.github.com/explore) and keep looking, you can always find projects that might pique your curiosity.

![GitHub Trending Repositories](/img/github-trending.JPG)
![GitHub Popular Topics](/img/github-pop.JPG)
![GitHub Events](/img/github-events.JPG)

Keep contributing to an organization and you might be granted a membership for it, where you can manage projects and merge requests for them.

![GitHub Organization Member](/img/github-org.JPG)

## What GitHub does not tell you?

Don't go around judging people from their GitHub profile. It is possible for someone to have 10+ years of experience and still their GitHub looks empty. The clients they work with can choose to have the code behind closed doors.

Not everybody likes and has the time to contribute to the open source community. A person not active on GitHub doesn't mean that he is a bad developer. Maybe they don't like to show their work to others.

Some programmers use GitHub as a way to back up their code, some want to collaborate, others just want a hosted page for their projects and documents, etc. Some projects may be well-documented and useful software, others could be experiments or code you could hardly call software. In the end, all that you see is not always useful in a GitHub profile. And most importantly, what if you decide to keep your projects private. Unlike open source projects and contributions, these won't be visible to your recruiter.

## To sum it up

Keep in mind that GitHub may not be as important in hiring as it totally depends upon the kind of recruiter you are looking at. They may look at it or they may just ignore it.

The real value of GitHub is that it confirms people are passionate about what they do as an occupation (because they contribute or commit to other projects while in the office or not). Sure, being good at coding is one thing, but being passionate and good is another.

Yet, in spite of its shortcomings, you can use your GitHub profile as a leverage to score a great new job. With only a bit of effort, you can make it more self-explanatory and recruiter-friendly. And if you're a student like me, then your open-source contributions will definitely play in your favor.

Want to talk? Just drop me a mail @[AbhishekArya](mailto:abhishekarya102@gmail.com) and I'll be happy to talk to you.
