---
layout: post
title:  "TDD For Beginners"
date:   2018-08-31 20:33:12 +0700
categories: tech method
---

***"I decided to start anew, to strip away what I had been taught." - Georgia O'Keeffe***

When I first saw TDD, it were being best practice and requirement for hiring engineers. I have no clue what is this thing and why it is so important for development process and life cycle of apps. Started search for the TDD keywords on Google, read bunch of artciles and sites, and ask to colleagues about it. Until I found that TDD is so deep and excite me to learn it. At first, it was mind-blown how a line of code could ruin your entire apps without it. I decided to try TDD with writing tests and refactoring code, and I have lot of fun with it. The repetition of this cycle of development process is enjoyable and decide me to write this opinion and (maybe) facts.

![TDD + Pair Programming!](/images/tddpair.jpg "TDD Pairing")

## What is TDD ?
Test Driven Development (TDD) is a programming practice or development technique that instructs engineers to write code only when tests are failed. So tests are being written first before every logic of the bussiness written as code. But that does not mean..
> "lets write some of test and write code that pass the tests"

OR

> "lets replace QA job with our tests code"

To write test you must know and understand what your inputs and what your expected outputs. Every single functionality has its own test, even bunch of tests would do. Coverage your code with tests, the more it coveraged the more it will be a good code base. TDD wont replace QA job but it will make your code less bugs and make QA do the job more efficient and flawless because you already cover test cases that might be simple bugs or just typo.

There is two approach of TDD, *bottom-up* and *top-down* depend on system or application requirement. When information/requirement gathered and collected, you start doing TDD and so on regarding to the requested requirement &mdash; this what called *top-down* because you already know every function of your system behavior. When you don't have requirement or not enough/lack of information to create system, you might want to do TDD slowly grow by the time you code &mdash; this what called *bottom-up* because you didn't know the behavior of the system before you write the code. Find yourself a right approach due to the project needs.

## Why TDD ?
There is traditional testing when you already done the functionality of your system. Sometimes it is good and make it fast for development process but very often it will cause bugs. When you try this way, codes are done before you tests therefore you are unable to discover what is missing with the code untill some of the functionality failed. In TDD, you write test before the code itself. Not because there is no reason, but because it is what you need to start in every reps.

There are some people experienced that TDD did not work but there is more people experienced TDD is an awesome way to do the development process. Here is a few reason why it did not work:
+ For those who work with a non-TDD way might wont use this method due to its time investment.
+ Some of them did not have enough knowledge about writing test case on unit test framework.
+ Very fast reps needs more time too for maintenance and refactoring the code.

Here is a reason why you should do TDD instead *trial and error* development process:
+ Automated test. When you do TDD, you will invest time to write test first before code. It is challenging also safe you another day and time compared to manually test the functionality.
+ Tests will runs in every reps or builds. Just in case you accidently delete `one line of code` that might ruin your system, test cases will run automatically in every build to make sure everything you add or change is fine with every its functionality. At this point, it will gain confidentiality of deploying and the quality of products.

## How TDD ?
When I did TDD for the first time, I experience lack of knowledge and hesitation then I realize that `we just need a little start` and when you do, you just need to improve and repeat it. There is a simple rule to start development process within TDD called `Red . Green . Refactor` that helped me a lot to understand how to start and doing TDD all the time.

### Red
This is where you start. Every functionality that you would develop. This is `the first phase`, means writing tests. For example, when you want to build a function it has to be a blank line of code. Write the test first for what you expect from the function to return or generate. In Go you could use their simple test framework or use another tools called `testify`, in Java you could use `JUnit`, in PHP you could use `PHPUnit`, and I believe every programming language support for test environment.

> Test environment and writing test before code is important. This culture should be mandatory for every developers or software engineer to cut-down their time for manually testing and fixing bugs that might caught from automate tests.

After write the test, run its command to check and it should be red (**`means the tests fail caused by wrong return or generate from the function`**). Because we didn't implement the function yet. After this phase, you might already know what function's behavior and it should be before you write the test. Let's go into the next phase.

### Green
You start write the function at this phase. Every logic in it and return/generate appropriate information or data. When you run the tests again, you find it works (assume that you are doing it right). Now, you might be wondered it is easy and simple because you already know the tests. That's might be right but what actually happened is, your brain think about what test should cover the function and you found several test should cover it and then you start code because you think the code (function) before write the test.

This phase would pass the tests since you already know what to do with the code. Everything should work like it meant to be at this phase. Eventhough sometimes your code seems wastefull and not efficient, but at least it is work like the function behavior.

### Refactor
The code should be refactored if there is something could be more simple and efficient. The key is ***Don't Repeat Yourself (DRY)***. When you have a repeated lines of code or some variable defined twice or have similiar responsibility, you have to make it simple and efficient. By meaning this should be done once and use it everytime when its needed.

Refactoring code is wasting time eventhough sometimes you need this phase because you want to improve your code quality and readability. But it is nice to have and keep in mind a readability code right the time when you write the code.


### Wrap it all!
Now, lets abstract it right before you write test. Write down the function behavior and what you expect for the function to work properly. Don't think about the test yet either the code of its implementation. Think and write down about the function. After that, write down what should you cover or expect from the function. When the list is up, then try to write tests code. Do it like you mean it, start and keep expect returns from the function for every different parameters including the negative tests. This is what you would do likely in the **RED** phase.

After you done with the test, it's time to read the test again and start implement code to the function regarding the tests. The goal is to make sure the function would turn tests into **GREEN** when it's executed. This phase is that simple. You look something in the test are vulnerable, then fix it at the function.

It's done by turn **RED** tests into **GREEN**, and you might check the code again and want some **REFACTOR** because the codes are a mess. It's okay and you should go ahead, but don't forget to run the test again after you done.

When you build this alone (wihtout pairing) that it's quite easy and predictable for the behavior, test, and what syntax you would write down to the code. But, that's the actual problem. If you don't pair programming, then you only think one-sided implementation. Not to mention, even if someone experienced/advanced in TDD would found this not the best practices and hard to implement two-sided implementation, the tests and the code (function) seperately-thinking. This is where pair programming helps who want to implement TDD.

## Pair Programming
> It's about two programmers working together at one workstation &mdash; one pc, one keyboard, one mouse, one monitor.
> One programmer is the **driver** and writes code. The other is the observer or **navigator** who reviews each line of code as it is typed in.

To do pair programming, both have to agree for what they want to build including used tech stack. They sit together on one code base and talk about it and breaking the tasks/problems down.

You might think that it seems like not effective method to develop a system because we use **two programmers** which could both be build different features for a month. And at the end of the month, we will have more features coming up. But this is could led you into catasthropic system bugs because it might not robust and resilience as you did when pairing.

### Pair Profit!

You might wondering about what is the profit of doing this thing instead of regular way. Well, I'm telling you these are the profit.

#### Mistakes and Bugs caught!
If one of you are doing something wrong, then the other one could help you to find which one that is wrong. This could be something stupid like typo or even the entire approach or strategies are wrong. The pair, one of you, might encounter this problem before and might be have the answer before you go *wrong* deeper.

#### No Procrastinate!
In managed team or big company, there is project manager and you could tell them you are on schedule, you are just lying around to gain some free time to do something else that you might enjoy more. When you pairing, things getting more bigger, like you could end up two times more spend time for code instead of relax and chill at your seat waiting for time is up to go home.

#### Supportive!
When you shared a problem by your pair, you felt that this problem should be done and we have to try something else to make this thing works. By the time, you and your pair would support each other rather than pointing fingers and keep blaming each other.

#### Transfer Knowledge, **Unconsciously**
This is what I like when do pairing, you *unconsciously* transfering or being transfered a knowledge of the projects. Whether it is business, tech, best practices, tools, paradigm, ideas, innovations, fundamental, or a way to solve problem. That way, when you have new employee that don't know about the project or even programming language are being used to the project, you could easily assign a pair to do the timeline of the project. The goal is still, done the project. But, the skill would grow much bigger than self-taught employee.

#### The Satisfaction
This one could affect entire company employees. When you did pairing, you code together, talk and discuss about something together and it is done for hours in a day. Day by day, you would be more closer by sharing experience with your pair and have such in common to do with. Even lunch or after office hour you could hangout and have lunch/dinner together with other people and connected wider to different people. This effect could reduce your employee to change turn into another company caused by social-mental problem. For some people, this satisfaction of being connected and help other people would make them stay loyal and keep the spirit for go to work as well.

### Pairing Goes Bad

Cool that pairing has more profit of something you might need. But don't make it wrong, pairing also has its *darkside* when you did these.

#### Complexity
When you got complex problem to solve with your pair, you and your pair start thinking what should be done by lines of code and write it down to the IDE and *voila!*, here comes the complex code &mdash; a mess that every programmers don't want to work with. Yes, this is bad. Sometimes when complexity getting higher you should discuss it together not about the code instead, you should explain and draw the problem and found the solution. It would be more efficient than write solution in code without discuss it before.

#### Credit Goes To?
You and your pair did perfectly a well-done job. Everyone especially your project manager are happy, your user are very pleased about the result. They congrats you OR your pair individually when they meet you at the cafe or when you go to toilet you meet them or just passing by and they say thanks for your work. What did you do to reply the compliment? Yes, you should tell them about how you AND your pair did the work, **not just by yourself** eventhough sometimes this become an objective matter that who did that and who did this. But on top of that, you should make the ownership of the project is both, you and your pair.

#### Too much!
I want to explain what `too much` mean in this aspect, pair programming. You do pairing all day long and did not have any other activities like talking with other teams and learn new tech or tools or maybe read bunch of books. When forcing someone to do this, it's bad. They, the pairs would end up hate each other and wont do the work as a pair. The ego would raise because of this. And the project either the timeline and purposes would messed up and this is why pair programming wont work. Just make sure you and your pair have their time to do something personal. Do two or three hours a day to do pairing is good, not lower not higher than that, thought it would be good for both pairs and company.

There might be one more thing that would be that `too much` is when you or your pair or might be both of you stressed and tired. Well, this is bad because it could cause any other problems between the pairs, for example bad communication would end up the code is not good. So there should be a time to relax yourself or let your pair take a rest for a bit before do pairing again.

## Conclusion

TDD is good, even if you just try with small projects that had fewer tests. It covers a small bugs or typo that programmers facing early and really often. Rather you do `GREEN` first before `RED`, in TDD we found `RED` should be the first thing to do. A good time to use TDD is when you have support and have more time than before to implement the project whether *bottom-up* or *top-down* depends on the project.

Mind that you have option to implement TDD with pair programming. This would help most of people that did not TDD before. Pair programming is helpful and being used by tech companies and solve complex problems. When pairing is done with its best practices, the benefits would come to the projects. Whether it is more robust or resilience, and to the pairs themselves to get more knowledge technically and mentally.