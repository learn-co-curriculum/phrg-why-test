# Testing

The Nitro Developer Bootcamp is a test-driven learning experience. Tests help guide us through our studies of programming languages and libraries. Having tests provides a way to assert that the code we write accomplishes our required tasks. It also provides us with a fast feedback loop:

1. Write a test, run it, and watch it fail.
1. Based the the error from the test failure, write code to make the test pass.
1. Run the test and see it pass, or the error change.
1. Repeat.

This feedback loop helps us write better code. It points out errors and helps identify ways to better design our code.

## A growing application (Nitro)

As applications grow, having test coverage becomes vital to an app's survival. And not only for the process of developing new features. Tests give us some assurance that something we added will not break the rest of the app. They also let us extend and revise existing features, with the same assurances. A test suite will give developers more confidence, and helps prevent bugs.

Although tests take time to write, they become a big time saver. Tests save time because they can set up complex scenarios that would be very hard to produce by hand. The value of the test grows each time it runs.

Let's say we are working on a new feature in our application. Then we run our test suite and see a unexpected breaking test. At first, seeing that random test fail feels like a bummer. The broken test has identified a place where we introduced a regression. Now we can use the failure to figure out why did this fail? Did we make a change that had an unintended change to how the existing code works? Does the existing code not support the new needs of the feature. The earlier we can detect that something may break, the faster we can ship value to our end users.

## Documentation

Well written tests are also a great place to learn what a codebase does. Tests serve as executable documentation. Writing comments in application code can be helpful to describe what the code is doing. But what happens after a few weeks, or a year; will we remember to update the comments? Tests are less likely to fall out of sync with documentation. When the code changes in semantic way, the test should fail. Good descriptions and tests make it easier for developers to learn new codebases.


# Tests in an MVC Framework - An Automobile Analogy

It's not enough to know *how* to test applications; we must also understand *why* it makes sense to test them in a certain way. To help with this, try thinking of an MVC application like a car:

- **Models** are the **basic parts** that make cars useful, like the fuel tank,
  engine, and tires.

- **Views** are the **interactive parts** that the driver (user) can see and
  touch, like the steering wheel, pedals, and gear shift.

- **Controllers** are the rest of the **connecting parts** under the hood that
  connect the views to the models, like how the steering column (along with the
  rest of the steering assembly) connects the wheel to the tires. The users don't
  really see them, think of them, or even necessarily know they exist, but they're
  just as necessary.

Models are not too difficult to test because they have very specific purposes that can be easily separated from the rest of the application. This holds true for cars as well: a good tire has a tread that grips the road in adverse conditions, doesn't puncture easily, and so on. You don't really need to think about the rest of the car when you're testing what makes a good wheel.

The tests you became familiar with in the Object Oriented Ruby section were often essentially Model tests. They asserted that particular methods in your class operated as expected. Checking return types, and validating that instances had changed attributes properly.

View and controller test get a little trickier. We will talk more about these later on.
