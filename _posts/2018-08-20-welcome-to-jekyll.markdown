---
layout: post
title:  "TDD For Beginners"
date:   2018-08-20 22:46:07 +0700
categories: tech method
---

***"I decided to start anew, to strip away what I had been taught." - Georgia O'Keeffe***

When I first saw TDD were being best practice and requirement for hiring engineers, I have no clue what is this thing and why it is so important for development process and life cycle of apps. Started search for the TDD keywords on Google, read bunch of artciles and books, and ask to colleagues until I found that TDD is so deep and excite me to learn it. At first, it was mind-blown how a line of code could ruin your tests and refactoring it could be more fun. The repetition of this cycle of development process is enjoyable and decide me to write this opinion and (maybe) facts.

# What is TDD ?
Test Driven Development (TDD) is a programming practice or development technique that instructs engineers to write code only when tests are failed. So tests are being written first before every logic of the bussiness written as code. But that does not mean `lets write some of test and write code that pass the tests` OR `lets replace QA job with our tests code`. To write test you must know and understand what your inputs and what your expected outputs. Every single functionality has its own test, even bunch of tests would do. Coverage your code with tests, the more it coveraged the more it will be a good code base. TDD wont replace QA job but it will make your code less bugs and make QA do the job more efficient and flawless because you already cover test cases that might be bugs (if you did not use TDD).

# Why TDD ?
There is traditional testing when you already done the functionality of your system. Sometimes it is good and make it fast for development process but very often it will cause bugs. When you try this way, codes are done before you tests therefore you are unable to discover what is missing with the code untill some of the functionality failed. In TDD, you write test before the code itself. Not because there is no reason, but because it is what you need to start in every reps.

There are some people experienced that TDD did not work but there is more than that people that experienced TDD is an awesome way to do the development process. Here is a few reason why it did not work:
+ For those who work with a non-TDD way might wont use this method due to its time investment.
+ Some of them did not have enough knowledge about writing test case on unit test framework.
+ Very fast reps needs more time too for maintenance and refactoring the code.
Here is a reason why you should do TDD instead *trial and error* development process:
+ Automated test. When you do TDD, you will invest time to write test first before code. It is challenging also safe you another day and time compared to manually test the functionality.
+ Tests will runs in every reps or builds. Just in case you accidently delete `one line of code` that might ruin your system, test cases will run automatically in every build to make sure everything you add or change is fine with every its functionality. At this point, it will gain confidentiality of deploying and the quality of products.

# How TDD ?
When I did TDD on my first time, I experience lack of knowledge and hesitation then I realize that `we just need a little start` and when it is done, you just need to improve and repeat it. There is a simple rule to start development process within TDD called `Red . Green . Refactor` that helped me a lot to understand how to start and doing TDD all the time.
## Red
This is where you start. Every functionality that you would develop this is `the first phase`, means writing tests.