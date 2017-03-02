### What makes a good test


#### Descriptive
note:
- describe what you're testing
- how can I know when/how to update it?
  - requirements change
- serve as documentation


#### Accurate
note:
- You can only be confident if
  you trust the tests
- if 4/15 fail, had I broken something?
  - I didn't change any code
- did I not set it up correctly?
- should I ignore the failures?
- Should I remove them?
  - YES! It is ok to remove tests & code
    if they are no longer relevant


#### Easy to run
note:
- How much effort to get the tests to even run?
- If it takes 30 minutes to set up
  - "_Don't have time to set everything up_"
  - "_It was just a small code change_"
  - "_I couldn't have broken anything..._"  


#### Fast
note:
- Should be able to find out **quickly**

- Fast: < 30 seconds
  - Ideally on low end of ~ 0-10


##### If your tests

<p class="fragment">
aren't fast... people won't run them
</p>

<p class="fragment">
aren't run often... they won't stay accurate
</p>

<p class="fragment">
aren't accurate... they are useless
</p>

note:
- Slow: don't wanna wait for them...
  - Again, "_I just made a small change_"

- This ends up piling on itself

