---
title: "First steps on R"
teaching: 30
exercises: 25
questions:
- "What is R and why is important to be learned?"
- "What types of data does R language have?"
- "Data-frames. What they are and how to manage them? "
- "How do I use R tools to manage an R object?"
objectives:
- "Undestand why R is important,"
- "Learn the types of data that we can manage in R"
- "Understand what is a data-frame and manipulate it."
- "Use the help command to get more insight on R functions."
keypoints:
- "RStudio is just one of the myriad of tools to work with data."
- "Every hability, as programming in R, need practice"
---

# RStudio: First steps of a wonderful journey 
*It takes courage to sail in uncharted waters*
  -Snoopy
 
## RStudio setup 

### What is R and for what can it be used for?

"R" is used to refer to the programming language and the software that reads and 
interpets what is it on the scripst. RStudio is the most popular program to write
scripts and interact with the R software.

R use a series of written commands, that is great, believe us! When you rely in clicking, 
pointing, and remembering where and why to point here or click that, mistakes
are prone to occur. Moreover, if you manage to get more data, it is easier to just
*re-run* your script to obtain results. Also, working with scripts makes the steps 
you follow for your analysis clear and shareable. Here are some of the advantages
for working with R:
- R code is reproducible
- R produce high-quality graphics
- R has a large community
- R is interdisciplinary 
- R works on data of all colors and sizes
- R is free!

### A nautical chart of RStudio

RStudio is an [Integrated Development Environment(IDE)](https://en.wikipedia.org/wiki/Integrated_development_environment#:~:text=An%20integrated%20development%20environment%20(IDE,automation%20tools%20and%20a%20debugger.) which we will use to write code,
navigate the files from our computer/cloud, try code, inspect the variables we are 
going to create, and visualize our contrived plots.

Here is what you may look at the first time you open RStudio:
![image](https://user-images.githubusercontent.com/67386612/118720027-ba433c00-b7ee-11eb-87e5-7496fde5763e.png)
Figure 1. RStudio interface screenshot.

If we click in the option `File` :arrow_right: `New File` :arrow_right: `R Script`,
we get what we can call _RStudio nautical cahrt_

![image](https://user-images.githubusercontent.com/67386612/112203976-c046e300-8bd8-11eb-9ee6-72c95f9134f3.png)
Figure 2. RStudio interface screenshot. Clockwise from top left: Source, Environment/History, 
Files/Plots/Packages/Help/Viewer, Console.

You can enter your online RStudio to see your own environment. Let's copy your instance address into your browser
(Chrome or Firefox) and login into R studio.  
The address should look like:  `http://ec2-3-235-238-92.compute-1.amazonaws.com:8787/`  
Your credencials are **user**:dcuser **pass**:data4Carp.  

Although data are already stored in your instance, in case you need it you can donwload it [here](https://drive.google.com/file/d/15dW1sQCIhtmCUvS0IUOMPBH5m1gqNB0m/view?usp=sharing).

### Review of the set-up

As we have revisited throughout the lesson, maintaining related data, analyses in a single folder
is desireable. In R, this folder is called **Working directory**. Here is where R will be looking 
for and saving the files. If you need to check where your working directory is located use `getwd()`.
If your working directory is not what you expected, always can be changed by clicking on the blue 
gear icon and pick the option "Set As Working Directory". Alternatively, you can use the `setwd()`
command for changing it.

Let's use this commands to set or working directiry where we have stored our files from the previos 
lessons:

~~~
$ setwd("~/dc_workshop/results/")
~~~
{: .language-r}

### Having a dialogue with R

There are two main paths to interact with R:(i) by using the console or (ii)by using script files.
The console is where commands can be typed and executed immediately by the software and where the 
results from executed commands will be shown. If R is ready to accept commands, the R console shows
a > prompt. You can type instructions directly into the console and press "Enter", but they will 
be forgotten when you close the session.

For example, let's do some math and save it in R objects:
~~~ 
$ 4+3
$ suma <- 4+3
$ resta <- 2+1
$ total <- suma -resta
$ total
~~~

What would happend if you tap `ctrl` + `l`. Without the lesson page, could you remember of which 
sum of numbers is `suma` made?. Reproducibility is in our minds when we program. For this purpose, 
is convenient to type the commands we want in the script editor, and save the script periodically. 
We can run our code lines in the script by the shortcut `ctrl` + `Enter` 
(on Macs, `Cmd` + `Return` will work). Thus, the command on the current line, or the instructions
in the currently selected text will be sent to the console and will be executed.

### Seeking help

If you face some trouble with some function, let's say `summary()`, you can always type `?summary()`
and a help page will be displayed with useful information for the function use. Furthermore, if you
already know what you want to do, but you do not know which function to use, you can type `??` 
following your inquiry, for example `??barplot` will open a help files in the RStudio's help
panel in the lower right corner.


