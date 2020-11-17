# Notes 

## [Strongbox](https://github.com/strongbox/strongbox/) 

Strongbox had a hardware requirement of SSD, 16 GB RAM and i7 processor or the equivalent. The maintainers said that with a worse machine, build times will be very long which will
kill beginner enthusiam. I joined chat to ask maintainers questions, mistakingly glossed over specific Maven version requirement and was politely told to pay better attention to
the doc. I had thought version were minimum requirements, but some projects only support a specific version adn have not upgraded to support newer versions.

All in all, strongbox was a fail since my laptop did not meet thier hardware requirements and I need to find a different project


## XWiki 

XWiki has a quickstart VM for making one-time contributions. It has extensive docs and tags goodfirstissue. 

### Chats
I'm having trouble understanding the method of comunications. XWiki uses Riot as a bridge to IRC but apparenlty it's read only and I need to register my username to get access? 
I'll look into it later but for now, I want to see how the community communications and delegates tasks. I subscribed to the development mailing list.

### Jira 
issue tracking is done via [Jira](https://jira.xwiki.org/secure/Dashboard.jspa)

## Code vs Non Code Contributions 

One of the first things I learned is that despite your technical proficiency, making non-code contributions is the best way to learn and explore an open source project. I had intially tried to start on a code issue for XWiki called "Trim Server Name Aliases" It seemed like a good easy first contribution. The difficult level was trivial and the label was onboarding. Perfect! I am onboaring. So I sent a message through Jira, the project's issue tracker, and the maintainer responded with "Please do pick it up!" So, I opened the code and was greeted by XML. Shoot. I don't know XML. It's okay, I reassured myself. I've dealt with having to write code for programming languages I haven't experienced before. So, I tried to understand the file only to realize I have no idea how web development files are stored. I have no idea where to start. Lesson #1: Pick a language/framework you are familiar with. Lesson #2: Don't code, document instead. 

## [Airflow](https://github.com/apache/airflow)

### Learning Airflow
While I have never used airflow before this, I have used Airflow's competitor, Luigi (also an open source project). Before starting to contribute to open source, it is best to have a good understanding of the project oyu work on, at least at a high level. I used to take the approach where I tried to dive into contributing (not just in open soucre) and try to figure stuff out along the way. I've recently learned that it is much better to learn the project and the organization of the codebase before making any contributions, even documentation related ones.

How to pick the best resources for learning? 
1. Know their audience. For example, an Airflow tutorial geared towards data scientists will assume little coding knowledge with one geared towards data engineers will assume that you already know all the jargon in data engineering. 
2. Know your learning style.  Depending on your learning style, you can learn about the project through [videos](https://www.youtube.com/watch?v=YWtfU0MQZ_4), [documentation](https://airflow.readthedocs.io/en/latest/tutorial.html), or [blogs](https://towardsdatascience.com/data-pipelines-luigi-airflow-everything-you-need-to-know-18dc741449b7). Oftentimes, its best to have a combination of all three. 
3. Know if you are in over your head. If you find yourself googling every other word or in a field that you have never worked in or studied, it might be a good idea to revaluate your open source project. It is a lot easier and more fulfiling to work on a project that uses concepts you already know. For example, if you have never heard of a data pipeline or have any idea how to build one, Airflow might not be the project for you.   
4. Don't sweat the details. The goal of learning about the open source project is to provide yourself with a baseline of knowledge to become productive quickly. When you start working on issues, you can learn the concepts needed for that issue more in depth without wasting your time learning everything. 


Here is a list of resources I used to learn Airflow:


### Windows Trouble 
A lot of open source projects do not contain information on developing in a windows environment. Build tools can heavily rely on bash scripts and other Unix/Linuz features. Oftentimes, documentation will point out what do to differently for Mac, but disregard windows. In the case of Airflow, its build tool breeze relies on Docker. Breeze requires Docker running on [WSL 2](https://docs.microsoft.com/en-us/windows/wsl/about) (Windows Subsystems for Linux), which allows windows user to directly run on a Linux within Windows.

### Issues I encountered
* Installed Docker with WSL 2 but my Ubuntu Terminal was running WSL 1.
How to fix: 
1. Run `wsl --list --verbose` on powershell to see what version each emulator is running and verify that it is running a different version than docker. 
2. Identify the name of the linux terminal you are using. For me, this is Ubuntu. 
3. Run `wsl --set-version Ubuntu 2` to upgrade Ubuntu's WSL version. 

After fixing this, docker still did not work; however, after restarting my machine, the docker container was started up. To verify this, open docker desktop and see that the container is running. 

### Contributions 
Airflow uses github issues to track thier issues. Apache as a whole uses Jira as an issue tracker, but in the Airflow documentation, they suggested to look at open issues on github. While an organization as a whole might have certain standard practices, each project may have it's own practices as well. 

Searched issues on [github](https://github.com/apache/airflow/labels/good%20first%20issue) with label `good first issue`

### [Documenting TaskGroup vs SubDag](https://github.com/apache/airflow/issues/12298)
Commented on Issue to ask to pick it up. Asked a clarifying question on where the documentation should go. 
Lessons: 
* Look at design docs/ issues for the feature that is being documented. A feature is only created if there is a use case for it and the original design doc is the best place to learn the use case. [Design doc for TaskGroup](https://cwiki.apache.org/confluence/display/AIRFLOW/AIP-34+TaskGroup%3A+A+UI+task+grouping+concept+as+an+alternative+to+SubDagOperator)
