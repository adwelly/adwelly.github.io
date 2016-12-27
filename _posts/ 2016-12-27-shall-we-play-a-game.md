---
layout: post
title: Shall we play a game?
---

Google rather unhelpfully defines the prefix 'meta-' as:

1. denoting a change of position or condition.
2. denoting position behind, after, or beyond.
3. denoting something of a higher or second-order kind.

I prefer 'X about (or of) X'

So metalanguage is' language about language', metadata is 'data about data' and of naturally, meta-tic-tac-toe is 'tic-tac-toe of tic-tac-toe' or MT3 for short.

I first saw the game years ago on the Math with bad drawings blog,  and since I'm giving a short talk on Clojure and a 2 day course on the same subject early in the new year, it seems like a good moment to write about it. It's a good basis for a talk. And fun (admittedly, for my own rather nerdile sense of fun). Besides which, it's Christmas. Also you can play it on Twitter, and if anyone wants to challenge me, I'm @adwelly; please do — I'll only be working on my thank you letters otherwise.

This is how it works: imagine a larger than normal tic-tac-toe board, with the cells numbered from 0 in the top left hand corner, to 8 in the bottom right.

```   |   |   

   |   |   
 0 | 1 | 2
   |   |   
-----------
   |   |   
 3 | 4 | 5
   |   |   
-----------
   |   |   
 6 | 7 | 8
   |   |  
```



Each of these cells contains its own game of tic-tac-toe, and you have to win 3 of the little games in a row, column, or a diagonal to win the over all game. So in this case, X won in position 0 and 1, O has won in position 4 and 5, and it's X's turn to play. If X plays in the bottom right hand position of cell 2 (* below), X has won the game. That move is cell 2, subposition 8, so I'd probably write it as 2-8, or (2 8) in Clojure.

```
XXO| O | O   
OX |XXX|O   
  X|O  |XX*  
-----------
   | X |  O
   | X |  O
   |OOO|  O
-----------
   |   |   
   |   |   
   |   |  
```

 I've written a short Clojure program that keeps track of moves, and shows who one each little game. It draws this situation as:

```
\ /|\ /| O 
 X | X |O  
/ \|/ \|XX 
-----------
   |+-+|+-+
   || ||| |
   |+-+|+-+
-----------
   |   |   
   |   |   
   |   |   
```

There is however, one additional rule that makes this all much more interesting. When someone plays in a subposition in a little game, that forces the next player into that cell for the next move. So on this board, if X plays at 0-8 (a below), winning cell 0, O will have to play in cell 8, probably at position 8 (b below), which wins the game. 

```
XOO|\ /|+-+
 X | X || |
  a|/ \|+-+
-----------
   |   |+-+
   |   || |
   |   |+-+
-----------
   |   |OX 
   |   | O 
   |   |  b  
```

So you have to be careful. if it's not possible to play in the next cell because it was already won or drawn, the next player can go where they like, so you have to be even more careful.

House rules: if you want to play me on Twitter, you can go first as O, and please use # MT3 as the hashtag, or I may not see it. I can keep track of the board, and will tweet it when I play. I should warn you that I am a truly dreadful player, so don't expect too much.

There's an ulterior motive of course. I'm interested in exploring a number of topics in programming, microservice architectures, AI, front ends, mobile programs, and so on, but if I have to read one more tutorial on an MVC todo list, I shall swing for it. I think MT3 makes a novel substitute and I shall be playing with it for the next little while.



