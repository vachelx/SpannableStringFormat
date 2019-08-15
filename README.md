# SpannableStringFormat
富文本中常用样式组合的简单工具类

### 2种用法
##### 1. 一条文本前后样式不一： text的前三个字为颜色"#000000"，15sp字体后面的剩下的字体为颜色"#23262F"，20sp的粗体字
```
 SpannableString spannableString = SpannableStringFormat.createBuild(text)
                     .textColorSize(0 , 3, Color.parseColor("#000000"), 15, true)
                     .textColorStyleSize( 3,  text.length(), Color.parseColor("#23262F"), Typeface.BOLD, 20, true)
                    .build();
```


##### 2.不确定有多少文本，每一个文本段添加不同颜色
```
SpannableString spannableString = SpannableStringFormat.createBuild()
                     .addSpannable(text1, color1)
                    .addSpannable(text2, color2)
                    .build();
```
