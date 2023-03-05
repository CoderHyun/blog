# 正则表达式大全

**正则表达式可视化网站**
https://www.wolai.com/coderhyun/nyqpThwsA9W4WVCiEVb7ar#wrQn5SKE7fB2XZyB3w1xVY

## ☎️号码相关

- 手机号（以 1 开头）：`/^(?:(?:+|00)86)?1\d{10}$/`
- 手机号（以 13 至19 开头）：`/^(?:(?:+|00)86)?1[3-9]\d{9}$/`
- 手机号（以工信部公布的手机号段开头）：`/^(?:(?:+|00)86)?1(?:(?:3[\d])|(?:4[5-79])|(?:5[0-35-9])|(?:6[5-7])|(?:7[0-8])|(?:8[\d])|(?:9[189]))\d{8}$/`
- 国内固话号码：`/\d{3}-\d{8}|\d{4}-\d{7}/`
- 邮箱号：`/^\w+([-+.]\w+)*@\w+([-.]\w+)*.\w+([-.]\w+)*$/`
- 邮政编码：`/[1-9]\d{5}(?!\d)/`
- 身份证号：`/^[1-9]\d{5}(?:18|19|20)\d{2}(?:0[1-9]|10|11|12)(?:0[1-9]|[1-2]\d|30|31)\d{3}[\dXx]$/`
- 银行卡号（公、私账户）：`/^[1-9]\d{9,29}$/`
- 车牌号：`/^[京津沪渝冀豫云辽黑湘皖鲁新苏浙赣鄂桂甘晋蒙陕吉闽贵粤青藏川宁琼使领][A-HJ-NP-Z][A-HJ-NP-Z0-9]{4,5}[A-HJ-NP-Z0-9挂学警港澳]$/`
- QQ 号：`/^[1-9][0-9]{4,10}$/`
- 微信号：`/^[a-zA-Z][-_a-zA-Z0-9]{5,19}$/`
- 版本号（ x.y.z ）：`/^\d+(?:.\d+){2}$/`
- 合法账号1（字母开头，5-16位，允许字母数字下划线）：`/^[a-zA-Z][a-zA-Z0-9_]{4,15}$/`
- 合法账号2（4-16位，允许字母，数字，下划线，减号）：`/^[a-zA-Z0-9_-]{4,16}$/`
- 强密码1（必须包含大小写字母和数字的组合，不能使用特殊字符，长度在8-10之间）：`/^(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,10}$/`
- 强密码2（必须包含字母、数字、特殊字符：**@#$%^& *`~()-+=** ）：

    `/^(?![a-zA-Z]+$)(?![A-Z0-9]+$)(?![A-Z\W_!@#$%^&* ~()-+=]+$)(?![a-z0-9]+$)(?![a-z\W_!@#$%^& *~()-+=]+$)(?![0-9\W_!@#$%^&* ~()-+=]+$)[a-zA-Z0-9\W_!@#$%^&*~()-+=]/`
- 网址：`/^(((ht|f)tps?):\/\/)?(^!@#$%^&*?.\s-?.)+[a-z]{2,6}\/?/`
- 网址带端口号：`/^((ht|f)tps?:\/\/)?[\w-]+(.[\w-]+)+:\d{1,5}\/?$/`
- ip-v4：`/\b(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\b/`
- ip-v6：`/(([0-9a-fA-F]{1,4}:){7,7}[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,7}:|([0-9a-fA-F]{1,4}:){1,6}:[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,5}(:[0-9a-fA-F]{1,4}){1,2}|([0-9a-fA-F]{1,4}:){1,4}(:[0-9a-fA-F]{1,4}){1,3}|([0-9a-fA-F]{1,4}:){1,3}(:[0-9a-fA-F]{1,4}){1,4}|([0-9a-fA-F]{1,4}:){1,2}(:[0-9a-fA-F]{1,4}){1,5}|[0-9a-fA-F]{1,4}:((:[0-9a-fA-F]{1,4}){1,6})|:((:[0-9a-fA-F]{1,4}){1,7}|:)|fe80:(:[0-9a-fA-F]{0,4}){0,4}%[0-9a-zA-Z]{1,}|::(ffff(:0{1,4}){0,1}:){0,1}((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])|([0-9a-fA-F]{1,4}:){1,4}:((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9]))/`

## 🔢**数字相关**

- 只有数字：`/^[0-9]*$/` 或 `/^\d{1,}$/`
- 整数：`/^-?[0-9]\d*$/`
- 正整数：`/^+?[1-9]\d*$/`
- 非正整数：`/^-[1-9]\d*|0$/`
- 负整数：`/^-[1-9]\d*$/`
- 非负整数：`/^\d+$/`
- 浮点数：`/^(-?\d+)(.\d+)?$/`
- 正浮点数：`/^[1-9]\d*.\d*|0.\d*[1-9]\d*$/`
- 负浮点数：`/^-([1-9]\d*.\d*|0.\d*[1-9]\d*)/`
- 小数：`/^-?\d+.\d+$/`
- 正数/负数/小数：`/^(-|+)?\d+(.\d+)?$/`
- 正实数保留小数点后 2 位：`/^[0-9]+(.[0-9]{2})?$/`
- 正实数保留小数点后 1 到 3 位：`/^[0-9]+(.[0-9]{1,3})?$/`
- n 位数字：`/^\d{n}$/`
- 至少 n 位数字：`/^\d{n,}$/`
- m 至 n 位的数字：`/^\d{m,n}$/`
- 数字和字母至少包含其一：`/^[A-Za-z0-9]+$/`
- 必须包含数字和字母：`/^(?=.*[a-zA-Z])(?=.*\d).+$/`
- md5 值 ：`/^([a-f\d]{32}|[A-F\d]{32})$/`
- base64 值：`/^\s*data:(?:[a-z]+\/[a-z0-9-+.]+(?:;[a-z-]+=[a-z0-9-]+)?)?(?:;base64)?,([a-z0-9!$&',()*+;=-._~:@/?%\s]*?)\s*$/i`

## 🔣字符相关

- m 至 n 位的字符：`/^.{3,20}$/`
- 英文字母字符：`/^[A-Za-z]+$/`
- 大写英文字母字符：`/^[A-Z]+$/`
- 小写英文字母字符：`/^[a-z]+$/`
- 汉字：`/^[\u4e00-\u9fa5]{0,}$/`
- 全角符号：`/[\uFF00-\uFFFF]/`
- 半角符号：`/[\u0000-\u00FF]/`
- 汉字、英文、数字、下划线至少其一：`/^[\u4E00-\u9FA5A-Za-z0-9_]+$/`
- 不包含字符 “~” ：`/[^~\x22]+/`
- 字符连续重复：`/(.)\1+/`

## ⌚时间相关

- 24小时制时间（HH:mm:ss）：`/^(?:[01]\d|2[0-3]):[0-5]\d:[0-5]\d$/`
- 12小时制时间（hh:mm:ss）：`/^(?:1[0-2]|0?[1-9]):[0-5]\d:[0-5]\d$/`
- 24小时制时间（HHmmss）：`/([0-1]?[0-9]|2[0-3])([0-5][0-9])([0-5][0-9])$/`
- 日期1（yyyy-MM-dd，如 2222-01-01，年份必为4位）：`/^\d{4}-\d{1,2}-\d{1,2}/`
- 日期2（如 333-01-01，年份可小于4位）：`/^\d{1,4}(-)(1[0-2]|0?[1-9])\1(0?[1-9]|[1-2]\d|30|31)$/`
- 日期3（yyyyMMdd，如 20220202）：`/^((([0-9]{3}[1-9]|[0-9]{2}[1-9][0-9]{1}|[0-9]{1}[1-9][0-9]{2}|[1-9][0-9]{3})(((0[13578]|1[02])(0[1-9]|[12][0-9]|3[01]))|((0[469]|11)(0[1-9]|[12][0-9]|30))|(02(0[1-9]|[1][0-9]|2[0-8]))))|((([0-9]{2})(0[48]|[2468][048]|[13579][26])|((0[48]|[2468][048]|[3579][26])00))0229))$/`
- 日期+时间1（YYYYMMDD HH:mm:ss）：`/^\d{4}([/:-\S])(1[0-2]|0?[1-9])\1(0?[1-9]|[1-2]\d|30|31) (?:[01]\d|2[0-3]):[0-5]\d:[0-5]\d$/`
- 日期+时间2： `/^[1-9]\d{3}-(0[1-9]|1[0-2])-(0[1-9]|[1-2][0-9]|3[0-1])\s+(20|21|22|23|[0-1]\d):[0-5]\d:[0-5]\d$/`
- 一年 12 个月（(01～09 或 1～12)）：`/^(0?[1-9]|1[0-2])$/`
- 一个月 31 天（01～09 或 1～31）：`/^((0?[1-9])|((1|2)[0-9])|30|31)$/`
- 有 31 天的月份：`/^(0?[13578]|1[02])$/`
- 有 30 天月的份：`/(0[469]|11)-(0[1-9]|[12][0-9]|30)/`
- 2 月 28 天（"02-28"）：`/^02-(0[1-9]|[1][0-9]|2[0-8])$/`
- 闰年：`/^(((19|20)([13579][26]|[2468][048]|0[48]))|(2000))$/`
- 闰年 2 月（比如 2008-02-01）：`/^(((19|20)([13579][26]|[2468][048]|0[48]))|(2000))-0?2-(0?[1-9]|[12]\d)$/`
- 日期（包括闰年、大小月的判断）：`/((((19|20)\d{2})-(0?(1|[3-9])|1[012])-(0?[1-9]|[12]\d|30))|(((19|20)\d{2})-(0?[13578]|1[02])-31)|(((19|20)\d{2})-0?2-(0?[1-9]|1\d|2[0-8]))|((((19|20)([13579][26]|[2468][048]|0[48]))|(2000))-0?2-29))$/`
- 年份区间-年（比如 19 年至 20 年）：`/^((19|20)\d{2})$/`
- 年份区间-年月（比如 1999-01）：`/^((((19|20)\d{2})-(0?[13-9]|1[012]))|(((19|20)\d{2})-(0?[13578]|1[02]))|(((19|20)\d{2})-0?2)|((((19|20)([13579][26]|[2468][048]|0[48]))|(2000))-0?2))$/`
- 年份区间-年月日（比如 1999-01-01）：`/^((((19|20)\d{2})-(0?[13-9]|1[012])-(0?[1-9]|[12]\d|30))|(((19|20)\d{2})-(0?[13578]|1[02])-31)|(((19|20)\d{2})-0?2-(0?[1-9]|1\d|2[0-8]))|((((19|20)([13579][26]|[2468][048]|0[48]))|(2000))-0?2-29))$/.test('2021-02-21')$/`
- 年份区间-年月日（间隔符号可为 - / 或空）：`/^(?:(?:1[6-9]|[2-9][0-9])[0-9]{2}([-/.]?)(?:(?:0?[1-9]|1[0-2])\1(?:0?[1-9]|1[0-9]|2[0-8])|(?:0?[13-9]|1[0-2])\1(?:29|30)|(?:0?[13578]|1[02])\1(?:31))|(?:(?:1[6-9]|[2-9][0-9])(?:0[48]|[2468][048]|[13579][26])|(?:16|[2468][048]|[3579][26])00)([-/.]?)0?2\2(?:29))$/`

## 💻编程相关

- 16进制颜色：`/^#?([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$/`
- 提取网页颜色代码：`/^#([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})$/`
- 视频链接地址：`/^https?:\/\/(.+\/)+.+(.(swf|avi|flv|mpg|rm|mov|wav|asf|3gp|mkv|rmvb|mp4))$/i`
- 图片链接地址：`/^https?:\/\/(.+\/)+.+(.(gif|png|jpg|jpeg|webp|svg|psd|bmp|tif))$/i`
- mac 地址：`/^((([a-f0-9]{2}:){5})|(([a-f0-9]{2}-){5}))[a-f0-9]{2}$/i`
- 子网掩码：`/^((?:(?:25[0-5]|2[0-4]\d|[01]?\d?\d)\.){3}(?:25[0-5]|2[0-4]\d|[01]?\d?\d))$/`
- 文件扩展名效验：`/^([a-zA-Z]\:|\\)\\([^\\]+\\)*[^\/:*?"<>|]+\.txt(l)?$/`
- java包名（x.x.x）：`/^([a-zA-Z_]\w*)+([.][a-zA-Z_]\w*)+$/`
- xml文件：`/^([a-zA-Z]+-?)+[a-zA-Z0-9]+\.[x|X][m|M][l|L]$/`
- html 注释：`/<!--[\s\S]*?-->/g`
- html 标签1：`/<(\w+)[^>]*>(.*?<\/\1>)?/`
- html 标签2：`/<(\S*?)[^>]*>.*?</\1>|<.*? />/`
- 首尾空白字符：`/^\s*|\s*$/`
- 查找CSS属性:`/^\s*[a-zA-Z\-]+\s*[:]{1}\s[a-zA-Z0-9\s.#]+[;]{1}/`
- 提取页面超链接:`/(<a\s*(?!.*\brel=)[^>]*)(href="https?:\/\/)((?!(?:(?:www\.)?'.implode('|(?:www\.)?', $follow_list).'))[^" rel="external nofollow" ]+)"((?!.*\brel=)[^>]*)(?:[^>]*)>/`
- 提取网页图片：`/\< *[img][^\\>]*[src] *= *[\"\']{0,1}([^\"\'\ >]*)/`
- 迅雷链接：`/^thunder:\/\/[a-zA-Z0-9]+=$/`
- ed2k链接：`/^ed2k:\/\/|file|.+|\/$/`
- linux"文件"路径：`/^\/(\w+\/)+\w+.\w+$/`
- window下"文件"路径：`/^[a-zA-Z]:\(?:\w+\)*\w+.\w+$/`

## 🍕生活相关

- 金额（宽松，可为负、首位可为0，支持千分位分隔）：`/^-?\d+(,\d{3})*(.\d{1,2})?$/`
- 金额（大于 0 ，两位小数）：`/(^[1-9]{1}[0-9]*$)|(^[0-9]*.[0-9]{2}$)/`
- 金额（严格，不为负、小数点后最多两位，首位不为0）：`/(^[1-9]([0-9]+)?(.[0-9]{1,2})?$)|(^(0){1}$)|(^[0-9].[0-9]([0-9])?$)/`
- 护照：`/(^[EeKkGgDdSsPpHh]\d{8}$)|(^(([Ee][a-fA-F])|([DdSsPp][Ee])|([Kk][Jj])|([Mm][Aa])|(1[45]))\d{7}$)/`
- 香港身份证：`/^[a-zA-Z]\d{6}\([\dA]\)$/`
- 澳门身份证：`/^[1|5|7]\d{6}\(\d\)$/`
- 湾湾身份证：`/^[a-zA-Z][0-9]{9}$/`
- 股票代码：`/^(s[hz]|S[HZ])(000[\d]{3}|002[\d]{3}|300[\d]{3}|600[\d]{3}|60[\d]{4})$/`
- 不含 abc 的单词：`/\b((?!abc)\w)+\b/`

## 实际使用

### 千分位格式化

在项目中经常碰到关于货币金额的页面显示，为了让金额的显示更为人性化与规范化，需要加入货币格式化策略。也就是所谓的数字千分位格式化。

1. `123456789` => `123,456,789`
2. `123456789.123` => `123,456,789.123`

想想如果不是用正则，还可以用什么更优雅的方法实现它？

```JavaScript
const formatMoney = (money) => {

  return money.replace(new RegExp(`(?!^)(?=(\d{3})+${money.includes('.') ? '\.' : '$'})`, 'g'), ',')  

}

formatMoney('123456789') // '123,456,789'

formatMoney('123456789.123') // '123,456,789.123'

formatMoney('123') // '123'
```

### 解析链接参数

你一定常常遇到这样的需求，要拿到 url 的参数的值，像这样：

```JavaScript
// url [https://qianlongo.github.io/vue-demos/dist/index.html?name=fatfish&age=100#/home](https://qianlongo.github.io/vue-demos/dist/index.html?name=fatfish&age=100#/home)

const name = getQueryByName('name') // fatfish

const age = getQueryByName('age') // 100
```

通过正则，简单就能实现 getQueryByName 函数：

```JavaScript
const getQueryByName = (name) => {

  const queryNameRegex = new RegExp(`[?&]${name}=([^&]*)(&|$)`)

  const queryNameMatch = window.location.search.match(queryNameRegex)

  // Generally, it will be decoded by decodeURIComponent

  return queryNameMatch ? decodeURIComponent(queryNameMatch[1]) : ''

}

const name = getQueryByName('name')

const age = getQueryByName('age')

console.log(name, age) // fatfish, 100
```

### 驼峰字符串

JS 变量最佳是驼峰风格的写法，怎样将类似以下的其它声明风格写法转化为驼峰写法？
  1. foo Bar => fooBar
  2. foo-bar---- => fooBar
  3. foo_bar__ => fooBar

  复制代码

正则表达式分分钟教做人：

```JavaScript
const camelCase = (string) => {

  const camelCaseRegex = /[-_\s]+(.)?/g

  return string.replace(camelCaseRegex, (match, char) => {

    return char ? char.toUpperCase() : ''

  })

}

console.log(camelCase('foo Bar')) // fooBar

console.log(camelCase('foo-bar--')) // fooBar

console.log(camelCase('foo_bar__')) // fooBar
```

### 小写转大写

这个需求常见，无需多言，用就完事儿啦：

```JavaScript
const capitalize = (string) => {

  const capitalizeRegex = /(?:^|\s+)\w/g

  return string.toLowerCase().replace(capitalizeRegex, (match) => match.toUpperCase())

}

console.log(capitalize('hello world')) // Hello World

console.log(capitalize('hello WORLD')) // Hello World
```

### 实现 **trim()**

trim() 方法用于删除字符串的头尾空白符，用正则可以模拟实现 trim：

```JavaScript
const trim1 = (str) => {

  return str.replace(/^\s*|\s*$/g, '') // 或者 str.replace(/^\s*(.*?)\s*$/g, '$1')

}

const string = '   hello medium   '

const noSpaceString = 'hello medium'

const trimString = trim1(string)

console.log(string)

console.log(trimString, trimString === noSpaceString) // hello medium true

console.log(string)
```

trim() 方法不会改变原始字符串，同样，自定义实现的 trim1 也不会改变原始字符串；

### HTML 转义

防止 XSS 攻击的方法之一是进行 HTML 转义，符号对应的转义字符：

正则处理如下：

```JavaScript
const escape = (string) => {

  const escapeMaps = {

    '&': 'amp',

    '<': 'lt',

    '>': 'gt',

    '"': 'quot',

    "'": '#39'

  }

  // The effect here is the same as that of /[&amp;<> "']/g

  const escapeRegexp = new RegExp(`[${Object.keys(escapeMaps).join('')}]`, 'g')

  return string.replace(escapeRegexp, (match) => `&${escapeMaps[match]};`)

}

console.log(escape(`

  <div>

    <p>hello world</p>

  </div>

`))

/*

&lt;div&gt;

  &lt;p&gt;hello world&lt;/p&gt;

&lt;/div&gt;

*/
```

### HTML 反转义

有了正向的转义，就有反向的逆转义，操作如下：

```JavaScript
const unescape = (string) => {

  const unescapeMaps = {

    'amp': '&',

    'lt': '<',

    'gt': '>',

    'quot': '"',

    '#39': "'"

  }

  const unescapeRegexp = /&([^;]+);/g

  return string.replace(unescapeRegexp, (match, unescapeKey) => {

    return unescapeMaps[ unescapeKey ] || match

  })

}

console.log(unescape(`

  &lt;div&gt;

    &lt;p&gt;hello world&lt;/p&gt;

  &lt;/div&gt;

`))

/*

<div>

  <p>hello world</p>

</div>

*/
```

### 校验 24 小时制

处理时间，经常要用到正则，比如常见的：校验时间格式是否是合法的 24 小时制：

```JavaScript
const check24TimeRegexp = /^(?:(?:0?|1)\d|2[0-3]):(?:0?|[1-5])\d$/

console.log(check24TimeRegexp.test('01:14')) // true

console.log(check24TimeRegexp.test('23:59')) // true

console.log(check24TimeRegexp.test('23:60')) // false

console.log(check24TimeRegexp.test('1:14')) // true

console.log(check24TimeRegexp.test('1:1')) // true
```

### 校验日期格式

常见的日期格式有：yyyy-mm-dd, yyyy.mm.dd, yyyy/mm/dd 这 3 种，如果有符号乱用的情况，比如2021.08/22，这样就不是合法的日期格式，我们可以通过正则来校验判断：

```JavaScript
const checkDateRegexp = /^\d{4}([-.\/])(?:0[1-9]|1[0-2])\1(?:0[1-9]|[12]\d|3[01])$/

console.log(checkDateRegexp.test('2021-08-22')) // true

console.log(checkDateRegexp.test('2021/08/22')) // true

console.log(checkDateRegexp.test('2021.08.22')) // true

console.log(checkDateRegexp.test('2021.08/22')) // false

console.log(checkDateRegexp.test('2021/08-22')) // false
```

### 匹配颜色值

在字符串内匹配出 16 进制的颜色值：

```JavaScript
const matchColorRegex = /#(?:[\da-fA-F]{6}|[\da-fA-F]{3})/g

const colorString = '#12f3a1 #ffBabd #FFF #123 #586'

console.log(colorString.match(matchColorRegex))

// [ '#12f3a1', '#ffBabd', '#FFF', '#123', '#586' ]
```

### 判断 **HTTPS/HTTP**

这个需求也是很常见的，判断请求协议是否是 **HTTPS/HTTP**

```JavaScript
const checkProtocol = /^https?:/

console.log(checkProtocol.test('[https://medium.com/](https://medium.com/)')) // true

console.log(checkProtocol.test('[http://medium.com/](http://medium.com/)')) // true

console.log(checkProtocol.test('[//medium.com/](//medium.com/)')) // false
```

### 校验版本号

版本号必须采用 x.y.z 格式，其中 XYZ 至少为一位，我们可以用正则来校验：

```JavaScript
// x.y.z

const versionRegexp = /^(?:\d+.){2}\d+$/

console.log(versionRegexp.test('1.1.1'))

console.log(versionRegexp.test('1.000.1'))

console.log(versionRegexp.test('1.000.1.1'))
```

### 获取网页 img 地址

这个需求可能爬虫用的比较多，用正则获取当前网页所有图片的地址。在控制台打印试试，太好用了~~

```JavaScript
const matchImgs = (sHtml) => {

  const imgUrlRegex = /<img[^>]+src="((?:https?:)?\/\/[^"]+)"[^>]*?>/gi

  let matchImgUrls = []

  sHtml.replace(imgUrlRegex, (match, $1) => {

    $1 && matchImgUrls.push($1)

  })

  return matchImgUrls

}

console.log(matchImgs(document.body.innerHTML))
```

### 格式化电话号码

这个需求也是常见的一匹，用就完事了：

```JavaScript
let mobile = '18379836654' let mobileReg = /(?=(\d{4})+$)/g 

console.log(mobile.replace(mobileReg, '-')) // 183-7983-6654
```
