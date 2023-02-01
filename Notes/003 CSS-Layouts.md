**LAYOUT**


----

## building a layout



**Page layout**

**Component layout**

(more detailed layout)



**1. Float Layouts**

* old way

**2. `Flexbox`**

* modern way
* 1-dimensional
* perfect for component layouts



**3. `CSS Grid`**

* 2-dimensional grid
* perfect for page layouts and complex components





----

## Using Floats



**The image has been taken OUT OF the page flow **

but it can create some ==margins== around it 

using float:

```css
.author-img {
  float: left;
}
```


![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012013762.png)






>tips: enter `Lorem`, then enter, a bunch of fake text would be created



>tips: ![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012013588.png)




**Th collapsing elements**

* if the child element is shifted to float, it'll have effect on the parent elements
* the container will not adjust its height to the element





----

## Clear floats

**#Solution 1**

* add a child element in the parent elements of floating child elements

```html
  <header class="main-header">
      <h1>📘 The Code Magazine</h1>
  
      <nav>
          <!-- <strong>This is the navagation</strong> -->
          <a href="blog.html">Blog</a>
          <a href="#">Challenges</a>
          <a href="#">FlexBox</a>
          <a href="#">CSS Grid</a>
      </nav>
  
      <div class="clear"></div>
  </header>
  ```

  >Assume that the `<h1>`and `<nav>`are floating

* then the css

```css
  .clear {
    clear: both;
  }
  ```

  >Here we have the prop `clear`, with its parameter `left`, `right`, `both`,which means to clear the left floating, right floating and both floating







**#Solution 2**

* add another class to the parent element

```html
  <header class="main-header clearfix">
      <h1>📘 The Code Magazine</h1>
  
      <nav>
          <!-- <strong>This is the navagation</strong> -->
          <a href="blog.html">Blog</a>
          <a href="#">Challenges</a>
          <a href="#">FlexBox</a>
          <a href="#">CSS Grid</a>
      </nav>
  </header>
  ```

* then use pseudo elements `::after`

 ```css
  .clearfix:after {
    clear: both;
    content: "";
    display: block;
  }
  ```

  >that works because the pseudo class created an element right after the last child element,similar to the last Solution.
  >
  >==**NOTICE**==
  >
  >**The pseudo elements would appear in the case its content is not empty**. The content here is indispensable.
  >
  > and the `clear` would work if the element is a **BLOCK** element, so we change it to block.





----


## BORDER BOX

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012014458.png)




* default: content-box
* reset: border-box





---
