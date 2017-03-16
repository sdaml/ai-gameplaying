# Alphabeta Pruning Algorithm

An improvement on the runtime of a minimax search tree. Returns the same result that a minimax search would, but ignores branches of the search tree that cannot possibly influence the final result.

We can ignore branches by keeping track of the previously examined best move from earlier points in the search tree

```
# Pseudocode
procedure alphabeta(node, depth, α, β, maximizingPlayer):
    if depth = 0 or node is a terminal node
        return the heuristic value of node
    if maximizingPlayer
        v := -∞
        for each child of node
            v := max(v, alphabeta(child, depth – 1, α, β, FALSE))
            α := max(α, v)
            if β ≤ α
                break (* β cut-off *)
        return v
    else
        v := ∞
        for each child of node
            v := min(v, alphabeta(child, depth – 1, α, β, TRUE))
            β := min(β, v)
            if β ≤ α
                break (* α cut-off *)
        return v
```