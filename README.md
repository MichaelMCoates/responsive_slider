# responsive_switch

[Live Link](http://www.michaelmcoates.com/responsive_switch/)

Lessons learned from this:
- It's incredibly difficult to make a both vertically and horizontally-responsive circle. The best technique I found used an svg.
- It's bad practice to default `transition` to `all`. You will end up triggering transitions for all of your styles.
  - Placing an empty `script` tag at the bottom of the page fixes this problem for initial page load, but doesn't fix it for page refresh.
- When I was making the switch responsive, it was easy to set transitions against the page view width, but I had to be more careful when setting against a containing `div`.
  - To translate the `handle` responsively, I had to create a `handle-wrapper` `div` and translate that instead, because I needed a reference to the `switch-button`'s width.
- Using CSS variables is sweet, but when trying to set variables to percentages, those percentages are based on the current element, not the first parent element for that variable. 
