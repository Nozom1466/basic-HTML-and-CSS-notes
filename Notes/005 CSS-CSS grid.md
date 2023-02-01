**CSS GRID**

----
## COLUMNS AND ROWS
```css
display: grid;

grid-template-columns:  . . . . ;
...			-rows...

column-gap: 30px;
row-gap: 60px;
```





![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012016453.png)




![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012016821.png)






![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202302012016799.png)




----

## fr Unit

* fr unit
* (fraction)

```css
grid-template-columns: 3fr 1fr 1fr auto;
```

to fill the backgroud

```css
grid-template-columns: repeat(4, 1fr);
```

* implicit rows && explicit rows
----

## PANNING

cross the grids :

**M1** : 
```css
.el--8{
	grid-column: column_start / column_end;
	grid-row: row_start / row_end;
}
```
>the `column_start ` parameter and those alike are the **sequnce number** of the grid.

```css
.el--8{
	//strecth to the end
	grid-column: column_start / -1;
	grid-row: row_start / row_end;
}
```
>the end param could be `-1` , if a cell if designed to stretch to the end.



**M2**:
```css
.el--8{
	grid-column: column_start / span 2;
	grid-row: row_start / span 4;
}
```
>`span + length/height` could be used to define the length / height, with the start at `column_start` or `row_start`


==Notice==
- One cell actually has two sequnce number, one from the left in positive numbers, the other from the right in negtive numbers.


![](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301021605640.png)


----
## Aligning grid items and tracks



- for boxes
```css
//horizental
align-content: center;

//vertical
jusstify-content: center;

```


- for items
```css
//horizental
align-items: center;

//vertical
justify-items: center;
```



![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301021726656.png)


- you can adjust the items separately
```css
.el--3 {
        align-self: center;
        justify-self: center;
      }
```

![image.png](https://sandox-1316371247.cos.ap-shanghai.myqcloud.com/ObsidianImg/202301021756656.png)



----
