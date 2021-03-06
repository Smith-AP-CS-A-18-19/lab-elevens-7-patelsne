# Elevens 7

Follow the instructions provided for Activity 7 in the student lab guide. This is more of an exploratory lab, so you will not need to copy any of your previous code into the repo. Answer the questions from the Student Guide in this document and ensure that you save and push the repo. You have one week to complete this lab.

1. What items would be necessary if you were playing a game of Elevens at your desk (not on the computer)? List the private instance variables needed for the `ElevensBoard` class.

    *  A deck of cards

2. Write an algorithm that describes the actions necessary to play the Elevens game.

    * Check if the sum of the two cards is 11, if they are they will be replaced, two new cards will be randomly picked from the deck, then it should check if there are any combinations of card to add up to eleven (if not then the player loses). If the sum of the two cards isn't 11, then nothing will happen.


3. Now examine the partially implemented `ElevensBoard.java` file found in this repository. Does the `ElevensBoard` class contain all the state and behavior necessary to play the game?

    * No, we need a method to check all combination summations to see if the game is lost or not.

4. `ElevensBoard.java` contains three helper methods. These helper methods are private because they are only called from the ElevensBoard class.

  * a. Where is the `dealMyCards` method called in ElevensBoard?

      * The method is first called to create a new board

  * b. Which `public` methods should call the `containsPairSum11` and `containsJQK` methods?

      * in isLegal()

  * c. It’s important to understand how the `cardIndexes` method works, and how the list that it returns is used. Suppose that `cards` contains the elements shown below. Trace the execution of the `cardIndexes` method to determine what list will be returned. Complete the diagram below by filling in the elements of the returned list, and by showing how those values index `cards`. Note that the returned list may have less than 9 elements.

    * `cards`

| 0  | 1  |  2   | 3  |  4   |  5   | 6  | 7  |  8   |
|:--:|:--:|:----:|:--:|:----:|:----:|:--:|:--:|:----:|
| J♥ | 6♣ |`null`| 2♠ |`null`|`null`| A♠ | 4♥ |`null`|

   *  * Answer - This list should contain the indices of the cards, not the cards themselves

| 0  | 1  | 2  | 3  | 4  | 5  | 6  | 7  | 8  |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
|  J |  6 | 2  | A  | 4  |  null  | null   | null   | null   |

  * d. Complete the following `printCards` method to print all of the elements of cards that are indexed by `cIndexes`.
```java
public static printCards(ElevensBoard board) {
    List<Integer> cIndexes = board.cardIndexes();
    /* Your code goes here. */
    for(int i : cIndexes){
      System.out.println(board.get(i));
    }
}
```

  *  * Answer

  * e. Which one of the methods that you identified in question 4b above needs to call the `cardIndexes` method before calling the `containsPairSum11` and `containsJQK` methods? Why?

      * The method anotherPlayPossible needs to be called to confirm that the game can continue by finding another pair of 11s or a facecard triplet.

## Feedback
4.c is slighty off
19/20

## Feedback
Failed to compile
00/20
