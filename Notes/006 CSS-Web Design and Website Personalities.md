
----

## About the HTML

### span
- Span is a generic INLINE text element, it doesn't have any meaning. It's like a div element, but inline
```html
<ul>
	<li>
		<span>item1</span>
	</li>
	<li>
		<span>item2</span>
	</li>
</ul>
```


### blockquote
- used to indicate that the block is a quote, for sematic purpose
```html
<blockquote class="testimonial-text">
	Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor
    repellat at, nesciunt quia cum minima ipsum culpa totam sapiente
    recusandae earum debitis doloribus in quasi voluptatibus!
</blockquote>
```


----
## Overview of Web Design

### Web design && Development
- designer 
	- look && feel
- web design
	- implement


### Take it seriosly
- good impression
- trust
- preceived value
- perspicuous for users


### Web Design ingredients

- typography
- colors
- images / illustrations
- icons
- shadows
- border-radius
- whitespace
- user experience
- components / layout


### Website Personalities

- Serious/Elegant:
	- For luxury and elegance, based on thin serif typefaces,golden or pastel colors, and big high-quality images
- Minimalist/Simple:
	- Focusses on the essential text content, using small ormedium-sized sans-serif black text, lines, and few images and icons
- Plain/Neutral: 
	- Design that gets out of the way by using neutral and smalltypefaces, and a very structured layout. Common in big corporations
- Bold/Confident: 
	- Makes an impact, by featuring big and bold typography,paired with confident use of big and bright colored blocks
- Calm/Peaceful: 
	- For products and services that care, transmitted bycalming pastel colors, soft serif headings, and matching images/illustrations
- Startup/Upbeat: 
	- Widely used in startups, featuring medium-sized sans-serif typefaces, light-grey text and backgrounds, and rounded elements
- Playful/Fun: 
	- Colorful and round designs, fueled by creative elements likehand-drawn icons or illustrations, animations, and fun language


----
## Typography

### Concept
- legible
- readable
- appealing


### Serif vs. Sans-serif

- Serif typeface
	- traditional/classic
	- trustworthiness
	- long text
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091600325.png)


- Sans-serif typeface
	- mordern look and feel
	- clean and simple
	- easier to choose for beginner designer
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091602016.png)





### Good Typefaces

- good && popular typeface

- Font Source
	- TOOLBOX
	- [Google Fonts](https://fonts.google.com/)
	- Font squirrel

- Sans-serif recommandation
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091609963.png)


- Serif recommandation
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091610140.png)


- Limit to 2 typeface

- Choose `right` typeface according to website personality
	- choose personality
	- decide serif or sans-serif
	- experiment
	- try on more typeface




### Sizes and Weights

- limit choice
	- [type scale](https://type-scale.com/)
	- pre-defined range
- use a font size between `16px` and `32px` for "normal" text
- for **long text** (blog text), try a size of `20px` or even bigger
- for **headlines**, you can go really big (`50px`+) and bold (`600`+) , depending in personality
- for any text, don't use a font weight under 400 (regular)

- example
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091622626.png)



### Reading Experience

- use less than 75 charactors per line
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091624918.png)

- for noraml-sized text, use a line height between 1.5 and 2. For big text, go below 1.5
	- The smaller / longer the text, the larger the line height need to be.
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091628025.png)

- Decrease letter spacing in headlines, if it looks unnatural
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091629423.png)

- Experiment with all caps for short titles. Make them small and bold and increase letter spacing
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091631643.png)

- Usually, don't justify text

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091633447.png)


- Don't center long text blocks. Small blocks are fine
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091634346.png)



----
## Implementing Typography



### typeface
```css
body {
	font-family : 'Inter', sans-serif;
}
```
>priority on `Inter` and if it dosen't work, use `sans-serif`


### size and weight
- [type-scale](https://type-scale.com/)
- define a system for fonts and space
```css
/*
SPACING SYSTEM (px)
2 / 4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 80 / 96 / 128
FONT SIZE SYSTEM (px)
10 / 12 / 14 / 16 / 18 / 20 / 24 / 30 / 36 / 44 / 52 / 62 / 74 / 86 / 98
*/
```

>trick : computed section in dev tools

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091713575.png)

>trick : change values in dev tools with `arrow up/down` or `Alt + arrow up/down`


### Spacing

### Line height

>be consistant in the page 



----
## Color

- main color
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091933674.png)

1. 
- color tone
	- no random
	- no CSS named colors
	- useful tools
		- [Open color](https://yeun.github.io/open-color/)
		- tailwindcss
		- FLAT UI COLORS 2


2. 
- at least 2 colors in your color palette 
	- main color
	- grey color
	- accent color (more experienced)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091941648.png)



3. 
- create lighter and darker "versions" of colors
	- tints
	- shades
	- useful tool
		- Tint & Shade Generator
		- palleton.com
		- COOLORS
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301091944036.png)




4. 
- main color : DRAW ATTENTION
	- button
	- logo

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301092047653.png)



5. 
- use colors to add interesting accents to make components or sections stand out


6. 
- use color strategically in images and illustrations
	- use colors in the illustration

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301092046696.png)


7. 
- On dark colored backgrounds, use a tint of the background("lighter version") for text

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301092049437.png)



8. 
- the text should not be completely black. Lighten up if it looks and uninviting
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301092051583.png)




9. 
- Don't make text too light 
	- useful tools for contrast
		- [COOLORS](https://coolors.co/contrast-checker/112a46-acc8e5)
	- contrast ratio
		- AT LEAST 4.5 : 1 for normal text
		- AT LEAST 3 : 1 for large text (19px+)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301092106633.png)


----

>use the same class in all the buttons and add specific second class to modify the details

```html
<a href="#" class="btn btn--big">button1</a>
<a href="#" class="btn btn--small">button2</a>
```


>add a footer line of the page
```css
body {
	...
    border-bottom: 8px solid #087f5b;
}
```



----
## Images && Illustrations

* [Beautiful Free Images & Pictures | Unsplash](https://unsplash.com/)
* [Home - UI Faces](https://www.uifaces.co/)


### Use good images

1. 
- different types
	- product photos
	- storytelling photos
	- illustrations
		- 2D
		- 3D
	- pattens


#### type examples

>product (physical && digital)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151432219.png)


>storytelling
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151433547.png)


>illustrations (2D)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151434498.png)


>illustrations(3D)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151434687.png)


>patterns (visual details)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151435202.png)


2. 
- use img to support **message and story** , no irrelevant images



3. 
- Prefer original images. or use original-looking stock imgs (not generic ones!)
- useful tools
	- Unsplash
	- Pexels
	- DrawKit
	- unDraw





### Use images well

4. 
- show real people to trigger users' emotions

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151440205.png)



5. 
- crop images to fit your message if neccesary


6. 
- experiment combining photos, illustrations and patterns



### Handling Text on Images

7. 
- Method 
	- Darker or brighten your images
	- Position the text into neutral images area
	- Put text in a box

>method1 : darker or brighter
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151443170.png)


>in the neutral area
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151444176.png)


>in the box
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151446620.png)


### Technical details

8. 
- To account for **high-res screens**, make image dimensions ==2x as big== as their displayed size
- **Scale factor**
	- Actual pixels the screen contains / Pixelsrepresented on screen
- On **high-res screens**, ==scale factor is 2x or even 3x==, on “normal"screens it's just 1x (1 physical pixel = 1 design pixel)


- visiable : `200 * 200 px`
- original : `600 * 600 px`




9. 
- compress the images for lower file size for better performance
- useful tools
	- Squoosh


10. 
- images should have exact same dimensions


----
## Icons


### Use good Icons

1. 
- good icon pack matters
- useful tools
	- Phosphor icons
	- ionicons
	- ICONSS
	- [heroicons](https://heroicons.com/)


2. 
- use only one icon pack (do not mix)



3. 
- use SVG or icon fonts 
- do not use bitmap formats (`.jpg` and `.png`)
- no Google images 

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151512270.png)



4. 
- Adjust to website personality, **weight** and **filled/outlined** depend on typography
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151513340.png)


### When to use Icons

5. 
- use icons to provide visual assistance to text 
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151515817.png)


6. 
- use icons for product feature blocks
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151516462.png)


7. 
- use icons associated with actions, and label them (unless no space or icon is 100% clear)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151519190.png)


8. 
- use icons as bullet points
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151520847.png)



### Use Icons Well

9. 
- to keep icons neutral, use same color as text
- or diff color to accent sth
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151521475.png)


10. 
- fit the text  or action


11. 
- do not make icons larger than what they are designed for.
- If needed, enclose them in a shape

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151523800.png)


----

- `SVG` : essentially is set of code
```html
<svg
      xmlns="http://www.w3.org/2000/svg"
	  class="feature-icon"
	  fill="none"
	  viewBox="0 0 24 24"
	  stroke-width="1.5"
	  stroke="currentColor"
	  class="w-6 h-6"
>
	<path
		stroke-linecap="round"
		stroke-linejoin="round"
		d="M9.75 3.104v5.714a2.25 2.25 0 01-.659 1.591L5 14.5M9.75 3.104c-.251.023-.501.05-.75.082m.75-.082a24.301 24.301 0 014.5 0m0 0v5.714c0 .597.237 1.17.659 1.591L19.8 15.3M14.25 3.104c.251.023.501.05.75.082M19.8 15.3l-1.57.393A9.065 9.065 0 0112 15a9.065 9.065 0 00-6.23-.693L5 14.5m14.8.8l1.402 1.402c1.232 1.232.65 3.318-1.067 3.611A48.309 48.309 0 0112 21c-2.773 0-5.491-.235-8.135-.687-1.718-.293-2.3-2.379-1.067-3.61L5 14.5"
	/>
</svg>
```
>icon of a beaker


- the color of a `SVG` image (OUTLINE)
```css
.features-icon {
  stroke: #087f5b;
  /*fill: red;*/ /*if you want to FILL the svg icon*/
}
```
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151549561.png)


- the color of a `SVG` image (SOLID)
```css
.featrues-icon {
	fill: #087f5b;
}
```
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151549832.png)




- mutiple cursors
- `Alt + Ctrl + C` copy mutiple lines
- `Alt + <multiple select cursor> + Ctrl + V` paste multiple lines at the same time



----
## Shadows


### Concepts
- brief history in shadows
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151743328.png)


- Shadow creates depth (3D): 
	- the more shadow, the further away from the interface the element is
- Used in **boxes and text**

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151745674.png)



### Use shadow well


1. 
- dont have to use shadows. 
- only if it make sense for the website personality
- Styles
	- serious : less shadows
	- playful : more shadows

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151751232.png)




2. 
- use shadows in small doses
- dont add it to every element
	- visual hierarchy



3. 
- go light on shadows and dot make them too dark



### Use shadows in the Right Situation

4. 
- use **small** shadows for smaller elements that should stand out (draw attention)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151759898.png)


5. 
- use **medium-sized** shadows for larger areas that should stand out a bit more
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151800583.png)


6. 
- use **large** shadows for elements that should really float above the interface
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151801759.png)


7. 
- Experiment with changing shadows on mouse interaction
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151802389.png)
>medium sized shadow "pulls" closer to the user
>smaller shadow "pushes" button into the interface



8. 
- Bonus : experiment with **glows** (colored shadows)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301151804388.png)


----

- the shadow
```css
.chair-box {
  padding: 24px;
  box-shadow: 20px 20px 20px 10px #000;
}
```

```css
.sth {
	box-shadow: horizental-offset vertical-offset blur shadow-scale color;
}
```



- `figure` element
- The figure element represents some flow content, optionally with a caption, that is self-contained
- like cart for each item
```html
<figure>
	content
</figure>
```




- use shadows on box or **text**


**BOX SHADOW**

- shadow : basically shining down from the top
>horizental offset : 0

- blur : turn a box
>blur  : 0

- shadow-scale
>the radius of shadow

```css
.chair {
  box-shadow: 0 20px 10px 0 rgba(0, 0, 0, 0.8);
}
```
![[03 CSS_JS-006_shadow]]




**TEXT SHADOW**
```css
.h1 {
	text-shadow: 0 20px 30px rgba(0, 0, 0, 0.07);
}
```
>text shadow has 3 args for shadow shape, missing radius compared with box-shadow


----
## Border-radius

### Use border-radius well

1. 
- more playful more radius
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301161318607.png)




2. 
- match the roundness of border-radius of typefaces
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301161321680.png)



3. 
- use border-radius on buttons, images, around icons, standout sections and other elements

>buttons
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301161324294.png)


>images
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301161325501.png)


>around icons
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301161327818.png)


>standout sections
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301161327417.png)


>other elements
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301161328190.png)



----

```css
.sth {
	border-radius: 12px;
	border-bottom-left-radius: 0;    /*control the cornors separately*/
} 
```


----
## Whitespace


### Why Whitespace

- clean, modern and polished
- communicates how different pieces of infomation are related to 
- implies invisible relationships between the elements


### Where to use whitespace

1. 
- between sections, groups of elements
- between elements

- use whitespace instead of lines
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301161354829.png)


2. 
- the more elements belong together, the closer they should be


3. 
- start with a lot of whitespace then remove whitespace from there
	- too much whitespace looks detatched 
	- too little -> crammed


4. 
- match other design choices
	- big text or icons -> more whitespace
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301161358270.png)


5. 
- tyr a hard rule (mutiple of `16px` for all spacing)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301161359634.png)
>limit your choice on whitespacing

----
## Visual Hierarchy

### What is visual hierarchy

- establishing which elements of a design are the most important ones
- drawing attention to the most important elements
- defining a path for users(guiding)
- combination pf position, size, colors, spacing, borders, shadows

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182155600.png)



### Fundamentals

1. 
- position elements closer to the top the page
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182156527.png)


2. 
- use image mindfully (cause'in it draws lots of attention)
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182305383.png)



3. 
-  whitespace separation, use whitespace strategically
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182306183.png)


### Test Elements

4. 
- use **font size, font weight color whitesapce**
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182308775.png)

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182309567.png)

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182310418.png)



5. 
- what elements to emphsize ? 
	- titles
	- sub-titles
	- links
	- buttons
	- data points
	- icons

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182312044.png)

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182313545.png)



### Between Components



6. 
- background color, shadow, border
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182315944.png)


7. 
- try to emphasize some component A over B by **de-empahsizing** component B
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182317734.png)
>background color



- what to emphasize ? 
	- testmonials
	- call-to-action sections
	- highlight sections
	- preview cards
	- forms
	- pricing tables
	- important rows/columns in tables

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182320077.png)

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182321186.png)


----
## User Experience (UX)


### What is Experience?

- User Interface : beautiful
	- Layout
	- Personality
	- Typography, colors, icons, etc

- User Experience : beautiful && functional
	- logical ?
	- navagation works intuitively ?
	- users reaching their goals?



### UI and UX Design

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182353812.png)




### UX Design guiding Principle : GOALS

- reasons
	- user : visiting
	- business : creating

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182357324.png)



>example : Highlight an option in the product pricing table
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301182359010.png)


>negative example
>	pop-up form to capture email addresses
>	hiding button to cancel subscription



### UX Rules for Usability

1. 
- No compicated layouts
- Don't reinvent the wheel
- use patterns that users know
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301190011991.png)




2. 
- make call-to-action the most prominent element 
- make the text descriptive
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301190013003.png)



3. 
- Use blue text and underlined text only for links !!!!
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301190014992.png)



4. 
- Animations
	- have a purpose
	- fast




5. 
- In forms, align labels and fields in a sigle vertical line, to make them easier to scan
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301190017842.png)



6. \[web apps\]
- Offer users **good feedback** of all actions
	- form errors
	- form success

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301190019017.png)




7. \[web apps\]
- place the action buttons where they will create an effect
- **law of locality**

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301190021569.png)



### UX Rules for Website Content

8. 
- Use a descriptive, keyword-focused headline on the main page
- DON'T be vague for fancy

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301190025715.png)





9. 
- Only include relevant information, effectively!
- **Cut out fluff** and make thhe content 100% clear




10. 
- Use simple words
- Avoid technical jargon and "smart-sounding" words
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301190030450.png)


11. 
- Break up long text wwith **sub-headings, images, block quotes, bullet points**, etc

----
## Website Personalities Framework

### Framework

- 7 personalities
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301190035501.png)


- workflow
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301190036960.png)
>limited choices according to different personalities


### Serious/Elegant

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191758204.png)

>examples
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191808075.png)





### Minimalist/Simple

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191809563.png)


>examples
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191810368.png)






### Plain/Neutral

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191810210.png)


>examples
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191811412.png)






### Bold/Confident

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191812078.png)


>examples
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191813404.png)




### Calm/Peaceful

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191813487.png)


>examples
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191814532.png)







### Startup/Upbeat

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191815638.png)


>examples
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191816319.png)








### Playful/Fun
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191817892.png)




>examples
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191818540.png)





### Combining Playfulness and Boldness

- different types are embeded into others
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191822672.png)
>move vertically to customize the personality


>examples
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191826543.png)


![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191828645.png)


![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301191828708.png)

----
## Steal like an Artist!!


- websites for designs
	- [land-book](https://land-book.com)
	- [onepagelove](https://onepagelove.com/)
	- [awwwards](https://www.awwwards.com/)
	- [screenlane](https://screenlane.com/)

