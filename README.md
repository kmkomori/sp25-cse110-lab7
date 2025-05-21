# CSE 110 Lab Week 7 - Unit & E2E Testing 
## (Members: Roy Lee and Kumiko Komori from Group 28)

1) Where would you fit your automated tests in your Recipe project development pipeline? Select one of the following and explain why.

   **1. Within a Github action that runs whenever code is pushed**
   2. Manually run them locally before pushing code
   3. Run them all after all development is completed

    We would fit our automated tests within a Github action that runs whenever code is pushed. The reason we chose this option is because it gives us feedback on every single one of our code edits immediately and automatically (not having to be manually run, and won't get forgotten). This can help us find issues immediately after they are introduced to the code base. It also supports the idea of having a CI/CD pipeline, and ensures all the code we make public is bug free.

    The other options are not ideal as having to manually run tests leads to extra work/friction for developers, and may also be forgotten on occasion due to the manual nature of the tests. Running tests after development is completed is a bad idea because tackling all issues at once will take extra time and effort, as fixing some issues may create new issues elsewhere. By incrementally testing and coding, we can ensure issues are dealt with from their root.

2) Would you use an end to end test to check if a function is returning the correct output? (yes/no)

    **No**, because end to end testing is used to simulate the entire user interaction and ensure all the different pieces of the program work well together, not just a single function in the program. It would be more accurate to say we are testing the function within the context of the entire program being run for a specific user interaction.

3) What is the difference between navigation and snapshot mode?

    Navigation mode analyzes a page right after it loads, and provides an overall performance metric, but can't analyze interactions or changes in content.

    Snapshot mode is similar in that it can't analyze JS performance or changes to the DOM tree, but it is able to analyze a page in its current state and is best used for finding accessibility issues.

    Navigation is best used to evaluate the page upon its initial load, while snapshot should be used if you want to analyze the performance of a specific page after some number of user interactions or changes (although it cannot analyze the actual JS performance or changes to the DOM tree as they occur).

4) Name three things we could do to improve the CSE 110 shop site based on the Lighthouse results.

    The biggest issue with the CSE 110 shop site is the speed index. 
    
    One way we can improve it is by using the optimal/proper sizing for certain images (some of the files are larger than necessary, and can be compressed to improve performance). 
    
    A second thing we can implement are preconnections and preloads to ensure the browser gets some hints or information to get a head start in loading large images or setting up connections to third party domains. 
    
    Another quick fix we can implement is adding the <meta name="viewport"> tag with width and initial-scale, as this can prevents a delay to user input.