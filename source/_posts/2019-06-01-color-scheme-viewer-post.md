---
title: "Viewing Sass Themes Colors with Color Swatches"
published: true
---


# Color Swatch


<div class="box">
  <div class="swatch_group">
    <div class="swatch color-maximumred">
      <span class="swatch__name">maximumred</span>
      <span class="swatch__color" data-color="#d92121"></span>
      <span class="swatch__bgcolor" data-color-name="maximumred"></span>
    </div>
    <div class="swatch color-indianred">
      <span class="swatch__name">indianred</span>
      <span class="swatch__color" data-color="#b94e48"></span>
      <span class="swatch__bgcolor" data-color-name="indianred"></span>
    </div>
    <div class="swatch color-orangered">
      <span class="swatch__name">orangered</span>
      <span class="swatch__color" data-color="#ff5349"></span>
      <span class="swatch__bgcolor" data-color-name="orangered"></span>
    </div>
  </div>
</div>


```html
 <div class="swatch_group">
   ...
   <div class="swatch color-${COLOR_NAME}">
     <span class="swatch__name">${COLOR_NAME}</span>
     <span class="swatch__color" data-color="${COLOR_VALUE}"></span>
     <span class="swatch__bgcolor" data-name="${COLOR_NAME}"></span>
   </div>
   ....
 </div>
```

One of the problems that comes up with frontend development using libraries and functions to create your stylesheets is that you dont always have a visual reference to what is available in your current project.  

If youre using bootstrap you can go to their site and check out the styleguide, but in a lot of cases (almost always) the styles have been added to, modified, or combined with other libraries.

So how do you see all the colors the project your'e working on has if there is no realtime reference guide.  This is what motivated me to create the color swatch component for my style library. The color swatch is basically a single block element that uses the 'currentColor' property and inheritance to show you several variations of text and color using a color utility class.  The data-[property] fields are used to display the text for ::before and ::after elements, which lets me set the text once and display it in both the light and dark variation.

I also have a handful of sass mixins that will dynamicaly write in comment blocks to the color sections of the color definition sections with html to show all the colors in a theme.

For an example I created a swatch set for the Crayola color set https://www.crayola.com/explore-colors/

<div class="swatch_group">
  <h2 class="swatch_group__title">standard</h2>
<div class="swatch color-red">
  <span class="swatch__name">red</span>
  <span class="swatch__color" data-color="#ed0a3f"></span>
  <span class="swatch__bgcolor" data-color-name="red"></span>
</div>
<div class="swatch color-maroon">
  <span class="swatch__name">maroon</span>
  <span class="swatch__color" data-color="#c32148"></span>
  <span class="swatch__bgcolor" data-color-name="maroon"></span>
</div>
<div class="swatch color-scarlet">
  <span class="swatch__name">scarlet</span>
  <span class="swatch__color" data-color="#fd0e35"></span>
  <span class="swatch__bgcolor" data-color-name="scarlet"></span>
</div>
<div class="swatch color-brickred">
  <span class="swatch__name">brickred</span>
  <span class="swatch__color" data-color="#c62d42"></span>
  <span class="swatch__bgcolor" data-color-name="brickred"></span>
</div>
<div class="swatch color-englishvermilion">
  <span class="swatch__name">englishvermilion</span>
  <span class="swatch__color" data-color="#cc474b"></span>
  <span class="swatch__bgcolor" data-color-name="englishvermilion"></span>
</div>
<div class="swatch color-madderlake">
  <span class="swatch__name">madderlake</span>
  <span class="swatch__color" data-color="#cc3336"></span>
  <span class="swatch__bgcolor" data-color-name="madderlake"></span>
</div>
<div class="swatch color-maximumred">
  <span class="swatch__name">maximumred</span>
  <span class="swatch__color" data-color="#d92121"></span>
  <span class="swatch__bgcolor" data-color-name="maximumred"></span>
</div>
<div class="swatch color-indianred">
  <span class="swatch__name">indianred</span>
  <span class="swatch__color" data-color="#b94e48"></span>
  <span class="swatch__bgcolor" data-color-name="indianred"></span>
</div>
<div class="swatch color-orangered">
  <span class="swatch__name">orangered</span>
  <span class="swatch__color" data-color="#ff5349"></span>
  <span class="swatch__bgcolor" data-color-name="orangered"></span>
</div>
<div class="swatch color-sunsetorange">
  <span class="swatch__name">sunsetorange</span>
  <span class="swatch__color" data-color="#fe4c40"></span>
  <span class="swatch__bgcolor" data-color-name="sunsetorange"></span>
</div>
<div class="swatch color-bittersweet">
  <span class="swatch__name">bittersweet</span>
  <span class="swatch__color" data-color="#fe6f5e"></span>
  <span class="swatch__bgcolor" data-color-name="bittersweet"></span>
</div>
<div class="swatch color-darkvenetianred">
  <span class="swatch__name">darkvenetianred</span>
  <span class="swatch__color" data-color="#b33b24"></span>
  <span class="swatch__bgcolor" data-color-name="darkvenetianred"></span>
</div>
<div class="swatch color-venetianred">
  <span class="swatch__name">venetianred</span>
  <span class="swatch__color" data-color="#cc553d"></span>
  <span class="swatch__bgcolor" data-color-name="venetianred"></span>
</div>
<div class="swatch color-lightvenetianred">
  <span class="swatch__name">lightvenetianred</span>
  <span class="swatch__color" data-color="#e6735c"></span>
  <span class="swatch__bgcolor" data-color-name="lightvenetianred"></span>
</div>
<div class="swatch color-vividtangerine">
  <span class="swatch__name">vividtangerine</span>
  <span class="swatch__color" data-color="#ff9980"></span>
  <span class="swatch__bgcolor" data-color-name="vividtangerine"></span>
</div>
<div class="swatch color-middlered">
  <span class="swatch__name">middlered</span>
  <span class="swatch__color" data-color="#e58e73"></span>
  <span class="swatch__bgcolor" data-color-name="middlered"></span>
</div>
<div class="swatch color-burntorange">
  <span class="swatch__name">burntorange</span>
  <span class="swatch__color" data-color="#ff7f49"></span>
  <span class="swatch__bgcolor" data-color-name="burntorange"></span>
</div>
<div class="swatch color-redorange">
  <span class="swatch__name">redorange</span>
  <span class="swatch__color" data-color="#ff681f"></span>
  <span class="swatch__bgcolor" data-color-name="redorange"></span>
</div>
<div class="swatch color-orange">
  <span class="swatch__name">orange</span>
  <span class="swatch__color" data-color="#ff8833"></span>
  <span class="swatch__bgcolor" data-color-name="orange"></span>
</div>
<div class="swatch color-macaroniandcheese">
  <span class="swatch__name">macaroniandcheese</span>
  <span class="swatch__color" data-color="#ffb97b"></span>
  <span class="swatch__bgcolor" data-color-name="macaroniandcheese"></span>
</div>
<div class="swatch color-middleyellowred">
  <span class="swatch__name">middleyellowred</span>
  <span class="swatch__color" data-color="#ecb176"></span>
  <span class="swatch__bgcolor" data-color-name="middleyellowred"></span>
</div>
<div class="swatch color-mangotango">
  <span class="swatch__name">mangotango</span>
  <span class="swatch__color" data-color="#e77200"></span>
  <span class="swatch__bgcolor" data-color-name="mangotango"></span>
</div>
<div class="swatch color-yelloworange">
  <span class="swatch__name">yelloworange</span>
  <span class="swatch__color" data-color="#ffae42"></span>
  <span class="swatch__bgcolor" data-color-name="yelloworange"></span>
</div>
<div class="swatch color-maximumyellowred">
  <span class="swatch__name">maximumyellowred</span>
  <span class="swatch__color" data-color="#f2ba49"></span>
  <span class="swatch__bgcolor" data-color-name="maximumyellowred"></span>
</div>
<div class="swatch color-bananamania">
  <span class="swatch__name">bananamania</span>
  <span class="swatch__color" data-color="#fbe7b2"></span>
  <span class="swatch__bgcolor" data-color-name="bananamania"></span>
</div>
<div class="swatch color-maize">
  <span class="swatch__name">maize</span>
  <span class="swatch__color" data-color="#f2c649"></span>
  <span class="swatch__bgcolor" data-color-name="maize"></span>
</div>
<div class="swatch color-orangeyellow">
  <span class="swatch__name">orangeyellow</span>
  <span class="swatch__color" data-color="#f8d568"></span>
  <span class="swatch__bgcolor" data-color-name="orangeyellow"></span>
</div>
<div class="swatch color-goldenrod">
  <span class="swatch__name">goldenrod</span>
  <span class="swatch__color" data-color="#fcd667"></span>
  <span class="swatch__bgcolor" data-color-name="goldenrod"></span>
</div>
<div class="swatch color-dandelion">
  <span class="swatch__name">dandelion</span>
  <span class="swatch__color" data-color="#fed85d"></span>
  <span class="swatch__bgcolor" data-color-name="dandelion"></span>
</div>
<div class="swatch color-yellow">
  <span class="swatch__name">yellow</span>
  <span class="swatch__color" data-color="#fbe870"></span>
  <span class="swatch__bgcolor" data-color-name="yellow"></span>
</div>
<div class="swatch color-greenyellow">
  <span class="swatch__name">greenyellow</span>
  <span class="swatch__color" data-color="#f1e788"></span>
  <span class="swatch__bgcolor" data-color-name="greenyellow"></span>
</div>
<div class="swatch color-middleyellow">
  <span class="swatch__name">middleyellow</span>
  <span class="swatch__color" data-color="#ffeb00"></span>
  <span class="swatch__bgcolor" data-color-name="middleyellow"></span>
</div>
<div class="swatch color-olivegreen">
  <span class="swatch__name">olivegreen</span>
  <span class="swatch__color" data-color="#b5b35c"></span>
  <span class="swatch__bgcolor" data-color-name="olivegreen"></span>
</div>
<div class="swatch color-springgreen">
  <span class="swatch__name">springgreen</span>
  <span class="swatch__color" data-color="#ecebbd"></span>
  <span class="swatch__bgcolor" data-color-name="springgreen"></span>
</div>
<div class="swatch color-maximumyellow">
  <span class="swatch__name">maximumyellow</span>
  <span class="swatch__color" data-color="#fafa37"></span>
  <span class="swatch__bgcolor" data-color-name="maximumyellow"></span>
</div>
<div class="swatch color-canary">
  <span class="swatch__name">canary</span>
  <span class="swatch__color" data-color="#ffff99"></span>
  <span class="swatch__bgcolor" data-color-name="canary"></span>
</div>
<div class="swatch color-lemonyellow">
  <span class="swatch__name">lemonyellow</span>
  <span class="swatch__color" data-color="#ffff9f"></span>
  <span class="swatch__bgcolor" data-color-name="lemonyellow"></span>
</div>
<div class="swatch color-maximumgreenyellow">
  <span class="swatch__name">maximumgreenyellow</span>
  <span class="swatch__color" data-color="#d9e650"></span>
  <span class="swatch__bgcolor" data-color-name="maximumgreenyellow"></span>
</div>
<div class="swatch color-middlegreenyellow">
  <span class="swatch__name">middlegreenyellow</span>
  <span class="swatch__color" data-color="#acbf60"></span>
  <span class="swatch__bgcolor" data-color-name="middlegreenyellow"></span>
</div>
<div class="swatch color-inchworm">
  <span class="swatch__name">inchworm</span>
  <span class="swatch__color" data-color="#afe313"></span>
  <span class="swatch__bgcolor" data-color-name="inchworm"></span>
</div>
<div class="swatch color-lightchromegreen">
  <span class="swatch__name">lightchromegreen</span>
  <span class="swatch__color" data-color="#bee64b"></span>
  <span class="swatch__bgcolor" data-color-name="lightchromegreen"></span>
</div>
<div class="swatch color-yellowgreen">
  <span class="swatch__name">yellowgreen</span>
  <span class="swatch__color" data-color="#c5e17a"></span>
  <span class="swatch__bgcolor" data-color-name="yellowgreen"></span>
</div>
<div class="swatch color-maximumgreen">
  <span class="swatch__name">maximumgreen</span>
  <span class="swatch__color" data-color="#5e8c31"></span>
  <span class="swatch__bgcolor" data-color-name="maximumgreen"></span>
</div>
<div class="swatch color-asparagus">
  <span class="swatch__name">asparagus</span>
  <span class="swatch__color" data-color="#7ba05b"></span>
  <span class="swatch__bgcolor" data-color-name="asparagus"></span>
</div>
<div class="swatch color-grannysmithapple">
  <span class="swatch__name">grannysmithapple</span>
  <span class="swatch__color" data-color="#9de093"></span>
  <span class="swatch__bgcolor" data-color-name="grannysmithapple"></span>
</div>
<div class="swatch color-fern">
  <span class="swatch__name">fern</span>
  <span class="swatch__color" data-color="#63b76c"></span>
  <span class="swatch__bgcolor" data-color-name="fern"></span>
</div>
<div class="swatch color-middlegreen">
  <span class="swatch__name">middlegreen</span>
  <span class="swatch__color" data-color="#4d8c57"></span>
  <span class="swatch__bgcolor" data-color-name="middlegreen"></span>
</div>
<div class="swatch color-green">
  <span class="swatch__name">green</span>
  <span class="swatch__color" data-color="#3aa655"></span>
  <span class="swatch__bgcolor" data-color-name="green"></span>
</div>
<div class="swatch color-mediumchromegreen">
  <span class="swatch__name">mediumchromegreen</span>
  <span class="swatch__color" data-color="#6ca67c"></span>
  <span class="swatch__bgcolor" data-color-name="mediumchromegreen"></span>
</div>
<div class="swatch color-forestgreen">
  <span class="swatch__name">forestgreen</span>
  <span class="swatch__color" data-color="#5fa777"></span>
  <span class="swatch__bgcolor" data-color-name="forestgreen"></span>
</div>
<div class="swatch color-seagreen">
  <span class="swatch__name">seagreen</span>
  <span class="swatch__color" data-color="#93dfb8"></span>
  <span class="swatch__bgcolor" data-color-name="seagreen"></span>
</div>
<div class="swatch color-shamrock">
  <span class="swatch__name">shamrock</span>
  <span class="swatch__color" data-color="#33cc99"></span>
  <span class="swatch__bgcolor" data-color-name="shamrock"></span>
</div>
<div class="swatch color-mountainmeadow">
  <span class="swatch__name">mountainmeadow</span>
  <span class="swatch__color" data-color="#1ab385"></span>
  <span class="swatch__bgcolor" data-color-name="mountainmeadow"></span>
</div>
<div class="swatch color-junglegreen">
  <span class="swatch__name">junglegreen</span>
  <span class="swatch__color" data-color="#29ab87"></span>
  <span class="swatch__bgcolor" data-color-name="junglegreen"></span>
</div>
<div class="swatch color-caribbeangreen">
  <span class="swatch__name">caribbeangreen</span>
  <span class="swatch__color" data-color="#00cc99"></span>
  <span class="swatch__bgcolor" data-color-name="caribbeangreen"></span>
</div>
<div class="swatch color-tropicalrainforest">
  <span class="swatch__name">tropicalrainforest</span>
  <span class="swatch__color" data-color="#00755e"></span>
  <span class="swatch__bgcolor" data-color-name="tropicalrainforest"></span>
</div>
<div class="swatch color-middlebluegreen">
  <span class="swatch__name">middlebluegreen</span>
  <span class="swatch__color" data-color="#8dd9cc"></span>
  <span class="swatch__bgcolor" data-color-name="middlebluegreen"></span>
</div>
<div class="swatch color-pinegreen">
  <span class="swatch__name">pinegreen</span>
  <span class="swatch__color" data-color="#01786f"></span>
  <span class="swatch__bgcolor" data-color-name="pinegreen"></span>
</div>
<div class="swatch color-maximumbluegreen">
  <span class="swatch__name">maximumbluegreen</span>
  <span class="swatch__color" data-color="#30bfbf"></span>
  <span class="swatch__bgcolor" data-color-name="maximumbluegreen"></span>
</div>
<div class="swatch color-robinseggblue">
  <span class="swatch__name">robinseggblue</span>
  <span class="swatch__color" data-color="#00cccc"></span>
  <span class="swatch__bgcolor" data-color-name="robinseggblue"></span>
</div>
<div class="swatch color-tealblue">
  <span class="swatch__name">tealblue</span>
  <span class="swatch__color" data-color="#008080"></span>
  <span class="swatch__bgcolor" data-color-name="tealblue"></span>
</div>
<div class="swatch color-lightblue">
  <span class="swatch__name">lightblue</span>
  <span class="swatch__color" data-color="#8fd8d8"></span>
  <span class="swatch__bgcolor" data-color-name="lightblue"></span>
</div>
<div class="swatch color-aquamarine">
  <span class="swatch__name">aquamarine</span>
  <span class="swatch__color" data-color="#95e0e8"></span>
  <span class="swatch__bgcolor" data-color-name="aquamarine"></span>
</div>
<div class="swatch color-turquoiseblue">
  <span class="swatch__name">turquoiseblue</span>
  <span class="swatch__color" data-color="#6cdae7"></span>
  <span class="swatch__bgcolor" data-color-name="turquoiseblue"></span>
</div>
<div class="swatch color-outerspace">
  <span class="swatch__name">outerspace</span>
  <span class="swatch__color" data-color="#2d383a"></span>
  <span class="swatch__bgcolor" data-color-name="outerspace"></span>
</div>
<div class="swatch color-skyblue">
  <span class="swatch__name">skyblue</span>
  <span class="swatch__color" data-color="#76d7ea"></span>
  <span class="swatch__bgcolor" data-color-name="skyblue"></span>
</div>
<div class="swatch color-middleblue">
  <span class="swatch__name">middleblue</span>
  <span class="swatch__color" data-color="#7ed4e6"></span>
  <span class="swatch__bgcolor" data-color-name="middleblue"></span>
</div>
<div class="swatch color-bluegreen">
  <span class="swatch__name">bluegreen</span>
  <span class="swatch__color" data-color="#0095b7"></span>
  <span class="swatch__bgcolor" data-color-name="bluegreen"></span>
</div>
<div class="swatch color-pacificblue">
  <span class="swatch__name">pacificblue</span>
  <span class="swatch__color" data-color="#009dc4"></span>
  <span class="swatch__bgcolor" data-color-name="pacificblue"></span>
</div>
<div class="swatch color-cerulean">
  <span class="swatch__name">cerulean</span>
  <span class="swatch__color" data-color="#02a4d3"></span>
  <span class="swatch__bgcolor" data-color-name="cerulean"></span>
</div>
<div class="swatch color-maximumblue">
  <span class="swatch__name">maximumblue</span>
  <span class="swatch__color" data-color="#47abcc"></span>
  <span class="swatch__bgcolor" data-color-name="maximumblue"></span>
</div>
<div class="swatch color-bluei">
  <span class="swatch__name">bluei</span>
  <span class="swatch__color" data-color="#4997d0"></span>
  <span class="swatch__bgcolor" data-color-name="bluei"></span>
</div>
<div class="swatch color-ceruleanblue">
  <span class="swatch__name">ceruleanblue</span>
  <span class="swatch__color" data-color="#339acc"></span>
  <span class="swatch__bgcolor" data-color-name="ceruleanblue"></span>
</div>
<div class="swatch color-cornflower">
  <span class="swatch__name">cornflower</span>
  <span class="swatch__color" data-color="#93ccea"></span>
  <span class="swatch__bgcolor" data-color-name="cornflower"></span>
</div>
<div class="swatch color-greenblue">
  <span class="swatch__name">greenblue</span>
  <span class="swatch__color" data-color="#2887c8"></span>
  <span class="swatch__bgcolor" data-color-name="greenblue"></span>
</div>
<div class="swatch color-midnightblue">
  <span class="swatch__name">midnightblue</span>
  <span class="swatch__color" data-color="#00468c"></span>
  <span class="swatch__bgcolor" data-color-name="midnightblue"></span>
</div>
<div class="swatch color-navyblue">
  <span class="swatch__name">navyblue</span>
  <span class="swatch__color" data-color="#0066cc"></span>
  <span class="swatch__bgcolor" data-color-name="navyblue"></span>
</div>
<div class="swatch color-denim">
  <span class="swatch__name">denim</span>
  <span class="swatch__color" data-color="#1560bd"></span>
  <span class="swatch__bgcolor" data-color-name="denim"></span>
</div>
<div class="swatch color-blueiii">
  <span class="swatch__name">blueiii</span>
  <span class="swatch__color" data-color="#0066ff"></span>
  <span class="swatch__bgcolor" data-color-name="blueiii"></span>
</div>
<div class="swatch color-cadetblue">
  <span class="swatch__name">cadetblue</span>
  <span class="swatch__color" data-color="#a9b2c3"></span>
  <span class="swatch__bgcolor" data-color-name="cadetblue"></span>
</div>
<div class="swatch color-periwinkle">
  <span class="swatch__name">periwinkle</span>
  <span class="swatch__color" data-color="#c3cde6"></span>
  <span class="swatch__bgcolor" data-color-name="periwinkle"></span>
</div>
<div class="swatch color-blueii">
  <span class="swatch__name">blueii</span>
  <span class="swatch__color" data-color="#4570e6"></span>
  <span class="swatch__bgcolor" data-color-name="blueii"></span>
</div>
<div class="swatch color-wildblueyonder">
  <span class="swatch__name">wildblueyonder</span>
  <span class="swatch__color" data-color="#7a89b8"></span>
  <span class="swatch__bgcolor" data-color-name="wildblueyonder"></span>
</div>
<div class="swatch color-indigo">
  <span class="swatch__name">indigo</span>
  <span class="swatch__color" data-color="#4f69c6"></span>
  <span class="swatch__bgcolor" data-color-name="indigo"></span>
</div>
<div class="swatch color-manatee">
  <span class="swatch__name">manatee</span>
  <span class="swatch__color" data-color="#8d90a1"></span>
  <span class="swatch__bgcolor" data-color-name="manatee"></span>
</div>
<div class="swatch color-cobaltblue">
  <span class="swatch__name">cobaltblue</span>
  <span class="swatch__color" data-color="#8c90c8"></span>
  <span class="swatch__bgcolor" data-color-name="cobaltblue"></span>
</div>
<div class="swatch color-celestialblue">
  <span class="swatch__name">celestialblue</span>
  <span class="swatch__color" data-color="#7070cc"></span>
  <span class="swatch__bgcolor" data-color-name="celestialblue"></span>
</div>
<div class="swatch color-bluebell">
  <span class="swatch__name">bluebell</span>
  <span class="swatch__color" data-color="#9999cc"></span>
  <span class="swatch__bgcolor" data-color-name="bluebell"></span>
</div>
<div class="swatch color-maximumbluepurple">
  <span class="swatch__name">maximumbluepurple</span>
  <span class="swatch__color" data-color="#acace6"></span>
  <span class="swatch__bgcolor" data-color-name="maximumbluepurple"></span>
</div>
<div class="swatch color-violetblue">
  <span class="swatch__name">violetblue</span>
  <span class="swatch__color" data-color="#766ec8"></span>
  <span class="swatch__bgcolor" data-color-name="violetblue"></span>
</div>
<div class="swatch color-blueviolet">
  <span class="swatch__name">blueviolet</span>
  <span class="swatch__color" data-color="#6456b7"></span>
  <span class="swatch__bgcolor" data-color-name="blueviolet"></span>
</div>
<div class="swatch color-ultramarineblue">
  <span class="swatch__name">ultramarineblue</span>
  <span class="swatch__color" data-color="#3f26bf"></span>
  <span class="swatch__bgcolor" data-color-name="ultramarineblue"></span>
</div>
<div class="swatch color-middlebluepurple">
  <span class="swatch__name">middlebluepurple</span>
  <span class="swatch__color" data-color="#8b72be"></span>
  <span class="swatch__bgcolor" data-color-name="middlebluepurple"></span>
</div>
<div class="swatch color-purpleheart">
  <span class="swatch__name">purpleheart</span>
  <span class="swatch__color" data-color="#652dc1"></span>
  <span class="swatch__bgcolor" data-color-name="purpleheart"></span>
</div>
<div class="swatch color-royalpurple">
  <span class="swatch__name">royalpurple</span>
  <span class="swatch__color" data-color="#6b3fa0"></span>
  <span class="swatch__bgcolor" data-color-name="royalpurple"></span>
</div>
<div class="swatch color-violetii">
  <span class="swatch__name">violetii</span>
  <span class="swatch__color" data-color="#8359a3"></span>
  <span class="swatch__bgcolor" data-color-name="violetii"></span>
</div>
<div class="swatch color-mediumviolet">
  <span class="swatch__name">mediumviolet</span>
  <span class="swatch__color" data-color="#8f47b3"></span>
  <span class="swatch__bgcolor" data-color-name="mediumviolet"></span>
</div>
<div class="swatch color-wisteria">
  <span class="swatch__name">wisteria</span>
  <span class="swatch__color" data-color="#c9a0dc"></span>
  <span class="swatch__bgcolor" data-color-name="wisteria"></span>
</div>
<div class="swatch color-lavenderi">
  <span class="swatch__name">lavenderi</span>
  <span class="swatch__color" data-color="#bf8fcc"></span>
  <span class="swatch__bgcolor" data-color-name="lavenderi"></span>
</div>
<div class="swatch color-vividviolet">
  <span class="swatch__name">vividviolet</span>
  <span class="swatch__color" data-color="#803790"></span>
  <span class="swatch__bgcolor" data-color-name="vividviolet"></span>
</div>
<div class="swatch color-maximumpurple">
  <span class="swatch__name">maximumpurple</span>
  <span class="swatch__color" data-color="#733380"></span>
  <span class="swatch__bgcolor" data-color-name="maximumpurple"></span>
</div>
<div class="swatch color-purplemountainsmajesty">
  <span class="swatch__name">purplemountainsmajesty</span>
  <span class="swatch__color" data-color="#d6aedd"></span>
  <span class="swatch__bgcolor" data-color-name="purplemountainsmajesty"></span>
</div>
<div class="swatch color-fuchsia">
  <span class="swatch__name">fuchsia</span>
  <span class="swatch__color" data-color="#c154c1"></span>
  <span class="swatch__bgcolor" data-color-name="fuchsia"></span>
</div>
<div class="swatch color-pinkflamingo">
  <span class="swatch__name">pinkflamingo</span>
  <span class="swatch__color" data-color="#fc74fd"></span>
  <span class="swatch__bgcolor" data-color-name="pinkflamingo"></span>
</div>
<div class="swatch color-violeti">
  <span class="swatch__name">violeti</span>
  <span class="swatch__color" data-color="#732e6c"></span>
  <span class="swatch__bgcolor" data-color-name="violeti"></span>
</div>
<div class="swatch color-brilliantrose">
  <span class="swatch__name">brilliantrose</span>
  <span class="swatch__color" data-color="#e667ce"></span>
  <span class="swatch__bgcolor" data-color-name="brilliantrose"></span>
</div>
<div class="swatch color-orchid">
  <span class="swatch__name">orchid</span>
  <span class="swatch__color" data-color="#e29cd2"></span>
  <span class="swatch__bgcolor" data-color-name="orchid"></span>
</div>
<div class="swatch color-plum">
  <span class="swatch__name">plum</span>
  <span class="swatch__color" data-color="#8e3179"></span>
  <span class="swatch__bgcolor" data-color-name="plum"></span>
</div>
<div class="swatch color-mediumrose">
  <span class="swatch__name">mediumrose</span>
  <span class="swatch__color" data-color="#d96cbe"></span>
  <span class="swatch__bgcolor" data-color-name="mediumrose"></span>
</div>
<div class="swatch color-thistle">
  <span class="swatch__name">thistle</span>
  <span class="swatch__color" data-color="#ebb0d7"></span>
  <span class="swatch__bgcolor" data-color-name="thistle"></span>
</div>
<div class="swatch color-mulberry">
  <span class="swatch__name">mulberry</span>
  <span class="swatch__color" data-color="#c8509b"></span>
  <span class="swatch__bgcolor" data-color-name="mulberry"></span>
</div>
<div class="swatch color-redviolet">
  <span class="swatch__name">redviolet</span>
  <span class="swatch__color" data-color="#bb3385"></span>
  <span class="swatch__bgcolor" data-color-name="redviolet"></span>
</div>
<div class="swatch color-middlepurple">
  <span class="swatch__name">middlepurple</span>
  <span class="swatch__color" data-color="#d982b5"></span>
  <span class="swatch__bgcolor" data-color-name="middlepurple"></span>
</div>
<div class="swatch color-maximumredpurple">
  <span class="swatch__name">maximumredpurple</span>
  <span class="swatch__color" data-color="#a63a79"></span>
  <span class="swatch__bgcolor" data-color-name="maximumredpurple"></span>
</div>
<div class="swatch color-jazzberryjam">
  <span class="swatch__name">jazzberryjam</span>
  <span class="swatch__color" data-color="#a50b5e"></span>
  <span class="swatch__bgcolor" data-color-name="jazzberryjam"></span>
</div>
<div class="swatch color-eggplant">
  <span class="swatch__name">eggplant</span>
  <span class="swatch__color" data-color="#614051"></span>
  <span class="swatch__bgcolor" data-color-name="eggplant"></span>
</div>
<div class="swatch color-magenta">
  <span class="swatch__name">magenta</span>
  <span class="swatch__color" data-color="#f653a6"></span>
  <span class="swatch__bgcolor" data-color-name="magenta"></span>
</div>
<div class="swatch color-cerise">
  <span class="swatch__name">cerise</span>
  <span class="swatch__color" data-color="#da3287"></span>
  <span class="swatch__bgcolor" data-color-name="cerise"></span>
</div>
<div class="swatch color-wildstrawberry">
  <span class="swatch__name">wildstrawberry</span>
  <span class="swatch__color" data-color="#ff3399"></span>
  <span class="swatch__bgcolor" data-color-name="wildstrawberry"></span>
</div>
<div class="swatch color-lavenderii">
  <span class="swatch__name">lavenderii</span>
  <span class="swatch__color" data-color="#fbaed2"></span>
  <span class="swatch__bgcolor" data-color-name="lavenderii"></span>
</div>
<div class="swatch color-cottoncandy">
  <span class="swatch__name">cottoncandy</span>
  <span class="swatch__color" data-color="#ffb7d5"></span>
  <span class="swatch__bgcolor" data-color-name="cottoncandy"></span>
</div>
<div class="swatch color-carnationpink">
  <span class="swatch__name">carnationpink</span>
  <span class="swatch__color" data-color="#ffa6c9"></span>
  <span class="swatch__bgcolor" data-color-name="carnationpink"></span>
</div>
<div class="swatch color-violetred">
  <span class="swatch__name">violetred</span>
  <span class="swatch__color" data-color="#f7468a"></span>
  <span class="swatch__bgcolor" data-color-name="violetred"></span>
</div>
<div class="swatch color-razzmatazz">
  <span class="swatch__name">razzmatazz</span>
  <span class="swatch__color" data-color="#e30b5c"></span>
  <span class="swatch__bgcolor" data-color-name="razzmatazz"></span>
</div>
<div class="swatch color-pigpink">
  <span class="swatch__name">pigpink</span>
  <span class="swatch__color" data-color="#fdd7e4"></span>
  <span class="swatch__bgcolor" data-color-name="pigpink"></span>
</div>
<div class="swatch color-carmine">
  <span class="swatch__name">carmine</span>
  <span class="swatch__color" data-color="#e62e6b"></span>
  <span class="swatch__bgcolor" data-color-name="carmine"></span>
</div>
<div class="swatch color-blush">
  <span class="swatch__name">blush</span>
  <span class="swatch__color" data-color="#db5079"></span>
  <span class="swatch__bgcolor" data-color-name="blush"></span>
</div>
<div class="swatch color-ticklemepink">
  <span class="swatch__name">ticklemepink</span>
  <span class="swatch__color" data-color="#fc80a5"></span>
  <span class="swatch__bgcolor" data-color-name="ticklemepink"></span>
</div>
<div class="swatch color-mauvelous">
  <span class="swatch__name">mauvelous</span>
  <span class="swatch__color" data-color="#f091a9"></span>
  <span class="swatch__bgcolor" data-color-name="mauvelous"></span>
</div>
<div class="swatch color-salmon">
  <span class="swatch__name">salmon</span>
  <span class="swatch__color" data-color="#ff91a4"></span>
  <span class="swatch__bgcolor" data-color-name="salmon"></span>
</div>
<div class="swatch color-middleredpurple">
  <span class="swatch__name">middleredpurple</span>
  <span class="swatch__color" data-color="#a55353"></span>
  <span class="swatch__bgcolor" data-color-name="middleredpurple"></span>
</div>
<div class="swatch color-mahogany">
  <span class="swatch__name">mahogany</span>
  <span class="swatch__color" data-color="#ca3435"></span>
  <span class="swatch__bgcolor" data-color-name="mahogany"></span>
</div>
<div class="swatch color-melon">
  <span class="swatch__name">melon</span>
  <span class="swatch__color" data-color="#febaad"></span>
  <span class="swatch__bgcolor" data-color-name="melon"></span>
</div>
<div class="swatch color-pinksherbert">
  <span class="swatch__name">pinksherbert</span>
  <span class="swatch__color" data-color="#f7a38e"></span>
  <span class="swatch__bgcolor" data-color-name="pinksherbert"></span>
</div>
<div class="swatch color-burntsienna">
  <span class="swatch__name">burntsienna</span>
  <span class="swatch__color" data-color="#e97451"></span>
  <span class="swatch__bgcolor" data-color-name="burntsienna"></span>
</div>
<div class="swatch color-brown">
  <span class="swatch__name">brown</span>
  <span class="swatch__color" data-color="#af593e"></span>
  <span class="swatch__bgcolor" data-color-name="brown"></span>
</div>
<div class="swatch color-sepia">
  <span class="swatch__name">sepia</span>
  <span class="swatch__color" data-color="#9e5b40"></span>
  <span class="swatch__bgcolor" data-color-name="sepia"></span>
</div>
<div class="swatch color-fuzzywuzzy">
  <span class="swatch__name">fuzzywuzzy</span>
  <span class="swatch__color" data-color="#87421f"></span>
  <span class="swatch__bgcolor" data-color-name="fuzzywuzzy"></span>
</div>
<div class="swatch color-beaver">
  <span class="swatch__name">beaver</span>
  <span class="swatch__color" data-color="#926f5b"></span>
  <span class="swatch__bgcolor" data-color-name="beaver"></span>
</div>
<div class="swatch color-tumbleweed">
  <span class="swatch__name">tumbleweed</span>
  <span class="swatch__color" data-color="#dea681"></span>
  <span class="swatch__bgcolor" data-color-name="tumbleweed"></span>
</div>
<div class="swatch color-rawsienna">
  <span class="swatch__name">rawsienna</span>
  <span class="swatch__color" data-color="#d27d46"></span>
  <span class="swatch__bgcolor" data-color-name="rawsienna"></span>
</div>
<div class="swatch color-vandykebrown">
  <span class="swatch__name">vandykebrown</span>
  <span class="swatch__color" data-color="#664228"></span>
  <span class="swatch__bgcolor" data-color-name="vandykebrown"></span>
</div>
<div class="swatch color-tan">
  <span class="swatch__name">tan</span>
  <span class="swatch__color" data-color="#d99a6c"></span>
  <span class="swatch__bgcolor" data-color-name="tan"></span>
</div>
<div class="swatch color-desertsand">
  <span class="swatch__name">desertsand</span>
  <span class="swatch__color" data-color="#edc9af"></span>
  <span class="swatch__bgcolor" data-color-name="desertsand"></span>
</div>
<div class="swatch color-peach">
  <span class="swatch__name">peach</span>
  <span class="swatch__color" data-color="#ffcba4"></span>
  <span class="swatch__bgcolor" data-color-name="peach"></span>
</div>
<div class="swatch color-burntumber">
  <span class="swatch__name">burntumber</span>
  <span class="swatch__color" data-color="#805533"></span>
  <span class="swatch__bgcolor" data-color-name="burntumber"></span>
</div>
<div class="swatch color-apricot">
  <span class="swatch__name">apricot</span>
  <span class="swatch__color" data-color="#fdd5b1"></span>
  <span class="swatch__bgcolor" data-color-name="apricot"></span>
</div>
<div class="swatch color-almond">
  <span class="swatch__name">almond</span>
  <span class="swatch__color" data-color="#eed9c4"></span>
  <span class="swatch__bgcolor" data-color-name="almond"></span>
</div>
<div class="swatch color-rawumber">
  <span class="swatch__name">rawumber</span>
  <span class="swatch__color" data-color="#665233"></span>
  <span class="swatch__bgcolor" data-color-name="rawumber"></span>
</div>
<div class="swatch color-shadow">
  <span class="swatch__name">shadow</span>
  <span class="swatch__color" data-color="#837050"></span>
  <span class="swatch__bgcolor" data-color-name="shadow"></span>
</div>
<div class="swatch color-rawsiennai">
  <span class="swatch__name">rawsiennai</span>
  <span class="swatch__color" data-color="#e6bc5c"></span>
  <span class="swatch__bgcolor" data-color-name="rawsiennai"></span>
</div>
<div class="swatch color-timberwolf">
  <span class="swatch__name">timberwolf</span>
  <span class="swatch__color" data-color="#d9d6cf"></span>
  <span class="swatch__bgcolor" data-color-name="timberwolf"></span>
</div>
<div class="swatch color-goldi">
  <span class="swatch__name">goldi</span>
  <span class="swatch__color" data-color="#92926e"></span>
  <span class="swatch__bgcolor" data-color-name="goldi"></span>
</div>
<div class="swatch color-goldii">
  <span class="swatch__name">goldii</span>
  <span class="swatch__color" data-color="#e6be8a"></span>
  <span class="swatch__bgcolor" data-color-name="goldii"></span>
</div>
<div class="swatch color-silver">
  <span class="swatch__name">silver</span>
  <span class="swatch__color" data-color="#c9c0bb"></span>
  <span class="swatch__bgcolor" data-color-name="silver"></span>
</div>
<div class="swatch color-copper">
  <span class="swatch__name">copper</span>
  <span class="swatch__color" data-color="#da8a67"></span>
  <span class="swatch__bgcolor" data-color-name="copper"></span>
</div>
<div class="swatch color-antiquebrass">
  <span class="swatch__name">antiquebrass</span>
  <span class="swatch__color" data-color="#c88a65"></span>
  <span class="swatch__bgcolor" data-color-name="antiquebrass"></span>
</div>
<div class="swatch color-black">
  <span class="swatch__name">black</span>
  <span class="swatch__color" data-color="#000000"></span>
  <span class="swatch__bgcolor" data-color-name="black"></span>
</div>
<div class="swatch color-charcoalgray">
  <span class="swatch__name">charcoalgray</span>
  <span class="swatch__color" data-color="#736a62"></span>
  <span class="swatch__bgcolor" data-color-name="charcoalgray"></span>
</div>
<div class="swatch color-gray">
  <span class="swatch__name">gray</span>
  <span class="swatch__color" data-color="#8b8680"></span>
  <span class="swatch__bgcolor" data-color-name="gray"></span>
</div>
<div class="swatch color-bluegray">
  <span class="swatch__name">bluegray</span>
  <span class="swatch__color" data-color="#c8c8cd"></span>
  <span class="swatch__bgcolor" data-color-name="bluegray"></span>
</div>
<style>
.color-red { color: #ed0a3f !important; }
.color-maroon { color: #c32148 !important; }
.color-scarlet { color: #fd0e35 !important; }
.color-brickred { color: #c62d42 !important; }
.color-englishvermilion { color: #cc474b !important; }
.color-madderlake { color: #cc3336 !important; }
.color-permanentgeraniumlake { color: #e12c2c !important; }
.color-maximumred { color: #d92121 !important; }
.color-indianred { color: #b94e48 !important; }
.color-orangered { color: #ff5349 !important; }
.color-sunsetorange { color: #fe4c40 !important; }
.color-bittersweet { color: #fe6f5e !important; }
.color-darkvenetianred { color: #b33b24 !important; }
.color-venetianred { color: #cc553d !important; }
.color-lightvenetianred { color: #e6735c !important; }
.color-vividtangerine { color: #ff9980 !important; }
.color-middlered { color: #e58e73 !important; }
.color-burntorange { color: #ff7f49 !important; }
.color-redorange { color: #ff681f !important; }
.color-orange { color: #ff8833 !important; }
.color-macaroniandcheese { color: #ffb97b !important; }
.color-middleyellowred { color: #ecb176 !important; }
.color-mangotango { color: #e77200 !important; }
.color-yelloworange { color: #ffae42 !important; }
.color-maximumyellowred { color: #f2ba49 !important; }
.color-bananamania { color: #fbe7b2 !important; }
.color-maize { color: #f2c649 !important; }
.color-orangeyellow { color: #f8d568 !important; }
.color-goldenrod { color: #fcd667 !important; }
.color-dandelion { color: #fed85d !important; }
.color-yellow { color: #fbe870 !important; }
.color-greenyellow { color: #f1e788 !important; }
.color-middleyellow { color: #ffeb00 !important; }
.color-olivegreen { color: #b5b35c !important; }
.color-springgreen { color: #ecebbd !important; }
.color-maximumyellow { color: #fafa37 !important; }
.color-canary { color: #ffff99 !important; }
.color-lemonyellow { color: #ffff9f !important; }
.color-maximumgreenyellow { color: #d9e650 !important; }
.color-middlegreenyellow { color: #acbf60 !important; }
.color-inchworm { color: #afe313 !important; }
.color-lightchromegreen { color: #bee64b !important; }
.color-yellowgreen { color: #c5e17a !important; }
.color-maximumgreen { color: #5e8c31 !important; }
.color-asparagus { color: #7ba05b !important; }
.color-grannysmithapple { color: #9de093 !important; }
.color-fern { color: #63b76c !important; }
.color-middlegreen { color: #4d8c57 !important; }
.color-green { color: #3aa655 !important; }
.color-mediumchromegreen { color: #6ca67c !important; }
.color-forestgreen { color: #5fa777 !important; }
.color-seagreen { color: #93dfb8 !important; }
.color-shamrock { color: #33cc99 !important; }
.color-mountainmeadow { color: #1ab385 !important; }
.color-junglegreen { color: #29ab87 !important; }
.color-caribbeangreen { color: #00cc99 !important; }
.color-tropicalrainforest { color: #00755e !important; }
.color-middlebluegreen { color: #8dd9cc !important; }
.color-pinegreen { color: #01786f !important; }
.color-maximumbluegreen { color: #30bfbf !important; }
.color-robinseggblue { color: #00cccc !important; }
.color-tealblue { color: #008080 !important; }
.color-lightblue { color: #8fd8d8 !important; }
.color-aquamarine { color: #95e0e8 !important; }
.color-turquoiseblue { color: #6cdae7 !important; }
.color-outerspace { color: #2d383a !important; }
.color-skyblue { color: #76d7ea !important; }
.color-middleblue { color: #7ed4e6 !important; }
.color-bluegreen { color: #0095b7 !important; }
.color-pacificblue { color: #009dc4 !important; }
.color-cerulean { color: #02a4d3 !important; }
.color-maximumblue { color: #47abcc !important; }
.color-bluei { color: #4997d0 !important; }
.color-ceruleanblue { color: #339acc !important; }
.color-cornflower { color: #93ccea !important; }
.color-greenblue { color: #2887c8 !important; }
.color-midnightblue { color: #00468c !important; }
.color-navyblue { color: #0066cc !important; }
.color-denim { color: #1560bd !important; }
.color-blueiii { color: #0066ff !important; }
.color-cadetblue { color: #a9b2c3 !important; }
.color-periwinkle { color: #c3cde6 !important; }
.color-blueii { color: #4570e6 !important; }
.color-wildblueyonder { color: #7a89b8 !important; }
.color-indigo { color: #4f69c6 !important; }
.color-manatee { color: #8d90a1 !important; }
.color-cobaltblue { color: #8c90c8 !important; }
.color-celestialblue { color: #7070cc !important; }
.color-bluebell { color: #9999cc !important; }
.color-maximumbluepurple { color: #acace6 !important; }
.color-violetblue { color: #766ec8 !important; }
.color-blueviolet { color: #6456b7 !important; }
.color-ultramarineblue { color: #3f26bf !important; }
.color-middlebluepurple { color: #8b72be !important; }
.color-purpleheart { color: #652dc1 !important; }
.color-royalpurple { color: #6b3fa0 !important; }
.color-violetii { color: #8359a3 !important; }
.color-mediumviolet { color: #8f47b3 !important; }
.color-wisteria { color: #c9a0dc !important; }
.color-lavenderi { color: #bf8fcc !important; }
.color-vividviolet { color: #803790 !important; }
.color-maximumpurple { color: #733380 !important; }
.color-purplemountainsmajesty { color: #d6aedd !important; }
.color-fuchsia { color: #c154c1 !important; }
.color-pinkflamingo { color: #fc74fd !important; }
.color-violeti { color: #732e6c !important; }
.color-brilliantrose { color: #e667ce !important; }
.color-orchid { color: #e29cd2 !important; }
.color-plum { color: #8e3179 !important; }
.color-mediumrose { color: #d96cbe !important; }
.color-thistle { color: #ebb0d7 !important; }
.color-mulberry { color: #c8509b !important; }
.color-redviolet { color: #bb3385 !important; }
.color-middlepurple { color: #d982b5 !important; }
.color-maximumredpurple { color: #a63a79 !important; }
.color-jazzberryjam { color: #a50b5e !important; }
.color-eggplant { color: #614051 !important; }
.color-magenta { color: #f653a6 !important; }
.color-cerise { color: #da3287 !important; }
.color-wildstrawberry { color: #ff3399 !important; }
.color-lavenderii { color: #fbaed2 !important; }
.color-cottoncandy { color: #ffb7d5 !important; }
.color-carnationpink { color: #ffa6c9 !important; }
.color-violetred { color: #f7468a !important; }
.color-razzmatazz { color: #e30b5c !important; }
.color-pigpink { color: #fdd7e4 !important; }
.color-carmine { color: #e62e6b !important; }
.color-blush { color: #db5079 !important; }
.color-ticklemepink { color: #fc80a5 !important; }
.color-mauvelous { color: #f091a9 !important; }
.color-salmon { color: #ff91a4 !important; }
.color-middleredpurple { color: #a55353 !important; }
.color-mahogany { color: #ca3435 !important; }
.color-melon { color: #febaad !important; }
.color-pinksherbert { color: #f7a38e !important; }
.color-burntsienna { color: #e97451 !important; }
.color-brown { color: #af593e !important; }
.color-sepia { color: #9e5b40 !important; }
.color-fuzzywuzzy { color: #87421f !important; }
.color-beaver { color: #926f5b !important; }
.color-tumbleweed { color: #dea681 !important; }
.color-rawsienna { color: #d27d46 !important; }
.color-vandykebrown { color: #664228 !important; }
.color-tan { color: #d99a6c !important; }
.color-desertsand { color: #edc9af !important; }
.color-peach { color: #ffcba4 !important; }
.color-burntumber { color: #805533 !important; }
.color-apricot { color: #fdd5b1 !important; }
.color-almond { color: #eed9c4 !important; }
.color-rawumber { color: #665233 !important; }
.color-shadow { color: #837050 !important; }
.color-rawsiennai { color: #e6bc5c !important; }
.color-timberwolf { color: #d9d6cf !important; }
.color-goldi { color: #92926e !important; }
.color-goldii { color: #e6be8a !important; }
.color-silver { color: #c9c0bb !important; }
.color-copper { color: #da8a67 !important; }
.color-antiquebrass { color: #c88a65 !important; }
.color-black { color: #000000 !important; }
.color-charcoalgray { color: #736a62 !important; }
.color-gray { color: #8b8680 !important; }
.color-bluegray { color: #c8c8cd !important; }
.bg-red { background-color: #ed0a3f !important; }
.bg-maroon { background-color: #c32148 !important; }
.bg-scarlet { background-color: #fd0e35 !important; }
.bg-brickred { background-color: #c62d42 !important; }
.bg-englishvermilion { background-color: #cc474b !important; }
.bg-madderlake { background-color: #cc3336 !important; }
.bg-permanentgeraniumlake { background-color: #e12c2c !important; }
.bg-maximumred { background-color: #d92121 !important; }
.bg-indianred { background-color: #b94e48 !important; }
.bg-orangered { background-color: #ff5349 !important; }
.bg-sunsetorange { background-color: #fe4c40 !important; }
.bg-bittersweet { background-color: #fe6f5e !important; }
.bg-darkvenetianred { background-color: #b33b24 !important; }
.bg-venetianred { background-color: #cc553d !important; }
.bg-lightvenetianred { background-color: #e6735c !important; }
.bg-vividtangerine { background-color: #ff9980 !important; }
.bg-middlered { background-color: #e58e73 !important; }
.bg-burntorange { background-color: #ff7f49 !important; }
.bg-redorange { background-color: #ff681f !important; }
.bg-orange { background-color: #ff8833 !important; }
.bg-macaroniandcheese { background-color: #ffb97b !important; }
.bg-middleyellowred { background-color: #ecb176 !important; }
.bg-mangotango { background-color: #e77200 !important; }
.bg-yelloworange { background-color: #ffae42 !important; }
.bg-maximumyellowred { background-color: #f2ba49 !important; }
.bg-bananamania { background-color: #fbe7b2 !important; }
.bg-maize { background-color: #f2c649 !important; }
.bg-orangeyellow { background-color: #f8d568 !important; }
.bg-goldenrod { background-color: #fcd667 !important; }
.bg-dandelion { background-color: #fed85d !important; }
.bg-yellow { background-color: #fbe870 !important; }
.bg-greenyellow { background-color: #f1e788 !important; }
.bg-middleyellow { background-color: #ffeb00 !important; }
.bg-olivegreen { background-color: #b5b35c !important; }
.bg-springgreen { background-color: #ecebbd !important; }
.bg-maximumyellow { background-color: #fafa37 !important; }
.bg-canary { background-color: #ffff99 !important; }
.bg-lemonyellow { background-color: #ffff9f !important; }
.bg-maximumgreenyellow { background-color: #d9e650 !important; }
.bg-middlegreenyellow { background-color: #acbf60 !important; }
.bg-inchworm { background-color: #afe313 !important; }
.bg-lightchromegreen { background-color: #bee64b !important; }
.bg-yellowgreen { background-color: #c5e17a !important; }
.bg-maximumgreen { background-color: #5e8c31 !important; }
.bg-asparagus { background-color: #7ba05b !important; }
.bg-grannysmithapple { background-color: #9de093 !important; }
.bg-fern { background-color: #63b76c !important; }
.bg-middlegreen { background-color: #4d8c57 !important; }
.bg-green { background-color: #3aa655 !important; }
.bg-mediumchromegreen { background-color: #6ca67c !important; }
.bg-forestgreen { background-color: #5fa777 !important; }
.bg-seagreen { background-color: #93dfb8 !important; }
.bg-shamrock { background-color: #33cc99 !important; }
.bg-mountainmeadow { background-color: #1ab385 !important; }
.bg-junglegreen { background-color: #29ab87 !important; }
.bg-caribbeangreen { background-color: #00cc99 !important; }
.bg-tropicalrainforest { background-color: #00755e !important; }
.bg-middlebluegreen { background-color: #8dd9cc !important; }
.bg-pinegreen { background-color: #01786f !important; }
.bg-maximumbluegreen { background-color: #30bfbf !important; }
.bg-robinseggblue { background-color: #00cccc !important; }
.bg-tealblue { background-color: #008080 !important; }
.bg-lightblue { background-color: #8fd8d8 !important; }
.bg-aquamarine { background-color: #95e0e8 !important; }
.bg-turquoiseblue { background-color: #6cdae7 !important; }
.bg-outerspace { background-color: #2d383a !important; }
.bg-skyblue { background-color: #76d7ea !important; }
.bg-middleblue { background-color: #7ed4e6 !important; }
.bg-bluegreen { background-color: #0095b7 !important; }
.bg-pacificblue { background-color: #009dc4 !important; }
.bg-cerulean { background-color: #02a4d3 !important; }
.bg-maximumblue { background-color: #47abcc !important; }
.bg-bluei { background-color: #4997d0 !important; }
.bg-ceruleanblue { background-color: #339acc !important; }
.bg-cornflower { background-color: #93ccea !important; }
.bg-greenblue { background-color: #2887c8 !important; }
.bg-midnightblue { background-color: #00468c !important; }
.bg-navyblue { background-color: #0066cc !important; }
.bg-denim { background-color: #1560bd !important; }
.bg-blueiii { background-color: #0066ff !important; }
.bg-cadetblue { background-color: #a9b2c3 !important; }
.bg-periwinkle { background-color: #c3cde6 !important; }
.bg-blueii { background-color: #4570e6 !important; }
.bg-wildblueyonder { background-color: #7a89b8 !important; }
.bg-indigo { background-color: #4f69c6 !important; }
.bg-manatee { background-color: #8d90a1 !important; }
.bg-cobaltblue { background-color: #8c90c8 !important; }
.bg-celestialblue { background-color: #7070cc !important; }
.bg-bluebell { background-color: #9999cc !important; }
.bg-maximumbluepurple { background-color: #acace6 !important; }
.bg-violetblue { background-color: #766ec8 !important; }
.bg-blueviolet { background-color: #6456b7 !important; }
.bg-ultramarineblue { background-color: #3f26bf !important; }
.bg-middlebluepurple { background-color: #8b72be !important; }
.bg-purpleheart { background-color: #652dc1 !important; }
.bg-royalpurple { background-color: #6b3fa0 !important; }
.bg-violetii { background-color: #8359a3 !important; }
.bg-mediumviolet { background-color: #8f47b3 !important; }
.bg-wisteria { background-color: #c9a0dc !important; }
.bg-lavenderi { background-color: #bf8fcc !important; }
.bg-vividviolet { background-color: #803790 !important; }
.bg-maximumpurple { background-color: #733380 !important; }
.bg-purplemountainsmajesty { background-color: #d6aedd !important; }
.bg-fuchsia { background-color: #c154c1 !important; }
.bg-pinkflamingo { background-color: #fc74fd !important; }
.bg-violeti { background-color: #732e6c !important; }
.bg-brilliantrose { background-color: #e667ce !important; }
.bg-orchid { background-color: #e29cd2 !important; }
.bg-plum { background-color: #8e3179 !important; }
.bg-mediumrose { background-color: #d96cbe !important; }
.bg-thistle { background-color: #ebb0d7 !important; }
.bg-mulberry { background-color: #c8509b !important; }
.bg-redviolet { background-color: #bb3385 !important; }
.bg-middlepurple { background-color: #d982b5 !important; }
.bg-maximumredpurple { background-color: #a63a79 !important; }
.bg-jazzberryjam { background-color: #a50b5e !important; }
.bg-eggplant { background-color: #614051 !important; }
.bg-magenta { background-color: #f653a6 !important; }
.bg-cerise { background-color: #da3287 !important; }
.bg-wildstrawberry { background-color: #ff3399 !important; }
.bg-lavenderii { background-color: #fbaed2 !important; }
.bg-cottoncandy { background-color: #ffb7d5 !important; }
.bg-carnationpink { background-color: #ffa6c9 !important; }
.bg-violetred { background-color: #f7468a !important; }
.bg-razzmatazz { background-color: #e30b5c !important; }
.bg-pigpink { background-color: #fdd7e4 !important; }
.bg-carmine { background-color: #e62e6b !important; }
.bg-blush { background-color: #db5079 !important; }
.bg-ticklemepink { background-color: #fc80a5 !important; }
.bg-mauvelous { background-color: #f091a9 !important; }
.bg-salmon { background-color: #ff91a4 !important; }
.bg-middleredpurple { background-color: #a55353 !important; }
.bg-mahogany { background-color: #ca3435 !important; }
.bg-melon { background-color: #febaad !important; }
.bg-pinksherbert { background-color: #f7a38e !important; }
.bg-burntsienna { background-color: #e97451 !important; }
.bg-brown { background-color: #af593e !important; }
.bg-sepia { background-color: #9e5b40 !important; }
.bg-fuzzywuzzy { background-color: #87421f !important; }
.bg-beaver { background-color: #926f5b !important; }
.bg-tumbleweed { background-color: #dea681 !important; }
.bg-rawsienna { background-color: #d27d46 !important; }
.bg-vandykebrown { background-color: #664228 !important; }
.bg-tan { background-color: #d99a6c !important; }
.bg-desertsand { background-color: #edc9af !important; }
.bg-peach { background-color: #ffcba4 !important; }
.bg-burntumber { background-color: #805533 !important; }
.bg-apricot { background-color: #fdd5b1 !important; }
.bg-almond { background-color: #eed9c4 !important; }
.bg-rawumber { background-color: #665233 !important; }
.bg-shadow { background-color: #837050 !important; }
.bg-rawsiennai { background-color: #e6bc5c !important; }
.bg-timberwolf { background-color: #d9d6cf !important; }
.bg-goldi { background-color: #92926e !important; }
.bg-goldii { background-color: #e6be8a !important; }
.bg-silver { background-color: #c9c0bb !important; }
.bg-copper { background-color: #da8a67 !important; }
.bg-antiquebrass { background-color: #c88a65 !important; }
.bg-black { background-color: #000000 !important; }
.bg-charcoalgray { background-color: #736a62 !important; }
.bg-gray { background-color: #8b8680 !important; }
.bg-bluegray { background-color: #c8c8cd !important; }
</style>
</div>
<div class="swatch_group">
  <h2 class="swatch_group__title">fluorescent</h2>
<div class="swatch color-radicalred">
  <span class="swatch__name">radicalred</span>
  <span class="swatch__color" data-color="#ff355e"></span>
  <span class="swatch__bgcolor" data-color-name="radicalred"></span>
</div>
<div class="swatch color-wildwatermelon">
  <span class="swatch__name">wildwatermelon</span>
  <span class="swatch__color" data-color="#fd5b78"></span>
  <span class="swatch__bgcolor" data-color-name="wildwatermelon"></span>
</div>
<div class="swatch color-outrageousorange">
  <span class="swatch__name">outrageousorange</span>
  <span class="swatch__color" data-color="#ff6037"></span>
  <span class="swatch__bgcolor" data-color-name="outrageousorange"></span>
</div>
<div class="swatch color-atomictangerine">
  <span class="swatch__name">atomictangerine</span>
  <span class="swatch__color" data-color="#ff9966"></span>
  <span class="swatch__bgcolor" data-color-name="atomictangerine"></span>
</div>
<div class="swatch color-neoncarrot">
  <span class="swatch__name">neoncarrot</span>
  <span class="swatch__color" data-color="#ff9933"></span>
  <span class="swatch__bgcolor" data-color-name="neoncarrot"></span>
</div>
<div class="swatch color-sunglow">
  <span class="swatch__name">sunglow</span>
  <span class="swatch__color" data-color="#ffcc33"></span>
  <span class="swatch__bgcolor" data-color-name="sunglow"></span>
</div>
<div class="swatch color-laserlemon">
  <span class="swatch__name">laserlemon</span>
  <span class="swatch__color" data-color="#ffff66"></span>
  <span class="swatch__bgcolor" data-color-name="laserlemon"></span>
</div>
<div class="swatch color-unmellowyellow">
  <span class="swatch__name">unmellowyellow</span>
  <span class="swatch__color" data-color="#ffff66"></span>
  <span class="swatch__bgcolor" data-color-name="unmellowyellow"></span>
</div>
<div class="swatch color-electriclime">
  <span class="swatch__name">electriclime</span>
  <span class="swatch__color" data-color="#ccff00"></span>
  <span class="swatch__bgcolor" data-color-name="electriclime"></span>
</div>
<div class="swatch color-screamingreen">
  <span class="swatch__name">screamingreen</span>
  <span class="swatch__color" data-color="#66ff66"></span>
  <span class="swatch__bgcolor" data-color-name="screamingreen"></span>
</div>
<div class="swatch color-magicmint">
  <span class="swatch__name">magicmint</span>
  <span class="swatch__color" data-color="#aaf0d1"></span>
  <span class="swatch__bgcolor" data-color-name="magicmint"></span>
</div>
<div class="swatch color-blizzardblue">
  <span class="swatch__name">blizzardblue</span>
  <span class="swatch__color" data-color="#50bfe6"></span>
  <span class="swatch__bgcolor" data-color-name="blizzardblue"></span>
</div>
<div class="swatch color-shockingpink">
  <span class="swatch__name">shockingpink</span>
  <span class="swatch__color" data-color="#ff6eff"></span>
  <span class="swatch__bgcolor" data-color-name="shockingpink"></span>
</div>
<div class="swatch color-razzledazzlerose">
  <span class="swatch__name">razzledazzlerose</span>
  <span class="swatch__color" data-color="#ee34d2"></span>
  <span class="swatch__bgcolor" data-color-name="razzledazzlerose"></span>
</div>
<div class="swatch color-hotmagenta">
  <span class="swatch__name">hotmagenta</span>
  <span class="swatch__color" data-color="#ff00cc"></span>
  <span class="swatch__bgcolor" data-color-name="hotmagenta"></span>
</div>
<div class="swatch color-purplepizzazz">
  <span class="swatch__name">purplepizzazz</span>
  <span class="swatch__color" data-color="#ff00cc"></span>
  <span class="swatch__bgcolor" data-color-name="purplepizzazz"></span>
</div>
<style>
.color-radicalred { color: #ff355e !important; }
.color-wildwatermelon { color: #fd5b78 !important; }
.color-outrageousorange { color: #ff6037 !important; }
.color-atomictangerine { color: #ff9966 !important; }
.color-neoncarrot { color: #ff9933 !important; }
.color-sunglow { color: #ffcc33 !important; }
.color-laserlemon { color: #ffff66 !important; }
.color-unmellowyellow { color: #ffff66 !important; }
.color-electriclime { color: #ccff00 !important; }
.color-screamingreen { color: #66ff66 !important; }
.color-magicmint { color: #aaf0d1 !important; }
.color-blizzardblue { color: #50bfe6 !important; }
.color-shockingpink { color: #ff6eff !important; }
.color-razzledazzlerose { color: #ee34d2 !important; }
.color-hotmagenta { color: #ff00cc !important; }
.color-purplepizzazz { color: #ff00cc !important; }
.bg-radicalred { background-color: #ff355e !important; }
.bg-wildwatermelon { background-color: #fd5b78 !important; }
.bg-outrageousorange { background-color: #ff6037 !important; }
.bg-atomictangerine { background-color: #ff9966 !important; }
.bg-neoncarrot { background-color: #ff9933 !important; }
.bg-sunglow { background-color: #ffcc33 !important; }
.bg-laserlemon { background-color: #ffff66 !important; }
.bg-unmellowyellow { background-color: #ffff66 !important; }
.bg-electriclime { background-color: #ccff00 !important; }
.bg-screamingreen { background-color: #66ff66 !important; }
.bg-magicmint { background-color: #aaf0d1 !important; }
.bg-blizzardblue { background-color: #50bfe6 !important; }
.bg-shockingpink { background-color: #ff6eff !important; }
.bg-razzledazzlerose { background-color: #ee34d2 !important; }
.bg-hotmagenta { background-color: #ff00cc !important; }
.bg-purplepizzazz { background-color: #ff00cc !important; }
</style>
</div>
<div class="swatch_group">
  <h2 class="swatch_group__title">bright</h2>
<div class="swatch color-sizzlingred">
  <span class="swatch__name">sizzlingred</span>
  <span class="swatch__color" data-color="#ff3855"></span>
  <span class="swatch__bgcolor" data-color-name="sizzlingred"></span>
</div>
<div class="swatch color-redsalsa">
  <span class="swatch__name">redsalsa</span>
  <span class="swatch__color" data-color="#fd3a4a"></span>
  <span class="swatch__bgcolor" data-color-name="redsalsa"></span>
</div>
<div class="swatch color-tartorange">
  <span class="swatch__name">tartorange</span>
  <span class="swatch__color" data-color="#fb4d46"></span>
  <span class="swatch__bgcolor" data-color-name="tartorange"></span>
</div>
<div class="swatch color-orangesoda">
  <span class="swatch__name">orangesoda</span>
  <span class="swatch__color" data-color="#fa5b3d"></span>
  <span class="swatch__bgcolor" data-color-name="orangesoda"></span>
</div>
<div class="swatch color-brightyellow">
  <span class="swatch__name">brightyellow</span>
  <span class="swatch__color" data-color="#ffaa1d"></span>
  <span class="swatch__bgcolor" data-color-name="brightyellow"></span>
</div>
<div class="swatch color-yellowsunshine">
  <span class="swatch__name">yellowsunshine</span>
  <span class="swatch__color" data-color="#fff700"></span>
  <span class="swatch__bgcolor" data-color-name="yellowsunshine"></span>
</div>
<div class="swatch color-slimygreen">
  <span class="swatch__name">slimygreen</span>
  <span class="swatch__color" data-color="#299617"></span>
  <span class="swatch__bgcolor" data-color-name="slimygreen"></span>
</div>
<div class="swatch color-greenlizard">
  <span class="swatch__name">greenlizard</span>
  <span class="swatch__color" data-color="#a7f432"></span>
  <span class="swatch__bgcolor" data-color-name="greenlizard"></span>
</div>
<div class="swatch color-denimblue">
  <span class="swatch__name">denimblue</span>
  <span class="swatch__color" data-color="#2243b6"></span>
  <span class="swatch__bgcolor" data-color-name="denimblue"></span>
</div>
<div class="swatch color-bluejeans">
  <span class="swatch__name">bluejeans</span>
  <span class="swatch__color" data-color="#5dadec"></span>
  <span class="swatch__bgcolor" data-color-name="bluejeans"></span>
</div>
<div class="swatch color-plumppurple">
  <span class="swatch__name">plumppurple</span>
  <span class="swatch__color" data-color="#5946b2"></span>
  <span class="swatch__bgcolor" data-color-name="plumppurple"></span>
</div>
<div class="swatch color-purpleplum">
  <span class="swatch__name">purpleplum</span>
  <span class="swatch__color" data-color="#9c51b6"></span>
  <span class="swatch__bgcolor" data-color-name="purpleplum"></span>
</div>
<div class="swatch color-sweetbrown">
  <span class="swatch__name">sweetbrown</span>
  <span class="swatch__color" data-color="#a83731"></span>
  <span class="swatch__bgcolor" data-color-name="sweetbrown"></span>
</div>
<div class="swatch color-brownsugar">
  <span class="swatch__name">brownsugar</span>
  <span class="swatch__color" data-color="#af6e4d"></span>
  <span class="swatch__bgcolor" data-color-name="brownsugar"></span>
</div>
<div class="swatch color-eerieblack">
  <span class="swatch__name">eerieblack</span>
  <span class="swatch__color" data-color="#1b1b1b"></span>
  <span class="swatch__bgcolor" data-color-name="eerieblack"></span>
</div>
<div class="swatch color-blackshadows">
  <span class="swatch__name">blackshadows</span>
  <span class="swatch__color" data-color="#bfafb2"></span>
  <span class="swatch__bgcolor" data-color-name="blackshadows"></span>
</div>
<div class="swatch color-fieryrose">
  <span class="swatch__name">fieryrose</span>
  <span class="swatch__color" data-color="#ff5470"></span>
  <span class="swatch__bgcolor" data-color-name="fieryrose"></span>
</div>
<div class="swatch color-sizzlingsunrise">
  <span class="swatch__name">sizzlingsunrise</span>
  <span class="swatch__color" data-color="#ffdb00"></span>
  <span class="swatch__bgcolor" data-color-name="sizzlingsunrise"></span>
</div>
<div class="swatch color-heatwave">
  <span class="swatch__name">heatwave</span>
  <span class="swatch__color" data-color="#ff7a00"></span>
  <span class="swatch__bgcolor" data-color-name="heatwave"></span>
</div>
<div class="swatch color-lemonglacier">
  <span class="swatch__name">lemonglacier</span>
  <span class="swatch__color" data-color="#fdff00"></span>
  <span class="swatch__bgcolor" data-color-name="lemonglacier"></span>
</div>
<div class="swatch color-springfrost">
  <span class="swatch__name">springfrost</span>
  <span class="swatch__color" data-color="#87ff2a"></span>
  <span class="swatch__bgcolor" data-color-name="springfrost"></span>
</div>
<div class="swatch color-absolutezero">
  <span class="swatch__name">absolutezero</span>
  <span class="swatch__color" data-color="#0048ba"></span>
  <span class="swatch__bgcolor" data-color-name="absolutezero"></span>
</div>
<div class="swatch color-wintersky">
  <span class="swatch__name">wintersky</span>
  <span class="swatch__color" data-color="#ff007c"></span>
  <span class="swatch__bgcolor" data-color-name="wintersky"></span>
</div>
<div class="swatch color-frostbite">
  <span class="swatch__name">frostbite</span>
  <span class="swatch__color" data-color="#e936a7"></span>
  <span class="swatch__bgcolor" data-color-name="frostbite"></span>
</div>
<style>
.color-sizzlingred { color: #ff3855 !important; }
.color-redsalsa { color: #fd3a4a !important; }
.color-tartorange { color: #fb4d46 !important; }
.color-orangesoda { color: #fa5b3d !important; }
.color-brightyellow { color: #ffaa1d !important; }
.color-yellowsunshine { color: #fff700 !important; }
.color-slimygreen { color: #299617 !important; }
.color-greenlizard { color: #a7f432 !important; }
.color-denimblue { color: #2243b6 !important; }
.color-bluejeans { color: #5dadec !important; }
.color-plumppurple { color: #5946b2 !important; }
.color-purpleplum { color: #9c51b6 !important; }
.color-sweetbrown { color: #a83731 !important; }
.color-brownsugar { color: #af6e4d !important; }
.color-eerieblack { color: #1b1b1b !important; }
.color-blackshadows { color: #bfafb2 !important; }
.color-fieryrose { color: #ff5470 !important; }
.color-sizzlingsunrise { color: #ffdb00 !important; }
.color-heatwave { color: #ff7a00 !important; }
.color-lemonglacier { color: #fdff00 !important; }
.color-springfrost { color: #87ff2a !important; }
.color-absolutezero { color: #0048ba !important; }
.color-wintersky { color: #ff007c !important; }
.color-frostbite { color: #e936a7 !important; }
.bg-sizzlingred { background-color: #ff3855 !important; }
.bg-redsalsa { background-color: #fd3a4a !important; }
.bg-tartorange { background-color: #fb4d46 !important; }
.bg-orangesoda { background-color: #fa5b3d !important; }
.bg-brightyellow { background-color: #ffaa1d !important; }
.bg-yellowsunshine { background-color: #fff700 !important; }
.bg-slimygreen { background-color: #299617 !important; }
.bg-greenlizard { background-color: #a7f432 !important; }
.bg-denimblue { background-color: #2243b6 !important; }
.bg-bluejeans { background-color: #5dadec !important; }
.bg-plumppurple { background-color: #5946b2 !important; }
.bg-purpleplum { background-color: #9c51b6 !important; }
.bg-sweetbrown { background-color: #a83731 !important; }
.bg-brownsugar { background-color: #af6e4d !important; }
.bg-eerieblack { background-color: #1b1b1b !important; }
.bg-blackshadows { background-color: #bfafb2 !important; }
.bg-fieryrose { background-color: #ff5470 !important; }
.bg-sizzlingsunrise { background-color: #ffdb00 !important; }
.bg-heatwave { background-color: #ff7a00 !important; }
.bg-lemonglacier { background-color: #fdff00 !important; }
.bg-springfrost { background-color: #87ff2a !important; }
.bg-absolutezero { background-color: #0048ba !important; }
.bg-wintersky { background-color: #ff007c !important; }
.bg-frostbite { background-color: #e936a7 !important; }
</style>
</div>
<style>
.swatch_group {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  max-width: 100%;
}
.swatch_group__title {
  padding: .9em 0;
  text-transform: capitalize;
  font-family: sans-serif;
  border-bottom: 1px dashed;
  margin-bottom: 1em;
}
.swatch_group .swatch {
  position: relative;
  height: auto;
  margin: 0;
  padding: 0;
}
.swatch {
  display: flex;
  max-width: 100%;
}
.swatch__name { flex: 1 1 15%; }
.swatch__color { flex: 0 1 15%; }
.swatch__bgcolor { flex: 1 1 50%; }
.swatch {
  font-size: 1em;
  font-weight: 400;
  border-bottom: 1px solid;
  font-family: monospace;
  text-align: center;
  border-left: 2em solid;
}
.swatch__name {
  font-size: 1em;
  margin: 0;
  color: #000;
  white-space: nowrap;
  padding-left: .5em;
  text-align: left;
}
.swatch__color {
  display: flex;
  color: inherit;
  padding: 0;
  margin: 0;
  border: 0;
  font-size: 1em;
  text-align: center;
  justify-content: space-around;
}
.swatch__color:after, .swatch__color:before {
  content: attr(data-color);
  color: inherit;
  border-left: 1em solid;
  display: inline-block;
  flex: 1;
}
.swatch__color:before { background-color: #000; }
.swatch__color:after { background-color: #fff; }
.swatch__bgcolor {
  background-color: currentColor;
  margin: 0;
}
.swatch__bgcolor:after, .swatch__bgcolor:before {
  content: attr(data-color-name);
  display: inline;
  text-transform: uppercase;
  font-family: monospace;
  padding: 0 1em;
}
.swatch__bgcolor:before { color: #fff; }
.swatch__bgcolor:after { color: #000; }
.styleguide_section .container {
  display: block;
  padding: 1em 2em;
  margin: 1em 0;
  border: 1px solid;
  border-color: #ccc #ccc #84cc4e;
  background: #fff;
}
.styleguide_section .container__name { display: block; }
.styleguide_section .container__content {
  display: inline-block;
  margin: 1em 0;
  border: 1px dotted #ccc;
  padding: 1em;
  background: #fff;
}
.styleguide_section .item__label {
  white-space: nowrap;
  background: #fff;
  padding: 3px;
}
body, html {
  overflow-x: hidden;
  padding: 0;
  margin: 0;
  font-size: 16px;
}
.debug_outline_structure > * { outline: 1px solid #123; }
.wireframe_guides * { outline: 1px dashed #c28181; }
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #1bbcff;
  background-color: #efefef;
  border-radius: 3px;
}
pre {
  display: block;
  padding: 0 1em;
  margin: 1em 0;
  font-size: 1em;
  line-height: 1.5;
  color: #919191;
  background-color: #ececec;
  border: 1px solid #d5d5d5;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
</style>
