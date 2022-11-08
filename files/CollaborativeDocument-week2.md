![](https://i.imgur.com/iywjz8s.png)


# Collaborative Document - week 2

2022-09-21 Reproducible Research with R Packages

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.


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
Day 2. Wed 21 September 2022
| Time | Topic |
|--:|:---|
| 09:00 	| Welcome and icebreaker
| 09:15 	| Recap & lessons learned, Testing (part 1)
| 10:15 	| Coffee break
| 10:30 	| Testing (part 2)
| 11:30 	| Coffee break
| 11:45 	| Test-driven development
| 12:45 	| Wrap-up
| 13:00 	| END


## 🔧 Exercises

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

**Put your name in the table if you did the following:**

| Topic | I did this! |
|--:|:---|
| Create a package structure for my own project	|   |
| Write additional functions for the toy package `mysterycoffee` 	|  |
| Improve the existing `mysterycoffee` functions | |
| Run into issues 	|   |
| Add a license to my own project | |
| Come up with questions |  |
| I created a package to plot a projection from PCA |  |


<details><summary>Function for XXX</summary>
<pre><code>
#For XXX

########add statistics column########
#the name stat_mat is derived from "statistics matrix" because the function expects a statistics matrix.

create_matrix <- function(stat_mat, threshold.lb, threshold.increment_unit, n_bootstraps ) {

  rownames(stat_mat) <- paste0("threshold_", seq(threshold.lb, threshold.ub, threshold.increment_unit))
  colnames(stat_mat) <- 1:n_bootstraps
  stat_mat.boot.app <-  matrix(nrow = length(seq(threshold.lb, threshold.ub, threshold.increment_unit)),
                                ncol = n_bootstraps)
  return(stat_mat.boot.app)

}
##########################################################
##########################################################
##########################################################

#example usage (this is how to call the function from from your script.)

###Required inputs#####
threshold.lb <- 1
threshold.ub <- 1
threshold.increment_unit <- 1
n_bootstraps <- 1

#statistic#
#statistic needs to be a matrix similar to accuracy.boot.app, true_positive_rate.boot.app, true_negative_rate.boot.app in your script)

statistic <- matrix(nrow = length(seq(threshold.lb, threshold.ub, threshold.increment_unit)),
                    ncol = n_bootstraps)

####example 1##
accuracy.boot.app <- create_matrix(statistic, threshold.lb, threshold.increment_unit, n_bootstraps)

####example 2###
true_positive_rate.boot.app <- create_matrix(statistic, threshold.lb, threshold.increment_unit, n_bootstraps)
</code></pre>
</details>


#### Room 4

List questions here:
- **Q: How to specify package for functions like `%>%` and `{{..}}`, since `::` not really possible?**
- *A: Just specify the library in your function with `library(...)`*
- *A: Better do:  NB! This will probably only work with Roxygen!*
- ```
  #' @import magrittr
  NULL
  ```
-  Until that time, see [this stackoverflow](https://stackoverflow.com/questions/27947344/r-use-magrittr-pipe-operator-in-self-written-package) question.
- **Q: Can I use `require(library)` inside a function?**
- *A: We'll get back to that.. :see_no_evil:*
- **Q: When would you advise to combine functions in one file over 2 seperate functions each in a seperate .R file?**


```
 # TODO: investigate namespace for print(summary(tpca))
  # load `.__T__[:base` to fix `! Objects of type prcomp not supported by autoplot.`
  library(ggfortify)
  ggfortify::`.__T__[:base`
  p <- ggplot2::autoplot(tpca, data = cols, colour = colorear,
                         loadings = pbiplot, loadings.colour = 'black',
                         loadings.label = pbiplot,
                         loadings.label.colour = 'black',
                         loadings.label.size = 4) + ggplot2::theme_bw()
  p <- p + ggplot2::labs(title = lp$title,caption = lp$caption)
  p <- p + ggplot2::theme(plot.title = ggplot2::element_text(hjust = 0.5))
  print(p)
```

#### Exercise: what does this test do?
Open a newly created testfile (after running `usethis::use_test([function])`, you will find it in `/tests/testthat/`) and take a look at its contents. It should contain something like this:

```r
test_that("multiplication works", {
  expect_equal(2 * 2, 4)
})
```

This is just an example test, that was created to make your life easier. You can use it as a template for writing your own tests.

Take 10 minutes to:
- Figure out what is happening inside this test. Can you understand it?
- Write another test, just below this one, that checks that addition also works. Tip: you can copy-paste and edit the current test.

Answers:
-  do we need to have library(testthat), it will not run without having the package loaded? I see X mentioning the run tests button, did not notice the button before. (A: Not in your test, but you do need to have the testthat package)
```
test_that("adding works",
    { expect_equal(2 + 2, 4)
    })
```
-   - done:
test_that("addition works", {
  expect_equal(2 + 2, 4)
})
'''

-   test_that("addition works", {
  expect_equal(3 + 3 , 6)
})

-  : done
-  : test_that("math works", {
  expect_equal(2^3, 8)
})

-   - done - test_that("addition works", {
                  expect_equal(2 + 2, 4)
               }) #and then click 'run tests'
-
-
-
 ```r
    test_that("addition works", {
    expect(2+2 == 4, failure_message = "Addition failed")
 ```
-
    test_that("tests (exponent) work", { expect_equal(10**2,100)})
-  : more fun:
    test_that("addition doesn't work", {
  expect_equal(2 + 2, 3)
})
-
`test_that("four people equals two pairs", {
  expect_equal(nrow(matrix(c("Bob", "Steve", "Mary", "John"), 2), 2)
})`
-
```r
test_that("addition works", {
  expect_equal(2 + 2, 4)
})
```
-  : done
    ```r
        testthat::test_that("addition works", {
          testthat::expect_equal(2 +3455, 3457)
        })
    ```
-  : done
     usethis::use_testthat("addition works", {
  expect_equal(2 + 2, 4)
})





#### Exercise: write your own test.
Now it is your turn to write a test. With a vector of 6 names as input, check that the output of `make_groups()` is a matrix with 3 rows and 2 columns.

Tip 1: tests can contain multiple assertions.
Tip 2: the functions `nrow` and `ncol` may come in handy.

-  : i ran into an issue with the `{{` testthat::quasi_label(enquo(expected), expected.label, arg = "expected") , have to adjust that i guess, so i will think on another test
-
    ```r
    test_that("test that input length is same as output length", {
  XStart <- 7.5
  PathLength <- calculate_distance(7.5, 7.8, 80.1, 80.2)
  expect_equal(length(XStart), length(PathLength))
  expect_false(is.null(PathLength))
    })
    ```
-
    ```r
    test_that("number of columns is two", {
  test_names <- c("Larry", "Mieke", "Sjoerd", "Cindy", "Jin", "Adebayo")
  new_groups <- make_groups(test_names)
  expect_equal(ncol(new_groups), 2)
})

test_that("number of rows is three", {
  test_names <- c("Larry", "Mieke", "Sjoerd", "Cindy", "Jin", "Adebayo")
  new_groups <- make_groups(test_names)
  expect_equal(nrow(new_groups), 3)
})

-
-  :
    ```r
    # With a vector of 6 names as input, check that the output of make_groups() is a matrix with 3 rows and 2 columns.
    test_that("With a vector of 6 names as input, check that the output of make_groups() is a matrix with 3 rows and 2 columns.", {
      instructor_names <- c("Uttie", "Rodri", "Dani", "Mia", "Aldo", "Lucas")
      grouped_names <- make_groups(instructor_names)


      expect_equal(ncol(grouped_names), 2)
      expect_equal(nrow(grouped_names), 3)
    })
    ```
-  :
    ```r
    test_that("number of elements in function equals input", {
      namedLetters <- c("A","B","C","D","E","F")
      grouped_names <- make_groups2(namedLetters)

      testthat::expect_equal(ncol(grouped_names),4)
      testthat::expect_equal(nrow(grouped_names),floor(length(namedLetters)/2))
    })
    ```
-
    ``` r
    test_that("nrows = 3, ncol = 2" {
    instructor_names <- c("1", "2", "3", "4", "5", "6")
    grouped_names <- make_groups(instructor_names)

    expect_equal(nrow(grouped_names), 3)
    expect_equal(ncol(grouped_names), 2)
    })
    ```
-

    ```r
    test_that("Test that the plot is created", {
      plt <- pcaproj("parameters.json")
      expect_equal(class(plt)[2], "ggplot")
    })
    ```


-
    ```r
    test_that("The matrix follows the expected dimensions", {
  instructor_names <- c("Barbara", "Lieke", "Ji", "Eva", "Pranav", "Djura")
  grouped_names <- make_groups(instructor_names)

  expect(ncol(grouped_names)==2, failure_message = "too many columns!")
  expect(nrow(grouped_names)==3, failure_message = "too many rows!")})
    ```

-
```r
test_that("Color pallete of distinct colors", {
  numColors <- 10
  colPallete <- get_pallete(n = 10)

  expect_equal(length(colPallete), numColors)
})
```


-
-
```r
test_that("demo",{
  these_names <- letters[1:6]
  group_names <- make_groups(these_names))
  expect_equal(nrow(group_names), 3)
  expect_equal(ncol(group_names), 2)
 })
```

-
```r
test_that("number of rows/columns in function equals input", {
  names_list <- c("A", "B", "C", "D", "E", "F")
  grouped_names <- make_groups(names_list)

  expect_equal(nrow(grouped_names), 3)
  expect_equal(ncol(grouped_names), 2)
})
```
-
    ``` r
        test_that("make_groups works well", {
            instructor_names=c("B","L,"J","E","P","D")
            grouped_names=make_groups(instructor_names) ##I dont remember how this function groups people, I guess by pairs
            expect_equal(ncol(grouped_names), 2)
            expect_equal(nrow(grouped_names), 3)
        })
    ```

-

## 🧠 Collaborative Notes

### Takeaways from homework

1. Using a function from a package with `::` is not always possible. In this case, the package can be imported at the beginning of the script like the following (more next week, uses roxygen):

```r
#' @import package_name
NULL
```

by replacing `package_name` with the concrete package.
- `{{  }}` is from `rlang`
- `%>%` is from `magrittr` (should native pipe `|>` be better, now it exists?)

2. Using `require()` inside a function is not a good practice.
3. Don't add any dependency unless you have to, since there is always a cost to load package.
4. Think about what your functions are doing, and try to make functions for each step.

### Topic 1: Testing

Developers write tests because they want to keep track of any possible change that may cause their code to fail.

Manual testing is to run your function from console and see if you got the expected output. This process can be automated, and this is known as automated testing.

#### *Initialization*

Tests are expected to be in the `tests` folder of the project. To initlaize the test folder and file, run the following in the console:

```r
usethis::use_testthat()
```

To write test for a specific function, run

```r
usethis::use_Test('function_name') # replace function_name with the desired function
```

, and this will generate the `test-function_name.R` file in the `testthat` folder.

**NB**: It is a good practice to always link your function and test with the same name.

#### *Write your own tests*

A sample test looks like this

```r
test_that("multiplication works", {
    expect_equal(2 * 2, 4)
})
```

, where `"multiplication works"` is a description of what the test should do, and `expect_equal(2 * 2, 4)` indicates the expected behavior/output from the function.

To perform a negative test, you can use `expect_false` with a expected failed condition (e.g., `expect_false(2 + 2 == 3)`). There are many useful statements other than `expect_equal` and `expect_false`.

You can do more complex things in a test, see the example below:

```r
test_that("number of elements in function equals input", {
    instructor_names <- c("Barbara", "Lieke", "Ji", "Eva", "Pranav", "Djura")
    grouped_names <- make_groups(instructor_names)

    expect_equal(ncol(grouped_names), 2)
    expect_equal(nrow(grouped_names), 3)
})
```

, which checks if the output matches the expected row and column size.

**NB**: It's possible to have multiple tests for a single function.

#### *Run your tests*

To run the tests, click on the `More` button in the `Build` tag on topright of the Rstudio interface, and then `Test Package`. Or, run the following command in the console:

```r
devtools::test()
```

You will see the testing results in detail.

#### *Test with data*

If you have a test data file, say `testdata.Rda` in the `testthat` folder, that is generated by the following code:

```r
instructor_names <- c("Barbara", "Lieke", "Ji", "Eva", "Pranav", "Djura")
save(instructor_names, "../tests/testthat/testdata.Rda")
```

and you want to use this file in the test above, you can replace the assignment statement with the following:

```r
load("testdata.Rda")
```

**NB**: if you want to have yout test data in other formats, the files will have to be stored in some other folders (depending on which format).


### Topic 2: Test-driven development

For test-driven development, an important goal of writing tests is to formalize how the code should work. A recommended route of doing this is to firstly write your tests, and then write/refactor your code to make these tests pass.

For instance, if you want the `make_groups` function to not accept dataframe, but only vector as input, you can first write a test like the follows

```r
test_that("Data frame not allowed as input", {
    df = data.frame(1:10, 11:20)
    expect_error(make_groups(df), "Input must be a vector!")
})
```

With this new test, your old code may fail. To make it pass, add the following code to the `make_group` function

```r
if(!class(names) %in% c("character", "integer")) {
    stop("Input must be a vector!")
}
```

And now the new test should pass as well.

## 📚 Resources
[About the R vs Magrittr Pipe]( https://kpress.dev/blog/2022-06-19-replacing-the-magrittr-pipe-with-native-r-pipe/)
[Yihui Xie's "Substitute the magrittr Pipe with R's Native Pipe Operator" ](https://yihui.org/en/2022/04/magrittr-native-pipe/)
[Best practices for writing R code](https://swcarpentry.github.io/r-novice-inflammation/06-best-practices-R/)
[Testthat documentation](https://testthat.r-lib.org/reference/index.html) which contains a list of `expect_` functions.
