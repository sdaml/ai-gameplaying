# Responsiveness

These game trees can become very very large very quickly
![](https://s3.amazonaws.com/content.udacity-data.com/courses/ud954/images/isolation-L6_leafValues.svg)

### Timeout
- We'll need some technique to ensure the AI responds in a timely fashion
 - Use a timer that throws a timeout exception after an alloted time
 - Calculate as much as possible in the alloted time and return the best result
 - How to ensure there's a result ready at timeout?