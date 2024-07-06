
# How to use breakpoints

<b>Available mixins</b><br>
<i>breakpoint-min(point)</i> - for @media (min-width: px)<br>
<i>breakpoint-max(point)</i> - for @media (max-width: px)<br>
<i>breakpoint-between(point, point) - for @media (min-width: px) and (max-width: px)</i> 

<b>Available breakpoints</b><br>
~~~txt  
Breakpoint    | Class infix | Dimensions
Small         |     sm      | 480px
Medium        |     md      | 720px
Large         |     lg      | 960px
Extra large   |     xl      | 1200px
~~~
<b>How to use</b><br>
~~~scss  
  // in scss file
  @import "ae-webkit";

  .element {
      display: grid;
      grid-template-columns: repeat(2, 1fr);

      @include breakpoint-max(md) {
          grid-template-columns: repeat(1, 1fr);
      }
  }
~~~ 
In css it will be like this:
~~~css  
  .element {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
  }

  @media only screen and (max-width: 720px) {
      .element {
          grid-template-columns: repeat(1, 1fr);
      }
  }
~~~  
