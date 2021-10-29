---
aliases: 
tags: [ note/info ]
---
# When to Tag
There is an arbitrary threshold on when a note should have a certain tag. The measurement that's used against this threshold is **Tag Power**. A tag is considered powerful enough to be added when the note related, either trivially and directly, to this tag.

Say for example we have relatedness `A~B~C~D`. 
`D` usually should only be tagged with `C`.
`B` should can have tags `A` and `C`.

> This is similar to how one may link notes.

### Expansion on Related Tags
`#scrum` is a direct descendant of `#agile` (`#agile` $\leftarrow$ `#scrum`). A note based on scrum is trivially related to `#scrum`, should also have `#agile`.

However, a note based on agile will have `#agile`, but should not have `#scrum`. 

The only exception is when a note is dedicated to talking of both topics on equal footing. `#gamedev` and `#photograpgy` are not immediately trivially related, but the exception allows it such that for both tags under the context of `Photography and Texture Mapping to Character Models`.

> **Tags should not be used to show relatedness between notes.**

**Source**
[[Note Tags]]