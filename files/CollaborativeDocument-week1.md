![](https://i.imgur.com/iywjz8s.png)


# Collaborative Document - week 1

2022-09-14 Reproducible Research with R Packages

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

This is the Document for today: [tinyurl.com/rpackaging-week1](https://hackmd.io/B_D159mIQSCxDUKO0ZdEKg?both)

Collaborative Document week 1: [tinyurl.com/rpackaging-week1](https://hackmd.io/B_D159mIQSCxDUKO0ZdEKg?both)

Collaborative Document week 2: [tinyurl.com/rpackaging-week2](https://hackmd.io/m5dLkEQtTr6rofVaLTDH6Q?both)

Collaborative Document week 3: [tinyurl.com/rpackaging-week3](https://hackmd.io/hLOwyjUkQCek-L8Pk0zYyQ?both)

Collaborative Document day 4: [tinyurl.com/rpackaging-week4](https://hackmd.io/gDCDSNw9Q2ynqahKr_SzBA?both) 

## 👮Code of Conduct

Participants are expected to follow these guidelines:
* Use welcoming and inclusive language.
* Be respectful of different viewpoints and experiences.
* Gracefully accept constructive criticism.
* Focus on what is best for the community.
* Show courtesy and respect towards other community members.

l.deboer@esciencecenter.nl, b.vreede@esciencecenter.nl
 
## ⚖️ License

All content is publicly available under the [Creative Commons Attribution License 4.0](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, raise your hand in the zoom window, or ask a question in the chat.

You can ask questions in the document or chat window and helpers will try to help you.

## 🖥 Workshop website

💻 [Workshop website](https://esciencecenter-digital-skills.github.io/2022-09-14-ds-rpackaging/)

🛠 [Setup instructions](https://esciencecenter-digital-skills.github.io/2022-09-14-ds-rpackaging/#setup)

## 👩‍🏫👩‍💻🎓 Instructors

Barbara Vreede, Lieke de Boer

## 🧑‍🙋 Helpers

Eva Viviani, Pranav Chandramouli, Djura Smits, Ji Qi 

### Icebreaker
What do you want to keep (remembering, or keep doing) from your summer (holidays)?
- Martine: remembering and keep doing: sailing in Friesland
- Djura: remembering: supping with my mom
- Pranav: Vacationing! more specifically hiking/travelling
- Bas: keep doing - read a book
- Jessica: lol, I didn't have summer holidays as a research supporter. But I can say, I'll continue working on getting my new house in order. Also gardening!
- Ji: the beautiful beaches from Lagos, Portugal
- Kat: Holiday in Scotland (Isles of Skye and Harris)
- Samar: I remember the chilly and sunny days in front of beach on north coast in Egypt
- Eric: Dance festivals and renovating the house, trying new sports this summer
- Barbara: exercising! I got an exercise bike & did a lot of swimming during the summer & it was a nice change from 2 years of covid-sitting-on-my-behind...
- Pim: remember & keep exploring wine-tourism throughout Europe
- Rodrigo: I would like to keep my sun tan.
- Utkarsh: Evening walks when it's still bright even at 10 pm. 
- Joshua: I also didn't have holiday yet, but the summer was still nice :).
- Lieke: take time to do nothing every now and then
- Frank: Hiking Norwegian highlands and not seeing anyone for miles (except my complaining teenage kids...)
- Venustiano: Beach, mountains, beertjes, mexican food
-
-
- Eva: waking up at 9 every day and having a creme cornetto with coffee. 
-


## 🗓️ Agenda
Day 1. Wed 14 September 2022
| Time | Topic |
|--:|:---|
| 09:00 	| Welcome and icebreaker
| 09:15 	| Introduction, Accessing packages
| 10:15 	| Coffee break
| 10:30 	| Getting started
| 11:30 	| Coffee break
| 11:45 	| Licenses
| 12:45 	| Wrap-up
| 13:00 	| END

## 🔧 Exercises

**Q: What problems have you encountered that were the result of messy coding?** 


* Martine: different versions of packages, when getting other persons R project (or mine projec to them), especially Rlang, do not know why
* Kat: My results differ from that of my collaborator
* Jessica: not being able to immediately remember what the code means if I haven't used it in a while, having to spend a lot of time refreshing my memory; errors from: typos in functions; and problems with references to files if I accidentally changed where the file is located. It can also be hard to use another person's code from GitHub if it's poorly documented (or documented in a way that assumes you know a certain concept without explaining what that concept might be)
* Joshua: Bugs 
* Utkarsh: Not able to understand after few days what I did actually. End up re-doing everything from scratch.
* Samar: had to repeat the analysis several times cz I did not get a reasonable finding, considering that my assisatnts coded the data well and then discovered the there are a lot of mkstakes in data coding 
* Anke: breaking something that worked before
* Not remembering what I did and why
* Frank: "lost" data (pre-)processing steps, "wrong" processing workflow, legacy testing artefacts
* Venustiano: forget what the code does and how it works, not finding results or source code. Not saving the results after a 2-week running algorithm
* Federica: not being able to reproduce previous results
* Rodrigo: I dont have messy code (I wish). I think the worst problem was having a very specific code, an unexpected bug happened and it was VERY hard to track it. At the end it was not even my mistake: I had was that I used a function from another package in a specific way, and that when I updated R and the packages, that specific base version of R had a bug in one function that was called by this function, and it didn't work well with this specific type of call and the type of input I used in this function. So... very hard to track bugs.
* Pim: messing up the sequence of operations; "just testing this really quickly" (and then it ends up being 90% of unorganized code)
* Forgetting I changed a variable somewhere and getting different results and not knowing why
* Eric: assumptions where made during code, or input files where changed without notice. Non unique variables, variable names which where like a,b, c etc, basically interpret other peoples code is sometimes very diffuclt. Also continue projects after awhile and it takes time to start again. 
* Eva: not able to improve upon the code without breaking it
* Valentini: Sometimes loosing my data,or forget the code names or their functions
* Ji: not only for myself, but also for the others, understanding the code is hard.
*



#### Exercise: find a package on github, bitbucket, or gitlab and install it with `devtools`.
If you have trouble finding a package, [try this one](https://github.com/PabRod/kinematics).
1. What package did you install? Share a link!
2. What code did you use to install it?
3. Did it work? What problems did you encounter?
4. Bonus: take a look at the `DESCRIPTION` file of the package you installed. Did you notice that other packages mentioned in this file were installed also?

- Rodrigo: I installed MetBrewer (https://github.com/BlakeRMills/MetBrewer). It has color palettes inspired by works at the Metropolitan Museum of Art in New York/ devtools::install_github("BlakeRMills/MetBrewer")  / All OK / The packages in DESCRIPTION were already installed
- Kat: I installed [flexgsea](https://github.com/NKI-CCB/flexgsea-r). I used renv::install("NKI-CCB/flexgsea-r"), but you could also use devtools::install_github("NKI-CCB/flexgsea-r")
- Utkarsh: I installed CARD package from github repository (https://github.com/YingMa0107/CARD), using `devtools::install_github('YingMa0107/CARD')` command. Yes, it was installed successfully. The packages mentioned in the description were installed as well.
- Martine: `devtools::install_github("PabRod/kinematics")`, problem: did not know what part of the URL to enter, I mimicked the examples in the help. The description file mentions some packages being installed as well, but I do not know if I did not have them before. 
- Samar: I tried to use this code'devtools::install_github(MetBrewer) but I receive an error
Er
- Pim: devtools::install_github("tidyverse/dplyr")
- Eric: Same as Rodrigo, for R 4.2.1 ->Dependacies:Installing 10 packages: colorspace, viridisLite, RColorBrewer, munsell, labeling, farver, scales, isoband, gtable, ggplot2
- Venustiano: I installed [cowplot] (https://github.com/wilkelab/cowplot). ```devtools::install_github('wilkelab/cowplot')```  
Yes, it did work, no problems. Yes, other packages were installed as well.
- Anke: devtools::install_github("PabRod/kinematics"), ERROR: this R is version 3.6.3, package 'kinematics' requires R >= 3.50, non-zero exit status, solved by using devtools::install_github("bvreede/kinematics")
- Jessica: I installed devtools::install_github("r-lib/httr"). 
- Frank: I just went with the default kinematics, all good so far
- Joshua: Not sure what I installed but it's EPIC:  `devtools::install_github("GfellerLab/EPIC")`
- Samar: It is working now for two packages 


### FOR THOSE WHO HAD AN ERROR with PabRod/kinematics:
Can you try `devtools::install_github("bvreede/kinematics")`

#### Exercise: edit the function, and reload the package.
The default package generates `Hello, world!` when the only function`hello()` is called.

1. Change this function to generate a different output. (Have fun with it, perhaps add an argument or two!)
2. Build and install the package, and call the function again to see that it works differently.
- Martine: done
- Frank: done; also added a more functions and another script
- Bas
- Pim: done
- Jessica: done
- Venustiano: done
- Samar: I did that but have an issue `callr::add_hook(hello(mysterycoffee))
Error in hello(mysterhellycoffee) : unused argument (mysterycoffee)`  
Samar: I tried putting quotation and had the same issue [callr::add_hook(hello("mysterycoffee"))
Error in hello("mysterycoffee") : unused argument ("mysterycoffee")] (Martine: do you have an argument in your function?)Samar: how to configure Martine: between the () of function, like function(variablename)hayes it appears in t.Did you do the install again?ar: yes Maybe the teachers have ideas :). I dont think you have to install the package again after you adjusted a function, you can source it again. "Source on Save", I lost my way
Teachers can probably help :) when you share maybe  Samar: thank you
I meant via the button in the tab build.

- Valentini: i still have trouble with Rtools Do I need to put Rtools on the PATH?it's not clear to me how to do that..
- Eric:done
- Utkarsh: Done. Added another function for getting time and greeting. hello() function to take name from user.
- Anke: done
- Lana: re-installing r-tools (sounds fun). Done, I don't have administrator rights on the laptop that is why I was worried about the installation. Error is solved. All fine. (Frank: I installed R, RStudio, and RTools in the user's home folder to avoid such issues, used to work well)
- Joshua: done
- Kat: done
- Rodrigo: done 
- Ranran: done
- 


#### Exercise: Open the DESCRIPTION file. What do you see here?

Take 5 minutes to edit this file with the information it asks. In particular, edit the following fields (when needed): Title, Version, Author, Maintainer, Description. For now, ignore the rest.

- Martine: done
- Frank: filled in some stuff... 
- Bas: done
- Pim: done
- Jessica: done
- Venustiano: done
- Samar:done
- 
- Valentini: usethis
- Eric: Done
- Utkarsh: Done.
- Anke: done
- Lana: done
- Joshua: done
- Kat: done
- Rodrigo: done done
- Ranran: done









/// for future exercise, please don't edit! ///
- Martine: 
- Frank: 
- Bas
- Pim: 
- Jessica: 
- Venustiano: 
- Samar:
- Valentini: 
- Eric:
- Utkarsh: 
- Anke: 
- Lana: 
- Joshua: 
- Kat: 
- Rodrigo: 
- Ranran: 

#### Exercise: change the license of your package.

1. Change the license of your package to Apache, using `usethis::use_apache_license()`. Look at the `DESCRIPTION` and `License` files and see how they have changed.
2. Change the license of your package to the license you want to use. What function did you use?

- Martine: i choose the example apache
- Frank: done using MIT 
- Bas: done. usethis::use_gpl_license(version=3)
- Pim: done (usethis::use_gpl_license(); TUe recommends either a GPL or MIT/BSD-like license)
- Jessica: done. I used MIT `usethis::use_mit_license()`
- Venustiano:done, `usethis::use_agpl3_license()` 
- Samar: done.. I used usethis::use_apache_license() and it changed to apache 
- 
- Valentini: 
- Eric:
- Utkarsh: used the agpl license
- Anke: usethis::use_agpl_license()
- Lana: done
- Joshua: done `usethis::use_mit_license()`
- Kat: 
- Rodrigo:  `usethis::use_agpl3_license("R")`
- Ranran: 

### Homework for 21 September
Homework for next week (21 September):
    
Create a package using your own R project, if you have one (see the last point below if you do not have one). Create functions in the R folder of that package.

Remember the following:

* When you are using external functions inside your package, add double colons `::` before calling that function
* Separate out different functions, think about main functions and helper functions
* If you start from a script, you can keep the leftovers (if there are any after separating out functions) in a script that calls your package's functions and runs your workflow. 
* The following was not discussed in class, but it is very good if **at least one of your functions gives an output** (so, it doesn't just "do" something, like print `Hello World`, it actually creates a data frame, or a vector, or an object of some other kind)! We will see why next week. 
* Don't forget through `Install (and Restart)` whenever you change anything. 
* If you are creating your own package, don't forget to update the `DESCRIPTION` file. 
* If you are not using your own project, take some time to improve the current `make_groups` function and perhaps add another function. 

Don’t worry if you run into issues, this is expected. See if you can fix them, but don't be afraid to bring them next week, so we can solve them together. 

## 🧠 Collaborative Notes
**How to check your R version**
type:

```
R.version
```
Please note that the latest R version at the moment of writing (14/09/2022) is 4.2.1


# Introduction
**Benefit of a package**
- usability
- maintance
- sharing
- collaboration

FYI: To write a package it's easier to use Rstudio because it has many built-in functions.


**What is a package?**
- A project structured around a standardised folder structure
- Centered around functions


**How do you use a function from a package?**
You can import the package by writing:
```
library(knitr)
```
and then call the function directly into your console:

```
knit()
```

however, if you wish not to import the whole package, but rather use only a specific function, you can use the name of the package + semicolon:

```
knitr::knit()
```

Benefit of the semicolon method:
- it clarifies from which package the function comes from
- there might be functions called with the same name among packages. This overlap might cause confusion. Calling the function with the semicolon method allows you to use the function you wanted without ambiguities (and conflicts!)
- it allows you to report back to the user any import messages (more on this in the example below)


#### EXAMPLE OF BAD PRACTICE WHEN LOADING A PACKAGE WITHIN A FUNCTION:
In this *bad* example, we load the `library(dplyr)` as part of the function `test()` in order to use dplyr's function `add_row()`. 

```
test <- function(x){
    library(dplyr) # load the dplyr library
    add_row(x) # use the dplyr's function add_row()
}
```

Once a user types `test()` in the console, the function will load the package `dplyr` without informing him/her that it has loaded the package.

*INSTEAD DO THIS:*
```
test <- function(x){
    dplyr::add_row(x)
}
```

# How do you install a package?
**First method:**

You can type in the console the name of the package you want to install (e.g., in this case, knitr):
```
install.packages('knitr')
```

**TIP:** When using this method, make sure that the name of the package is within quotation marks ('' or "").

**Second method:**
Press the button `install` in the Rstudio IDE and type in the name of the package.


**Third method:** 
Using the package `devtools`'s functions. When we use the method `install.packages()`, the package is installed from [CRAN](https://cran.r-project.org/) (which is R's official package repository). However, if a package is not listed in CRAN, (e.g., if for example the package is still in development, or its newest features have not been updated yet on CRAN) you can install it from github by using `devtools`. For example:

```
devtools::install_github(PabRod/kinematics) 
```

If the installation was successful, when we type:

```
library(kinematics)
```

We should not see any error.

Note that packages installed via github are not reviewed, while packages on CRAN are.

# How to create a package
Go to `File > new project` , or press the button on the R studio IDE (the one with a transparent cube with a green +). This opens up a window where we click on `new directory`, and we choose `R package`. This will open up a window named **Create R Package**. 

Today we're making a toy example. We're creating a package called `misterycoffee`. The package is saved into a directory that you can see within the `create project as subdirectory of` section. To use version control, click on `create a git repository`. We tick also `Open in new session` (bottom-left part of the window), and then click on `create new project`.

This will automatically open a new project into a fresh R studio session, called 'mysterycoffee'.

#### How to install our R package
Click on the `Build` tab, and `Install and Restart`. This restarts the R session, and attaches a package:

```
library(mysterycoffee)
```

We can now use all the functions within the `R` folder. By default, the package has a `hello.R` file. This file contains a dummy function that you can use by typing `hello()` in the console.

#### The structure of an R package
Once we have installed the package via R studio, this will create a standard R package structure:

```
.
├── R
│   └── <R functions>
├── README.md
├── LICENSE
├── DESCRIPTION
└── NAMESPACE
```

This is the minimal structure of an R package. However, you can add/modify this structure based on the needs of your package. For instance, if your package needs in-built data, you can add those in the `/data` folder (note that R accepts in the `/data` folder only rda/r.data objects, but not .csv/.txt files).

Other optional folders that can be added:

```
- tests
- vignettes
- inst
```

We will talk more about the `data`, `tests`, `inst` and `vignettes` folders.

### Edit the `mysterycoffee` package
First of all, we delete the default `hello.R` file permanently, and we create a new script.

Click on the + symbol, and save the new R-file in the `/R` folder. We try to give it a meaningful name: `make_groups.R` (it is a good habit to name function by its goal).

This file will contain a basic skeleton of our function `make_groups()`. This function takes `names` as input, and returns `names_coupled` as output. 
The goal is to shuffle the elements contained in `names` and arrange them into a matrix. The only constrain we give to this matrix is that it should have 2 columns (`ncol = 2`). Once done that, we want the function to return us the matrix just created.

```
make_groups <- function(names){
    #Shuffle the names
    names_shuffled <- sample(names)
    
    #Arrange the names
    names_coupled <- matrix(names_shuffled, ncol = 2)
    
    return(names_coupled)
}
```

**TIP:** Note that we're using the R's base inbuilt `sample()` function. You can check what this function does by typing `?` + name of the function:
```
?sample
```

**TIP:** you can save the file by clicking on `File > save` but there is a keyboard shortcut. On windows: `ctrl + s`, on mac: `cmd + s`.

**TIP:** Note that the `return()` statement is not necessary, but it is best practice to make this explicit to anyone that is debugging this function (i.e., it increases clarity and readability).

Let's try our make_groups() function. In the console, type:

```
make_groups(c("Djura", "Lieke", "Ji", "Eva"))
```

This will gives us a matrix with 2 columns:

```
     [,1]    [,2]   
[1,] "Djura" "Lieke"
[2,] "Eva"   "Ji" 
```

Let's try to add new names. In the console, type:

```
make_groups(c("Djura", "Lieke", "Ji", "Eva", "Barbara", "Pablo"))
```

The output now has changed to integrate Barbara and Pablo names:

```
     [,1]      [,2]   
[1,] "Ji"      "Pablo"
[2,] "Barbara" "Djura"
[3,] "Eva"     "Lieke"
```

In general, in an R package you can make single files per function, or group them into one file. For instance, *helper functions* (functions that help shorten code for frequently used minor tasks) can be nested into other *main* functions. You can decide to group the main function + the helper function into a single file, or to save each function into a different file.

There is no general rule on which strategy is best. There are pros and cons in both. For instance, if you have a file for each funtion you can search them easily in your directory, but it increases complexity in your package. Conversely, if you have a very complex task (e.g., making coffee) which requires many steps (i.e., grind coffee beans, add water, etc), it makes much more sense to group them into one single file (e.g., make_coffee.R), but it will make finding the single functions harder.
We will come back on this later on.

##### Example
We can add a helper function `my_sample()` within `make_groups()`. We define this function right after make_groups() in the make_groups.R file and we save the file.
 
```
make_groups <- function(names){
    #Shuffle the names
    names_shuffled <- my_sample(names) #note the changes occur here
    
    #Arrange the names
    names_coupled <- matrix(names_shuffled, ncol = 2)
    
    return(names_coupled)
}


my_sample <- function(names){
    names_shuffled <- sample(names)
    return(names_shuffled)
}
```

This time, when we use `make_groups()`, the function will automatically call `my_sample()` and not `sample()` anymore.

**TIP:** if you decide to group helper functions and main functions into one file, you can reorder them as you wish (i.e., you can put make_groups() first or my_sample() first -- it doesn't matter). This is possible when you build/install the package because when R calls `library(mysterycoffee)` it will load both functions independently.


### Add dependencies within the DESCRIPTION file
If your package is built upon other packages (e.g., 'knitr'), you can list these packages  within the DESCRIPTION file: 

```
Imports:
    knitr
```

# Licenses
Licenses allows you to tell to anyone using your code/package what are the conditions to use or *not* to use your package. If you don't specify a License, although users can technically run your package locally on their laptop, they cannot build upon it, or share it. Note also that CRAN accepts a package only if it has a license specified.

There are two* types of open source licenses:

- **Permissive:** makes your code open source, but do not extend this feat to code made by someone else, even if it derives directly from your code. Examples of this license: MIT, Apache, BSD.
- **Viral:** your licenses extends mandatorily to anyone using your code or building upon it. Example of this license: GPL.

##### *there are many licenses, a compehensive list can be found at: https://choosealicense.com/. 

### Specify a license within your package
The license is specified within the DESCRIPTION file. Let's say that we want to use a *permissive* type of license: Apache.

We *could* modify manually this file, but it is not recommended because it is sensitive to identation. Thankfully, the package `usethis` solves this for you. So, you can type:

```
usethis::use_apache_license()
```
This will automatically add the Apache license to the DESCRIPTION file.

**TIP:** You can explore the wide range of licenses provided by the `usethis` package by typing `usethis::use_` + tab. This will prompt R'studio IDE to suggest you a possible autocompletion (i.e., many other licenses). 

Or you can copy and paste this:

```
library(magrittr)
library(dplyr)

tools::CRAN_package_db() %>%
    group_by(License) %>%
    summarise(count = n()) %>%
    arrange(desc(count))
```

## Feedback

### Tops (what went well?)
- It was very interesting and helpful. Also super nice the note taking service Thanks!
- I think it was very nice to have everything summarized in this document. Thanks a lot for your work!

- It was really informative from the start regarding using existing packages; I'd never had the :: system explained in the past so now I can go back and fix a bunch of code that I can now make better
- The documentation provides a great overview. Thank you.
- Nice to see you take time to cover some seemingly 'unrelated to packages' Rstuff when that comes up in the discussions.
- The collaborative document is idea to maintain the discussion and also to refer back to what we learnt.

### Tips (what can we improve?)
- The level is quite low / pacing is slow so far. Perhaps it could be structured in a way that all users can attend a lesson, then the people with issues can stay and solve those.
    - Thanks for the pacing comments! Completely understand that this is somewhat slow for some R users - we want to make sure everyone is on the same page after week 1. Next week, I believe we will dive deeper and introduce a lot more material that's new to experienced R users. Hope to see you again then :)
- Pacing can be a bit faster. 
    - Thanks for the pacing comments! Completely understand that this is somewhat slow for some R users - we want to make sure everyone is on the same page after week 1. Next week, I believe we will dive deeper and introduce a lot more material that's new to experienced R users. Hope to see you again then :)
- I would have liked to have more information about the licenses.

- Pacing early on was a bit slow for me, but I think it picked up later on.
- Like someone mentioned earlier, I was expecting a course where people fulfills the basic requirement like knowing R/RStudio, which was not the case. So the first week was a lot slower for me.

## 📚 Resources
[CRAN](https://cran.r-project.org/)
[Licensing R](https://thinkr-open.github.io/licensing-r/)
[Visual representation of licenses](https://thinkr-open.github.io/licensing-r/intro.html#a-visual-representation-of-the-licenses)
[tutorial on branches in version control Git](https://www.atlassian.com/git/tutorials/using-branches)
[to integrate python with R](https://www.rstudio.com/blog/three-ways-to-program-in-python-with-rstudio/)
[attaching python code while writing an R package](https://stackoverflow.com/questions/60150956/attaching-python-script-while-building-r-package)
[To update your R](https://www.r-project.org/)
[Renv and Rstudio](https://www.rstudio.com/blog/renv-project-environments-for-r/)
[About semantic versioning](https://semver.org/)
[About metadata](https://r-pkgs.org/Metadata.html)
[About licenses](https://choosealicense.com/)
