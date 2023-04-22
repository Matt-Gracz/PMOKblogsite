# PMOKblogsite
Matt Gracz's PMOK blog, chronicling his development of a computational solver of an arbitrary PMOK problem

<div name = "entry1">
  <h2>Entry 1, 4/21/2023: Beginnings</h2>
<p style="font-size:10px;font-family:arial">
This is the first entry in a hopefully short blog describing my already very interesting journey of attempting to create an efficient computational solver for PMOK (Paper Mario and the Origami King) problems.  What started as a programmer wanting to dive deeper into a beloved video game's world ended up with me apparently having to get pretty creative.  And to be clear - I am writing this blog as I am developing the solution.  Here's where I am at as of 4/21/2023:<br />
I’ve tried solving this analytically for about 10 hours now, and I have come to believe that the problem space is just ever so slightly large enough that I myself with my particular math chops will never be confident in writing a provably perfect solving algorithm for an arbitrary PMOK problem.  Therefore, since we can’t have the “hard” solution, at least not provably as I claim, then we want “the hardest possible soft solution”, and unfortunately I think that means deferring to a machine learning model.  The analytical solutions I come up with keep forcing me to enjoy perplexing counter-examples where even patchwork meta-algorithms start falling apart.  At some point it has to be said that the size of the problem space and the “chaotic”/unstructured nature of the transition paths to solutions means that we need to fit a machine learning model tightly to this problem space to have any chance of getting a reliable.<br />
Questions without (current) answers:
    <ul>
      <li>What’s our tolerated failure rate?</li>
      <li>What’s our tolerated max user response time profile for the full compute?</li>
      <li>Do we owe the user anything other than the solution?</li>
    </ul>
  Technical Notes:
  <ul>
  <li>PMOK Problems are either perfectly solve-able or are completley not solve-able; there is no such thing as partially solved.  A problem may have more than 1 solution.  Each solution to a given problem is equally useful / “valid”, even if some solutions take quite a few moves or contain unintuitive state transition choices
  </li>
  <li> Compute / reponse speed only really matters at the UX level since this we are ultimately mapping the model's problem space to what people will be literally typing into webpage UI elements </li>
  </ul>
  </p>
</div>
