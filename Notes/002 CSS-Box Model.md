

----


## Box Model



![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012012235.png)




![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012012650.png)




----
## Paddings and margins

## Universal selectors

* background colors -----> paddings to create some space 
* boxes that contains more child elements is placed on the top





* padding 

  ```css
    .main-header {
      background-color: #f7f7f7;
      padding: 20px;
      padding-left: 40px;
      padding-right: 40px;
    }
    ```

    

  * shorthand

 ```css
    .main-header {
      background-color: #f7f7f7;
      padding: 20px 40px;
    }
    ```

    >the first parameter is up&&down while the second one is left&&right





* margin

  * common to use `padding-bottom`to create vertical space

  ```css
    h2 {
      font-size: 40px;
      margin-bottom: 30px;
    }
    ```



* collapsing margins
  * the bigger margin would be on the screen if two margins overlap each other
  * like a paragraph has a `margin-bottom` of `15px`, while the title of next block has a `margin-top` of `40px` , then the space between the the paragraph and the title would be `40px`, not the sum of two margins.





* global reset

  * at the beginning, we can simply reset all the margins and paddings.

  * All the default properties collapsed after the reset, which is helpful for us to control the spaces between elements.

  * we gernerally use `universal selector` to reset all paddings and margins.

    ```css
    * {
      margin: 0;
      padding: 0;
    }
    ```

     >==WHY NOT `body`?==
     >
     >* the `margin` , `padding` property is not the properties related to **the text**. Therefore, it would not be inherited.

  * the `universal selector` has the lowest priority, which means it will be **overridden** if more specific properties are declared.

----
## Width and height


* width
  * the height of **CONTENT**
* height
  * has effect on the text align





use percentages

automatically adapted

* height: designated
* width: auto



----


## centering the page

**Centering our page**

```html
<div>
	main body...

</div>
```





----
## Box model


**Type of boxes**

* inline boxes
  * no \\n
  * 
* block level boxes
  * (\\n added)
  * 100% of the parent element's width
  * stacked vertically

**the property of box model is not accessible in inline elements**

```css
  nav a:link {
    background-color: orangered;
    margin: 20px;
  }
  /*This wouldn't work in the verticle direction*/
  ```



* change in inline to block level

  ```css
    display: block;
    ```

    

* inline-block boxes
  * occupy only content's space
  * causes no line-breaks
  * box-model appliesas showed

* img are **inline-block** elements





---

## ABSOLUTE Positioning



* normal flow

  * default
  * *in flow*
  * according to their order in HTML

  



* absolute positioning
  * *out of flow*
  * no impact on surrounding elements, might overlap
  * `top bottom left right` are used to offset the element from its **relatively positioned container**



>`Windows + .`: open emoji box



*We don't usually use this tech to build big blocks, but for some small elements*



----

## Pseudo-elements



* not alctually exist in html



* we use `::`to feature pseudo class

```css
  h1::first-letter {
    font-style: normal;
    margin-right: 5px;
  }
  
  p::first-line {
    color: red;
  }
  
  ```





* adjacent sabling selector

  * int the same container 

  * adjacent

 ```css
    h3 + p::first-line {
      color: red;
    }
    /*only the p after the h3 will be selected*/
    ```

    



* `::after`, `::before`

  * set content

  * set colors

  * set fonts

  * **the pseudo ele created is *inline-ele*, turn it into *inline-bolock ele***

  ```css
    h2::after {
      content: "TOP";
      background-color: #ffe70e;
      color: #444;
      font-size: 16px;
      font-weight: bold;
      display: inline-block;
      padding: 5px 10px;
      position: absolute;
      top: -10px;
      right: -25px;
    }
    
    ```

    >no where to find this thing in html	(top tag)
    >
    >![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012013298.png)




* negative length
  * move in the opposite direction



==**NOTICE**==

**The pseudo elements would appear in the case its content is not empty**. The content is indispensable.

----

## learning methology

**Googling and Reading Documentation**

* no `W3C School`
* `Stackoverflow`
* `MDN Dcumentation`


----
## Debugging && Asking Questions



* Debugging
* html
  * `html validator`
  * `diff checker`

* css
  * (selector conflict) Selector Specificity
    * show up when the cursor hovering on the selector
  * spelling mistake
    * inspector
  * experimenting 
    * click on the value & use up/down keys
    * `Shift + up/down`
  * check out The css link connection



----
## Default settings


* set the line padding double as vertical padding

 ```css
  article::before
  {
      padding: 7px 15px;
  }
  ```





* several classes attached to one element

 ```css
  <div class="colors">
          <div class="color"></div>
          <div class="color color-blue"></div>
          <div class="color color-red"></div>
          <div class="color color-yellow"></div>
          <div class="color color-green"></div>
          <div class="color color-brown"></div>
  </div>
  ```

  
----
