
### TDD


#### Describe _what_ we're building
<!-- .element: class="fragment"
-->Not how
note:
- in TDD, we describe the functionality
- this adds context for future devs


#### <span style="color: red">Red</span>
#### <span class="fragment" style="color: green">Green</span>
#### <span class="fragment">Refactor</span>


#### Not really an approach to testing
note:
- it's a development process
- like we don't wash our hands to have washed hands
  - we wash them to avoid illness and disease
  - do it for the benefits


We don't test to see  
if our _code_ works as expected
note:
- most tests written this way
- we don't get paid for code
  - we get paid for functionality
- test to see if APP works
- if our _code_ does what the app needs it to,
  then it also works


#### Refactoring
note:
- TDD is very much about refactoring
- Knowing getValue is `fib`, we can safely refactor
  - couldn't by just knowing "it gives correct value"


#### Verifiable code
note:
- Our tests show how to interact with the code


#### Tight cycles between test and code
<!-- .element: class="fragment"
-->Failing tests are a good thing
note:
- seconds to minutes

- failing tests let you know
  something isn't working
- broke something?
  - something you did in the last few moments


#### Good design
note:
- think about how to interact with the API up front
- because test is written first, it's very testable


#### Do less
note:
- We build too much 'cause we think we'll need it
- We waste time even thinking about the edge cases
- Solving a problem, not every problem


#### Short feedback loop
note:
- just like agile
- find out what to do next ASAP


#### Moving target
note:
- development is fast-paced
- if you plan to write tests later, you won't
  - something else always comes up
- testing first == no debt

