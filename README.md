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
x ∈ S, its current number of wins is wx. Also, for two teams x, y ∈ S, they still have to play gxy games against one another. Finally, we are given a specific team z.
We will use maximum-flowtechniques to achieve the following two things.
First, we give an efficient algorithm to decide whether z has been eliminated
from first place—or, to put it in positive terms, whether it is possible to choose
outcomes for all the remaining games in such a way that the team z ends with
at least as many wins as every other team in S. Second, we prove the following
clean characterization theorem for baseball elimination—essentially, that there
is always a short “proof” when a team has been eliminated.
As a second, more complex illustration of how the averaging argument in
works, consider the following example. Suppose we have the same four
teams as before, but now the current number of wins is
New York: 90, Baltimore: 88, Toronto: 87, Boston: 79.
The remaining games are as follows. Boston still has four games against each
of the other three teams. Baltimore has one more game against each of New
York and Toronto. And finally, New York and Toronto still have six games left
to play against each other. Clearly, things don’t look good for Boston, but is it
actually eliminated?
The answer is yes; Boston has been eliminated. To see this, first note
that Boston can end with at most 91 wins; and now consider the set of teams
T = {New York, Toronto}. Together New York and Toronto already have 177
wins; their six remaining games will result in a total of 183; and 183/2 > 91.
This means that one of them must end up with more than 91 wins, and so
Boston can’t finish in first. Interestingly, in this instance the set of all three
teams ahead of Boston cannot constitute a similar proof: All three teams taken
togeher have a total of 265 wins with 8 games left among them; this is a total
of 273, and 273/3= 91— not enough by itself to prove that Boston couldn’t end
up in a multi-way tie for first. So it’s crucial for the averaging argument that we
choose the set T consisting just of New York and Toronto, and omit Baltimore.
