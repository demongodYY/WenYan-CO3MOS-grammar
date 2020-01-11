# WenYan-CO3MOS 语法
based on:
- https://github.com/wenyan-lang/wenyan/blob/master/README.md
- https://github.com/wenyan-lang/wenyan/blob/master/documentation/Standard-Lib.md

## 基础语法
#### 变量

| wenyan | JavaScript |
|---|---|
|`吾有一數。曰三。名之曰「甲」。` | `var a = 3;` |
|`有數五十。名之曰「大衍」。` | `var dayan = 50;` |
|`昔之「甲」者。今「大衍」是矣。` | `a = dayan;` |
|`吾有一言。曰「「噫吁戲」」。名之曰「乙」。` | `var b = "alas!";` |
|`吾有一爻。曰陰。名之曰「丙」。` | `var c = false;` |
|`吾有一列。名之曰「丁」。` | `var d = [];` |
|`吾有三數。曰一。曰三。曰五。名之曰「甲」曰「乙」曰「丙」。` | `var a=1,b=3,c=5;` |
|`吾有一元` | `(auto type)` | 

#### 控制

| wenyan | JavaScript |
|---|---|
|`若三大於二者。乃得「「想當然耳」」也。` | `if (3>2){ return "of course"; }` |
|`若三不大於五者。乃得「「想當然耳」」。若非。乃得「「怪哉」」也。` | `if(3<=5){return "of course"}else{return "no way"}` |
|`為是百遍。⋯⋯ 云云。` | `for (var i = 0; i < 100; i++){ ... }` |
|`恆為是。⋯⋯ 云云。` | `while (true) { ... }` |
|`凡「天地」中之「人」。⋯⋯ 云云。` | `for (var human of world){ ... }` |
|`乃止。`|`break;`|
|`乃止是遍`|`continue`|
|`或若`|`else if` | 
|`若其然者` |`if (ans) {` | 
|`若其不然者`|`if (!ans) {` | 

#### 计算

| wenyan | JavaScript |
|---|---|
|`加一以二。` | `1+2` |
|`加一於二。` | `2+1` |
|`加一以二。乘其以三。` | `(1+2)*3` |
|`除十以三。所餘幾何。` | `10%3` |
|`減七百五十六以四百三十三。名之曰「甲」。` | `var a = 756-433;` |
|`夫「甲」「乙」中有陽乎。` | `a \|\| b` |
|`夫「甲」「乙」中無陰乎。` | `a && b` |


#### 容器
Arrays are 1-indexed.

| wenyan | JavaScript |
|---|---|
|`吾有一列。名之曰「甲」。充「甲」以四。以二。` | `var a = []; a.push(4, 2);` |
|`銜「甲」以「乙」。以「丙」` | `a.concat(b).concat(c);` |
|`夫「甲」之一。` | `a[0]` |
|`夫「甲」之其餘。` | `a.slice(1);` |
|`夫「玫瑰」之「「名」」。` | `rose["name"]` |
|`夫「寶劍」之長。` | `sword.length;` |


#### 对象

| wenyan | JavaScript |
|---|---|
|`吾有一物。名之曰「甲」。` | `var a = {};` |
|`吾有一物。名之曰「甲」。其物如是。物之「「乙」」者。數曰三。物之「「丙」」者。言曰「「丁」」。是謂「甲」之物也。` | `var a = {b:3, c:"d"}` |


#### 函数

| wenyan | JavaScript |
|---|---|
|`吾有一術。名之曰「吸星大法」。是術曰。⋯⋯是謂「吸星大法」之術也。`|`function f(){...}`|
|`吾有一術。名之曰「六脈神劍」。欲行是術。必先得六數。曰「甲」。曰「乙」。曰「丙」。曰「丁」。曰「戊」。曰「己」乃行是術曰。⋯⋯是謂「六脈神劍」之術也。`|`function f(a,b,c,d,e,f){...}`|
|`吾有一術。名之曰「翻倍」。欲行是術。必先得一數。曰「甲」。乃行是術曰。乘「甲」以二。名之曰「乙」。乃得「乙」。是謂「翻倍」之術也。`|`function double(a){var b = a * 2; return b;}`|
|`施「翻倍」於「大衍」。`|`double(dayan);`|
|`吾有一術。名之曰「甲」。欲行是術。必先得一數曰「乙」。二言。曰「丙」。曰「丁」`|`function a(float b, string c, string d)`|
|`夫「甲」。夫「乙」。夫「丙」。取二以施「丁」。取二以施「戊」。名之曰「己」。` | `var f = e(a,d(b,c))`|
|`夫「甲」。夫「乙」。夫「丙」。取二以施「丁」。取二以施「戊」。取一以施「己」。夫「庚」。夫「辛」。取三以施「壬」。名之曰「癸」。` | `var j = i(f(e(a,d(b,c))),g,h)`|
| `乃得四十九` | `return 49;` |
| `減五十以一。乃得矣` | `return 50-1;` |
| `乃歸空無` | `return;` |


#### 导入

| wenyan | JavaScript |
|---|---|
|`吾嘗觀「「算經」」之書。方悟「正弦」「餘弦」之義。` | `var {sin,cos} = require("math");` |
|`吾嘗觀「「某樓」」中「「某閣」」中「「某書」」之書。`|`require('path/to/something')` |


#### 输出

| wenyan | JavaScript |
|---|---|
|`吾有一數。曰五。書之。`|`console.log(5);`|

#### 注释

| wenyan | JavaScript |
|---|---|
|`批曰。「「文氣淋灕。字句切實」」。` | `/*文氣淋灕。字句切實*/` |
|`注曰。「「文言備矣」」。` | `/*文言備矣*/` |
|`疏曰。「「居第一之位故稱初。以其陽爻故稱九」」。` | `/*居第一之位故稱初。以其陽爻故稱九*/` |

## 标准库
吾嘗觀「...」之書。方悟「...」「...」之義。

#### [列經](../lib/列經.wy)

| Wenyan | Javascript Equivalent |
|---|---|

#### [易經](../lib/易經.wy)

| Wenyan | Javascript Equivalent |
|---|---|

#### [曆法](../lib/曆法.wy)

| Wenyan | Javascript Equivalent |
|---|---|
| [`今何紀元時`](../lib/曆法.wy#L9) | `Date.now() / 1000` |
| [`言今之日時`](../lib/曆法.wy#L14) | `new Date().toString(), in Chinese calendar` |
| [`言今之年月日`](../lib/曆法.wy#L19) | `new Date().toDateString(), in Chinese calendar` |
| [`言今之時刻`](../lib/曆法.wy#L24) | `new Date().toTimeString(), in Chinese calendar` |
| [`今年何年號`](../lib/曆法.wy#L29) | `"西元" for modern dates` |
| [`今年何年`](../lib/曆法.wy#L34) | `new Date().getFullYear() for modern dates, in Chinese calendar` |
| [`今年何干支`](../lib/曆法.wy#L40) | `Get index (1 to 60) of this year in the 60-year cycle` |
| [`今年積何年`](../lib/曆法.wy#L46) | `new Date().getFullYear() + 2697, in Chinese calendar` |
| [`今月何月`](../lib/曆法.wy#L53) | `new Date().getMonth() + 1, N + 0.5 for leap months, in Chinese calendar` |
| [`今月積何月`](../lib/曆法.wy#L60) | `Get continuously counting month number of this month` |
| [`今日何日`](../lib/曆法.wy#L67) | `new Date().getDate(), in Chinese calendar` |
| [`今日何干支`](../lib/曆法.wy#L74) | `Get index (1 to 60) of today in the 60-day cycle` |
| [`今日積何日`](../lib/曆法.wy#L80) | `Get continuously counting day number of today` |
| [`今時何時`](../lib/曆法.wy#L87) | `Get index (1 to 12) of current time in the 12 divisions of day` |
| [`今時何小時`](../lib/曆法.wy#L94) | `new Date().getHours()` |
| [`今刻何刻`](../lib/曆法.wy#L101) | `Math.floor(new Date().getMinutes() / 15)` |
| [`今分何分`](../lib/曆法.wy#L108) | `new Date().getMinutes() % 15` |
| [`今秒何秒`](../lib/曆法.wy#L113) | `new Date().getSeconds()` |
| [`言彼之日時`](../lib/曆法.wy#L232) | `new Date(x * 1000).toString(), in Chinese calendar` |
| [`言彼之年月日`](../lib/曆法.wy#L241) | `new Date(x * 1000).toDateString(), in Chinese calendar` |
| [`言彼之時刻`](../lib/曆法.wy#L248) | `new Date(x * 1000).toTimeString(), in Chinese calendar` |
| [`彼年何年號`](../lib/曆法.wy#L255) | `"西元" for modern dates` |
| [`彼年何年`](../lib/曆法.wy#L260) | `new Date(x * 1000).getFullYear() for modern dates, in Chinese calendar` |
| [`彼年何干支`](../lib/曆法.wy#L265) | `Get index (1 to 60) in the 60-year cycle` |
| [`彼年積何年`](../lib/曆法.wy#L271) | `new Date(x * 1000).getFullYear() + 2697, in Chinese calendar` |
| [`彼月何月`](../lib/曆法.wy#L278) | `new Date(x * 1000).getMonth() + 1, N + 0.5 for leap months, in Chinese calendar` |
| [`彼月積何月`](../lib/曆法.wy#L289) | `Get continuously counting month number` |
| [`彼日何日`](../lib/曆法.wy#L294) | `new Date(x * 1000).getDate(), in Chinese calendar` |
| [`彼日何干支`](../lib/曆法.wy#L300) | `Get index (1 to 60) in the 60-day cycle` |
| [`彼日積何日`](../lib/曆法.wy#L306) | `Get continuously counting day number` |
| [`彼時何時`](../lib/曆法.wy#L313) | `Get index (1 to 12) in the 12 divisions of day` |
| [`彼時何小時`](../lib/曆法.wy#L322) | `new Date(x * 1000).getHours()` |
| [`彼刻何刻`](../lib/曆法.wy#L330) | `Math.floor(new Date(x * 1000).getMinutes() / 15)` |
| [`彼分何分`](../lib/曆法.wy#L338) | `new Date(x * 1000).getMinutes() % 15` |
| [`彼秒何秒`](../lib/曆法.wy#L346) | `new Date(x * 1000).getSeconds()` |

#### [曆表](../lib/曆表.wy)

| Wenyan | Javascript Equivalent |
|---|---|

#### [算經](../lib/算經.wy)

| Wenyan | Javascript Equivalent |
|---|---|
| [`圓周率`](../lib/算經.wy#L166) | `Math.PI` |
| [`倍圓周率`](../lib/算經.wy#L169) | `Math.PI * 2` |
| [`半圓周率`](../lib/算經.wy#L172) | `Math.PI / 2` |
| [`四分圓周率`](../lib/算經.wy#L175) | `Math.PI / 4` |
| [`自然常數`](../lib/算經.wy#L177) | `Math.E` |
| [`歐拉常數`](../lib/算經.wy#L179) | `0.5772156649015329` |
| [`黃金分割數`](../lib/算經.wy#L181) | `1.618033988749895` |
| [`二之平方根`](../lib/算經.wy#L183) | `Math.SQRT2` |
| [`二之對數`](../lib/算經.wy#L185) | `Math.LN2` |
| [`十之對數`](../lib/算經.wy#L187) | `Math.LN10` |
| [`不可算數乎`](../lib/算經.wy#L190) | `Number.isNaN` |
| [`浮點移位`](../lib/算經.wy#L392) | `x * Math.pow(2, y), y is integer` |
| [`析浮點數`](../lib/算經.wy#L428) | `N/A` |
| [`取底除`](../lib/算經.wy#L474) | `{ 商: Math.floor(x / y), 餘: x - y * quo }` |
| [`取整除`](../lib/算經.wy#L491) | `{ 商: Math.round(x / y), 餘: x - y * quo }` |
| [`正弦`](../lib/算經.wy#L565) | `Math.sin` |
| [`餘弦`](../lib/算經.wy#L593) | `Math.cos` |
| [`反正弦`](../lib/算經.wy#L621) | `Math.asin` |
| [`反餘弦`](../lib/算經.wy#L648) | `Math.acos` |
| [`正切`](../lib/算經.wy#L655) | `Math.tan` |
| [`反正切`](../lib/算經.wy#L693) | `Math.atan` |
| [`勾股求角`](../lib/算經.wy#L727) | `Math.atan2` |
| [`勾股求弦`](../lib/算經.wy#L745) | `Math.hypot` |
| [`對數`](../lib/算經.wy#L782) | `Math.log` |
| [`指數`](../lib/算經.wy#L825) | `Math.exp` |
| [`冪`](../lib/算經.wy#L861) | `Math.pow` |
| [`平方根`](../lib/算經.wy#L885) | `Math.sqrt` |
| [`絕對`](../lib/算經.wy#L946) | `Math.abs` |
| [`取頂`](../lib/算經.wy#L951) | `Math.ceil` |
| [`取底`](../lib/算經.wy#L956) | `Math.floor` |
| [`取整`](../lib/算經.wy#L971) | `Math.round, but rounded away from zero when the fractional part is exactly 0.5` |
| [`捨餘`](../lib/算經.wy#L985) | `Math.trunc` |
| [`正負`](../lib/算經.wy#L995) | `Math.sign` |

#### [籌經](../lib/籌經.wy)

| Wenyan | Javascript Equivalent |
|---|---|
| [`求和`](../lib/籌經.wy#L1) | `reduce((a,b)=>a+b)` |

#### [位經](../lib/js/位經.wy)

| Wenyan | Javascript Equivalent |
|---|---|

#### [畫譜](../lib/js/畫譜.wy)

| Wenyan | Javascript Equivalent |
|---|---|

#### [西曆法](../lib/js/西曆法.wy)

| Wenyan | Javascript Equivalent |
|---|---|

## 可思摩斯
吾嘗觀「可思摩斯」之書。方悟「...」「...」之義。
#### 场景
| wenyan | JavaScript |paramsLength|
| ---- | ---- | ---- |
|保存場景狀態| save() | 0|
|恢復場景狀態| restore() | 0|
|設置底圖| setBackground(imgUrl) | 1|
|設置底色| setColor(color) | 1|
|書寫| text(txt,dx,dy,size) | 4|
|移動場景| translate(DSTX ,DSTY ) | 2|
|轉動場景| rotate(angle) | 1|
#### 精灵
| wenyan | JavaScript |paramsLength|
| ---- | ---- | ---- |
|創建圖片精靈| createSprite(imgUrl) | 1|
|創建精靈| createSprite(srcX,srcY,width,height) | 4|
|繪製精靈| render(sprite) | 1|
|克隆精靈| cloneSprite(sprite) | 1|
|銷毀精靈| destroy(sprite) | 1|
|按住按鈕| btn(['up'\|'down'\|'left'\|'right'\|'a'\|'b']) | 1|
|鬆開按鈕| btnp(['up'\|'down'\|'left'\|'right'\|'a'\|'b']) | 1|
|檢測精靈觸碰| touchSprite(sprite,['up'\|'down\|'pressed']) | 2|
|移動到| s => x => y => { s.DSTY = y;s.DSTX = x; } | 3|
|垂直移動| x => y => x.DSTY += y | 2|
|水平移動| x => y => x.DSTX += y | 2|
|檢測精靈碰撞| `x => y => ${collisionLogic}`| 2|
|檢測精靈邊緣碰撞| `x => ${borderCollisionDetect}`| 1|
|獲得屬性| x => y => x\[y\] |2|
|改變屬性| x => y => z => x[y] = z |3|
|實行方法| x => y => x\[y\]() |2|
#### 几何
| wenyan | JavaScript |paramsLength|
| ---- | ---- | ---- |
|描邊筆| border(width, color) | 2|
|填充筆| fill([true\|false], color) | 2|
|繪弧| arc(DSTX,DSTY,radius,startAngle,endAngle) | 5|
|繪直線| line(DSTX0,DSTY0,DSTX1,DSTY1) | 4|
|繪圓| circ(DSTX,DSTY,radius) | 3|
|繪方| rect(DSTX,DSTY,width,height) | 4|
|繪三角| triangle(DSTX0,DSTY0,DSTX1,DSTY1,DSTX2,DSTY2) | 6|
|繪橢圓| ellipse(x, y, radiusX, radiusY) | 4|
#### 点、向量
| wenyan | JavaScript |paramsLength|
| ---- | ---- | ---- |
|創建點| plot(DSTX,DSTY) | 2|
|點繞點旋轉| x => y => z => x.rotatedAround(y\| z) |3|
|點到點距離| x => y => x.distance(y) | 2|
|創建二維向量| vec2(DSTX,DSTY) | 2|
|二維向量| vec2(DSTX,DSTY) | 2|
|二維向量长度| x => x.length() | 0|
|二維向量之和| x => y => x.add(y) | 2|
|二維向量之別| x => y => x.min(y) | 2|
|二維向量之积| x => y => x.mul(y) | 2|
|二維向量之夾角| x => y => x.angleBetween(y) * 180 / Math.PI | 2|
|二維向量旋轉| x => y => x.rotated(y * Math.PI / 180) 2 |2|

