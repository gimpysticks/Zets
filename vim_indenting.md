---
title: vim_indenting
date: 2023-05-17 14:41
---
* 4== will indent the current line, and the next three.

* =ap will indent Around the current Paragraph. Having no empty lines, this method qualifies as a paragraph.

* =% will indent to the the end of the method. Note this implies the use of the matchit plugin. But % works with common curly brace blocks, parens, etc out of the box.

* V3j= will do a visual select on the current line and the three below and apply indenting to them.

* These cover a lot of ground when trying to keep your code tidy.

* Lastly, the nuclear option gg=G can be used to indent an entire file.


