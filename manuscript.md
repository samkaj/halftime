# Presentation

## Intro

## The Problem

Slides.

## Our Task

Slides.

## Some Background

Before we get into it, let's go through some background to understand some fundamental basics of this project. The first thing you need to be aware of is JMH, a benchmarking framework for Java which is used to measure your projects' performance.

Secondly, our bot is implemented as a GitHub App, which is a service provided by GitHub to send updates to repositories on GitHub via an API. This enables the developer to integrate with GitHub in their recommended way.

We will also make use of MongoDB, a NoSQL, document-based database as a persistence layer for our data. A lot of you may be familiar with SQL, and the difference here is that we save our data in JSON-like objects, rather than tables, which provides flexibility when saving unstructured data.

## The Plan

To solve our aforementioned problem of the lack of CI tooling in the perfomance benchmarking space, we have devised the following plan:

-   We will listen for projects who want to use the bot by being subscribed to events sent by GitHub using their GitHub Apps API. These requests contain a project with instructions on how to run performance benchmarks.
-   The Performance Bot delegates work to a worker, which will run the benchmarks
-   The results from the benchmark is sent from the worker back to our performance bot, which saves them to the database
-   Once saved, results are historically analysed
-   Once analysed, the data is formatted and visualised before finally sent back to the repository in the form of an issue, making the developer aware of potential performance drops or improvements in the code change.

## Progress and Continuation

Onto the state of the project as it is! We a kind of workflow MVP ready for use. The workflow works as previously described in the plan, which is listening for webhooks, running tests in containers, storing the results in the database as well as posting an issue on the Github page of the repo that has the bot installed.

Everything is barebones, displaying raw data of test results, only works on repos using Maven and runs all tests in the repo. Therefore, the steps coming up include presenting the data of our analysis in a comprehensive way. What kind of analysis this will contain is in need of consideration.

We also need configurability. Whether this involves choosing what kind of analysis is displayed remains to be seen, but what the bot definitely needs is the ability to run on different build tools, such as Maven, Gradle or custom made build tools. We also need to implement the ability to choose which tests should be ran, as performance testing is a very resource heavy and time consuming task.

## Scientific Relevancy and our Thesis

Creating an open source framework that can be installed via Github will hopefully lead to less work on the side of developers wanting to run preformance tests on their product. Eliminating unnecessary work is therefore one of the key aspects of our contribution to the software community, either because they install the bot to their program or create their own variant to suit their needs.

Even if the bot doesn't apply to a specific product, it can act as inspiration for developer when it comes to setting up git bots and CI. Often times looking at projects similar to your own is the best way of understanding how you solve certain problems.

There's also the opportunity for further work to be done on the git bot, as the open-source nature makes it ever-developable. We also aim to get a strong object oriented structure for the project, allowing further extension. Open sourcing makes it possible for anyone to contribute changes which is good considering that we are a small team only focusing on Java at the moment. If someone wants to make it possible for other languages, we have the API provided.

## Evaluation ideas

Another aspect that needs to be solved going forward is how exactly we, and more importantly, the examiner, will be able to decide if the project is successful or not? This is something we have yet to set in stone, and have only discussed briefly, but we have some fundamental ideas.

Essential to the project is its ability to run on projects implementing JMH tests, and what better way to test this than to use it on large Java JMH projects to see if there are any issues. How this will work in detail is still undecided.

Last but not least, consulting our supervisor and the faculty is essential to moving the project forward, as they are as close to stakeholders as we're gonna get in this project.

## Some experiences

To conclude, we will go through some of our personal experiences working on the project. It poses the challenge of grasping a relatively large stack, demanding a lot of learning. Every group member has come into contact with frameworks they haven't worked with before.

This learning process has been tackled in different ways, but one thing that has been made clear is the importance of learning by doing. You can spend an almost infinite amount of time learning about a framework, and in the end you won't know what you have use of learning before you encounter a problem.
