# Minimax algorithm

In two player adversarial games, one player aims to maximize their own score based on some heuristic and the other
player aims to minimize the other players scores (effectively maximizing their own).

Choose the best moves based on the maximum value on levels of the game tree where it's our turn, and minimum valued moves when it isn't our turn.

```
# Pseudocode
procedure minimax(node, depth, maximizingPlayer):
    if depth = 0 or node is a terminal node
        return the heuristic value of node

    if maximizingPlayer
        bestValue := −∞
        for each child of node
            v := minimax(child, depth − 1, FALSE)
            bestValue := max(bestValue, v)
        return bestValue

    else
        bestValue := +∞
        for each child of node
            v := minimax(child, depth − 1, TRUE)
            bestValue := min(bestValue, v)
        return bestValue
```