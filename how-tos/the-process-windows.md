# The Process: Windows

## Can I Skip This Explanation?

If you took 1502 with Tyson in the Fall, you might be OK. But still...I'd go through all of this anyway.

## In a Nutshell

There is a process that you will follow to complete all your drills, assignments, coding topic tests, and the coding portion of the final exam. 

Here's what you need to do:

1. accept an assignment (GitHub Classroom, which we will use, calls _everything_ an assignment)
2. cloning the assignment from its GitHub repository (aka repo) to your local machine
3. import the assignment into Eclipse
4. complete the assignment
5. push your changes back to the GitHub repo
6. "submit" the results of your work via GitHub
 
> _Because these assessments make up **50% of your final grade**, it's in your best interest to be comfortable with this process._

## Detailed Explanation

> _The following steps are demonstrated in this video [33:47]: https://youtu.be/Yq3WWxqnogs_  
>   
> _Though you **can** just jump to the different steps in the video - that's why I have the time links in the steps below - I like to think I **do** say some useful stuff throughout the video that you might miss if you just jump around. Maybe it's best just to play the video at double-speed if you're in a hurry?_

### Before We Start

Make sure you have completed the steps laid out in these how-tos first: 

1. [Creating a GitHub Account & Making a Private Repo](github-account.md)
2. Installing Git ([Windows](installing-git-windows.md) or [Mac](installing-git-mac.md))
3. Installing JDK, Eclipse, and plugins ([Windows](installing-jdk-eclipse-windows.md) or [Mac](installing-jdk-eclipse-mac.md))

It will also be useful if you're **logged into GitHub** and **have Eclipse open, with all projects there closed**.

### The Steps

#### Accepting an Assignment

1. [[01:50]](https://youtu.be/Yq3WWxqnogs?t=110) for drills, you can start the process over in the [Drill Checkpoints page](https://github.com/MRU-CSIS-2503-202101-001/course-resources/blob/main/drill-checkpoints.md) that's accessible through our [course resources wiki](https://github.com/MRU-CSIS-2503-202101-001/course-resources/wiki/Comp2503---Winter-2021) and go to the instructions for the drill you want to do
   
2. [[04:02]](https://youtu.be/Yq3WWxqnogs?t=242) drills will have a link that lets you accept the drill, so click on that and follow the on-screen instructions to go through the acceptance procedure.

    > _Note_  
    > _In the video, you don't see the authentication verification that GitHub asks you when you connect to GitHub Classroom for the first time. Just accept it if it does appear. Also, the "...but something went wrong...." message seen when I accept the assignment was there because of a change I had recently done to that drill - you shouldn't see that disturbing message when you do your accepting!_
    
3. [[05:45]](https://youtu.be/Yq3WWxqnogs?t=345) after refreshing the page when directed, you can go to the **second link** - the one underneath `Then, access your assignment:` - on the resulting page

    > _Note_  
    > _You'll also receive an email which confusingly gives you a way to accept the assignment...that you just accepted! Weird. You can safely delete these emails._
    

#### Cloning to Local Machine

1. [[09:33]](https://youtu.be/Yq3WWxqnogs?t=573) go to the location where you want to have the drill contents saved (likely your Eclipse workplace folder) and open up a Git Bash window there (using right-click > `Git Bash here`)

2. [[10:43]](https://youtu.be/Yq3WWxqnogs?t=643) copy the GitHub location using the `Code` button back on the GitHub repo page

3. [[11:08]](https://youtu.be/Yq3WWxqnogs?t=668) enter the following command in the Git window:

    ```bash
    git clone [location you copied]
    ```

    > _Note_  
    > _Remember that you can't Ctrl+V in this window - you'll either have to right-click or use the Shift+Insert keyboard shortcut here instead._
    
    > _Note 2_  
    > _Because I had done something behind the scenes before this screencast, I had to go through the GitHub authentication procedure again...you shouldn't have that trouble, though. I babble a lot at this point in the 'cast - sorry._


#### Importing into Eclipse

1. [[14:22]](https://youtu.be/Yq3WWxqnogs?t=862) import the folder into Eclipse by going `File` > `Import` > `General` > `Existing Projects into Workspace`

2. [[15:00]](https://youtu.be/Yq3WWxqnogs?t=900) select the folder that you cloned earlier and click `Finish`


#### (Some Eclipse Suggestions)

[[15:19]](https://youtu.be/Yq3WWxqnogs?t=919) A variety of things happen from this point, including:

- how to run - and re-run - tests
- how to easily compare what tests want versus what your code provides
- how to get to ToDo items easily
- what PMD and Checkstyle warnings look like

#### Pushing Back to GitHub

1. [[24:14]](https://youtu.be/Yq3WWxqnogs?t=1454) open up a new Git window in our Eclipse project folder

2. [[24:42]](https://youtu.be/Yq3WWxqnogs?t=1482) issue the Trinity of commands to get our work up to GitHub:

    ```bash
    git add --all
    git commit -m "Submit or some message"
    git push
    ```

3. [[26:38]](https://youtu.be/Yq3WWxqnogs?t=1598) be paranoid and check to make sure the changes got to GitHub by looking at the timestamp and message on the `src` directory back on the repository's page in GitHub

#### Submitting Results

1. [[28:41]](https://youtu.be/Yq3WWxqnogs?t=1721) head to the Actions tab in the repository page on GitHub

2. [[28:50]](https://youtu.be/Yq3WWxqnogs?t=1730) choose `Submit this assessment`, then click the `Run workflow` dropdown, enter your **MRU USERNAME** (not your GitHub username, or your "real" name), and finally click `Run workflow`

3. Wait for the workflow to complete....it usually takes about 60 to 90 seconds.

4. [[30:30]](https://youtu.be/Yq3WWxqnogs?t=1730) hopefully, you'll have a green checkmark by your build

5. [[31:21]](https://youtu.be/Yq3WWxqnogs?t=1881) go to the `Issues` tab and select the most recent report - hopefully, you'll see there were no issues!