# DOM的概念

## DOM ->Document Object Model
是將文件內的每一個標籤物件進行分層

```
<div>
    <h1><img></h1>
    <ul>
      <li><a></a></li>
      <li><a></a></li>
      <li><a></a></li>
      <li><a></a></li>
      <li><a></a></li>
    </ul>
</div>
```

以DOM的概念分層後………
```
div{}

h1{}
h1 img{}

ul{}
ul li{}
ul li a{}
ul li a :hover{}
```
# 為什麼這個實例不需要使用box-sizing？
  因為所有在div裡的物件被限制以“position: relative”做為對齊點，所以不需使用box-sizing

# 如何區分position與float的使用時機？？？

  position ->當標籤物件不要做水平對齊時

  float ->當標籤物件需要做水平對齊時