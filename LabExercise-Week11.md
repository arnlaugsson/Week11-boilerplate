SC-T-303 HUGB - Week 11, autumn 2018
# Functional testing
Functional testing, user acceptance testing, end-to-end testing, full-stack testing, black box testing, are often sunonyms, even though their focus and intended audience is different. These tests rely on a functioning piece of sotware, not simply units as in unit testing, or a combination of components as with integration, but a live functioning system.

These types of tests aren't suited for testing everything, but can be very useful for testing some functional aspects of software. The should be used sparingly as they are prone to failure and take a long time to run. Unit tests run in the millisecond range, integration from milliseconds to maybe seconds, and functional tests can take a few seconds up to anywhere much longer. They are therefor not suited to run on each save in an editor (who wants to wait for that?), but can be very helpful in a CI and CD environment.

For testing web applications, there are mulitple tools that can be used, this year we are introducing [Puppeteer][puppeteer] from Google for this purpose (we have used [Selenium][selenium] in the past). Puppeteer is a high level API tool to control a web broswer (Chromium or Chrome) to automate tasks a user would do in the browser.

When we combine Puppeteer with Jest, we can write tests that simulate a user in the SUT (System under test), and we can verify that the functionality, that should be supported, is supported.

## Getting started
1. Fork this repository: https://github.com/arnlaugsson/Week11
2. Read up on [Puppeteer][puppeteer]
3. Look at the unimplemented tests in the `src/` folder.

## Writing the tests
### Grab a screenshot
1. Open up the `/src/screenshot.test.js` file. 
2. Remove the `NotImplementedError` line.
3. Change the tests to actually grab a screenshot of the page, both in the simulated iPhoneX version and the Desktop version.

### Check the response code
1. Open up `/src/checkResponse.test.js` file.
2. Remove the `NotImplementedError` line.
3. Change the test to verify that the status code given when the page is loaded is equal to 200.

### Submit a form and check the results
1. Open up `src/interactWithForm.test.js` file.
2. Remove the `NotImplementedError` line.
3. Change the test to do as described in the test file.

## Where does this belong?
### Late term project
For the late term project the teams must create functional tests that cover the functions of their game, for example creating a new game, playing a game, checking for a winner, for example. These examples above are only showing a very small subset of options that Puppeteer can offer, check the documenation and Google to find more possibilities.

### Where to run
Functional tests need to be run against a live (deployed) server, although it's possible to run tests locally against a local server, in our pipeline, functional tests should be run against a deployed server, a staging server.

In order to achieve this, we need to deploy our branch to a staging server in our CI configuration and run our functional tests against that deployed server, and if (and only if) these functional tests pass should we consider updating our production environment. The key is to figuring out how to fit all of this together (Github, Circle CI, Heroku) with different environments.

[puppeteer]: https://github.com/GoogleChrome/puppeteer
[selenium]: https://www.seleniumhq.org/