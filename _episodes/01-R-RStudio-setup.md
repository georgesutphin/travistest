---
# Please do not edit this file directly; it is auto generated.
# Instead, please edit 01-R-RStudio-setup.md in _episodes_rmd/
title: "Getting started with R and RStudio"
classdate: "8/27/2019"
teaching: 45
exercises: 10
questions:
- "What is R? What is RStudio?"
- "How do I use the RStudio graphical user interface?"
- "How do I perform basic calculations in R?"
- "How do I assign values to variables in R?"
- "What are functions, and how are they used in R?"
- "Where can I get help?"
objectives:
- "Get familiar with RStudio interface."
- "Understand the difference between scripts and the console."
- "Understand how to input and read out basic information in R."
- "Assign values to variables."
- "Execute functions."
- "Demonstrate useful shortcuts."
- "Know when to use setwd()."
- "Know how to install and load packages."
- "Know what resources are available if you get stuck."
keypoints:
- "R is the programming language; RStudio is a user friendly environment for interacting with R."
- "Using RStudio can make programming in R much more productive."
- "Consider what working directory you are in when sourcing a script."
- "Use help() and ? to get basic information about functions."
- "Online forums have the answers to almost any R-related question you can come up with. Know how to Google your question!"
source: Rmd
---



### Introduction to R and RStudio

If we only had one data set to analyze, it would probably be faster to load the file into a spreadsheet and use that to plot some simple statistics.

But what if we have twelve files to check? What if we are running analysis that we will be repeating in the future?

**What is R?**

R is a statistical programming language widely used by working scientists that provides a broad spectrum of tools for data manipulation, statistical analysis, machine learning, and more. R is one of the fastest growing programming languages and new tools are being created all the time. 

Advantages of R:
* **Versatility** -- you can do just about anything in the data analysis world
* **Repeatability** -- Because R is a programming language, a properly designed script can be repeated and automated.
* **Community** -- Because R is widely used, there is a large and active online community producing resources, answering questions, and trying to solve new problems.

Disadvantages of R:
* **Learning Curve** -- R is a programming language. If you don't have programming experience, it can be a bit daunting.
* **Slow for one-time operations** -- R is great of any analysis that you plan to perform more than once. Other tools are better for quick, one-time projects.

**What is RStudio?**

RStudio is an integrated development environment (IDE) for R. It basically provides a convenient working environment for writing and employing R scripts. While you can work directly in the IDE provided with R, RStudio has a number of tools that make R easier to learn and interact with. We will be working exclusively in RStudio during this course.

***
### Installing R and RStudio

To participate in both in-class exercises and homework, you will need access to a computer with the current versions of the following installed:

1. [R software](https://cran.r-project.org/mirrors.html)
1. [RStudio Desktop](https://www.rstudio.com/products/rstudio/download/#download)

You also need to download some files to follow along with the lessons in class:

1. Make a new folder in your Desktop called `MCB585`.
2. Download [MCB585-sample-data.zip]({{ page.root }}/data/MCB585-sample-data.zip)
   and move the file to this folder.
3. If it's not unzipped yet, double-click on it to unzip it. You should end up
   with a new folder called `data`.

&nbsp;
#### Using RStudio

Here are the basic elements of RStudio:

<img src="../fig/01-RStudio-overview.png" alt="RStudio Visual Interface" />

* Code and workflow are more reproducible if we can document everything that we do.
* Our end goal is not just to "do stuff" but to do it in a way that anyone can
  easily and exactly replicate our workflow and results.
* The best way to achieve this is to write scripts. RStudio provides an
  environment that allows you to do that.

&nbsp;
#### Interacting with R using RStudio

There are two main ways of interacting with R: using the console or using
script files (plain text files that contain your code).

**Console:** The console window (bottom left panel in RStudio) is the place where R is
waiting for you to tell it what to do, and where it will show the results of a
command.  You can type commands directly into the console, but they will be
forgotten when you close the session. 

**Script:** The script window (top left panel) It is better to enter the commands in the
script editor, and save the script. This way, you have a complete record of what
you did, you can easily show others how you did it and you can do it again later
on if needed. To run commands from script, you can either copy-paste them into the R console, or you can use the script window to 'send' the current line or the currently selected text to the R console using the <kbd>Ctrl</kbd>+<kbd>Return</kbd> (Mac) or <kbd>Ctrl</kbd>+<kbd>Enter</kbd> (Windows) keyboard shortcut.

At some point in your analysis you may want to check the content of variable or
the structure of an object, without necessarily keep a record of it in your
script. You can type these commands directly in the console. RStudio provides
the <kbd>Ctrl</kbd>+<kbd>1</kbd> and <kbd>Ctrl</kbd>+<kbd>2</kbd> shortcuts allow you to jump between the script and the
console windows.

If R is ready to accept commands, the R console shows a `>` prompt. If it
receives a command (by typing, copy-pasting or sent from the script editor using
<kbd>Ctrl</kbd>+<kbd>Return</kbd>/<kbd>Ctrl</kbd>+<kbd>Enter</kbd>, R will try to execute it, and when ready, show the results and come back with a new `>`-prompt to wait for new commands.

If R is still waiting for you to enter more data because the command you entered is not yet complete, the console will show a `+` prompt. This means that you haven't finished entering
a complete command, perhaps because you haven't 'closed' a parenthesis or quotation. If you're in RStudio and this happens, either complete the command and press <kbd>Enter</kbd> or click inside the console window and press <kbd>Esc</kbd> to cancel the current command. That should help you out of trouble.

***
### Interacting with the console

&nbsp;
#### Basic commands

At the simplest level, the console can be used as a calculator to directly ask for basic operations. Try a few of the following:

*To run the command, try to copy-paste each line into the console and run. Also try copying/typing each line into the script, highlighting the text (or just make sure your cursor is on the right line), and pressing <kbd>Ctrl</kbd>+<kbd>Enter</kbd>.*



~~~
# Addition
40+2
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}


~~~
# Subtraction
98-56
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}


~~~
# Multiplication
6*7
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}


~~~
# Division
74088/1764
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}


~~~
# Exponential
6.480741^2
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}


~~~
# Equations with parenthetical operations
(((6 + 4) + 2)^2 + 9)/3 - 9
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}

&nbsp;
#### Commenting

Note above the use of `#` signs to add comment. Comments are for you and anyone coming later to read your script. Anything to the right of a `#` is ignored by R. Comment liberally in your R scripts. We will discuss best practices in coding and the use of comments more later on in the course.

&nbsp;
#### Assignment Operator

We can create a new variable and assign a value to it using `<-` or '=', which are the assignment operators in R. It assigns values on the right to objects on
the left. So, after executing `x <- 3`, the value of `x` is `3`. The arrow can
be read as 3 **goes into** `x`.  You can also use `=` for assignments but not in
all contexts so it is good practice to use `<-` for assignments.

In RStudio, the <kbd>Alt</kbd>+<kbd>-</kbd> will write `<-` in a single keystroke. Let's give it a go:


~~~
weight_kg <- 55   # using <- sets the value of the variable x to 42.
weight_kg = 42    # using `=` in place of `<-` works in almost all situation (but not quite all; it is better to get into the habit of using `<-`).
~~~
{: .language-r}

Once a variable is created, we can use the variable name to refer to the value it was assigned. The variable name now acts as a tag. Whenever R reads that tag (`x`), it substitutes the value (`42`).

<img src="../fig/tag-variables.svg" alt="Variables as Tags" />


~~~
# if you want to see the value of a variable, just type the variable name into the console:
weight_kg
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}

Also note that when you assign a value to a variable, a new object is created in the Environment panel (upper right). This panel lists all *objects* in your *workspace*. Note that whenever you make an assignment with `<-` or `=`, R creates a new object in memory. Your workspace is simply the collection of objects currently stored in memory that are available to access in your current R session.

Assigning a new value to a variable breaks the connection with the old value; R forgets that number and applies the variable name to the new value. 

When you assign a value to a variable, R only stores the value, not the calculation you used to create it. This is an important point if you're used to the way a spreadsheet program automatically updates linked cells. Let's look at an example.

First, we'll convert `weight_kg` into pounds, and store the new value in the variable `weight_lb`:


~~~
weight_lb <- 2.2 * weight_kg
# weight in kg...
weight_kg
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}



~~~
# ...and in pounds
weight_lb
~~~
{: .language-r}



~~~
[1] 92.4
~~~
{: .output}

In words, we're asking R to look up the value we tagged `weight_kg`,
multiply it by 2.2, and tag the result with the name `weight_lb`:

<img src="../fig/new-variables.svg" alt="Creating Another Variable" />

If we now change the value of `weight_kg`:


~~~
weight_kg <- 100.0
# weight in kg now...
weight_kg
~~~
{: .language-r}



~~~
[1] 100
~~~
{: .output}



~~~
# ...and weight in pounds still
weight_lb
~~~
{: .language-r}



~~~
[1] 92.4
~~~
{: .output}

<img src="../fig/memory-variables.svg" alt="Updating a Variable" />

Since `weight_lb` doesn't "remember" where its value came from, it isn't automatically updated when `weight_kg` changes.

This is different from the way spreadsheets work.

<img src="../fig/arithmetic-variables.svg" alt="Variables as Tags" />

What happens if you don't complete a line?

~~~
100 + 
~~~
{: .language-r}

R hangs with a `+` in the console, waiting for you to finish your thought...

~~~
1
~~~
{: .language-r}

All better.


You can use the `ls()` command to list all variables currently defined in your workspace.


~~~
ls()
~~~
{: .language-r}



~~~
[1] "args"          "dest_md"       "missing_pkgs"  "required_pkgs"
[5] "src_rmd"       "weight_kg"     "weight_lb"    
~~~
{: .output}

&nbsp;
> ## What is allowed or not allowed with variable names?
>
> Try assigning values to the following variables. Which work and which do not? What is 
> causing the errors?
>
> 
> ~~~
> min_height <- 1
> max.height <- 1
> _age <- 1
> .mass <- 1
> MaxLength <- 1
> min-length <- 1
> 2widths <- 1
> celsius2kelvin <- 1
> ~~~
> {: .language-r}
>
> > ## Solution
> > 
> > 
> > ~~~
> > min_height <- 1
> > ~~~
> > {: .language-r}
> > 
> > ~~~
> > max.height <- 1
> > ~~~
> > {: .language-r}
> > 
> > ~~~
> > _age <- 1 # error; starts with a symbol
> > ~~~
> > {: .language-r}
> > 
> > 
> > 
> > ~~~
> > Error: <text>:1:1: unexpected input
> > 1: _
> >     ^
> > ~~~
> > {: .error}
> > 
> > ~~~
> > .mass <- 1 # no error --> the . results in a hidden variable
> > ~~~
> > {: .language-r}
> > 
> > ~~~
> > MaxLength <- 1
> > ~~~
> > {: .language-r}
> > 
> > ~~~
> > min-length <- 1 # error; "-" is an operator
> > ~~~
> > {: .language-r}
> > 
> > 
> > 
> > ~~~
> > Error in min - length <- 1: could not find function "-<-"
> > ~~~
> > {: .error}
> > 
> > ~~~
> > 2widths <- 1 # error; starts with a number
> > ~~~
> > {: .language-r}
> > 
> > 
> > 
> > ~~~
> > Error: <text>:1:2: unexpected symbol
> > 1: 2widths
> >      ^
> > ~~~
> > {: .error}
> > 
> > ~~~
> > celsius2kelvin <- 1
> > ~~~
> > {: .language-r}
> >
> {: .solution}
{: .challenge}

&nbsp;
#### Cleaning up

Try clicking on the brush icon in the Environment panel and clicking <kbd>Yes</kbd> in the pop-up box. What happened to your variable? What happens if you try to display the variable in the console?


~~~
x
y
~~~
{: .language-r}

You can also remove variables one at a time.


~~~
x = 3
y = x + 2
z1 = x - y
z2 = x + y

rm(x)
rm(y)
rm(list = ls()) # remove all variables currently in environment
~~~
{: .language-r}


It is generally good practice to start off each session with a clean slate. When you start RStudio, the Environment will be clear (unless you load a previously saved workspace). If you are finished with one analysis and starting another, it is a good idea to clear you Environment. That way if you reuse a variable name (e.g. `x`) you won't accidentally end up using the value stored in your workspace during the previous analysis.

&nbsp;
### Functions in R

Functions are predefined commands that take *input* values (aka [arguments]({{ page.root }}/reference.html#argument), perform some operation, and generates some output. The format is:


~~~
output <- functionX(argument1, argument2, ...)
~~~
{: .language-r}

&nbsp;

if the output variable and `<-` are not used, the output is written directly to your console window. Let's define a new function `fahrenheit_to_kelvin` that converts a temperature value in Fahrenheit (the *argument*) to Celsius (the *output*):


~~~
FtoC <- function(temp_F) {
  temp_C <- (temp_F - 32) * (5 / 9)
  return(temp_C)
}
~~~
{: .language-r}

&nbsp;

Now let's give is a try:

~~~
FtoC(32) # output to console
~~~
{: .language-r}



~~~
[1] 0
~~~
{: .output}



~~~
Temp_C <- FtoC(32) # assign the output to a new variable called Temp_C
Temp_C
~~~
{: .language-r}



~~~
[1] 0
~~~
{: .output}

&nbsp;

Some functions take no *arguments*, like the previously discussed `ls()` (which just returns a list of variables currently in memory). Others take many different *arguments*, separated by `,`s, that modify the output. For example, the `sum()` function will output the sum of all input values:


~~~
sum(1,2,6)
~~~
{: .language-r}



~~~
[1] 9
~~~
{: .output}

&nbsp;

Functions can also be nested:


~~~
sum(FtoC(32),FtoC(75),FtoC(13))
~~~
{: .language-r}



~~~
[1] 13.33333
~~~
{: .output}

&nbsp;
#### Working directories in R

Your *working directory* refers to the file path on your computer where the current session of R will go to look for files. You need to have any external data that you are working with in a file in your working directory in order to load it into R (or know how to specify a different location, if it isn't in your working directory). Any output (data or charts) that you save in R will also be stored in the working directory by default unless you specify a different location on your computer. 

A collection of scripts and data in R are defined as a *Project*. Among other things, the project will define the default working directory. Let's try staring a new project:

1. In RStudio, click **File > New Project...**.
2. Click **Existing Directory**.
3. Click <kbd>Browse...</kbd>.
4. Navigate to your *MCB585* folder and click <kbd>Create Project</kbd>.

RStudio will reload with a clean working environment. If you click on the **Files** tab (lower right panel), you will see that the current folder is you *MCB585* folder, and that RStudio will have created a new file called **MCB585.Rproj**.

In the future, you can either just open this file from you file explorer to load you MCB585 project, or you can open it from RStudio by clicking **File > Open Project...**, navigating to your *MCB585* folder, and selecting the **MCB585.Rproj** file.

You can change the active working directly by using the function `setwd()`. For example, we can set the working directory to our *MCB585/data* folder using the following command:


~~~
setwd("./data")
setwd("data") 
setwd("..") 
~~~
{: .language-r}

&nbsp;

Note that unless you specify the entire path, all entries will be relative to the current working directory. Relative navigation:
* '.' = the current working directory
* '..' = the directory one level above the working directory (i.e. the Desktop in our case)
* Note that "./data" and "data" both mean "go to the *data* folder inside the working directory"

If you are unsure what your current working directory is, you can define the entire path:


~~~
setwd("C:/Users/<username>/Desktop/MCB585/data") # Windows
setwd("/Users/<username>/Desktop") # MacOS
~~~
{: .language-r}

**Caution for Windows users:** If you copy a file path from Windows Explorer and paste it into `setwd()`, you have to change the backslashes ("\\") used in Windows to forwardslashes ("/"). R interprets "\\" as a type of special type of character called an *escape character* rather than a part of the string. If you don't replace them, you will get errors:

&nbsp;


~~~
setwd(".\data")
~~~
{: .language-r}

&nbsp;

We can also ask R what the current working directory is using `getwd()`, and ask for a list of files in the current directly with `list.files()`:


~~~
# Retrieve the current working directory
getwd()
~~~
{: .language-r}



~~~
[1] "C:/Users/sutph/Documents/GitHub/MCB585/_episodes_rmd"
~~~
{: .output}


~~~
# List all files in the current working directory
list.files()
~~~
{: .language-r}



~~~
[1] "01-R-RStudio-setup.Rmd"                
[2] "02-introduction-to-R-basics.Rmd"       
[3] "03-introduction-to-R-data-plotting.Rmd"
[4] "data"                                  
[5] "results"                               
~~~
{: .output}

&nbsp;
> ## Be careful when using `setwd()`
>
> One should exercise caution when using `setwd()`. Changing directories in a script file can limit reproducibility:
> * `setwd()` will return an error if the directory to which you're trying to change doesn't exist or if the user doesn't have the correct permissions to access that directory. This becomes a problem when sharing scripts between users who have organized their directories differently.
> * If/when your script terminates with an error, you might leave the user in a different directory than the one they started in, and if they then call the script again, this will cause further problems. If you must use `setwd()`, it is best to put it at the top of the script to avoid these problems.
> The following error message indicates that R has failed to set the working directory you specified:
> ```
> Error in setwd("~/path/to/working/directory") : cannot change working directory
> ```
> It is best practice to have the user running the script begin in a consistent directory on their machine and then use relative file paths from that directory to access files (see below).
{: .callout}

&nbsp;
#### Installing and loading packages

R comes preloaded with a decently wide range of functions for basic data manipulation, but you will inevitably want to do something more interesting. There are many, many 'packages' that are available online for download. Each package is a set of related functions designed for a specific area of analysis. For example, later in the course we will use specialized packages that contain functions for power analysis (the `pwr` package) and survival analysis (the `survival` package). 

To use a package, you have to do two things:
1. **Install** -- Download the package from an external source, and make the functions accessible to R and RStudio. This is accomplished with the `install.packages()` function and only has to be done just per computer.
2. **Load** -- Installing the package does not immediately allow you to access the associated functions. You first have to load the package into your local workspace. This is done with the `library()` function.

Let's give it a try by installing and loading the `pwr` package:


~~~
# Install required packages
install.packages("pwr")
~~~
{: .language-r}



~~~
package 'pwr' successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\sutph\AppData\Local\Temp\RtmpGS4OK8\downloaded_packages
~~~
{: .output}


~~~
# Load required packages into memory
library("pwr")
~~~
{: .language-r}

&nbsp;

Generally, a Google search will let you find packages for just about any type of analysis. These usually come from one of two sources (which R mostly takes care of automatically, with a few exceptions):
* [CRAN](https://cran.r-project.org/) for basic R packages
* [Bioconductor](https://www.bioconductor.org/) for biological packages

***
### Resources -- where to turn for help

There are a variety of resources available when you have questions. Here are a few places to look:

&nbsp;
#### Getting help in R

R has a built in function called `help()` that provides basic information about specific functions. You can either use this function like any other function, or use the `?` operator. Let's give it a try to get more detailed information on how the `setwd()` function works.


~~~
help(setwd)
?setwd
~~~
{: .language-r}

&nbsp;

When you enter either command, notice that the **Help** panel opens (lower right panel in RStudio). This panel provides information on the purpose, inputs, and outputs of the queried function. It also provides useful examples of how to use the function at the end of the documentation. `help()` is usually a good first place to look to get a feel for what a function is doing.

&nbsp;
#### Online Forums

Perhaps the most valuable resource available to both basic and advanced R users is the vast online community. Many people are actively using the R language for a variety of analysis tasks. You will find that most questions have already been asked and answered on one of the various online forums. If you can't find the answer, sign up for a forum and post your question. You will generally get an answer (or a pointer to another forum where the question has already been answered) within a day or two.

To find answers, the simplest way is to just type what you are trying to do into Google. Preceedign your question with "R" will tend to find questions within the R community: 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*R calculate standard deviation*

There are many online forums with R user discussions, but I find the most common to be [stackoverflow](https://stackoverflow.com/).

&nbsp;
#### The Carpentries

[The Carpentries](https://carpentries.org/) and [Software Carpentry](https://software-carpentry.org/) in particular offer free online introductory programming lessons for R and other languages. Much of the material in the early part of this course is based on the Software Carpentry material. They are a good resource for beginners.

&nbsp;
#### Resources at the University of Arizona

The University of Arizona has several resources for both statistics and programming:
* [Statistics resources](https://it.arizona.edu/documentation/statistical-resources)
* [Statistics consulting](https://it.arizona.edu/service/statistical-consulting) (pay service, free consultation)
* [BIO5 StatLab](https://statlab.bio5.org/) (pay service, free consultation)
* [Cancer Center biostatistics](https://cancercenter.arizona.edu/researchers/shared-resources/biostatistics)
* [Cancer Center bioinformatics](https://cancercenter.arizona.edu/researchers/shared-resources/bioinformatics)

***

{% include links.md %}
