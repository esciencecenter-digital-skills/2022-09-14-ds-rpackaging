![](https://i.imgur.com/iywjz8s.png)


# Collaborative Document - week 3

2022-09-28 Reproducible Research with R Packages

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

This is the Document for today: [tinyurl.com/rpackaging-week3](https://hackmd.io/hLOwyjUkQCek-L8Pk0zYyQ?both)

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


## 🗓️ Agenda
Day 3. Wed 28 September 2022
| Time | Topic |
|--:|:---|
| 09:00 	| Welcome and icebreaker
| 09:15 	| Recap and lessons learned
| 10:15 	| Coffee break
| 10:30 	| Documenting your package
| 11:30 	| Coffee break
| 11:45 	| Data, dependencies
| 12:45 	| Wrap-up
| 13:00 	| END

## :ice_cream: Icebreaker
What's your favourite breakfast (of all time!)? 
- Huevos Rancheros (Lieke) OR pancakes with cheese and syrup and hot sauce OR cinnamon buns / cardamom buns from when I lived in Sweden + COFFEE
- Bas: american pancakes
- Jessica: homemade waffles with butter and maple syrup 
- Pim: croissant + espresso
- Martine: cold pizza from the last night, and coca cola (memories of student days)
- Utkarsh: bowl of muesli+cornflakes+some fruits, a good coffee
- Quickly whipped up nasi (from leftover rice) or leftover indian food from dinner (Barbara)
- Anke: homemade pancakes with hot chocolate sauce
- Eric: Ice Coffee and cold pancakes with honey
- Frank: Huevos Rancheros!
- Rodrigo: I prefer sleeping!

## 🔧 Exercises

### Exercise: what is in a README?

[Take a look at this README file](https://github.com/PabRod/kinematics)

What subjects are addressed in this README?
Is there anything that you miss, as a potential user?

- Bas: what does the package do and a lot more
- Jessica: description of what the package entails, how to install it, how to use it (this one is really nicely detailed and easy to read; many are not. I particularly like the part about unit)
- Pim: short description - purpose - installation - usage - examples - citation - license. Missing: nothing much
- Martine: Purpose = the get started info (which includes goals, etc)? Indeed very detailed, love that there are multiple examples
- Utkarsh: Really nice documentation. May be too much in some cases or somebody.
- Anke
- Eric
- Frank: one of the most detailed readme's I have seen; it goes beyond what I would expect: at least a short intro, installation instructions, a basic usage example, and citation/contact information
- Rodrigo: description + installation + usage + examples + citation + authors + license / missing: a separate example script
- Samar
- Venus
- Joshua:  I think its too much =/, I would just like to know which problem this package attempts solve (and whether that is also my problem).

### Exercise: create a roxygen skeleton, and fill it out!
- Anke
```r
#' hello
#'
#' A function printing "Hi" followed by input name.
#' @param first_name is the input name. 
#'
#' @return message "Hi" followed by input name.
#'
hello <- function(first_name) {
  print(paste("Hi", first_name))
}
```
- Bas
```r
#' Title: calculate_distance
#' Calculates the geodetic distance between two points
#' 
#' @param XStart vector of starting longitude points
#' @param XEnd vector of ending longitude points
#' @param YStart vector of starting latitude points
#' @param YEnd vector of ending latitude points
#'
#' @return A vector with path lengths in kms
#' @export 
```
- Eric: done
```r
#' Title
#' Checks sample names in input df and substitutes special characters, creates RDS object which contains group info variable, checks if input df contains labelled data
#' @param dataframe_from_Excel input dataframe created from MS_data.xlsx file
#'
#' @return dataframe with adjusted sample names
#' @export
#'
#' @examples
```
- Frank done
```r
#' Title
#' Extracts Xi Optics from point data
#'
#' @param filename a csv containing x,y coordinates in columns 7,8
#'
#' @return a dataframe with the csv content and the cluster ID added as column
#' @export
#'
#' @examples
```
- Jessica: done - 
```r
#' Title
#' Ingests pdf file as a list and selects required part of that list
#' @param pdfinput a pdf file of received emails
#'
#' @return a list containing the selected email data 
#' @export
```
- Joshua: 
```r
#' answer_me
#'
#' Answers all your questions!
#'
#' @param input <- A string containing a question.
#'
#' @return Returns an answer to your question
#' @export
#' @examples
#' Example 1
#' answer_me() #Returns a input prompt.
#'
#' Example 2
#' answer_me("How are you feeling today?")
```
- Martine: done
- Pim: 
```r
#' MysterycoffePlanner
#' This package allows you to input a vector containing names, and the functions
#' will create a matrix of pairs, including their drink of choice which is
#' randomly assigned.
#' @param names a vector of names to be grouped
#'
#' @return a matrix with matched names & their drink of choice
#' @export
#'
```
- Rodrigo
```r
#' Title 
#' Hello friends
#' @param ncat a number or a character
#'
#' @return an expression according to the value given
#' @export
#'
#' @examples
```
- Samar
- Utkarsh
```r
#' Title
#' Color Pallete
#' The function gives a list of mentioned number of distinct color hex values
#'
#' @param n : number of distinct colors to be chosen
#'
#' @return list of `n` distinct hex values representing colors
#' @export
#'
#' @examples
```
- Venus

```r
#' Title
#' Reads columns from a data table
#'
#' @param filename a string filename including the relative
#' @param select_columns a vector including the column names from the data file
#'
#' @return if succeds, this function returns a data table
#' @export
#'
```

### Exercise: run ‘Check’ 

Run the ‘Check’ function (either with the button, or with devtools::check(). Look for information about your dependencies in the resulting text. Are any dependencies missing, or declared dependencies unused? Copy the warnings you get (only those about dependencies!) below.

- Anke: no warnings
- Bas: 
```
-- R CMD check results -------------------------------------------------------------------------------------------------- brainlink 0.1.0 ----
Duration: 18.3s

> checking DESCRIPTION meta-information ... WARNING
  Non-standard license specification:
    What license is it under?
  Standardizable: FALSE

> checking for future file timestamps ... NOTE
  unable to verify current time

0 errors v | 1 warning x | 1 note x
```
- Eric:
```r
 checking dependencies in R code (985ms)
   '::' or ':::' imports not declared from:
     'Hmisc' 'WriteXLS' 'filesstrings' 'forcats' 'ggplot2' 'ggridges'
     'gplots' 'randomcoloR' 'stringi' 'tibble' 'tidyr'
   Namespace in Imports field not imported from: 'readxl'
     All declared Imports should be used.
```
- Frank: only errors from wrong tests that I need to fix
- Jessica: '::' or ':::' import not declared from: ‘stringr’
- Joshua: '::' or ':::' import not declared from: ‘jsonlite’ 
fixed using: ```rusethis::use_package("jsonlite")```
- Martine: > checking package dependencies ... ERROR
  Namespace dependency missing from DESCRIPTION Imports/Depends entries: 'rlang'. Adding this to DESCRIPTION and rechecking: now two other packages not there (scales, tidyselect), so added them as well. can also be done by typing in the DESCRIPTION file. "R CMD check succeeded" jippie. i do get a lot of "no visible binding "messages.
- Pim:
```r
v  checking dependencies in R code ... 
```
- Rodrigo: `
    ```r
    * checking dependencies in R code ... OK
    ```
- Samar
- Utkarsh
- Venus
```r
❯ checking dependencies in R code ... WARNING
  '::' or ':::' imports not declared from:
    ‘data.table’ ‘dplyr’ ‘ggfortify’ ‘ggplot2’ ‘htmlwidgets’ ‘jsonlite’
    ‘jsonvalidate’ ‘plotly’
```

#### Don't write here: list of participants for future exercises ####
- Anke
- Bas
- Eric
- Frank
- Jessica
- Joshua
- Martine
- Pim
- Rodrigo
- Samar
- Utkarsh
- Venus

```r
```


## 🧠 Collaborative Notes

### Recap & Discussion

#### Points to note:
 - During testing, test elements of the package that have a fixed behaviour (functions/expected output). Do not test for transient behaviour unless relevant within the function (datasets).
 - Make tests for output, not for input. Input checks (on user input) can be in the function - this also ensures that the function does not fail when incorrect inputs are provided.
 - Ensure that an existing package does not have the same name as your package to avoid overlap 
     - Check CRAN
     - Check Google
     - Check Github (Good luck with that!)
 - In testing, you want to hard code inputs and outputs - opposite to functions. You want to make sure that functions explicitly output something when given a certain input.
- Test scripts are always stored in the `tests/` folder.
    - Testthat package tends to use the `tests/testthat/` folder 
- Add data to package if user needs access to the data. Otherwise, create an `R` object which ensures that only the tests have access to the data.
- usethis::use_test(`<name>`) will generate the file called `test-<name>.R` in the tests/testthat folder


### Documenting your package

#### Readme file:
- Exists in root folder of the project with the name `README.md`
- The file gives a first introduction of the package on what the package is supposed to do - it can include motivation, application, installation, etc.
- It is good practice to always include a README, especially in github repositories.
- Sample `README.md` for the Mysterycoffee package (format: text file or R Markdown):
```
# Mysterycoffee: A package to plan online coffee meetings

This package contains a function that randomly pairs up 
colleagues to have coffee together. You need R.
```

#### Documenting functions with `roxygen2`:
- `roxygen2` allows the addition of a standard template for documentation in your`R` package 
- Manual configuration for `roxygen2` to work:
    - Delete the `namespace` file
    - Delete the `man` folder
    - In the upper right panel, go to `Build > More > Configure Build Tools`.
    - Tick `Generate documentation with Roxygen`.
    - Tick `Install and restart`.
    ![menu](https://i.imgur.com/n9wk6ro.png)

- To create a skeleton, click `Code > Insert Roxygen skeleton`
![](https://i.imgur.com/zBzfYW0.gif)

- The `Roxygen` skeleton contains multiple fields - for more information on the definition on these and other optional parameters check the [roxygen2 documentation](https://cran.r-project.org/web/packages/roxygen2/vignettes/roxygen2.html)
- Each parameter of the function automatically gets its own line in the roxygen skeleton.

- A sample `roxygen2 skeleton` for `Mysterycoffee` function `make_groups`
    ```r
    #' Make groups of 2 persons
    #'
    #' @param names a vector of names
    #'
    #' @return A re-arranged matrix of names
    #' @export
    ```

##### Building documentation:
- With the `Build` command
![](https://i.imgur.com/CnCb9h2.gif)
- or use the console command `roxygen2::roxygenise()`, or `devtools::document()`

- The documentation files are stored in `man/`

##### `@export` argument: 
- The `@export` argument ensures that the function is available to the users for use.
- If the function is not to be accessible to the user, you can remove the `@export` argument.
    - The function still exists and is accessible to other functions in the package but not directly to the user.
    - Regardless of `@export`, the documentation file is created and is accessible throughout.

### Dependencies

##### Checking code:
- Run with:
    - `Build -> Check` command:
    - Can also be run with `devtools::check`
- Performs a detailed check of the package including:
    - dependencies in the code
    - tests

##### Dependencies:

- To add a new package dependency, use `usethis::use_package("package_name")`
- In `DESCRIPTION` document:
    - `Imports:` are packages that are mandatory for functions to work.
    - `Suggests:` are packages that are recommended as dependencies. 
- To add package to a specific field (Imports or Suggests): 
    `usethis::use_package("tidyr", type="suggests")`
- To remove dependencies, delete the package from `DESCRIPTION`
- To limit the minimum version of a dependency:
`usethis::use_package("dplyr",min_version = "1.0.0")`
- To limit all the current dependencies to their latest version as used in the package:
`usethis::use_latest_dependencies()`

##### Versioning:
The three numbers in a version of a package (say, `x.y.z`) are:
 - `z` is a patch number which indicates a minor update/bug fix to the package
 - `y` is the minor version number which indicates substantial work but no change in how the package works.
 - `x` is the major version number which indicates a break in functionality due to major updates/changes to the package.


## Feedback
### TIP
- Very very useful information, thank you
- The shared document is a great idea, and the helpers are really doing a great job adding all here
- Referring to other sources with helpful information
- Time taken to answer questions
- I found out today, just browsing through to use_this functions, because I thought there should be a function for it: There is also a `usethis::use_readme_md()`, so no need to make a new txt and save it as "readme.md". This function also creates some skeleton content, already with the name of the package. (MJ)
- (i always used to think that tips were recommendations, and tops were things to keep but here goes:) i really liked the structure: lecture > action/homework > feedback+ lecture > action/homework. this way you learn more.

### TOP
- The flow is not constant, it is usually getting interrupted. Perhaps it's better to explain everything at the beginning and then we test/ask questions.
- I liked the quick overview of the different topics. Really useful since I'm not actively building a package atm, so general info is nice to have. 
- Addition of examples of tests on more complex functions.
- (i always used to think that tips were recommendations, and tops were things to keep but here goes:) as described before me, a great deal of time was given to answering very in-detail questions (which is also a top), however, in an online session it is hard for the remaining people to stay in the flow.



## 📚 Resources
[Testthat documentation](https://testthat.r-lib.org/reference/index.html) which contains a list of `expect_` functions.

[Pablo's README file](https://github.com/PabRod/kinematics/blob/main/README.md)

[Markdown syntax](https://www.markdownguide.org/basic-syntax/)

[Use this - summary](https://usethis.r-lib.org/index.html)

[Introduction to renv](https://rstudio.github.io/renv/articles/renv.html)
    