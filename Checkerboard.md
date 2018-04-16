1. Reflect on (think about) the work you did for the challenge. How did you do? What did you get right? What did you get wrong? What did you do differently (and possibly better) than what was posted in the solution? What was hard to do?
** Overally, my implementation was pretty similar to the class solution, we both have a checkerboard class that builds the right checkerboard and passes an anchorpane back to the UI controller. When building the checkerboard I was right in having two different constructors to differentiate between the default checkerboard and the colored checkerboard. 

** However, one important difference I noticed was that when calling for the checkerboard class to initialize, the class solution uses a single object instance call where as I did two. The class solution used a switch case to call setter function to set the global dark and light colors so that it can make use of the second constructor to build both checkerboard cases. In my solution, however I have an if statement based on a boolean flag which calls for the right constructor.

** When assigning the dimension variables, I parsed the text of the menu and got the number where as the solution used switch cases to match them. In the long run, my solution would be able take in any dimensional size defined in the MenuItem where as the class solution would have to manually add switch case for each additional dimension. 

** Strangely enough, I remember I was having the problem of not being able to have the right square dimension when presenting the board, eventually I figured out to subtract the menubar height from the board height calculation. Glad to know the class solution did the same way.

2. How well did you understand the programming concepts and foundational knowledge needed to complete the challenge?


3. How well did you meet the requirements as set out in the challenge? What requirements did you not meet correctly (if any)?

4. How well does your solution match the posted solution? What is different?

5. How could you improve going forward? What don't you still understand that was required for the challenge?
