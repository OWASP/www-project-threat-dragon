---

title: Unit testing
layout: col-document
tags: threatdragon
document: Threat Dragon version 2.0
permalink: /docs-2/unit/

---

{% include breadcrumb.html %}

## Unit Testing

## What is Unit Testing... and why?

Unit tests are intended to test a single piece of functionality, while mocking away all external dependencies.
The goal of a unit test is to know that a particular function or piece of code works exactly as expected
under all of the possible code paths.
Unit tests should not include any external dependencies.

## Running Unit Tests

The complete suite of unit tests can be run locally using command `npm test` from the top directory.

### Jest (td.vue)

Unit testing for the vue application is done using [jest](https://jestjs.io/),
and lives in the `td.vue/tests/unit` directory.

If you'd prefer to work in a more TDD fashion, you can have the tests run continuously by
navigating to the `td.vue` directory and running `pnpm run test:unit -- --watch`

### Mocha (td.server)

Unit testing for the server application is done using [Mocha](https://mochajs.org/),
with a little help from our friends [sinon](https://sinonjs.org/) and [chai](https://www.chaijs.com/).
To run the tests locally navigate to the `td.server` directory and run: `pnpm run test:unit`

## Code Coverage

When you run unit tests for both the front-end and back-end application,
you will be presented with a code coverage report.
There will be an HTML report generated as well that you can view to
dig deeper into what sections may be missing coverage.

We hope to keep the code coverage as high as possible.  If you need help writing or updating tests, please just ask!
