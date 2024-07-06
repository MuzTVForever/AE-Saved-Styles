
# Æstetik Saved Styles  
My default styles and utils for future projects. Part of this code from [ÆstetikWeb](./src/_vars.scss).

## How to get this package

Install this package using npm or via other manager 

~~~bash  
  npm i @nvrbts/aestetik-saved-styles
~~~
or
~~~bash  
  bun add @nvrbts/aestetik-saved-styles
~~~

## Usage/Examples  
<b>Import into scss file</b>
~~~scss  
  // my-project/index.scss
  @import "@nvrbts/aestetik-saved-styles";
~~~  

<b>How to create own themes</b>
~~~html  
  // in html file
  <html data-theme='theme-1'>
~~~  
~~~scss  
  // in scss file
  @import "@nvrbts/aestetik-saved-styles";

  $themes: (
    "theme-1": (
      bg-color: white,
      text-color: black,
    ),
    "theme-2": (
      bg-color: black,
      text-color: white,
    ),
  );

  @include themify($themes) {
      background-color: themed('bg-color');
      color: themed('text-color');
  }
~~~  

<b>How to use breakpoints</b>

<i>breakpoint-min; breakpoint-max; breakpoint-between;</i> 
~~~scss  
  // in scss file
  @import "@nvrbts/aestetik-saved-styles";

  .element {
      display: grid;
      grid-template-columns: repeat(2, 1fr);

      @include breakpoint-max(md) {               -->    @media only screen and (max-width: 720px) {
          grid-template-columns: repeat(1, 1fr);  -->        grid-template-columns: repeat(1, 1fr);    
      }                                           -->    }
  }
~~~  
