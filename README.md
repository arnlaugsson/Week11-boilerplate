# SC-T-303 HUGB - Week 11 boilerplate project
A Jest + Puppeteer project for acceptance tests against a running server.

## Getting started
### Prerequisites
- [NPM][npm] version 6.4.1+ (could work on older, but not tested)

### Installing
After cloning the repo, run `npm install` in the project directory.

- `git clone https://github.com/arnlaugsson/Week12.git; cd Week11; npm install`

### Running the tests
This repository uses the [Jest][jest] testing framework and the [Puppeteer][puppeteer] library for writing automated acceptance tests for services.

### Writing tests
- Test files are located under the `src/` folder.
- For speeding up the tests, remove the `slowMo` parameter.
- To run in headless mode, set `headless` to true.
- The lab exercise description [is in the LabExercise markdown file](LabExercise-Week11.md).

## Additional resources
- [12 example usages of Puppeteer][12examples]
- Behavior driven development with [Cucumber and Puppeteer][cucumber]

[12examples]: https://www.aymen-loukil.com/en/blog-en/google-puppeteer-tutorial-with-examples/
[cucumber]: https://www.aymen-loukil.com/en/blog-en/google-puppeteer-tutorial-with-examples/
[jest]: https://jestjs.io/
[npm]: https://www.npmjs.com/
[puppeteer]: https://github.com/GoogleChrome/puppeteer