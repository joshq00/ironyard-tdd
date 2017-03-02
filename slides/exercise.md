
##### Exercise

Is this working properly?
```js
it( 'calculates the correct value', () => {
    expect( getValue( 4 ) ).to.eq( 5 )
    expect( getValue( 8 ) ).to.eq( 13 )
    expect( getValue( 13 ) ).to.eq( 377 )
} )
```
<small>
<code><span style="color: green">✓</span> calculates the correct value (1ms)</code>
</small>

note:
- The tests pass
- I know that
  - given 4, it should return 5,
  - 8 -> 13
  - 13 -> 377


<span style="font-size: 5em">¯\\\_(ツ)_/¯</span>
note:
- But I have no idea if it's working properly


<span style="color: red; font-size: 2em">!!!!!!!!!</span>

> Users are complaining their browsers
> freeze on our site

<span style="color: red; font-size: 2em">!!!!!!!!!</span>


###### After some investigation:
- Source:  
  `sequence.js:getValue`

- Steps to reproduce:  
  Use `-1` as an input  

_Note_:_ we think it's happening for all negatives_
note:
- what a coincidence - we were just looking at that


We need to add a test...
<pre><code data-trim data-noescape class="javascript">
it( 'calculates the correct value', () => {
    expect( getValue( -1 ) ).to.eq( <span class="fragment">'correct value?' )</span>
    expect( getValue( 4 ) ).to.eq( 5 )
    expect( getValue( 8 ) ).to.eq( 13 )
    expect( getValue( 13 ) ).to.eq( 377 )
} )</code></pre>


I guess we can look at the code...
<pre><code data-trim data-noescape class="javascript">
function getValue ( num ) {
  var a = 1, b = 0, temp;

  while ( num != 0 ){
    temp = a;
    a = a + b;
    b = temp;
    num--;
  }

  return b;
}</code></pre>

note:
that doesn't help much...


How about this?
<pre><code data-trim data-noescape class="javascript">
it( 'gives the Nth value in the fibonacci sequence', () => {
    <span class="fragment">expect( getValue( -1 ) ).to.eq( -1 )</span>
    expect( getValue( 4 ) ).to.eq( 5 )
    expect( getValue( 8 ) ).to.eq( 13 )
    expect( getValue( 13 ) ).to.eq( 377 )
} )</code></pre>
<small class="fragment">
<code><span style="color: red">✕</span> gives the Nth value in the fibonacci sequence</code>
</small>

