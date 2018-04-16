1. **How well does your solution match the posted solution? What is different?**
    * Overally, my implementation was pretty similar to the class solution, we both have a checkerboard class that builds the right checkerboard and passes an anchorpane back to the UI controller. When building the checkerboard I was right in having two different constructors to differentiate between the default checkerboard and the colored checkerboard. 

    * However, one important difference I noticed was that when calling for the checkerboard class to initialize, the class solution uses a single object instance call where as I did two. The class solution used a switch case to call setter function to set the global dark and light colors so that it can make use of the second constructor to build both checkerboard cases. In my solution, however I have an if statement based on a boolean flag which calls for the right constructor.
    
    * When building the checkerboard, the class solution returns the anchorpane as its return type where as I made it void and used the getAnchorPane function to receive it. I realize now that I could have saved few lines of code if I did it the other way.
    ```Java
        boardWidth = scene.getWidth();
        boardHeight = scene.getHeight() - menuBar.getHeight();
        
        stackPane.getChildren().clear();
        checkerBoard = new CheckerBoard(numRows, numCols, boardWidth, boardHeight, lightColor, darkColor);
        stackPane.getChildren().add(checkerBoard.build());
    ```
    * VS
    ```Java
        boardWidth = vBox.getWidth();
        boardHeight = vBox.getHeight() - menuBar.getHeight();  // height of anchorPane
        Checkerboard board;
        // flag is set to indicate different colored board initializaiton
        if (defaultColor == true) {
            board = new Checkerboard(numRows, numCols, boardWidth, boardHeight);
        } // no color specified instance
        else {
            board = new Checkerboard(numRows, numCols, boardWidth, boardHeight, lightColor, darkColor);
        }  // color specified instance
        clearBoard();              // clear board or remove current anchorpane when redrawing the different sized board
        board.build();             // call the public build board function in Checkerboard class 
        anchorPane = board.getBoard();
        vBox.getChildren().add(anchorPane);
    ```

    * When assigning the dimension variables, I parsed the text of the menu and got the number where as the solution used switch cases to match them. In the long run, my solution would be able take in any dimensional size defined in the MenuItem where as the class solution would have to manually add switch case for each additional dimension. 

    * Strangely enough, I remember I was having the problem of not being able to have the right square dimension when presenting the board, eventually I figured out to subtract the menubar height from the board height calculation. Glad to know the class solution did the same way.
    ```Java
      boardWidth = vBox.getWidth();
      boardHeight = vBox.getHeight() - menuBar.getHeight();
    ```
    
2. **How well did you understand the programming concepts and foundational knowledge needed to complete the challenge?**
    * because we had a in class example to draw a grid with multiple rectangles, and the foundational knowledge we have received during previous examples, I was able to figure out what exactly is needed to complete the challenge. 

3. **How well did you meet the requirements as set out in the challenge? What requirements did you not meet correctly (if any)?**
    * I met both the UI and the controller requirements sufficiently as I mentioned above in question 1. 
    * Below is the sample output of my checkerboard.
    * ![picture alt](https://github.com/OchirnyamB/RetrospectiveCheckerboard_ob44f/blob/master/BoardOutput.jpg "Checkerboard")

5. **How could you improve going forward? What don't you still understand that was required for the challenge?**
    * Keep in mind of SOLID design principles and always remember to stay away from duplication of code.
