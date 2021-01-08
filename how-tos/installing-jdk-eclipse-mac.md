# Installing JDK, Eclipse, and Plugins: Mac

## Can I Skip This Explanation?

If you're **100% certain** the things listed in the **In a Nutshell** section below are true, then you can skip to [Tweak the Settings](#tweak-the-settings).


## In a Nutshell

We need to have everyone's computer set up so that the following is true:

1. **OpendJDK 11** is installed
2. **Eclipse-2020-12** is installed
3. Eclipse is set to use the OpenJDK 11 ***by default***
4. Eclipse has the **Eclipse Checkstyle** and **PMD Plugin** plugins installed
5. Eclipse has the  **google-java-format** drop-in installed

> _Why?_  
> _Every drill, assignment, coding topic test, and coding portion of the final exam all depends on the above being true - if even ONE thing isn't true, you're going to run into problems. Neither of us wants that._


## Detailed Explanation

> _The following steps are demonstrated in this video [25:56]: https://youtu.be/lQqD-dLYz2Y_  
>   
> _Though you **can** just jump to the different steps in the video - that's why I have the time links in the steps below - I like to think I **do** say some useful stuff throughout the video that you might miss if you just jump around. Maybe it's best just to play the video at double-speed if you're in a hurry?_

### Before We Start

- take a deep breath...this is a long one!

### The Steps

#### Install OpenJDK 11

1. [[00:33]](https://youtu.be/lQqD-dLYz2Y?t=33) go to https://adoptopenjdk.net/
   
2. [[00:54]](https://youtu.be/lQqD-dLYz2Y?t=54) download OpenJDK 11 (LTS), HotSpot JVM

3. [[01:53]](https://youtu.be/lQqD-dLYz2Y?t=113) install the pkg, dealing with any Apple "App Store only" nonsense like we did for the Git install

#### Install Eclipse for Java Developers 2020-12

1. [[03:35]](https://youtu.be/lQqD-dLYz2Y?t=215) rename any existing version of Eclipse you have in Applications

2. [[04:55]](https://youtu.be/lQqD-dLYz2Y?t=295) go to https://eclipse.org/

3. [[05:08]](https://youtu.be/lQqD-dLYz2Y?t=308) from the `Download Packages` link, grab the **Eclipse IDE for Java Developers** installer. 
   
4. [[06:28]](https://youtu.be/lQqD-dLYz2Y?t=388) open up the dmg file and move Eclipse over into Applications

5. [[07:36]](https://youtu.be/lQqD-dLYz2Y?t=456) rename the Eclipse app to `Eclipse-2020-12`

6. [[08:23]](https://youtu.be/lQqD-dLYz2Y?t=503) start up Eclipse, ignoring any trust warnings, and take note of where your **worskpace** folder is - it's an important location you'll use often



#### Set up JDK as Default in Eclipse

1. [[11:31]](https://youtu.be/lQqD-dLYz2Y?t=691) open up the Preferences dialog with `Eclipse` > `Preferences` 

2. [[11:44]](https://youtu.be/lQqD-dLYz2Y?t=704) head to the **Installed JREs** settings by using the side menu and going to `Java` > `Installed JREs` 

3. [[11:50]](https://youtu.be/lQqD-dLYz2Y?t=710) check the new JDK to make it the default and then click `Apply`

4. [[12:24]](https://youtu.be/lQqD-dLYz2Y?t=744) head to the *Compiler* settings by using the side menu and going to `Java` > `Compiler`

5. [[12:31]](https://youtu.be/lQqD-dLYz2Y?t=751) set the `Compiler compliance level` to **11** from the dropdown and then click `Apply and Close`

#### Install the Checkstyle Plugin

1. [[13:11]](https://youtu.be/lQqD-dLYz2Y?t=791) go to `Help` > `Eclipse Marketplace`

2. [[13:29]](https://youtu.be/lQqD-dLYz2Y?t=809) search for **checkstyle**

3. [[13:41]](https://youtu.be/lQqD-dLYz2Y?t=821) install `Checkstyle Plug-In 8.35.0`. I recommend NOT restarting Eclipse after the installation.

#### Install the PMD Plugin

1. [[14:39]](https://youtu.be/lQqD-dLYz2Y?t=879) go to `Help` > `Eclipse Marketplace`

2. [[14:50]](https://youtu.be/lQqD-dLYz2Y?t=890) search for **pmd**

3. [[14:56]](https://youtu.be/lQqD-dLYz2Y?t=896) install `pmd-eclipse-plugin 4.19.0`. You can close Eclipse after the installation is complete.

#### Install the google-java-format Drop-in

1. [[17:29]](https://youtu.be/lQqD-dLYz2Y?t=1049) make sure Eclipse is closed and open up the `dropins` folder in the Eclipse install

2. [[18:31]](https://youtu.be/lQqD-dLYz2Y?t=1111) download the [google-java-format Eclipse plugin](https://github.com/google/google-java-format/releases/download/google-java-format-1.6/google-java-format-eclipse-plugin_1.6.0.jar). Your browser will likely warn you about the file being dangerous - it's not, so just tell the browser you know what the heck you're doing.

3. [[19:49]](https://youtu.be/lQqD-dLYz2Y?t=1188) place the downloaded file in the `dropins` folder in your Eclipse installation directory

#### Tweak the Settings

We want a few things to happen every time we save our work in Eclipse: the code should be auto-formatted

1. [[20:50]](https://youtu.be/lQqD-dLYz2Y?t=1250) open up the Preferences dialog by going to `Window` > `Preferences`

2. [[20:59]](https://youtu.be/lQqD-dLYz2Y?t=1259) open up the PMD settings by using the side menu and going to `PMD`

3. [[21:46]](https://youtu.be/lQqD-dLYz2Y?t=1306) uncheck `Show PMD perspective when checking code` and check `Check code after saving`, then click `Apply and Close`

4. [[22:47]](https://youtu.be/lQqD-dLYz2Y?t=1367) open up the Formatter settings by using the side menu and going to `Java` > `Code Style` > `Formatter`

5. [[22:53]](https://youtu.be/lQqD-dLYz2Y?t=1373) change the **Formatter implementation** to `google-java-format` through the dropdown and click `Apply`

6. [[23:10]](https://youtu.be/lQqD-dLYz2Y?t=1390) open up the Save Actions settings by using the side menu and going to `Java` > `Editor` > `Save Actions`

7. [[23:18]](https://youtu.be/lQqD-dLYz2Y?t=1398) check `Perform the selected actions on save` and`Format source code`, then click `Apply`

