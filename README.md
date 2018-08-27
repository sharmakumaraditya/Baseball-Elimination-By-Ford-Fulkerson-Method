# Baseball-Elimination-By-Ford-Fulkerson-Method
Problem Statement:
It is a Program to check wheteher there are chances for a team to win the tournament ith first place or not.
Suppose you’re a reporter for the Algorithmic Sporting News, and the following
situation arises late one September. There are four baseball teams trying to
finish in first place in the American League Eastern Division; let’s call them
New York, Baltimore, Toronto, and Boston. Currently, each team has the
following number of wins:
New York: 92, Baltimore: 91, Toronto: 91, Boston: 90.
There are five games left in the season: These consist of all possible pairings
of the four teams above, except for New York and Boston.
The question is: Can Boston finish with at least as many wins as every
other team in the division (that is, finish in first place, possibly in a tie)?
If you think about it, you realize that the answer is no. One argument is
the following. Clearly, Boston must win both its remaining games and New
York must lose both its remaining games. But this means that Baltimore and
Toronto will both beat New York; so then the winner of the Baltimore-Toronto
game will end up with the most wins.
Here’s an argument that avoids this kind of cases analysis. Boston can
finish with at most 92 wins. Cumulatively, the other three teams have 274
wins currently, and their three games against each other will produce exactly
three more wins, for a final total of 277. But 277 wins over three teams means
that one of them must have ended up with more than 92 wins.
So now you might start wondering: (i) Is there an efficient algorithm
to determine whether a team has been eliminated from first place? And (ii)
whenever a team has been eliminated from first place, is there an “averaging”
argument like this that proves it?
In more concrete notation, suppose we have a set S of teams, and for each
x ∈ S, its current number of wins is wx. Also, for two teams x, y ∈ S, they still
