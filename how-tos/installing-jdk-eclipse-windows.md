# Installing JDK, Eclipse, and Plugins: Windows

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

> _The following steps are demonstrated in this video [33:00]: https://youtu.be/BHlH07SLY24_  
>   
> _Though you **can** just jump to the different steps in the video - that's why I have the time links in the steps below - I like to think I **do** say some useful stuff throughout the video that you might miss if you just jump around. Maybe it's best just to play the video at double-speed if you're in a hurry?_

### Before We Start

- take a deep breath...this is a long one!

### The Steps

#### Install OpenJDK 11

1. [[00:57]](https://youtu.be/BHlH07SLY24?t=57) go to https://adoptopenjdk.net/
   
2. [[01:23]](https://youtu.be/BHlH07SLY24?t=83) download OpenJDK 11 (LTS), HotSpot JVM

3. [[02:45]](https://youtu.be/BHlH07SLY24?t=165) install with the JAVA_HOME and Javasoft options **on** 

#### Install Eclipse for Java Developers 2020-12

1. [[05:11]](https://youtu.be/BHlH07SLY24?t=311) go to https://eclipse.org/

2. [[06:10]](https://youtu.be/BHlH07SLY24?t=370) from the `Download Packages` link, grab the **Eclipse IDE for Java Developers** installer. (This may take a while...)
   
3. [[08:05]](https://youtu.be/BHlH07SLY24?t=485) I suggest unzipping the file into `C:\Software` (you'll need to make that folder yourself)

4. [[11:22]](https://youtu.be/BHlH07SLY24?t=682) rename the unzipped `eclipse` folder to `eclipse-2020-12` and create a shortcut to the `eclipse.exe` file someplace convenient

5. [[13:16]](https://youtu.be/BHlH07SLY24?t=796) start up Eclipse and take note of where your **worskpace** folder is - it's an important location you'll use often

6. [[15:38]](https://youtu.be/BHlH07SLY24?t=938) you might want to make a shortcut to your workspace folder someplace convenient so you can get to it easily


#### Set up JDK as Default in Eclipse

1. [[16:13]](https://youtu.be/BHlH07SLY24?t=973) open up the Preferences dialog with `Window` > `Preferences` 

2. [[16:29]](https://youtu.be/BHlH07SLY24?t=989) head to the **Installed JREs** settings by using the side menu and going to `Java` > `Installed JREs` 

2. [[16:45]](https://youtu.be/BHlH07SLY24?t=1005) add the OpenJDK 11 using `Add` > `Standard VM` > `Directory` > `C:\Program Files\AdoptOpenJDK\jdk-11.0.9.11-hotspot` 

3. [[17:59]](https://youtu.be/BHlH07SLY24?t=1079) check the new JDK to make it the default and then click `Apply`

4. [[18:44]](https://youtu.be/BHlH07SLY24?t=1079) head to the *Compiler* settings by using the side menu and going to `Java` > `Compiler`

5. [[18:50]](https://youtu.be/BHlH07SLY24?t=1130) set the `Compiler compliance level` to **11** from the dropdown and then click `Apply and Close`

#### Install the Checkstyle Plugin

1. [[19:23]](https://youtu.be/BHlH07SLY24?t=1163) go to `Help` > `Eclipse Marketplace`

2. [[19:48]](https://youtu.be/BHlH07SLY24?t=1188) search for **checkstyle**

3. [[20:14]](https://youtu.be/BHlH07SLY24?t=1214) install `Checkstyle Plug-In 8.35.0`. I recommend NOT restarting Eclipse after the installation.

#### Install the PMD Plugin

1. [[21:30]](https://youtu.be/BHlH07SLY24?t=1290) go to `Help` > `Eclipse Marketplace`

2. [[21:43]](https://youtu.be/BHlH07SLY24?t=1303) search for **pmd**

3. [[20:59]](https://youtu.be/BHlH07SLY24?t=1319) install `pmd-eclipse-plugin 4.19.0`. You can close Eclipse after the installation is complete.

#### Install the google-java-format Drop-in

1. make sure Eclipse is closed

2. [[26:28]](https://youtu.be/BHlH07SLY24?t=1588) download the [google-java-format Eclipse plugin](https://github.com/google/google-java-format/releases/download/google-java-format-1.6/google-java-format-eclipse-plugin_1.6.0.jar). Your browser will likely warn you about the file being dangerous - it's not, so just tell the browser you know what the heck you're doing.

3. [[27:52]](https://youtu.be/BHlH07SLY24?t=1672) place the downloaded file in the `dropins` folder in your Eclipse installation directory

#### Tweak the Settings

We want a few things to happen every time we save our work in Eclipse: the code should be auto-formatted

1. [[29:42]](https://youtu.be/BHlH07SLY24?t=1782) open up the Preferences dialog by going to `Window` > `Preferences`

2. [[29:50]](https://youtu.be/BHlH07SLY24?t=1790) open up the Formatter settings by using the side menu and going to `Java` > `Code Style` > `Formatter`

3. [[29:59]](https://youtu.be/BHlH07SLY24?t=1799) change the **Formatter implementation** to `google-java-format` through the dropdown and click `Apply`

4. [[30:22]](https://youtu.be/BHlH07SLY24?t=1822) open up the Save Actions settings by using the side menu and going to `Java` > `Editor` > `Save Actions`

5. [[29:59]](https://youtu.be/BHlH07SLY24?t=1799) check `Perform the selected actions on save` and`Format source code`, then click `Apply`

6. [[31:11]](https://youtu.be/BHlH07SLY24?t=1871) open up the PMD settings by using the side menu and going to `PMD`

7. [[31:24]](https://youtu.be/BHlH07SLY24?t=1884) uncheck `Show PMD perspective when checking code` and check `Check code after saving`, then click `Apply and Close`

