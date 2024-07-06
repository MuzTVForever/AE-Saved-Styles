
# How to create own themes

U can create your own themes, using this packege. 

1. Add to html tag attribute data-theme with name one of your theme.

~~~html  
  <!-- in html file -->
  <html data-theme='theme-1'>
~~~  
2. Create some themes in your scss file:
~~~scss  
  // in scss file
  @import "ae-webkit";

  $themes: (
      "theme-1": (
          bg-color: white,
          text-color: black,
          font-size: 16px,
      ),
      "theme-2": (
          bg-color: black,
          text-color: white,
          font-size: 12px,
      ),
  );
~~~  
3. Now, u can use mixin "themify", like this
~~~scss  
  @include themify($themes) {
      body {
          background-color: themed('bg-color');
          color: themed('text-color');
          font-size: themed('font-size');
      } 
  }
~~~  
In css it will be like this:
~~~css  
  [data-theme='theme-1'] body {
      background-color: white;
      color: black;
      font-size: 16px;
  }
  [data-theme='theme-2'] body {
      background-color: black;
      color: white;
      font-size: 20px;
  }
~~~  