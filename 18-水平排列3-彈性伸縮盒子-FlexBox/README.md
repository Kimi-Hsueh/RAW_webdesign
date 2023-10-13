# flexbox-彈性伸縮盒子

# 當有任何display:flex設定時，都是設定在母盒內
```
.box{ 
	display: flex; /*當有任何display:flex設定時，都是設定在母盒內*/
	flex-wrap: wrap;
	/*flex-direction: row; /*如果是以column做直行排列，需要設定盒高*/
	/*height: 1500px; /*設定盒高為1500px*/
	justify-content: space-evenly; /*水平並在所有div有水平間距*/	
}
```
width平均分配語法：
```
.box div{
	width: 30%;
	padding: 20px; /*設定邊界內縮20px*/
	box-sizing: border-box; /*設定以母盒作為邊界*/
	/*width: calc(100%/3); /*設定母盒內的div平分1200px*/
}
```

本章的DOM分類：
```
box{
    .box div{
        b1{}
        b2{}
        b3{}
    }
}
```