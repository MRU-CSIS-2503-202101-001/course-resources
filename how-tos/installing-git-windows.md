# Installing Git: Windows

## Can I Skip This Explanation?

If you're comfortable running Git commands from a command line interface on your computer, then sure!

## In a Nutshell

We want to be able to do two things "easily" (realizing that with Git, this is a relative term):

1. clone repositories on GitHub to local repositories on your machine, and
2. push changes in those local repositories back to GitHub.

> _Why?_  
> 1. _All drills, assignments, coding topic tests, and coding portions of the final exam are on GitHub._
> 2. _To submit your work, you need to first get it back into the GitHub repository it originated from._

## Detailed Explanation

> _The following steps are demonstrated in this video [22:02]: https://youtu.be/lYllJYmue74_  
>   
> _Though you **can** just jump to the different steps in the video - that's why I have the time links in the steps below - I like to think I **do** say some useful stuff throughout the video that you might miss if you just jump around. Maybe it's best just to play the video at double-speed if you're in a hurry?_

### Before We Start

- log into GitHub and head to the private repo that you created in the [Creating a GitHub Account & Making a Private Repo](github-account.md) how-to

### The Steps

####  Install Git for Windows

1. [[02:31]](https://youtu.be/lYllJYmue74?t=151) download the latest version from the [official Git website](https://git-scm.com/)
   
2. [[03:58]](https://youtu.be/lYllJYmue74?t=238) install without the GUI and with the default branch set to `main`

#### Let Git know your user info

1. [[06:00]](https://youtu.be/lYllJYmue74?t=360) head over to the [First-Time Git Setup section of the Pro Git book](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup) for reference in this part

2. [[06:57]](https://youtu.be/lYllJYmue74?t=417) open up the Git Bash by right-clicking on the Desktop and choosing `Git Bash Here`

3. [[10:03]](https://youtu.be/lYllJYmue74?t=603) tell Git about your username and email - I suggest you use the username and email you used for your GitHub account
   
    ```bash
    git config --global user.name "John Doe"
    git config --global user.email johndoe@example.com
    ```
    
4. [[11:22]](https://youtu.be/lYllJYmue74?t=682) confirm you've got things entered correctly

    ```bash
    git config --list
    ```

#### Clone your private repo

1. [[12:52]](https://youtu.be/lYllJYmue74?t=772) head over to your private repository page on GitHub and grab your repo link from the `Code` button

2. [[13:11]](https://youtu.be/lYllJYmue74?t=791) clone your repository

    ```bash
    git clone [the repo link you just copied]
    ```
3. [[13:47]](https://youtu.be/lYllJYmue74?t=827) if this is your first time to connect to a private GitHub repository through this Git tool, you'll need to authenticate

4. [[15:41]](https://youtu.be/lYllJYmue74?t=941) confirm that the cloned repo is now on your local machine

#### Make changes and push them back to GitHub

1. [[17:06]](https://youtu.be/lYllJYmue74?t=1026) make changes to the `README.md` file 

2. [[17:49]](https://youtu.be/lYllJYmue74?t=1069) open up the local repo folder using right-click > `Git Bash Here`

2. [[17:17]](https://youtu.be/lYllJYmue74?t=1037) perform the Holy Trinity to push your changes back up to the GitHub repository

    ```bash
    git add --all
    git commit -m "Some useful message"
    git push
    ```
3. [[19:48]](https://youtu.be/lYllJYmue74?t=1188) confirm that your changes are now in the GitHub repository     
