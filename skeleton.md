What happens to the layout when you resize the screen to less than 550 px. How do you think that works?

The websites goes from having some elements organized in a horizontal way to having all elements organized vertically. This is done via the use of media queries.

Skeleton is a mobile first designed website. This means that it set up the way in which it would look on a phone, in this case something 550px or less. Media queries are then used to adjust the sites elements to better suit screens with a higher resolution. 

For example, if we take padding in .section and see how it is adjusted to better suit different resolutions:

In the main part of the CSS you can see this

.section {
  padding: 8rem 0 7rem;
  text-align: center;
}

which is applied to only screens with a resolution of 550px or less. Further down the CSS you see this

@media (min-width: 550px) {
  .section {
    padding: 12rem 0 11rem;
  }

This overrides the above code for every screen bigger than 550px and makes the padding in .section 12rem 0 11rem instead of the original 8rem 0 7rem. This continues in the CSS all the way up to

@media (min-width: 1000px) {
  .section {
    padding: 20rem 0 19rem;
  }
