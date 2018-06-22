# Testing

The Nitro Developer Bootcamp is a test-driven learning experience. Tests help guide us through our studies of various programming languages and libraries. Having tests provides a great way to assert that the code we write accomplishes our required tasks. It also provides us with a fast feedback loop:

Write a test. Write some code. Run the test.

Write some more code. Test it again.

A fast feedback loop helps us write better code. It quickly points out errors and helps identify ways our code could be designed better.

## A growing application (Nitro)

As applications grow, having test coverage becomes vital to an app's survival. Not only for the process of development, but for some insurance that something we just added will not break something else. Having a test suite that verifies our API is functioning properly gives developers more confidence, and helps root out bugs.

Although tests take time to write, they become a big time saver very quickly. Tests save time because they can set up complex scenarios that would be very hard to manually produce by hand. Then their value grows each time they are run.

Let's say we are working on a new feature in our software. Then we run our test suite and see a breaking test from a different area of the codebase. At first, seeing that random test fail feels like a bummer. But the reality is the broken test has identified a place where our code needs to improve, so we can fix it and create a better product. The earlier we can detect that something may break, the faster we can ship value to our end users.

## Documentation

Well written tests are also a great place to learn what a codebase does. Tests serve as a self updating source of documentation. Good descriptions and good tests make it easier for developers to learn new codebases.

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
