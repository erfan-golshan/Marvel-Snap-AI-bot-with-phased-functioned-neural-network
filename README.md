# Marvel-Snap-card-game-with-phased-functioned-neural-network

Dream Rain game company

Erfan Golshan, Artificial intelligence maker and game designer

---------------------------------------------------------------------------


* Introduction

Neural networks have found applications in mobile games, enhancing the gaming experience and enabling intelligent behaviors. They can be used for various purposes, such as character recognition, game control, 
adaptive difficulty, and player behavior analysis. Neural networks can learn from player actions, adapt the game dynamics accordingly, and provide personalized experiences. They can also be utilized for visual 
recognition tasks, allowing games to recognize objects, characters, or gestures in real-time. With the integration of AI and neural networks, mobile games can offer more immersive and interactive experiences. 

They can adapt to players' preferences, provide challenging gameplay, and even simulate intelligent opponents. The use of AI technologies in mobile games continues to evolve, enabling developers to create more 
engaging and dynamic experiences for players.

---------------------------------------------------------------------------
* About Marvel Snap card game

In Marvel Snap, players build decks of 12 cards and battle against other players. Like other card battlers, each card has an energy cost (from one to six) and a power level (but no health – these cards do not 
fight each other). On turn one, you have one energy. On turn two, you have two, all the way up to six at turn six. Each battle takes place over three locations – neutral cards that have their own effects (e.g. 
“Cards can’t be played here after turn 4” or “Cards here get +1 power.”). The first location reveals itself on the first turn, the second location on the second turn, and the third on the third turn. In order to
win each battle, you simply need to win two of the three locations. Tiebreakers are determined by total power.

![marvel-snap-official-announcement-and-gameplay-first-look-4-37-screenshot_feature](https://github.com/erfan-golshan/Marvel-Snap-card-game-with-phased-functioned-neural-network/assets/129675348/13ed9bc7-4b33-474f-91d9-8ec63b94828b)
![screen_shot_4558](https://github.com/erfan-golshan/Marvel-Snap-card-game-with-phased-functioned-neural-network/assets/129675348/dab1d9f3-ccef-48d6-983b-e9cb18d917be)



---------------------------------------------------------------------------
* Our objective

Our goal is to build the artificial intelligence of a person. It means to upload his game data to the robot and the robot will learn from him and then play like him.

---------------------------------------------------------------------------
* Investigating the interpolation method

In this method, we give a series of points from the domain of an unknown function to the neural network and give the value of the function at that point as an answer. Then we train the network. Finally, the 
network takes the form of that unknown function and learns to relate the domain points to the solution points. Our problem is similar. In a situation, we need to extract the data of the cards in person's hand 
and give the card he played as an answer. Then, finally, when the network trained completely, we call it every turn and get the answer. If it has seen that situation before, it will give the exact answer, but if 
the answer was not in its dataset, because it has been learned, it will answer the interpolated value of that data. 

But it depends on good categorizing the data of each game.

---------------------------------------------------------------------------
* How to implement neural network

In each turn, the total energy(cost) defines the cards that can be played. And the result of power conquering of each location is given from the last turn. Imagine on turn n with location power result of t, the 
combinations of the valid cards (sum of the cost of them are equal to n) are p1, p2, p3, …, pi. For example, p1 is the set of two cards. First of all, a neural network should choose one of these valid 
combinations and second of all, a different neural network should choose which card of this combination should be played on which location.


---------------------------------------------------------------------------
* Training the network

By using the above algorithm (phased-function neural network), we trained our neural networks (with the help of PyTorch library). As you can see from this implementation, there are multiple parallel networks 
that are being trained simultaneously. 


