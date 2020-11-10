# Notes 

## Strongbox 

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

## Windows Trouble 
A lot of open source projects do not contain information on developing in a windows environment. Build tools can heavily rely on bash scripts and other Unix/Linuz features. Oftentimes, documentation will point out what do to differently for Mac, but disregard windows. In the case of Airflow, its build tool breeze relies on Docker. Breeze requires Docker running on [WSL 2](https://docs.microsoft.com/en-us/windows/wsl/about) (Windows Subsystems for Linux), which allows windows user to directly run on a Linux within Windows.

### Issues I encountered
* Installed Docker with WSL 2 but my Ubuntu Terminal was running WSL 1.
How to fix: 
1. Run `wsl --list --verbose` on powershell to see what version each emulator is running and verify that it is running a different version than docker. 
2. Identify the name of the linux terminal you are using. For me, this is Ubuntu. 
3. Run `wsl --set-version Ubuntu 2` to upgrade Ubuntu's WSL version. 