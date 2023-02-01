

## 7 Steps to Build a Website


### Define the Project

- WHO
	- client , business ?
- WHAT
	- user goals && business goals
- AUDIENCE
	- deifne target audience




### Plan the Project

- plan and gather web content
	- copy(text), images, videos
- contents are provided by client
	- charge the content if necessary
- sitemap
	- what pages the site needs
	- how they relate to one another
- sections of each page
- define web personality




### Sketch Layout and Component Ideas

- web components
	- layout patterns
- draw a draft
- iterative process
- don't make it perfect





### Design and Build Website

- build web with `HTML` and `CSS`
- design actual visual styles 
- design is based on web personality and design guidlines and inspiiration
- use client's branding: 
	- colors, typography, icons ...





### Test and Optimize

- make sure web works well in all major websites
- on autual mobile devices
- optimize all images
	- dimentions and size
	- compression
- accesibility problems
	- color contrast issues
- run the lighthouse performance test in Chrome DevTools and try to fix repotyed issues
- SEARCH ENGINE OPTIMIZATION (SEO)





### Launch the Masterpiece

- upload web files to a hosting platform
	- `Netlify`
- Choose and buy a great domain name



### Maintain and Keep Updating Website

- update over time
- analytics software
	- may inform future changes
- keep a blog
	- a good way to keep userss coming back
	- good for SEO


----
## Define the Project

* WHO
	* for a client
* WHAT
	- business goal : selling monthly food subscription
	- user goal : eating well effortlessly, without spending a lot of time and money
- AUNDIENCE
	- like tech
	- healthy diet
	- well-paying job


----
## Plan the Project

- plan and gather web content
	- defined
- site map
	- one-page marketing website (landing page)
- define web personality
	- startup / upbeat
	- calm / peaceful
- sections of each page
	- Logo + Navigation
	- Hero
	- Featured in
	- How it works
	- Meals (and list of diets)
	- Testimonials + Gallary
	- Pricing + features
	- Call to action
	- Footer




----
## First Ideas and Sketch

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301252330203.png)


- settings in the very beginning
```css
/*
--- 01 TYPOGRAPY SYSTEM
- Font sizes (px)
10 / 12 / 14 / 16 / 18 / 20 / 24 / 30 / 36 / 44 / 52 / 62 / 74 / 86 / 98

- Font weights:
Default: 400

- Line heights:
Default: 1


--- 02 COLORS
- Primary: #e67e22
- Tints:
- Shades:
- Accents:
- Greys:
#555

--- 05 SHADOWS

--- 06 BORDER-RADIUS

--- 07 WHITESPACE
- Spacing system (px)
2 / 4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 80 / 96 / 128

*/
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
  line-height: 1;
  font-weight: 400;
  color: #555;
}
```

----

## (Basics) Responsive Design Theory

- adjust its layout and visaul style to any possible screen size
- usable on desktop computers, tablets, and mobile phones


### Fluid Layouts

- allow webpage to adapt to the current **viewpoint** width (or even height)
-  Use `%` (or `vh` / `vw`) unit instead of `px` for elements that **should adapt to viewport (usually layout)**
- Use `max-width` instead of `width`




### Responsive Units

- Use `rem` unit instead of `px` for most lengths
- To make it easy to **scale the entire layout down(or up) automatically**
- Helpful trick
	- setting `1rem` to `10px` for easy calculations





### Flexible Images

- By default, **images don't scale automatically** as1we change the viewport, so we need to fix that
- Always use `%` for image dimensions, together with the `max-width` property




### Media Queries

- Bring responsive sites to life!
- To change CSS styles on **certain viewportwidths** (called breakpoints)




### Desktop-first vs. Mobile-first

- start writing for desktop / mobile device
- shrink / expand design

>mobile-first forces up to reduce websites and apps to the absolute essentials


----
## (Basics) Responsive Design Implement



### max-width

`max-width: XX px`
- if the view width is larger than the `XX` then 
	- the width of the component is `max-width`
- else 
	- the width of the component is `100%` view width




### rem unit

- `1 rem` default : `16px`

```css
html {
	font-size: 10px;
}

.text {
	font-size: 2rem;    /*2rem here -> 20px*/
}
```

>propose a problem of usablility : not fixed value for `font-size`


```css
html {
	/* 16 * 62.5%  = 10 */
	font-size: 62.5%;    /*Percentage of user's browser font-size setting*/
}
```


----
## Hero section


- button 
	- not related to nav
- links
	- nav


### fit the size of image

- scale image to full size in box
```html
<div class="hero">
<!-- hero : CSS GRID CONTAINER -->
	<div class="hero-text-box">
	  <h1 class="heading-primary">
		Headline: A healthy meal delivered to your door, every single day
	  </h1>
	  <p class="hero-description">
		The smart 365-days-per-year food subscription that will make you 
		eat healthy again. Tailored to your personal tastes and nutritional
		needs. We have delivered 250,000+ meals last year!
	  </p>
	  
	  <a href="#" class="btn">Start eating well</a>
	  <a href="#" class="btn">Learn more &downarrow;</a>
	</div>
	
	<div class="hero-img-box">
	  <img
		src="img/hero.png"
		class="hero-img"
		alt="Woman enjoying food, meals in storage container and foof bowls ina table"
	  />
	</div>
</div>
```

>text 50%, image 50%
```css
.hero {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.hero-img {
  width: 100%;
}
```




### centering the content

- use `max-width` and  `margin: 0 auto;` to center it 
```html
<section class="section-hero">
	<div class="hero">
		content
	</div>
</section>
```


```css
html {
  /* 10px */
  font-size: 62.5%;
}

.hero {
  max-width: 130rem;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
}
```
>`max-width` and centering !



### Why content wrapped in a div

>notice : wrap a `<div>` in the box to set a FIXED `max-width` for the content
```html
<section class="section-hero">
	<div class="hero">
		content
	</div>
</section>
```

```css
.hero {
  max-width: 130rem;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
}
```



- another reason why we have to use `<div class="hero"></div>`
	- `background-color`

```html
<section class="section-hero">
	<div class="hero">
		content
	</div>
</section>
```

>background-color added to `hero` in big screen
```css
.hero {
	  background-color: #fdf2e9;
}
```

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301272104777.png)

>background-color added to `section-hero`
```css
.section-hero {
	background-color: #fdf2e9;
}
```

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/20230127210546.png)








### get Tints and Shades

- Make Tints and Shades
	- [Tints and Shades Maker]([Tint and Shade Generator (maketintsandshades.com)](https://maketintsandshades.com/))
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301272058139.png)





### modifier class

- modifier class
```html
<a href="#" class="btn btn--full">Start eating well</a>
<a href="#" class="btn btn--outline">Learn more &downarrow;</a>
```
>`class--special`
```css
.btn--full:link,
.btn--full:visited {
  background-color: #e67e22;
}


.btn--outline:link,
.btn--outline:visited {
  background-color: #fff;
  color: #555;
}
```




### create inset border

- add border inside the button
	- why ? 
		- add `border`in the `btn:hover` will lead to additional vertical height 
	- how ?
		- use `box-shadow: inset`

```css
.btn--outline:hover,
.btn--outline:active {
  background-color: #fdf2e9;
  
  /*ADD BORDER INSIDE*/
  box-shadow: inset 0 0 0 3px #fff;
}
```





### simple animation

- simple animation
```css
.btn:link,
.btn:visited {
	transition: background-color 0.3s;    /*which property, time*/
}

```
>put the `transition` in the original state !!!!






### reusable helper class

- helper class
- give the element right margin
```css
.margin-right-sm {
  margin-right: 1.6rem !important;
}
```
>`!important` added to make sure no mater where the helper class is added, the `margin-right` is always applied






### Potraits Overlaping Style
- component
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301272325454.png)


```html
<div class="delivered-meals">
	<div class="delivered-imgs">
		  <img src="img/customers/customer-1.jpg" alt="customer photo" />
		  <img src="img/customers/customer-2.jpg" alt="customer photo" />
		  <img src="img/customers/customer-3.jpg" alt="customer photo" />
		  <img src="img/customers/customer-4.jpg" alt="customer photo" />
		  <img src="img/customers/customer-5.jpg" alt="customer photo" />
		  <img src="img/customers/customer-6.jpg" alt="customer photo" />
	</div>
	<p class="delivered-text">250,000+ meals delivered last year!</p>
</div>
```

```css
.delivered-meals {
  display: flex;
  align-items: center;
  gap: 1.6rem;
  margin-top: 8rem;
}

.delivered-imgs {
  display: flex;
}

.delivered-imgs img {
  height: 4.8rem;
  width: 4.8rem;
  border-radius: 50%;                   /*round*/
  margin-right: -1.6rem;                /*Overlaping*/
  border: 3px solid #fdf2e9;            /*Border*/
}

.delivered-imgs img:last-child {
  margin: 0;
}

.delivered-text {
  font-size: 1.8rem;
  font-weight: 600;
}
```



----

## Header

### Style text in paragraph

- change color of certain text

```html
<p class="delivered-text">
	  <span>250,000+</span> meals delivered last year!
</p>
```

```css
.delivered-text span {
	  color: #e67e22;
	  font-weight: 700;
}
```




### Standard HTML Division

- `<main>`, `<header>`, `<footer>`
- more clear and better for the browser
```html
<body>
	<header>
		HEADER
	</header>

	<main>
		MAIN
	</main>

	<footer>
		FOOTER
	</footer>
</body>
```
>`<header>` and `<footer>` could be in any page which shoule be separeted from `<main>`





----


## Navagation

### navagation list format
- format
- `<nav> + <ul> + <a>`
```html
<nav>
	<ul>
		<li><a href="#">LINK</a></li>
		<li><a href="#">LINK</a></li>
		<li><a href="#">LINK</a></li>
		<li><a href="#">LINK</a></li>
	</ul>
</nav>
```




## How it works section


### resuable grid

- reusable gird
```css
.grid {
  display: grid;
  gap: 9.6rem;
}

.grid--2-cols {
  grid-template-columns: repeat(2, 1fr);
}

.grid--3-cols {
  grid-template-columns: repeat(3, 1fr);
}
```

>say if you want 2 columns (add to parent element)
```html
<section class="section-how grid grid--2-cols">
        <div>Test1</div>
        <div>Test2</div>
        <div>Test3</div>
        <div>Test4</div>
</section>
```





### reusable centering (with html wraped in div)

- resusable centering
```css
.container {
  /* 1140px */              /*standard*/
  max-width: 120rem;        
  margin: 0 auto;           /*centering*/
  padding: 0 3.2rem;        
}
```
>added in the wrapper

```html
<section class="section-how">
	<div class="section-how container grid grid--2-cols">
		  <div>Test1</div>
		  <div>Test2</div>
		  <div>Test3</div>
		  <div>Test4</div>
	</div>
</section>
```




- add spacing between uppercase letter
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301281320001.png)



- split css code into several files
	- general part should be separated




### making a square

* make squre block : padding-bottom %
	- the first step of making a circle 

```css
.step-img-box::before {
  width: 60%;
  padding-bottom: 60%;
  background-color: #fdf2e9;
  z-index: -2;
}
```
>designate a `width` 
>DO NOT DESIGNATE A height
>use `padding-bottom` instead
>










### z-index overlapping

- use `z-index` property to specify overlapping relation between elements
	- bigger: on the top

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301281342561.png)

```css
.step-img-box::before {
  width: 60%;
  padding-bottom: 60%;
  background-color: #fdf2e9;
  z-index: -2;                      /* z-index */
}

.step-img-box::after {
  width: 45%;
  padding-bottom: 45%;
  background-color: #fae5d3;
  z-index: -1;
}
```




----
## Feature in section

### space-between and space-around

- space between
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301281357985.png)


- space-around
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301281358277.png)





### img property : filter


```css
img {
	filter: grayscale(100%);       /*turn to gray image*/
	filter:blur(5px);              /*blue scale*/
	filter: hue-rotate(45deg);     /*change the color*/
	filter: saturate(0.5);         /*change saturation*/
	filter: brightness(0);         /*change the brightness*/ /*turn to pure black:0*/

	 /*accompanied by opacity*/
}
```



----

## Meal Section

### polish text

- use `650 calories` instead of `Calories: 650`
- use tags for catagory



### icon without adding svg in HTML

- tool : 
	- [Ionicons: Premium Open Source Icon Pack for Ionic Framework](https://ionic.io/ionicons)


- Javascript in `<head>`
```html
<script
	  type="module"
	  src="https://unpkg.com/ionicons@5.4.0/dist/ionicons/ionicons.esm.js"
></script>
<script
	  nomodule
	  src="https://unpkg.com/ionicons@5.4.0/dist/ionicons/ionicons.js"
></script>
```


- injection
```html
<ion-icon name="flame-outline"></ion-icon>
```


- wrap text besides icon
```html
<li class="meal-attribute">
	<ion-icon name="flame-outline"></ion-icon><span>650 Calories</span>
</li>
```



### attempts on changing the color of icon

- `stroke`
- `fill`
- `color`


### deal with cornors of image inside the card


![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301281501002.png)
>set `border-radius` in cards, thus images overflows

```css
.meals {
	overflow: hidden;
}
```

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301281503629.png)



### link decoration

- do not use original underline decoration

```css
.link:link,
.link:visited {
  display: inline-block;
  color: #e67e22;
  text-decoration: none;
  border-bottom: 1px solid currentColor;
  padding-bottom: 2px;
}
```
>use `border-bottom` to simmulate the underline




- lead to `1px` up and down for the web page
- the border has a height
- to fix it : turn the border into `transparent`
```css
.link:hover,
.link:active {
  color: #cf711f;
  border-bottom: 1px solid transparent;
}
```









### currentColor

- get the color in line with text color

```css
.link:link,
.link:visited {
  display: inline-block;
  color: #e67e22;
  text-decoration: none;
  border-bottom: 1px solid currentColor;      /*get text color*/
  padding-bottom: 2px;
}
```
>useful when it come to `:hover`





### floating card when hovering

```css
.meal {
  box-shadow: 0 2.4rem 4.8rem rgba(0, 0, 0, 0.075);
  border-radius: 11px;
  overflow: hidden;
  transition: all 0.4s;                       /* add animation to original state */
}

.meal:hover {
  transform: translateY(-1.2rem);             /* transform to move it */
}
```


- details: shadow become larger when hovering


----
## Testimonial Section


## figure label
- `<figure></figure>`  
```html
<figure class="testimonial">
	<img
	sclass="testimonial-img"
	alt="Photo of customer Dave Bryson"
	src="img/customers/dave.jpg"
	/>
	<blockquote class="testimonial-text">
		Inexpensive, healthy and great-tasting meals, without even having
		to order manually! It feels truly magical.
	</blockquote>
	<p class="testimonial-name">&mdash; Dave Bryson</p>
</figure>
```

>figure caption label
```html
<div class="gallery">
	<figure class="gallary-item">
		<img
		  src="img/gallery/gallery-1.jpg"
		  alt="Photo of beautifully arranged food"
		/>
	<figcaption>Caption</figcaption>
	</figure>
</div>
```



### get rid of white space around img

- img default : `inline-block`
- turn it into : `block`
```css
img {
	display: block;
}
```



### use fr unit as percentage
```css
.section-testimonials {
  background-color: #fdf2e9;
  display: grid;
  grid-template-columns: 55fr 45fr;         /*what matters is the outcome ratio*/
}
```








### hover on img without overflowing

```html
<figure class="gallary-item">
	<img
	  src="img/gallery/gallery-3.jpg"
	  alt="Photo of beautifully arranged food"
	/>
</figure>
```


```css
.gallary-item {
  overflow: hidden;
}

.gallary-item img {
  display: block;
  width: 100%;
  transition: all 0.4s;
}
  
.gallary-item img:hover {
  transform: scale(1.1);
}
```



----
## Pricing & Features

### align the call to action button

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301301455103.png)

>add another point on the left side




### ribbon decoration

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301301523017.png)

```css  
.pricing-plan--complete::after {           /*pseudo element*/
  content: "Best value";
  position: absolute;
  text-transform: uppercase;
  font-size: 1.4rem;
  font-weight: 700;
  top: 6%;
  right: -18%;
  color: #333;
  background-color: #ffd43b;
  padding: 0.8rem 8rem;
  transform: rotate(45deg);                /*rotate the element*/
}
```




### fix the margin when multiple grid in a section

>complex
```css
.grid {
  display: grid;
  column-gap: 6.4rem;
  row-gap: 9.6rem;
  margin-bottom: 0;
}

.grid:last-child {         /*margin of last child is 0*/
  margin-bottom: 0;
}
```


>improved
```css
.grid {
  display: grid;
  column-gap: 6.4rem;
  row-gap: 9.6rem;
}

.grid:not(:last-child) {
  margin-bottom: 9.6rem;
}
```




### gradient

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301301935346.png)


>method1
```css
.cta {
	  background-image: linear-gradient(90deg, red, #e67e22);
}
```
>`image` but not `color`


>method2
```css
.cta {
	  background-image: linear-gradient(to right, red, #e67e22);
}
```


![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301301940817.png)
```css
.cta {
	  background-image: linear-gradient(to right bottom, red, #e67e22);
}
```



### background image size

```css
.cta-img-box {
  background-image: url("../img/eating.jpg");
  background-size: cover;
  background-position: center;
}
```
>`cover` to display complete image



### overlay mask  to fit with back-color

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301301953711.png)

```html
 <div class="cta-img-box"></div>
```

```css
.cta-img-box {
  background-image: linear-gradient(    /*stack*/
      to right bottom,
      rgba(235, 151, 78, 0.35),
      rgba(230, 125, 34, 0.35)
    ),
    url("../img/eating.jpg");
  background-size: cover;
  background-position: center;
}
```




### background image

>(from point in the front)
>NOT ACCESSIBLE TO SCREEN READER

```html
 <div class="cta-img-box"></div>
```

```css
.cta-img-box {
  background-image: linear-gradient(    /*stack*/
      to right bottom,
      rgba(235, 151, 78, 0.35),
      rgba(230, 125, 34, 0.35)
    ),
    url("../img/eating.jpg");
  background-size: cover;
  background-position: center;
}
```

- change the `HTML`
```html
<div
            class="cta-img-box"
            role="img"                           <!-- role as -->
            aria-label="Wonman enjoying food"    <!-- alt  -->
></div>
```




### form

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301302040762.png)


```html
<form class="cta-form" action="#">                  <!--form box-->
	<label>Full Name</label>                        <!--label before input bar-->
	<input type="text" placeholder="John Smith" />  <!--input type & placeholder-->
	<label>Email address</label>
	<input type="email" placeholder="me@example.com" />
	<button class="btn">Sign up now</button>        <!-- click button -->
</form>
```
>different types of input box
>place holder





### ligten the font of place holder
```css
.cta-form input::placeholder {
  color: #aaa;
}
```
>use pseudo element `placeholder`





### click the label to input

```html
<form class="cta-form" action="#">
	<label for="full-name">Full Name</label>
	<input id="full-name" type="text" placeholder="John Smith" />

	<label for="email">Email address</label>
	<input id="email" type="email" placeholder="me@example.com" />
	<button class="btn">Sign up now</button>
</form>
```
>`for` connects with `id`







### select option box

```html
<form class="cta-form" action="#">
	<label for="select-where">Where do you hear from us?</label>
	<select id="select-where">
		  <!--  empty value is not allowed when submitting -->
		  <option value="">Please choose one option:</option>
		  <option value="friends">Friends and family</option>
		  <option value="podcast">Podcast</option>
		  <option value="ad">Facebook ad</option>
		  <option value="others">Others</option>
	</select>
    <button class="btn">Sign up now</button>
</form>
```
>`<select>` & `<option>`
>define the `value` !!!!





### required for the box

```html
<form class="cta-form" action="#">
	<label for="full-name">Full Name</label>
	<input
	  id="full-name"
	  type="text"
	  placeholder="John Smith"
	  required                                  
	/>                                          <!-- required -->

	<label for="email">Email address</label>
	<input
	  id="email"
	  type="email"
	  placeholder="me@example.com"
	  required                                  
	/>                                          <!-- required -->

	<label for="select-where">Where do you hear from us?</label>
	<select id="select-where" required>         <!-- required -->
		  <option value="">Please choose one option:</option>
		  <option value="friends">Friends and family</option>
		  <option value="podcast">Podcast</option>
		  <option value="ad">Facebook ad</option>
		  <option value="others">Others</option>
	</select>
	<button class="btn">Sign up now</button>
</form>
```
>works for `<input>` and `<select>`

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301302135877.png)

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301302136752.png)





### font-family for placeholder

- it will not inherit the font-family  `body`
- as well as the text color

- lighten the `placeholder` and text `color`
```css
.cta-form input,
.cta-form select {
  font-family: inherit;
  color: inherit;
}
```


- use `inherit` to inherit the property of super class







### focus status 

- for users only use keyboard to navagate the page
>by hitting `TAB` on the keyboard

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301302333592.png)


>change the default style

```css
*:focus {
  outline: 4px dotted #e67e22;
  outline-offset: 8px;
}
```

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301310017086.png)




```css
*:focus {
  outline: none;
  box-shadow: 0 0 0 0.8rem rgba(230, 125, 34, 0.5);
}
```

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301310021769.png)




>set special border for certain area
```css
.cta *:focus {
  outline: none;
  box-shadow: 0 0 0 0.8rem rgba(253, 242, 233, 0.5);
}
```

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301310022585.png)


----
## Footer

### make address / phone number  links

```html
<div class="address-col">
  <p class="footer-heading">Contact us</p>
  <address class="contacts">
	<p>623 Harrison St., 2nd Floor, San Francisco, CA 94107</p>
	<p>
	  <a href="tel:415-201-6370">415-201-6370</a> 
	  <br/>
	  <a href="mailto:hello@omnifood.com">hello@omnifood.com</a>
	</p>
  </address>
</div>
```
>`address` for different types
>`a` : link could be phone number and mail address



### change address font-style

```css
.contacts {
  font-style: normal;
}
```


### padding

```css
.cta {
	/* clock circle : top / right / bottom / left*/
	padding: 9.6rem 0 12.8rem 0;

	/*top / horizontal / left*/
	padding: 9.6rem 0 12.8rem;
}
```


----
## Responsive Web design




### Media Queries (with max-width)

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301311343664.png)


- reset the css style
```css
@media (max-width: 1200px) {
  .section-hero {
    background-color: rebeccapurple;
  }
}
```


- the one that defined later would enjoy piority
```css
@media (max-width: 600px) {
  .section-hero {
    background-color: rgb(159, 148, 171);
  }
}

@media (max-width: 1200px) {
  .section-hero {
    background-color: rebeccapurple;      /*applied within the range of 0 - 600px*/
  }
}
```



- test on the browser
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301311353118.png)

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301311353138.png)





### Selecting Breakpoints for responsive design

- find ranges and find interval values -- GOOD
- find ==WHERE THE DESIGN BREAKS DOWN== !!!

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301311358367.png)






### Implementation


>Always include : 
```css
<head>
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
</head>
```


>in media queries, `rem` and `em` DO NOT depend on html font-size 
>`1 rem = 1 em = 16px` in media queries



#### em unit

>`rem` has bugs in media queries in some browsers, we use `em` instead

```css
@media (max-width: 84em) {
  .hero {
    max-width: 120rem;
  }
}
```




#### change the font-size

```css
@media (max-width: 75em) {
  html {
    font-size: 56.25%;         /*since font-size in html is defined in rem*/
  }
}
```





### transform the nav bar to mobile nav bar


- adding nav button
- add two icons and change the visibility

```html
<button class="btn-mobile-nav">
	<ion-icon class="icon-mobile-nav" name="menu-outline"></ion-icon>
	<ion-icon class="icon-mobile-nav" name="close-outline"></ion-icon>
</button>
```


- set visibility using `[]` selector
```css
.btn-mobile-nav {
  border: none;
  background: none;
  cursor: pointer;
  display: none;                /*set default to none and change it in @media()*/ 
}

.icon-mobile-nav {
  height: 4.8rem;
  width: 4.8rem;
  color: #333;
}

/*/select those with name="close-outline"*/
.icon-mobile-nav[name="close-outline"] {           
  display: none;
}
```



#### leave class for JS

```html
<header class="header nav-open">
	<nav class="main-nav">
	</nav>
</header>
```
>`nav-open` is left for JS later

```css
@media (max-width: 49em) {
	.main-nav {
		transition: all 0.3s;
		
		/*step 1 : hide it visually*/
		opacity: 0;
		
		/*step 2 : make it unaccessible to mouse and keyboard (for TAB)*/
		pointer-events: none;

		/*step 3 ：make it unaccessible to  screen reader*/
		visibility: hidden;
	}

	.nav-open .main-nav {
	    opacity: 1;
	    pointer-events: auto;
	    visibility: visible;
	}
}
```



#### the menu icon

```css

.icon-mobile-nav[name="close-outline"] {
  display: none;
}

@media (max-width: 49em) {
	.nav-open .icon-mobile-nav[name="close-outline"] {
	 display: block;
	}
  
	.nav-open .icon-mobile-nav[name="menu-outline"] {
		display: none;
	}
}

```
>only if `.nav-open` exists







#### menu slide from right side

- place menu to the right side (outside) of web page
```css

html {
	overflow-x: hidden;
}

body {
	/*only works of there is nothing absolutely positioned in relation to body*/
	overflow-x: hidden;
}

@media(max-width: 49em) {
	.main-nav {
	transform: translateX(100%);
	}
}

```
>notice that `overflow-x: hidden;` should be set in the `body` ==AND== `html` part







#### build asymetic gird 

- find `lcm` for the number of elements in each row
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301311921448.png)


```css
  .pricing-plan {
	    width: 100%;
  }

  .grid--footer {
	    grid-template-columns: repeat(6, 1fr);
  }


  .logo-col,
  .address-col {
	    grid-column: span 3;
  }


  .nav-col {
	    grid-row: 1;
	    grid-column: span 2;    /*1 element span 2*/
	    margin-bottom: 3.2rem;
  }
```




![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301311936580.png)



- move to the first row
```css
.step-img-box:nth-child(2) {
	grid-row: 1;
}
```













----

## A little bit Javascript


### connection with css

```css
<head>
	<script defer src="js/script.js"></script>
</head>
```





### console print

```js
console.log("Hello World!");
const myName = "Ming ttt";
console.log(myName);
```



### select class from js

```js
const h1 = document.querySelector(".heading-primary");
console.log(h1);
```



### respond to event

```js
h1.addEventListener("click", function () {
  h1.textContent = myName;
  h1.style.backgroundColor = "red";
  h1.style.padding = "5rem";
});
```



### update copyright year


```html
Copyright &copy; <span class="year">2027</span> by Omnifood, Inc.
```

```js
// get current year
const yearEl = document.querySelector(".year");
const currentYear = new Date().getFullYear();
yearEl.textContent = currentYear;
```





### make mobile nav work

```js
// Make mobile nav work
const btnNavEl = document.querySelector(".btn-mobile-nav");
const headerEl = document.querySelector(".header");

btnNavEl.addEventListener("click", function () {
	 headerEl.classList.toggle("nav-open");    // toggle for add and delete
});
```




----
## Smooth Scrolling

- in-page anchor
```html
<a href="#cta" class="btn btn--full margin-right-sm">Start eating well</a>

<section class="section-cta" id="cta"></section>
```
>unique `id` for anchor link


- scroll behavior : smooth
```css
html {
	scroll-behavior: smooth;
}
```
>not work for `Safari`



>using `js`
```js
// smoth scrolling
const allLinks = document.querySelectorAll("a:link");

allLinks.forEach(function (link) {
  link.addEventListener("click", function (e) {
    e.preventDefault();
    const href = link.getAttribute("href");
    
    //scroll back to top
    if (href === "#")
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });

    if (href !== "#" && href.startsWith("#")) {
      const sectionEl = document.querySelector(href);
      sectionEl.scrollIntoView({ behavior: "smooth" });
    }
  });
});
```


----
## Sticky navagation

- once leaves the hero section
- the nav becomes sticky

```js
//Sticky nav
const sectionHeroEl = document.querySelector(".section-hero");

const obs = new IntersectionObserver(
  function (entries) {
    const ent = entries[0];

    if (ent.isIntersecting === false) document.body.classList.add("sticky");
    if (ent.isIntersecting === true) document.body.classList.remove("sticky");
  },
  {
    // In the viewport
    root: null,
    threshold: 0,
    rootMargin: "-80px",
  }
);
obs.observe(sectionHeroEl);
```

----
## Test and Optimize


### browser support

- tool: [Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/)



### backdrop-filter

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302011657951.png)


>without prefix
```css
.main-nav {
	backdrop-filter: blur(10px);
}
```


>with prefix
```css
.main-nav {
	-webkit-backdrop-filter: blur(10px);
}
```

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302011659431.png)
>unfortunately, not supported on `Microsoft Edge`




>FIX THE PROPERTY `gap` in `flexbox` in older version of browsers
```js
// Fixing flexbox gap property missing in some Safari versions
function checkFlexGap() {
  var flex = document.createElement("div");
  flex.style.display = "flex";
  flex.style.flexDirection = "column";
  flex.style.rowGap = "1px";

  flex.appendChild(document.createElement("div"));
  flex.appendChild(document.createElement("div"));

  document.body.appendChild(flex);
  var isSupported = flex.scrollHeight === 1;
  flex.parentNode.removeChild(flex);
  console.log(isSupported);

  if (!isSupported) document.body.classList.add("no-flexbox-gap");
}
checkFlexGap();
```

```css
.no-flexbox-gap .main-nav-list li:not(:last-child) {
  margin-right: 4.8rem;
}

.no-flexbox-gap .list-item:not(:last-child) {
  margin-bottom: 1.6rem;
}

.no-flexbox-gap .list-icon:not(:last-child) {
  margin-right: 1.6rem;
}

.no-flexbox-gap .delivered-faces {
  margin-right: 1.6rem;
}

.no-flexbox-gap .meal-attribute:not(:last-child) {
  margin-bottom: 2rem;
}

.no-flexbox-gap .meal-icon {
  margin-right: 1.6rem;
}

.no-flexbox-gap .footer-row div:not(:last-child) {
  margin-right: 6.4rem;
}

.no-flexbox-gap .social-links li:not(:last-child) {
  margin-right: 2.4rem;
}

.no-flexbox-gap .footer-nav li:not(:last-child) {
  margin-bottom: 2.4rem;
}

@media (max-width: 75em) {
  .no-flexbox-gap .main-nav-list li:not(:last-child) {
    margin-right: 3.2rem;
  }
}

@media (max-width: 59em) {
  .no-flexbox-gap .main-nav-list li:not(:last-child) {
    margin-right: 0;
    margin-bottom: 4.8rem;
  }
}
```


----
## Test web with Lighthouse

>`Google Chrome`
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302011713894.png)


![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302011717920.png)





## Adding Favicon and Meta description

### meta description

```html
<head>
	<meta
      name="description"
      content="Omifood is an AI-powered food subscription that will make you eat healthy again"
    />
</head>
```




### Favicon

- shrink the image file
```css
<head>
	<link rel="icon" href="img/favicon - copy.png" />
</head>
```

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302011732353.png)








>for `ios` for `Android` :  add website to ==home screen==

- change the size of image
	- for `ios` : `180 * 180`
	- for `Android`
		- `192 * 192`
		- `512 * 512


- for `ios`
```css
<link rel="apple-touch-icon" href="img/apple-touch-icon.png" />
```


- for `Android`
- create a file named `manifest.webmanifest`
- add 
```
{
  "icons": [
    { "src": "img/favicon-192.png",
      "type": "image/png",
      "sizes": "192x192" },
      
    { "src": "img/favicon-512.png",
      "type": "image/png",
      "sizes": "512x512" }
  ]
}
```

```css
<link rel="manifest" href="manifest.webmanifest" />
```


----

## Image Optimazation




### Change the size of image
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302011752054.png)

- image size : two times of render size



### Compress the images

- tool : [Squoosh](https://squoosh.app/)

>`JPEG` would leave transparency

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302011758415.png)


>save as `webp` format




### leave choice  for webpage

* `.webp` is not allowed on several web engine
>leave choice for web page
```html
<picture>
	<source srcset="img/hero.webp" type="image/webp" />
	<source srcset="img/hero.png" type="image/png" />

	<img
	src="img/hero.png"
	class="hero-img"
	alt="Woman enjoying food, meals in storage container, and food bowls on a table"
	/>
</picture>
```


----

## Netlify !!

- [Develop and deploy websites and apps in record time | Netlify](https://www.netlify.com/)

- FREE PLAN !!




### make your form work on netlify

```html
<form class="cta-form" name="sign-up" netlify>       <!--netlify form name-->
	  <label for="full-name">Full Name</label>
	  <input
		id="full-name"
		type="text"
		placeholder="John Smith"
		name="full-name"                              
		required
	  />
	  <!--add name -->
</div>

	<div>
	  <label for="email">Email address</label>
	  <input
		id="email"
		type="email"
		placeholder="me@example.com"
		name="email"
		required
	  />
	  <!--add name -->
	</div>

	<div>
	  <label for="select-where">Where did you hear from us?</label>
	  <select id="select-where" name="select-where" class="select-where" required>
		<option value="">Please choose one option:</option>
		<option value="friends">Friends and family</option>
		<option value="youtube">YouTube video</option>
		<option value="podcast">Podcast</option>
		<option value="ad">Facebook ad</option>
		<option value="others">Others</option>
	  </select>
	</div>

	<button class="btn btn--form">Sign up now</button>
</form>
```



----
## WHERE TO GO

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012006892.png)
