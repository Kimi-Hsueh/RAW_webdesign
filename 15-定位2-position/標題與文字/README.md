# 今日上課內容

## 除了padding與margin去做定位設定之外，現在又來了個☆position☆

# position的用法：

## 用法一：postion:absolute
用法說明：
postion:absolute為絕對位置，需要與 left/top 及 top/bottom搭配使用
```
h1{
    position: absolute;
    left: 650px;
    top: 180px;
}
```

## 用法二：postion:relative
用法說明：
postion:relative為相對位置，是限制標籤內的所有格式以該標籤作為所有起始點使用
```
div{
    position: relative; /*此行為限制盒子內的h1及p的定位點以盒子邊界做計算*/
}

h1{
    position: absolute;
    left: 650px;
    top: 130px;
}
```

## 當有多個position時，會有層次順序的問題!!!
## 此時就要用到☆z-index☆進行層次順序的排定
用法說明：
設定標籤的層次順序時，順序越靠後的標籤會壓掉順序數字小的標籤：
例：h1的z-index為1，p的z-index為2，可是在top的設定上是一樣的，所以在頁面的呈現上會是p的內容蓋掉h1
```
h1{
    position: absolute;
    left: 650px;
    top: 130px;
    z-index: 1; /*設定標籤的層次順序為1，順序越靠後，會壓掉順序數字小的標籤*/
}

p{
    position: absolute;
    left: 650px;
    top: 130px;
    padding-right: 100px; /*設定文字右側距離為100px(margin-向外推)*/
    z-index: 2; /*設定標籤的層次順序為2，順序越靠後，會壓掉順序數字小的標籤*/
}
```