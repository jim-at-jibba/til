# How do you know your assumptions are wrong when debugging?

This has been compiled from a really interesting twitter [thread](https://twitter.com/b0rk/status/1402615810317750274?s=20)

**Original tweet**

> when you're debugging and one of your assumptions is wrong, how do you normally figure that out? The main thing that comes to mind for me is talking/writing to another person ("this makes NO SENSE, I've already checked X, and Y, and ... oh, wait."). What else works?

1. When finding the root cause of a bug, **make a list of things that work**
2. Write a list of all the things that you assume happen and then check them off one by one. As soon as one does not work, go into more detail
3. Write down the symptoms of the bug and detail the process in arriving at whatever (wrong, sometimes) conclusion about the bug's origin.  Along the way, it often becomes clear when I've made an bad assumption.
4. Take a break, go for a walk, brush your teeth
5. Try checking the things that are so obvious you did nto check
6. Rubber ducking
7. recreate the bug in an isolated context
8. describe the bug, writing in general — not to a specific person but to an abstract Reader. I find that the harder the bug is, the more “organized” my writing needs to be — starting with scribbles and ending up with something more like a blog post.
9. Change the context of your thoughts to something else and come back to the problem later