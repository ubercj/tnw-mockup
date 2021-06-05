# Building with Responsive Design

This is a project from The Odin Project's curriculum - read more about this assignment [here](https://www.theodinproject.com/paths/full-stack-ruby-on-rails/courses/html-and-css/lessons/building-with-responsive-design).

The goal of this project is to mimic the layout of [the TNW site](https://thenextweb.com/). They use media queries to gracefully transition between devices with different screen widths.

See my page live [here](https://ubercj.github.io/tnw-mockup/). To see the different layouts from the different media queries, you'll want to change the size of your browser window or use the Responsive Design mode in your browser's developer tools.

The 3 different layouts have the following breakpoints for screen width:
* 1024 px or wider
* Between 768 and 1023 px wide
* 767 px or less

I actually found this to be pretty fun, and the Responsive Design mode in Firefox Developer Tools was incredibly helpful and easy to use.

One cool thing that I learned while building this project was how to deal with content within a page that has a scrollbar, and sort of "disappears" as you scroll. The Videos and Channels sections of the page both have this.

I found out that the solution is 2-part. First, if you want to be able to scroll horizontally for example, you set the container element to `overflow-x: auto;`. Then - and this was the part that was unintuitive to me - the child elements must have a flex attribute like so: `flex: 0 0 150px`. The flex basis can be any size you want, but it has to be included, and both the `flex-grow` and `flex-shrink` must be set to 0.
