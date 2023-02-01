**FlexBox** ^47d81d

----
## Overview

```css
  .container {
          /* STARTER */
          font-family: sans-serif;
          background-color: #ddd;
          font-size: 30px;
          margin: 40px;
  
          /* FLEXBOX */
          display: flex;
        }
  ```

* the height is the same as the highest block


* aligned

  ```css
/*vertical aligned*/
.container{
	align-items: center;
}
    ```

    ![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012014785.png)


    >CSS block has fixed height

 ```css
/*bottom aligned*/
.container{
	aligned-items: flex-end;
}

/*top aligned*/
.container{
	aligned-items: flex-start;
}
```

 ```css
/*default layout*/
.container{
	aligned-items: stretch;
}
```





* 水平居中

  ```css
    .container{
        justify-content: center;
    }
    ```

>![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012014175.png)

  * 水平均匀排布

    ```css
    .container{
        justify-content: space-between;
    }
    ```

>![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012014482.png)






----

## TERMINOLOGIES

^b82d7d

* 1-demensional layouts



* Components

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012015955.png)






terminology 
![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012015481.png)
^flexShortHand







----

## Spacing and aligning flex Items



* the special behavior of certain element

```css
  /*the special position of certain element*/
  .el--1{
      align-self: flex-start;
  }
  ```

* .

  ```css
  /*the order of flex item*/
  .el--5{
      order: 1;
  }
  ```

  >Initially, the `order`of each item is 0, then you can mannually set the order value to any number
  >
  >All the orders could be arranged accroding to the value of order
  >
  >





* use `gap` in the container, but not the `margin`in the item

 ```css
  .container {
      /* STARTER */
      font-family: sans-serif;
      background-color: #ddd;
      font-size: 30px;
      margin: 40px;
  
      /* FLEXBOX */
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 30px;
  }
  ```

  



---

* what is the **CONTAINER**??, always be  ==THE FIRST STEP== of flexbox


----
