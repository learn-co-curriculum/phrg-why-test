# Testing

The Power Code Academy is a test-driven learning experience. Tests help guide us through our studies of programming languages and libraries. Having tests provides a way to assert that the code we write accomplishes our required tasks. It also provides us with a fast feedback loop:

1. Write a test, run it, and watch it fail.
1. Based the the error from the test failure, write code to make the test pass.
1. Run the test and see it pass, or the error change.
1. Repeat.

This feedback loop helps us write better code. It points out errors and helps identify ways to better design our code.

## A Growing Application (Nitro)

As applications grow, having test coverage becomes vital to an app's survival. And not only for the process of developing new features. Tests give us some assurance that something we add will not break the rest of the app. They also let us extend and revise existing features, with the same assurances. A test suite will give developers more confidence, and helps prevent bugs.

Although tests take time to write, they become a big time saver. Tests save time because they can set up complex scenarios that would be very hard to produce by hand. The value of a test grows each time it runs.

Let's say we are working on a new feature in our application. We run our test suite and see an unexpected breaking test. At first, seeing a random test fail feels like a bummer. But the broken test has identified a place where we introduced a regression. Now we can use the failure to figure out what happened. Did we make a change that had an unintended change to how the existing code works? Does the existing code support the new needs of the feature? The earlier we detect that something may break, the faster we can ship value to our end users.

## Documentation

Well written tests are also a great place to learn what a codebase does. Tests serve as executable documentation. While writing comments in application code can be helpful to describe what the code is doing, after a few weeks or months they become stale. Tests are less likely to fall out of sync with documentation because when the code changes in significant way, the test should fail. Good descriptions and tests make it easier for developers to learn new codebases.

## Testing Spectrum

There are two major classifications of tests: Integration and Unit. Between Integration and Unit tests, there is a spectrum. These two classifications of tests service different but complementary roles. It is important to understand the differences. We will need to ask ourselves what approach is best for what we are testing.

### Integration Tests:

An Integration test excels at describing and verifying how the application actually works. Integration tests check many parts of the application at once. Integration tests better reflect reality. They give us more confidence our code will work when compared to a unit test. But integration tests tend to be slower. With Integration tests, we are testing many parts of the application, so we are running more code. Running more code means slower tests compared to Unit tests. These tests are also more likely to fail, but that is because they are touching more parts of the system. When an Integration test does fail, it can be more difficult to understand why.

### Unit Tests:

A Unit test focuses on one part of the application and ignores the rest. They describe and verify a focused part. Unit tests tend to be faster than Integration tests. That speed comes at the cost of less confidence that the application will work. The added focus lets us better describe the logic of specific parts of the code. The focus will give better errors of what is causing the test to fail.

## Building and Maintaining a Test Suite

When it comes to building a project, we want a combination of Integration and Unit tests. We can picture a pyramid as our target. At the top of the pyramid are Integration focused tests, and at the bottom are Unit focused tests. Between the top and bottom are tests that are something between Unit and Integration. We want a few high value Integration focused tests at the top, and as we travel down the pyramid, we want more and more Unit focused tests.

When working on a feature, it is a good idea to start with a high level Integration focused test. Once we get the feature working, flesh out the code with Unit Tests. Once the feature is working, review the tests you have written. Consider making a commit that deletes low value tests. Tests can out live the value they once offered.

## Resources

- https://martinfowler.com/bliki/TestPyramid.html
- https://martinfowler.com/bliki/IntegrationTest.html
- https://www.martinfowler.com/bliki/UnitTest.html
- http://wiki.c2.com/?TestDrivenDevelopment
- http://wiki.c2.com/?IntegrationTest
- http://wiki.c2.com/?UnitTest
- https://robots.thoughtbot.com/testing-from-the-outsidein
