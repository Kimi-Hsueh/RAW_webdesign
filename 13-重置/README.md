# 今日上課設定筆記

## 為什麼要套用normalize.css的格式設定？

## Ans:因為normalize.css是將各種不同的網頁瀏覽器進行格式的統整，所以如果單獨匯入時，會感覺網頁沒有被調整格式，但實際上，在不同的網頁瀏覽器上已進行相對的調整
調整網頁的程式碼如下：
```
 html {
    -webkit-text-size-adjust: 100%; /* 2 */
  }
```

## 設定html檔與css檔的三種連結方式
### 方法一-在html檔上先後加上normalize.css及自訂的style.css
```
<link rel="stylesheet" href="./normalize.css">
<link rel="stylesheet" href="./style.css">
```

### 方法二-在style.css匯入normalize.css
```
@import url(./normalize.css)
```

### 方法三-直接將normalize.css檔的內容複制一份到style.csst檔內，然後再自己的設定檔再加入css的設定

---
# 為什麼在方法一的style. css檔內將將所有的網頁標籤設定margin及padding皆為0，網頁內容並沒有因style.css的後置順序修改呢？

# Ans:因為在normalize.css檔內，是根據個別的html標籤進行設定，所以權限高過於style.css檔案

## 參考style.css的設定
```
*{
    margin: 0;
    padding: 0;
}
```
 ## 再參考normalize.css的設定
 ```
   h1 {
    font-size: 2em;
    margin: 0.67em 0;
  }
 ```
 對比後，就可以看到萬用字元“*”的修改權限低於標籤“h1”了