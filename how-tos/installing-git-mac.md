# Installing Git: Mac

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

> _The following steps are demonstrated in this video [26:26]: https://youtu.be/fN4RneC4iPs_  
>   
> _Though you **can** just jump to the different steps in the video - that's why I have the time links in the steps below - I like to think I **do** say some useful stuff throughout the video that you might miss if you just jump around. Maybe it's best just to play the video at double-speed if you're in a hurry?_

### Before We Start

- log into GitHub and head to the private repo that you created in the [Creating a GitHub Account & Making a Private Repo](github-account.md) how-to

### The Steps

####  Confirm that you have Git already

1. [[01:29]](https://youtu.be/fN4RneC4iPs?t=89) open up a Terminal and go `git --version` - you should see that you have some version already installed
   
#### Install the MS Git credential manager

1. [[03:14]](https://youtu.be/fN4RneC4iPs?t=194) go to [Microsoft's Git Credential Manager Core GitHub page](https://github.com/microsoft/Git-Credential-Manager-Core/releases/tag/v2.0.289-beta) and download the latest pkg file for osx
2. [[03:46]](https://youtu.be/fN4RneC4iPs?t=226) install the pkg, possibly dealing with your Mac's paranoia in opening packages that don't come from the App Store
3. [[09:02]](https://youtu.be/fN4RneC4iPs?t=542) confirm that the credential manager is recognized in your Git configuration


#### Let Git know your user info

1. head over to the [First-Time Git Setup section of the Pro Git book](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup) for reference in this part and make sure you have a Terminal window open

2. [[11:45]](https://youtu.be/fN4RneC4iPs?t=705) tell Git about your username and email - I suggest you use the username and email you used for your GitHub account
   
    ```bash
    git config --global user.name "John Doe"
    git config --global user.email johndoe@example.com
    ```
3. [[12:37]](https://youtu.be/fN4RneC4iPs?t=757) confirm you've got things entered correctly (and if you mess up like I did, just repeat the previous commands!)

    ```bash
    git config --list
    ```

#### Clone your private repo

1. [[15:26]](https://youtu.be/fN4RneC4iPs?t=926) head over to your private repository page on GitHub and grab your repo link from the `Code` button

2. [[16:03]](https://youtu.be/fN4RneC4iPs?t=963) clone your repository

    ```bash
    git clone [the repo link you just copied]
    ```
    
3. [[16:16]](https://youtu.be/fN4RneC4iPs?t=976) if this is your first time to connect to a private GitHub repository through this Git tool, you'll need to authenticate

4. [[17:31]](https://youtu.be/fN4RneC4iPs?t=1051) confirm that the cloned repo is now on your local machine (likely in your Home directory)

#### Make changes and push them back to GitHub

1. [[17:59]](https://youtu.be/fN4RneC4iPs?t=1079) make changes to the `README.md` file (use a simple editor like TextEdit) 

2. [[19:29]](https://youtu.be/fN4RneC4iPs?t=1169) set up your Mac so you can open up folders easily in the Terminal with a right-click

2. [[17:17]](https://youtu.be/lYllJYmue74?t=1037) perform the Holy Trinity to push your changes back up to the GitHub repository

    ```bash
    git add --all
    git commit -m "Some useful message"
    git push
    ```
3. [[19:48]](https://youtu.be/lYllJYmue74?t=1188) confirm that your changes are now in the GitHub repository     