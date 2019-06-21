DITA from FrameMaker: Two Schools of Thought
============================================

Traditionally in our product group, we have been using unstructured
FrameMaker as the main authoring tool afor our product documentation. In
late 2017, we received a requirement that customer requires our
documentation source in DITA format with the PDFs too. This requirement
posed a challenge. We did not have any experience working with DITA
earlier, and we did not know the way forward. We spent a considerable
amount of time researching how to convert the sources. This customer had
two requirements:

-  Needs source in DITA
-  Needs product updates for the next two years (that means the DITA
   conversion is not a one-time job, and the DITA source must be
   up-to-date always).
-  Internal requirement
-  Reuse content across product lines

We reached out to other teams within my company to check if they had any
experience with DITA/conversion from FrameMaker and any other learning
experiences.

Converting FrameMaker to DITA
-----------------------------

Our research on this project led us to the following two schools of
thought:

-  Maintain our documentation source in FrameMaker and convert the files
   to DITA each release to the customer.
-  Convert the FrameMaker source to DITA, and continue to use the DITA
   source.

A team in our business group followed method 1. Whereas, we chose to use
method 2.

What the Other Team Did
-----------------------

The other team made it possible by moving to their content from
unstructured FrameMaker to structured FrameMaker.

1. Convert unstructured FrameMaker to structure FrameMaker
2. Create mapping tables to convert structured FrameMaker to DITA each
   release.
3. Run FrameMaker scripts to clean up the DITA sources.

What We Did
-----------

We took the second approach. Our internal content reuse was the main
reason we chose the second approach. We used a third-party service
(Stilo Migrate) to convert our unstructured FrameMaker source to DITA.
This task involved pre-conversion and post-conversion tasks. Continued
using DITA as a the main source for all our subsequent work.

You could choose either approaches. There is no correct and incorrect
approach. Approach 2 worked better for us our biggest driver was content
reuse. Approach 1 works better when there is no content reuse.

Challenges with our Approach
----------------------------

-  The number of objects to manage after conversion to DITA is huge. We
   might need a CCMS to manage the DITA source.
-  We needed to invest in a DITA-aware editor. We continue to use
   FrameMaker as the XML editor too.
-  With a regular repository as Perforce, we could not check out only
   the files that we need. A CCMS would solve this problem.

More about the pre-conversion and post-conversion tasks, CCMS, and DITA
to PDF publishing workflow in future posts.
