# Open Source Student Guide 

Welcome! This is a guide geared towards university students with little industry experience but want to contributed to open source. I will be drawing from my experience in contributing to o
pen source without have any prior experience.  

## Help! I don't how know to code.

There are two main ways to make non-code contributions to open source.
    1) Improve Documentation
    2) Report Issues

However, to make these contributions, you must be an active user of the project. So, if you don't know how to code and considered contributing to open source as a way to learn, 
I suggest doing this instead:
    1) Choose a open source product you want to use.
    2) Come up with a project that incorperates that open source project 
    3) Learn the neccesary programming laguages and technologies to complete the project.
    4) Make open source contributions based on the struggles you encounter using the tools.

Even if you know how to code, there's still a lot of benefits in going this route. By being a user of the product, you have more context on what improvements the project needs 
and will have an easier time onboarding as a contributer to the project. In fact, most people contribute to per source projects that they use in their day-to-day 


## I know how to code but I want real world experience. 

### How to find a project 

1. Choose something you know.
       I tried to contribute to was [XWiki](https://www.xwiki.org/xwiki/bin/view/Main/WebHome). I choose the project because it felt beginner friendly and had well written documentation. What I failed to consider  is that it's in the field of web development and I knew nothing about web development. I remember staring at the XML, wondering what it all does. First I thought, it would be easy to learn. I know 5 programming languages and no longer found the act of learning another language difficult. However, what I didn't realize at the time was that I didn't know how the web development stack was organized, how all of the components interacted with each other. In the end, I wrote a comment under the [issue](https://jira.xwiki.org/browse/XWIKI-6267) saying 
        
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
 
 1. Avoid Windows if you can. Seriously.   
   
   [Here](https://opensource.com/article/18/5/dual-boot-linux) is an article on how to dual boot Linux on a PC. If you have a really cheap PC with horrible specs like me, there’s not much you can do: you will have to suffer through Windows. Here are a few rules for developing on a windows laptop. 
            1)	Install WSL2 with Ubuntu. This allows you to run linux commands on your windows laptop. 
            2)	Accept that you will have worse performance. 
    The reason for this is that most onboarding guides are made for a Unix/Linux system. They may provide commands meant to run in a Unix/Linux system and you will need to figure out on your own how to set up windows. On the bright side, you can make a contribution of a onboarding guide for windows. 


