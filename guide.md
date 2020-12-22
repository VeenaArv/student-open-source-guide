# Open Source Student Guide 

Welcome! This is a guide geared towards university students with little industry experience but want to contributed to open source. I will be drawing from my experience in contributing to open source without have any prior experience.  

## Help! I don't how know to code.

There are two main ways to make non-code contributions to open source.
  1) Improve Documentation
  2) Report Issues

However, to make these contributions, you must be an active user of the project. So, if you don't know how to code and want to contribute to open source as a way to learn, 
I suggest doing this instead:
  1) Choose a open source product you want to use.
  2) Come up with a project that incorperates that open source project 
  3) Learn the neccesary programming laguages and technologies to complete the project.
  4) Make open source contributions based on the struggles you encounter using the tools.

Even if you know how to code, there's still a lot of benefits in going this route. By being a user of the product, you have more context on what improvements the project needs 
and will have an easier time onboarding as a contributer to the project. In fact, most people contribute to per source projects that they use in their day-to-day 


## I know how to code but I want real world experience. 

### How to find a project 

1. Pick a language/framework you are familiar with
      
      I tried to contribute to was [XWiki](https://www.xwiki.org/xwiki/bin/view/Main/WebHome). I choose the project because it felt beginner friendly and had well written documentation. I tried to start on a code issue for XWiki called "Trim Server Name Aliases" It seemed like a good easy first contribution. The difficult level was trivial and the label was onboarding. Perfect! I am onboaring. So I sent a message through Jira, the project's issue tracker, and the maintainer responded with "Please do pick it up!" So, I opened the code and was greeted by XML. Shoot. I don't know XML. It's okay, I reassured myself. I've dealt with having to write code for programming languages I haven't experienced before. So, I tried to understand the file only to realize I have no idea how web development files are stored. I have no idea where to start. I remember staring at the XML, wondering what it all does. What I didn't realize at the time was that I didn't know how the web development stack was organized, how all of the components interacted with each other. In the end, I wrote a comment under the [issue](https://jira.xwiki.org/browse/XWIKI-6267) saying 
        
        Hi, I'm no longer working on this issue since it doesn't align with my skills. If anyone else wants to pick it up, feel free to!.

    From this mistake, I realized I needed to work with something I feel comfortable with. I choose `Airflow,` a workflow management platform for data eengineering. I had used a similar tool called Luigi in my previous intership and I knew that many of the concepts will be transferable. 

    What if I don't konw if I have enough experience for the project I choose? 
       1. Read the docs to attain a high level understand of the product.
       1. Look through the codebase If what you're reading feels familiar to you or if can understand how the code follows from the docs on a high level (don't worry about the details), you should be in good shape.

    If you're still on the fence, I recoomend following the instructions in the `Help! I don't know how to code` section. As an example, for this [project](https://github.com/VeenaArv/covid-hate-speech)
    I used Maven to manage my java dependencies. After finishing that project, I feel confortable with the concepts and the goals of the project unlike before I used it. 

 1. Make sure you understand the build requirements.
 
    In my journey, the very first project I choose to contribute to was [Strongbox](https://strongbox.github.io/) I choose the project because the project is intended to be a learning exercise and specifically tries to be student friendly. However, Strongbox had a hardware requirement of SSD, 16 GB RAM and i7 processor or the equivalent. Since my laptop has only 8 GM RM and an i5 processor, I chatted the maintainers to ask if I could still work on the project. The maintainers said that with my machine, build times will be very long (over 30 min) which will kill beginner enthusiasm.  
 
 1. Look at engagement of issues. 
 
    * How quickly do the maintainers respond? 
    * What percentage of issues get picked up? 
    * Are there any google labels for newbies on issues such as `good-first-issue` or `onboarding`?
    * How does the members of the open source project communicate? Mailing lists? Slack? IRC? What is the response rate? 
    * How do they respond to newcomer questions?

 ### Once you find a project

1. Join the relevant mailing lists/chats/issue trackers.

    Contributing to open source requires a lot of communication and you can always reach out to other contributors if you feel you need help. I had done this for Strongbox when my build was not working. Turns out I mistakingly glossed over specific Maven version requirement and was politely told to pay better attention to the doc. 

1. If you have not used the product before, learn it. 

    I had chosen to contribute to Airflow becuase I experience with Airflow's competitor, Luigi (also an open source project) and felt that those skills would be transferable. 

    Before starting to contribute to open source, it is best to have a good understanding of the project you work on, at least at a high level. I used to take the approach where I tried to dive into contributing (not just in open source) and try to figure stuff out along the way. I've recently learned that it is much better to learn the project and the organization of the codebase before making any contributions, even documentation related ones.

    How to pick the best resources for learning?

      1. **Know their audience.** For example, an Airflow tutorial geared towards data scientists will assume little coding knowledge with one geared towards data engineers will assume that you already know all the jargon in data engineering. 
      2. **Know your learning style.**  Depending on your learning style, you can learn about the project through [videos](https://www.youtube.com/watch?v=YWtfU0MQZ_4), [documentation](https://airflow.readthedocs.io/en/latest/tutorial.html), or [blogs](https://towardsdatascience.com/data-pipelines-luigi-airflow-everything-you-need-to-know-18dc741449b7). Oftentimes, its best to have a combination of all three. 
      3. **Know if you are in over your head.** If you find yourself googling every other word or in a field that you have never worked in or studied, it might be a good idea to revaluate your open source project. It is a lot easier and more fulfiling to work on a project that uses concepts you already know. For example, if you have never heard of a data pipeline or have any idea how to build one, Airflow might not be the project for you.   
      4. **Don't sweat the details.** The goal of learning about the open source project is to provide yourself with a baseline of knowledge to become productive quickly. When you start working on issues, you can learn the concepts needed for that issue more in depth without wasting your time learning everything. 

1. Read Onboarding Docs/ Set up your build environment.
     
   **Avoid Windows if you can. Seriously.**  
       
   [Here](https://opensource.com/article/18/5/dual-boot-linux) is an article on how to dual boot Linux on a PC. If you have a really cheap PC with horrible specs like me, there’s not much you can do: you will have to suffer through Windows. Here are a few rules for developing on a windows laptop. 
            1)	Install WSL2 with Ubuntu. This allows you to run linux commands on your windows laptop. 
            2)	Accept that you will have worse performance. 
    The reason for this is that most onboarding guides are made for a Unix/Linux system. They may provide commands meant to run in a Unix/Linux system and you will need to figure out on your own how to set up windows. On the bright side, you can make a contribution of a onboarding guide for windows. 

    **Mentoring programs**:
    
    Some open source projects such as Apache projects have mentoring programing to help you better integrate yourself into the project and the community. 
    [Apache Mentoring program](https://community.apache.org/mentoringprogramme.html): As a mentee you must devolop a plan and show that you are making a serious time commitment and effort towards the project. Anyone can be a mentee and you will find a mentor by submitting your proposal to the apache mailing lists. Here is a link to the program [application](https://community.apache.org/mentorprogrammeapplication.html). The only caveat is that mentors will not teach technical skills required to complete the project and they expect mentees to have the techincal skills beforehand. 


1. Make Non Code Contributions first

    One of the first things I learned is that despite your technical proficiency, making non-code contributions specifically documentation  is the best way to learn and explore an open source project. Here is an issue that I picked up for Airflow and how I went about documenting it.

    [Documenting TaskGroup vs SubDag](https://github.com/apache/airflow/issues/12298)
    I commented on Issue to ask to pick it up and asked a clarifying question on where the documentation should go. 

    I looked at design docs/ issues for the feature that is being documented. A feature is only created if there is a use case for it and the original design doc is the best place to learn the use case. [Design doc for TaskGroup](https://cwiki.apache.org/confluence/display/AIRFLOW/AIP-34+TaskGroup%3A+A+UI+task+grouping+concept+as+an+alternative+to+SubDagOperator). 

    Here is my [PR](https://github.com/apache/airflow/pull/12741) in progress.

    Sometimes you choose to document a issue only to find out that the issue has already been fixed. Here is an example of one I found for [XWiki](https://jira.xwiki.org/browse/XINFRA-32) If that is the case, alert the maintainer and provide the link of the exact location where the issue was solved. That is also considered an open source contribution! 

1. Make Code Contributions 

    Finally, you're here! At this point, you have the experience to confidently work on code contributions. You might make some misteps like having a failing build that you don't know how to fix, but with some good communication with the ope source comminity, you should be in tip top shape. 

