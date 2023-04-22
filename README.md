# PMOKblogsite
Matt Gracz's PMOK blog, chronicling his development of a computational solver of an arbitrary PMOK problem

<div name = "entry1">
  <h2>Entry 1, 4/22/2023: Beginnings</h2>
<p>
NOTE: This is not the text of the first entry; it's a draft.  I'm just testing the site style out right now.  The real text will be up on 4/23 probably.
This is the first entry in a hopefully short blog describing my already interesting journey in attempting to create an efficient computational solver for PMOK problems.  To be clear - I am writing this blog as I am developing the solution.  Here's where I am at as of 4/21/2023:<br />
I’ve tried solving this analytically for about 10 hours now, and I have come to believe that the problem space is just ever so slightly large enough that I myself with my particular math chops will never be confident in writing a provably perfect solving algorithm for an arbitrary PMOK problem.  Unfortunately, this means deferring to a machine learning model.  Basically the conclusion that all the prototype testing has driven towards is that the size of the problem space and the “chaotic”/unstructured nature of the transition paths to solutions together imply that we need to fit a machine learning model tightly to this problem space to have any chance of getting a reliable solver deployed.<br />
Questions without (current) answers:
    <ul>
      <li>What’s our tolerated failure rate?</li>
      <li>What’s our tolerated max user response time profile for the full compute?  By this I mean, what is the mapping between response-time tolerances and user engagement?  This question might be moot if the solver is fast enough so it'll be tabled until well into implementation and testing.</li>
      <li>Do we owe the user anything other than the solution?</li>
    </ul>
  Technical Notes:
  <ul>
  <li>PMOK Problems are either perfectly solve-able or are completley not solve-able; there is no such thing as partially solved.  A problem may have more than 1 solution.  Each solution to a given problem is equally useful / “valid”, even if some solutions take quite a few moves or contain unintuitive state transition choices
  </li>
  <li> Compute / reponse speed only really matters at the UX level since this we are ultimately mapping the model's problem space to what people will be literally typing into webpage UI elements </li>
  <li>  As of writing this I’m about 15 hours deep into exploring predictive solvers (DNN,…) and, purely experimentally, I'm almost positive some sort of linear or nonlinear programming/optimization will suffice.  It might not be the <i>best</i> approach but I think it will do, partially because it did will in prototype testing  but also because I’m more familiar with it than any other type of solver, and lastly because its properties as an algorithmic process map intuitively and neatly to the relevant properties of the PMOK problem space.
  </li>
  </ul>
  </p>
</div>
