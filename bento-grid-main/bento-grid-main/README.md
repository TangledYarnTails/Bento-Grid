# Bento Grid

This was my first attempt at a bento grid. I also don't know what to really put in these README files, so here is a short reflection.

# Challenge 1: No Scrollbar
I wanted the grid to fit in the browser without scrollbars and to be centered in the viewport. I was hesitant to use the 'overflow: hidden' property since I didn’t want the content to just cut off, I wanted it to truly fit into the screen. But I ended up using it anyway since it was a sure way to get the scroll bar not to display. I also had issues when trying to scale down the entire grid while keeping the same dimension ratios of the child elements. I had gotten the grid how I liked it but it was overflowing ever so slightly. Eventually the line of code that fixed it was

```
scale: min(90vh / 1000px, 100vw / 1200px);

```
I don’t really know how this line of code works fully but I intend to learn more after completing this project. I just know that it scales the child within whatever this line is attached to. But the way it scales is similar to how you would zoom out of an image. It maintains the aspect ratio, and doesn’t scale everything individually (I think..)

# Challenge 2: Last Child in the Flex Grid
 I knew that I should use the flex grid when I started this project but where I ran into problems was with the last element in the grid and with centering/ scaling the overall grid within the body container. It took me a long time to figure out that the last child within my grid (bottom right rectangle) was what was causing the last row’s elements to be larger than what they were supposed to be. I knew that but I couldn’t figure out how to combat this problem for the longest time. Eventually I found that the solution to my issue was to change that specific element’s display from ‘flex’ to ‘grid’. This element was not being contained properly within its grid area, in other words it was not taking up two columns like I had assigned it to. So when I changed the display from flex to grid, I was able to assign it two distinct columns. Then in the overall grid, that element was able to properly nest itself across the two columns like I wanted.
