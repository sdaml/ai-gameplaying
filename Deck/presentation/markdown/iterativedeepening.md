# Iterative Deepening

The number of game states explored increases exponentially with respect to the depth searched.

Enter iterative deepening depth-first search: we can repeatedly run depth limited searches on the game tree to
yeild results for each depth limited search.

Somewhat surprisingly this strategy doesn't waste all that much time. Since the search is exponential the run time is actually dominated by the last level of the game tree we've explored.

```
 # Pseudocode
procedure IDDFS(root):
    for depth from 0 to ∞
        found ← DLS(root, depth)
        if found ≠ null
            yeild found
```