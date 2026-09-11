# Conclusions and recommendations

```{objectives}
- What is a realistic approach to automated test?
- How can I start?
```

---

## Discussion: What's easy and hard to test?

```{discussion} Discussion: Testing in practice

Use the collaborative notes to answer these questions:

1. Give examples of things (from your work) that are easy to test.
2. Give examples of things (from your work) that are hard to test.
```

---

Considering automated tests when writing code 
is a major mental shift, that you will hopefully embrace 
after attending this lesson.

## The basics: what knowledge do you need?

Learn one test framework well enough for basics:
- Explore and use the good tools that exist out there
- An incomplete list of testing frameworks can be found in the [Quick Reference](quick-reference)


## Don't over-test

- Not every code needs perfect {term}`test coverage<code coverage>`. 
- A simple script or notebook probably does not need an automated test.

## Take the low-hanging fruits first

You probably won't do everything perfectly when you start off... But
what are some of the easy starting points?

**If you have not got anything yet**:
1. Start with an end-to-end test. 
  Typically easy to add, from a typical "manual" use case.
  This should match (or serve as) an **example in the code documentation** anyway.
  - Describe in words how *you* check whether the code still works.
  - Translate the words into a script.
  - Run the script as often as reasonable 

2. Do you have some single functions that are easy to test, but hard to
  verify just by looking at them?  Add unit tests.

3. A local testing framework + GitHub actions/Gitlab CI-CD is very easy!
  And works well in the background - you do whatever you want and get an email
  if you break things.  It's actually pretty freeing.

**If you need to start modifying some existing code:**
1. Add a {term}`characterization test` for the part of the code you need to change
2. Add tests for any functionality you intend to add
3. Consider adding some end-to-end tests for the use case you have in mind.

## Going more in-depth

- Strike a healthy balance between unit tests and integration tests
- As the code gets larger and the chance of undetected bugs
  increases, tests should increase
- When adding new functionality, also add tests
- When you discover and fix a bug, also commit a test against this bug
- Use {term}`code coverage` analysis to identify untested or unused code.
  Remember [Goodhart's Law](https://en.wikipedia.org/wiki/Goodhart%27s_law)
- If you make your code easier to test, it becomes more modular
- **Learning how to test well make the rest of your code better, too.**

