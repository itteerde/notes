# Thoughts

- PDF seems to be the only robust rendering way.
- LaTeX ist the most mature typesetting, with XeLaTeX being the only free way with any resemblance of Unicode to PDF (with severe limitations)
- JavaScript has good enough Unicode support, but everything done in a programming language needs to address the persistance problem, unless writing the code (which means not getting the interaction). To be fair, the LaTeX solution has compilation runs, that take longer than it would take to reload or compile and run with most general purpose programming languages.
- Wolfram Language hat full Unicode support (technically), but in practise it requires using symbol names (if they are defined) or code points for everything out of ASCII, which is not really Unicode support without the GUI, which is not free -- at all. Also would be nice to do it with open standards or at least open source with broad community support.
- C++ has very little Unicode support.
- Back to Java might be an idea, though would that be much better than JavaScript? If the JavaScript runtimes are attractive (technically they are not, but availability is great), TypeScript might be an option to reduce bugs compared to doing plain JavaScript.
- If it is any general purpose programming language I need stabile persistence. So I should probably have another look at LevelDB and PostgreSQL.
- Do I at all  believe in the Markdown hipe, for quite structured data being represented? It also requires a renderer. Nope, don't think so.
- plain HTML could work, but would require some deployment for any case of sharing. There are reasons other than printing for PDF being very relevant and LaTeX continued use. This note taking project could however also be limited to data capture and/or data preparation (of such data captured).
- Being able to include time as time (being able to calculate, not just having strings somewhere) keeps coming up. And for the games application it includes points in time not well covered in many IT systems, including both before 1970-01-01 and 1900-01-01. To be fair, a Gregorian Calendar date a few thousand years back might work in Java (does it), but does not make that much sense (including the earth rotation slow down).
- Maybe I should make a PostgreSQL experiment asap, and consider locking it in with that hard, and do the minimum around it (reporting to XeLaTeX with some general purpose programming language, and rendering in XeLaTeX to PDF). It would however be a heavy component, that I am not sure I want to have if I can get by without any.

# Conclustions
- For analytic work the events/ notes have to be accessible with graph theory methods. So, that means the real core of this project should be creating notes in graphs, and modifying the graphs.
- The graph/s should get a renderer to XeLaTeX fro PDF creation.
- How do I author the graph/s? Do I end up with GraphML?
- Some analysis pretty much points at creating somewhat Microsoft Project logic. Being able to reason what someone was doing at some point in time is definately a standard case. Resource management is certainly a big part in the utility calculation.
- Fitting git version control well would be nice (in use, not just development). Database use would not. With the database any history functionality or rollback would have to be implemented using the database instead. For the intented use cases the database would however likely not grow to >100mb any time soon, which would be fine for almost unlimited backups -- therefore corruption would be a minor concern.