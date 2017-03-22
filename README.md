# CSDN
More information of `gradle-screen-record` with rich pictures, please see this blog:  
http://blog.csdn.net/a153614131/article/details/54137734
<br/>

# Supported OS
- Mac osx


# Usage
## 0. Working with gradle environment
Gradle is required.

<br/>

## 1. Prepare tools (Skip this part if installed)
Make sure these tools installed，or else install them first: 

 - **adb**:   We use it to get screen-record files with `.mp4` format.
 - **ffmpeg**:   We use it to convert the format of these files, from `.mp4` to `.gif`.

More infomation about [Prepare tools](./prepare-tools.MD)

<br/>

## 2. Apply `gradle-screen-record` (Just one line)
Apply `gradle-screen-record` in **rootProject/build.gradle**,
**don't forget to Sync Gradle !!!**:
```groovy
apply from: "https://raw.githubusercontent.com/fashare2015/gradle-screen-record/master/screen-record.gradle"
```
<br/>

## 3. Record Screen
### excute gradle cmd
excute gradle cmd with three params:

 - **PfileName**: **[Required]** Name of output gif**(without postfix)**.
 - **Psize**: **[Optional]** Size of output gif.
 - **Ptime**: **[Optional]** Time of output gif.

**For example:**
>./gradlew screenRecord -PfileName=test

Or:
>./gradlew screenRecord -PfileName=test -Psize=1080x1920 -Ptime=5

### operate your modile phone
When you see **"> Building 50% > :screenRecord"** in the terminal, the screen recording is begining.
Just **operate your modile phone** as you want, and it will stop after **"-Ptime"** second.

<br/>

## 4. Complete !!!
You will find the generated gif file in **rootProject/screen-record/test.gif** !!!

By the way, add it to git~
>git add screen-record/.

<br/>

# TODO
support for windows.

Make issues or pull request, if you have good ideas ~

<br/>

# Thanks
[Helper to upload Gradle Android Artifacts to Maven repositories](https://github.com/chrisbanes/gradle-mvn-push)

[深入理解Android之Gradle](http://www.jcodecraeer.com/a/anzhuokaifa/Android_Studio/2015/0911/3443.html)




