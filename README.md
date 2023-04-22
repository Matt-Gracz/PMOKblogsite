# PMOKblogsite
Matt Gracz's PMOK blog, chronicling his development of a computational solver of an arbitrary PMOK problem

<div>
  <h1>Entry 1: 4/21/2023</h1>
<p>
  This is the first entry in a hopefully short blog describing my already very interesting journey of attempting to create an efficient computational solver for PMOK (Paper Mario and the Origami King) problems.  What started as a programmer wanting to divie deeper into a beloved video game's world ended up with the computer scientist in me having to come out and get pretty creative.  And to be clear - I am writing this blog as I am developing the solution.  Here's where I am at as of 4/21/2023:
</p>
  <ol>
    <li> I’ve tried solving this analytically for about 10 hours now, and I have come to believe that the problem space is just ever so slightly large enough that I’ll never be confident in writing a provably perfect algorithm for any PMOK problem.  Therefore, since we can’t have the “hard” solution, at least not provably as I claim, then we want “the hardest possible soft solution”, and unfortunately I think that means deferring to a machine learning model at this point.  The analytical solutions I come up with keep enjoying perplexing counter cases where even patchwork meta-algorithms start falling apart.  At some point it has to be said that the size of the problem space and the “chaotic”/unstructured nature of the transition paths to solutions means that we need to fit a machine learning model tightly to this problem space to have any chance of getting a reliable solver. </li>
    <li> PMOK Problems are either perfectly solve-able or are completley not solve-able; there is no such thing as partially solved.  A problem may have more than 1 solution.  Each solution to a given problem is equally useful / “valid”, even if some solutions take quite a few moves or contain unintuitive state transition choices
    </li>
    <li>
      -	Questions without (current) answers:
      <ol>
        <li>What’s our tolerated failure rate?</li>
        <li>What’s our tolerated max user response time profile for the full compute?</li>
        <li>Do we owe the user anything other than the solution?</li>
      </ol>
    </li>
  </ol>
</div>
