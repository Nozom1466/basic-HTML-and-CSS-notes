# CSS

----

## basic selector

* Cascading Style Sheet
* visual style presentation & conent written in HTML
* countless properties



```css
h1{
    color : blue;
    text-align : center;
    font-size : 20px;
    
}
```

>* Selector
>
>* Declaration Block
>  * Declaration / Style
>    * Property : Value
>
>



----
## type of css


* types of css
  * inline css
  * internal css
  * external css



* inline css

```html
    <h1 style="color: blue">📘 The Code Magazine</h1>
    ```

  * **never should be used!!!**



* internal css

```html
    <head>
        <style>
            h1 {
                color: blue;
            }
        </style>
    </head>
    
```

* external css

 ```html
 <link href="style.css" rel="stylesheet"/>
	```

    

>decouple
>
>entangled
>
>the speration of concerns



----
## H selector


```css
h1{
    
    font-size : 20px;				/*font size*/
    font-family : sans-serif;		/*font family*/
    font-style : italic;`			/*font style*/
    text-transform : uppercase;		/*text transformation : capitalize the first letter*/
    text-align : center;			/*text align*/
    line-height : 1.5;				/*interval space between each line*/
    
}
```

----
## List selector


* list selector 

* descendant selector

  * there're chances of leading to  the confusion of labels in different places(header for the page or the article)

    Solution1: add another descendant selector for some specific labels
    
```css
 header p {
   font-style: italic;
 }
 
 article header p{
   font-style:italic;
 
 }
 ```
    
more coding
hard to maintain if any changes in html

> Solution2: classes && ids



----

## id and class

* id

  ```html
    <p id="copyright">Copyright &copy; 2027 The Code Magazine.</p>
        </footer>
    ```

  ```css
    #copyright {
      font-size: 16px;
    }
    ```

    >`id`could conly be used once!
    >
    >**never use series**
    >
    >use `#`



* class

  ```html
    <ul class="related">
    ```

  ```css
    .related {
      list-style: none;
    }
    ```

    >use `.` 
    >
    >`class`could be used in different places.



----
## colors


* COLORS



* RGB MODEL
  * 0-255
  * RED 255 0 0
  * GREEN 0 255 0
  * BLUE 00



* TWO WAYS TO MAKE COLOR

  * RGB
  * RGB with transparency 
  * Hexadecimal notation
    * `#00ffff`
    * shorthand when  all colors are identical pairs
      * `#0ff == #00ffff`

  * ==Gray==
    * colors in 3 channals are the same
    * rgb(69, 69, 69) / #444444 / #444
    * rgb(183, 183, 183) / `#b7b7b7`

  

```css
.main-header{
    background-color : #f7f7f7
}

```





* element selector
* class selecor
* id selector





```css
aside {
  border: 5px solid #1098ad;  /*shorthand properties*/
    /*dotted dashed*/
}

aside {
  border-top: 5px solid #1098ad;
  border-bottom: 5px solid #1098ad;
}

```







----

## pseudo class

* pseudo class

```css
  li:first-child {
    font-weight: bold;
  }
  
  li:last-child {
    font-style: italic;
  }
  
  li:nth-child(odd) {
    color: red;
  }
  ```

  >nth-child()
  >
  >* odd / even could be placed here



* mistakes

* if we want to select the first child \<p> in  \<article> ,we may use

  ```css
  article p :first-child {
    color: red;
  }
  ```

  >this won't work
  >
  >however , it will check whether the first element in article is \<p> or not.
  >
  >if false, nothing would happen





----
## styling hyperlinks


* styling hyperlinks

```css
/*set style for those a label with an actual link*/
a:link {
  color: #1098ad;
  text-decoration: none;
}

/*set style for the linkes which are visited*/
a:visited {
  /* color:#777;*/
  color: #1098ad;		/*Usually we set the color of visited labels to the same color of the link not visited*/
}

/*set color for the cursor hovering on a link*/
a:hover {
  color: orangered;
  font-weight: bold;
  text-decoration: underline orangered;
}

/*set style for the linkes the moment they are activated*/
a:active {
  background-color: black;
  font-style: italic;
}
```

 >these pseudo classes of a label is fixed in tis sequence,namely `LVHA`





----

## dev tools



* user agent stylesheet

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012011084.png)


>the default stylesheet of labels (Here is label `<h1>`) 


* test on the page


![image-20221102182242306](C:\Users\mts14\AppData\Roaming\Typora\typora-user-images\image-20221102182242306.png)

```css
a:link{
    color: #1098ad;
    text-decoration: none;
    font-size: 30px;		/*Added right on the dev tools*/
}
```


>>add certain properties on thedev tools 
>>
>>by clicking the hook square in front of it ,we could disable it or active it 







* quick director
* right click the element and gor for `inspect`
* the dev tool would locate where it is.







* fake hovering 
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012011979.png)


>on the right top corner, we have `:hov`, which is designed to simulate the action of the cursor `hover`,`active`,`visited`,etc.
>
>![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012012867.png)

>
>it seems like the cursor is hovering above the link
>
>**for test purpose**







----

## selector priority


**CONFLICTS BETWEEN SELECTORS**

* multiple selectors selecting the same element
  * ALL OF THEM get applied 
  * PRIORITY when conflicts exist





**PRIORITY**

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012012564.png)




Basically, it follows the rules of 

* `!important`

   ```css
    h1{
      color: blue !important;  
    }
    ```

    >this property will be applied ahead of others

    

* inline style

* ID selector

  ```html
    <p>test</p>
    ```

    

  ```css
    #copyright{
        color:red;
    }
    
    .copyright{
        color:blue;
    }
    
    .text{
        color:yellow;
    }
    
    footer {
        color: green;
    }
    ```

    >ID selector rendered red

* Class or Pseudo class

  * 

  ```css
    .copyright{
        color:blue;
    }
    
    .text{
        color:yellow;
    }
    
    footer {
        color: green;
    }
    ```

    > .text render yellow
    >
    > the last style of the same level would be rendered 

* element selector

  * the second lowest priority to be rendered

* universal selector





>_hint_:
> we could use the dev tools to active or disable the property
> without deleting the code itself







----

## Inheritance

**INHERITANCE**

* ALL the child labels would automatically inherit the property from its father label.
* Global property:
  * set in the body part
  * ALL labels would inherit the property from it



>use inheritance to include a all the child labels

**The inheritance would only have effect on ==TEXT PROPERTIES==**



**UNIVERSAL SELECTOR**

* use `*`

```css
  * {
    	border-top: 10px solid #1098ad;
  }
  ```

  





>==The difference in setting global property==:
>
>* once set in the body part, ***ALL PARTS*** would inherit property
>* ***NO PARTS*** would inherit the property in the universal selector



----

```css
button{
    cursor: pointer;
}
```

>set the cursor to a certain shape
>
>


----
