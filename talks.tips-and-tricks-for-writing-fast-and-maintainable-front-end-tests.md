---
id: dsspzsmzvb1cn7kjb0wi3ab
title: Tips and Tricks for Writing Fast and Maintainable Front-End Tests
desc: ''
updated: 1667331759102
created: 1667327987233
---

[Gleb Bahmutov](glebbahmutov.com)
![Pic of Gleb](images/d9895f21f22aa314ea369817e1d89f8544d2f97c3ef92306301bf8c7faad0455.png)  

Senior Director of Engineering,
MercariUS

## Front end tests

Web app tests should run in the browser. (`jest` runs Node, for instance)

Node code should be tested in Node

Browser code should be tested in a browser

Gleb uses Cypress

End-to-end testing recommended.

See the application like a user.

### Making E2E hard

- Random data
- External data
- timers and clocks
- conditional tests (don't do it)
- unclear test requirements

### Component Testing

Much faster than E2E.

Cypress understands how to load and mount the component, with styling

Try to avoid testing solutions that rely on framework-specific syntax.

Unit tests -
small chunks of code like functions / classes

Component tests -
Front-end components & easy to test edge functions

E2E tests -
User workflows

## Fast Tests

Do as much as possible using API calls

Cache created data
(users, listing)

Keep all tests shorter than 3 minutes

Parallelize everything

Work locally on a specific spec

Kinds of speed
- writing tests
- running tests
- debugging failures

## Maintainable

Must be maintainable by _someone else_.
Are the tests readable? (very important)
Use cusom commands, utilities, plugins

Sprinkle page abstractions _when needed_j

### Make errors actionable

Write a good error for when a test fails.

Notify people that can fix the problem.
Tags for the specific teams that are applicable.
