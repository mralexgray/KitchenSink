The use of zeroing weak references in combination with NSMapTable has the potential to simplify object management by providing automatic removal of unused entries. I recently struggled with unexpected behaviors in NSMapTable and decided to take a closer look. I came to the unfortunate conclusion that NSMapTable has undocumented limitations in its handling of zeroing weak references (at least under ARC, though I expect similar results with manual memory management).

To see NSMapTable in action, I wrote a simple test application that exercises NSMapTable, [published on github](https://github.com/cparnot/KitchenSink/tree/master/NSMapTable+Zeroing). I also wrote an accompanying [blog post](http://cocoamine.net/blog/2013/12/13/nsmaptable-and-zeroing-weak-references/).