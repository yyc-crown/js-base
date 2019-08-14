# CSS

### 00-字体 **渐变色**的设置

``` css
.content {
    background-image: -webkit-linear-gradient(left,#f346ba,#b909f0);
    -webkit-background-clip:text;
    -webkit-text-fill-color: transparent;
}
```







### 01-输入框样式的修改



```css
input {

  //先清除输入框的默认样式
  border: 0;
  outline: none;
  appearance: none;
  -webkit-appearance:none;
  
  //修改输入框样式
  height: 66px;
  color: #fd832d;
  border: 1px solid #fd832d;
  border-radius: 35px;
  background-color: #ffffff;
}
```



### 03-强制文字在一行显示，并且有省略号

``` css
         //第一步
         white-space: nowrap;
         //第二步
         overflow: hidden;
         //第三步
         text-overflow: ellipsis;
```





> 
>
> 
>
> 
>
> 
>
# JS-基础-一
>
 ### 00-js-数据-5种简单值类型
>
> ```js
>   // 交互
>   // 
>   // var a = 1;
> 
>   // 字符串：单双引号；
>   // var b = "1";
> 
> 
>   // console.log("今天班长真好看！");
> 
> 
>   // 我说："今天班长真好看！"
>   // console.log("我说："今天班长真好看"");
>   // 单双引号：单引号包着双引号
>   // console.log('我说："今天班长真好看"');
> 
>   // 用双引号包着单引号；
>   // console.log("我说：'今天班长真好看'");
> 
> 
>   // 转译字符： 加上\ 读取为JS可以认识的字符
>   // console.log("我说：\"今天班长\'真\\好看！\"");
> 
>   // 数字类型
>   // var a = NaN;
> 
>   // // 单双引号（英文）：字符串；
>   // var b = "NaN";
> 
>   // 3.布尔类型
>   // console.log(true,false);
> 
>   // 计算优先：比较运算，赋值；（比较优先于赋值）
>   // 比较运算之后，返回一个布尔；
>   // var a = 4>=4;
>   // console.log(a);
> 
> 
>   // 4.null值；复杂类型；Object;
>   // 
>   // var a = null;
> 
> 
>   // 5.声明变量的时候，没有赋值。JS默认给一个值 undefined
>   var a;
>   // undefined 我也不知道要给你什么；
>   // console.log(a);
> ```
>
> 
>
> 
>
 ### 01-js-数据-检查类型
>
> - 语法：
>
> ```js
>   typeof 数据
>   typeof(数据);
> 
> 
> // 1.数字类型
>   // var a = 1;
>   // console.log(a, typeof a);
>   // console.log(NaN, typeof NaN);
> 
>   // 2.字符类型
>   // var b = "NaN";
>   // console.log(b, typeof b);
> 
> 
>   // 3.布尔类型：true false
>   // var c = true;
>   // console.log(c, typeof c);
> 
> 
>   // 4.null值，不是简单类型
>   // var d = null;
>   // console.log(d, typeof d);
> 
>   // 5.undefined类型：值也是undefined
>   // var e;
>   // console.log(e, typeof e);
> ```
>
 ### 02-js-转化-转数字
>
> ```js
>  // 其他 变 数字
> 
>   // 1.字符串类型
>   // var a = "abc";
>   // console.log(a, Number(a));
> 
> 
>   // 2.布尔
>   // var a = true;
> 
>   // 布尔类型：true false; 1 0;
>   // console.log(a, Number(a));
> 
> 
> 
>   // 3.null值；空；转为0；
>   // var a = null;
>   // console.log(a, Number(a));
> 
>   // 4.undefined 我也不知道给你啥值。
>   // var a;
>   // console.log(a, Number(a));
> 
> 
>   // --------------------------------------------------------------------
>   // parseInt(); 
>   // 目标：转为整数
>   // 接受：只能接受字符串；
> 
> 
>   // 1.字符类型:里面的数字的字符，只能写在前面
>   // var a = '10.1abc';
>   // console.log(a, parseInt(a));
> 
>   // var a = 'a10.1';
>   // console.log(a, parseInt(a));
> 
> 
>   // 2.布尔类型
>   // var a = true;
>   // console.log(a, parseInt(a));
> 
> 
>   // ----------------------------------------------------------------------
>   // parseFloat()
>   // 目标：转为小数
>   // 接受：只能接受字符串,要转成功：必须字符串里的数字写在前面；
> 
>   // var a = '10.1abc';
>   // console.log(a, parseFloat(a));
> 
> 
>   // var a = 'a10.1';
>   // console.log(a, parseFloat(a));
> ```
>
> 
>
 ### 03-js-转化-转字符串
>
> - 特点：肯定也是能转成功，效果就是数据两边加单(双)引号；
>
> ```js
>   // String()
>   // 其他：数字类型、布尔类型、null（值）、undefined（值undefined）
> 
>   // 1.数字
>   // var a = 123;
>   // console.log(a, String(a));
> 
>   // var a = NaN;
>   // console.log(a, String(a));
> 
> 
>   // 2.布尔类型 true false
>   // var a = true;
>   // console.log(a, String(a));
> 
> 
>   // 3. null undefined
> 
> 
>   // --------------------------------------------------------------------
>   // .toString()
>   // 1.数字类型
>   // var a = 123;
>   // console.log(a, a.toString());
> 
> 
>   // 2.null undefined不能用这个方法；
>   var a = null;
>   console.log(a, a.toString());
> ```
>
> 
>
> 
>
> 
>
> 
>
 ### 04-js-转化-转Boolean
>
> - 特点 ：肯定能出来布尔值。
>
> ```js
>   //  转 Boolean 结果：存在 不存在 返回就是一个布尔值；
>   // 逻辑：只要是确认的，存在的数据，都是ture;
> 
>   // 其他类型：字符类型、数字类型、null(值)、undefined(类型、值)
>   // 1.字符类型：
>   // var res = "abc";
>   // 转化之前，转化之后，查看转化后的类型
>   // console.log(res, Boolean(res), typeof Boolean(res));
> 
>   // 2.数字类型
>   // var res = 10.1;
>   // console.log(res, Boolean(res));
> 
>   // true 1 false 0;
>   // var res = 0;
>   // console.log(res, Boolean(res));
> 
>   // var res = NaN;
>   // console.log(res, Boolean(res));
> 
>   // 3.null:空
>   // var res = null;
>   // console.log(res, Boolean(res));
> 
> 
>   // 4.undefined
>   // var res = undefined;
>   // console.log(res, Boolean(res));
> 
>   // ------------------------------------------------
>   // 6中情况转false 
>   // var res = "";
>   // console.log(res, Boolean(res));
> 
>   // var res = 0;
>   // console.log(res, Boolean(res));
> 
>   // var res = NaN;
>   // console.log(res, Boolean(res));
> 
>   // var res = null;
>   // console.log(res, Boolean(res));
> 
> 
>   // var res = undefined;
>   // console.log(res, Boolean(res));
> 
>   // var res = false;
>   // console.log(res, Boolean(res));
> ```
>
> 
>
 ### 05-js-转化-小结
>
> - 转数字：
>   - Number()：
>   - parseInt()、parseFloat()
>     - 数字
>     - NaN
> - 转字符串：
>   - String（）:相当于给你要转的这个数据左右两边加单双引号；
>   - .toString():null undefined 不能用；
> - 转布尔值：
>   - Boolean（）：给你一个布尔值
>   - 转false6种情况
>     - 空字符串：“”
>     - 0、NaN
>     - null、undefined
>
 ### 06-js-操作符-算术操作符
>
> 算术：常规：要数字类型
>
> 不常规：
>
>  字符串遇见+：左右临近的类型都会转换为字符串；
>  字符串遇见- / * %：参与运算，我们要的数据类型，字符串隐式转换为数字类型
>
 ### 07-js-操作符-比较运算符
>
> ```js
>   // 比较运算符：> < >= <=
> 
> 
>   // 常规操作：比数字类型
>   // 返回:这个比较后的结果状态 Boolean；
> 
>   // 比较操作符 优先级高于 赋值操作符
>   // var a = 4 >= 4;
>   // console.log(a);
> 
>   // var a = 3 > 4;
>   // console.log(a);
> 
>   // 非常规：
>   // 比较运算符：两边都是需要数字类型；
>   // 不是数字类型， 隐式转化 为 数字类型；
> 
> 
>   // 1.字符串
>   // var a = "abc" > 1;
>   // 比较运算符：需要数字类型；
>   // 不是数字类型，隐式转化为数字类型；
>   // NaN > 1;
>   // console.log(a);
> 
> 
>   // 2.Boolean
>   // var a = true > 0;
>   // 比较运算符：需要数字类型；
>   // 不是数字类型，隐式转化为数字类型；
>   // 1 > 0
>   // console.log(a);
> 
> 
>   // 3.null
>   // var a = null > 6;
>   //
>   // console.log(a);
> 
> 
> 
>   //---------------------------------------------------------
> 
>   // ==:比较运算符，优先级高于 赋值运算符；
>   // 先看类型:
>   // 1.若类型相同，比值；
>   // 2.若类型不同，隐式转化 数字类型
> 
>   // var a = 1 == 1;
>   // console.log(a);
> 
>   // console.log("1" == 1);
> 
>   // console.log("abc" == "abc");
>   // console.log(false == false);
> 
>   // NaN:泛指，不是某个数；
>   // console.log(NaN == NaN);
> 
> 
>   // ===：直接比类型，
>   // 先看类型:
>   // 1.如果类型相同，比值；
>   // 2.如果类型不同，直接false;
>   console.log("1" == 1);
>   console.log("1" === 1);
> 
> 
>   // != !==：和上面是同理，只不过是判断数据的值不等；
> ```
>
 ### 08-js-操作符-优先级
>
> - 大致的优先级：
>   - 括号先算
>   - 其次算算术：++a优先;
>   - 再次算比较  > ==
>   - 然后算逻辑 && ||
>   - 最后算赋值 =
>
 ### 09-总结
>
> - JS：交互；
> - 变量：var a = 数据；
>   - 根据业务场景设置变量名。推荐驼峰；
> - 数据类型：
>   - 字符串类型、数字类型、布尔类型、null(值)、undefined类型（值）
>   - 查看数据类型：typeof  数据；typeof(数据)，返回数据类型
> - 需要数据转化：
>   - Number():
>     - 数字
>     - NaN：不是某个数；
>   - String()：给你的数据两边加一个单双引号；
>   - .toString()：null /undefined不能用这个方法；
>   - Boolean():返回布尔值；存在或者不存在；
> - 操作符：
>   - 运算：
>     - 常规：数字类型；
>     - 非常规：
>       - 字符串
>         - 字符串遇见+：把它临近数据类型转字符串类型，形成拼接；
>         - 字符串遇见其他（- * / %）：隐式转化为数字类型；
>       - 其他类型：布尔值、null(值)、undefined
>   - 比较：
>     - 常规：需要两边都是数字类型；
>     - 非常规：转化为数字类型，进行比较；
>   - 逻辑：
>     - 需要什么类型进行判断？布尔类型，若不是，要隐式转化为布尔类型
>     - 返回：成立或者不成立条件判断上的位置的数据返回;   null&&1------>null
>   - 赋值：配合运算操作符，简写；
>   - 优先级：
>     - 括号先算
>     - 其次算算术：++a优先;
>     - 再次算比较  > ==
>     - 然后算逻辑 && ||
>     - 最后算赋值 =
>
> 
>
> -


# JS-基础-二
### 01-分支结构 

- **if结构**：单个if结构，解决的一个分支的判断问题；

  ```js
  if(true) {
     // 当 条件表达式 的结果是 true 时 执行的代码
  }
  
  ```

  

- **if-else**：解决两个分支的判断问题

  ```js
  if(条件表达式){
     //当条件表达式的结果是 true 时执行的代码
  }else {
    //当条件表达式的结果是 false 时执行的代码
  }
  ```

  

- switch-case结构：主要用于多个**固定值**之间的判断，只能做固定值的判断

  ```
  switch （数据）{
    case 固定值1: 
      // 当 数据 === 固定值1 时执行的代码; 先看类型，看值；
      
      // 表示当前 情况结束；
      break;
          
    case 固定值2: 
      // 当数据 === 固定值2时执行的代码;
      break;
          
    case 固定值3: 
      // 当数据 === 固定值3时执行的代码;
      break;
    // 中间还可以写多个判断
    
    
    default : 
      // 当数据和上面的所有固定值都不相等的时候执行的代码
      break;
  }
  //注意：这个结构里面的break并不是必须的，如果两个 case 之间没有break ，执行完了一个break 之后，会继续执行下面的case的代码；但是一般情况都是带着break的；
  
  
  ```

  



### 02-三元表达式

- 表达式：**有值会返回；

- 语法：if else 的简写；有返回值；

  ```js
  // 表达式1 ? 表达式2 : 表达式3;
  
  // 首先 要知道 表达式 会返回结果；
  // 先执行表达式1，判断其结果是true还是false，
  // 如果是true，则执行表达式2，然后将 表达式2的执行结果 作为整个三元表达式的结果，
  // 如果是false，则执行表达式3，并 表达式3的结果 作为整个三元表达式的结果
  ```

  





### 03-循环结构



#### 03-1-while循环

- 语法：

  ```js
  // 条件表达式结果返回布尔值；true;
  while (条件表达式){
    // 循环体  就是重复执行的代码
  }
  ```

  

#### 03-2-for循环！！！

##### 语法

```js
for(初始化表达式; 条件表达式; 自增表达式){
  // 循环体
}
//执行过程：
1. 执行初始化表达式(只执行一次)**
2. **执行条件表达式**
3. 如果条件表达式的结果为false, 结束循环；
4. 如果条件表达式的结果为true，执行循环体
5. **执行自增表达式**
6. 重复2~5的步骤，直到条件表达式的结果为false，结束循环
```







#### 03-3-do-while循环(补充)

```js
do {
  //循环体
}while(条件表达式)
```

- 执行过程：

  ​	。先执行循环体

  ​        。执行条件表达式

  - 如果条件表达式结果为false，结束循环
  - 如果条件表达式结果为true，执行循环体
  - 重复2~4的步骤，直到条件表达式结果为false，结束循环

### 04-小结

- while、do-while 循环不易看出循环的次数，一般用于**未知次数的循环**
- for循环明显看出循环的次数，一般用于已知次数的循环；**使用最多是for；**
- while、for循环可能一次循环都不会执行
- do-while 循环至少执行一次；


# JS-基础-三
### 00-数组的构造函数

- 数组在JS中还可以使用另一种方式创建，这个方式我们称为 ： 构造函数

```js
// 使用 构造函数 创建数组
var arr = new Array();
// 存储数据
arr[0] = 10;
arr[1] = 20;
console.log(arr);

var arr = new Array(10,20);
console.log(arr);
```

var arr = new Array(10);

console.log(arr); // 输出 [empty × 10]

- 注意：一个数据，不要使用这个方式存储数据；它会认为你想要设置数组的长度，而不是要把数据存储在数组中。





### 02-总结

- 能够通过断点调试一段代码；
- 能够说出数组的作用：先后顺序，有长度的数据集合；为了更好的管理数据；
- 能够使用字面量的方式创建数组

```
var arr = []
```

- 能够通过索引获取或设置数组中的数据

```
var arr = [];
arr[0] = 10;
console.log(arr[0])
```

- 能够通过for循环遍历数组中的数据并打印

```
// for循环遍历数组：index;
```

- 能够说出实现求一组数字中最大值的思路
  - 随机指定一个元素为最大；arr[0]
  - 那 你指定的这个元素和所有的元素作对比
- 能够说出Math对象的3个方法 

```js
Math.random()  0-1，不包括1；
Math.floor();  向下取整；
Math.ceil();   向上取整；
```

- 能够说出Date对象的3个方法

```
日期  getDate();
星期几  getDay();
```

- 清空数组中的元素

```
arr.length = 0;
```

- 知道通过构造函数Array创建数组

```js
var arr = new Array();
```
# JS-基础-四
### 01-函数

- 函数：我们**把一段相对独立的具有特定功能的代码块封装起来**，形成一个**独立实体**，起个名字（函数名），在后续开发中可以**随时反复调用**。
- 作用：**封装（包起来）一段代码，将来可以随时拿来使用。**
- **封装：功能要单一**

> - 语法：
>
> ```js
> // 声明函数：
> // function :关键字 
> // tell_story：函数名
> function tell_story(param) {
> // 函数体；
> console.log("山上有庙");
> console.log("庙有和尚");
> console.log("和尚说事");
> console.log("老和尚对小和尚：");
> }
> 
> // 调用执行：函数名后面跟着一个(),表示会执行前面声明好的函数；
> tell_story();
> ```
>
> 
>
### 02-函数-参数-配置
>
> - 语法：把你要抽象的数据配置为参数，记得要放入声明函数时，后面的（）
>
> ```js
> // 函数声明，配置两个参数：
> function tell_story(name_1, name_2) {
> // 函数体；
> console.log("山上有庙");
> console.log("庙有和尚");
> console.log(name_1 + "说事");
> console.log(name_1 + "对" + name_2 + "说：");
> }
> 
> 
> 
> // 调用函数
> tell_story("铁头", "熊大");
> 
> 
> // 如何去配置参数：
> // 根据你的业务需求，把一些你要抽象的数据，配置为参数。
> // 记得：在函数的()内，写上你配置的变量名；
> // 在声明函数的，内部的变量才算是声明了。
> ```
>
> 
>
 ### 03-函数-参数-不赋值
>
> - 语法
>
> ```js
> // 函数声明，配置两个参数：
> function tell_story(name_1, name_2) {
> // 函数更严谨的写法；
> // 判断一下name_1, name_2是否为undefined;
> // if (name_1 == undefined) {
> //   name_1 = "大哥";
> // }
> 
> // 配置对参数的默认值；
> // if (name_2 == undefined) {
> //   name_2 = "二哥";
> // }
> 
> // 三元表达式；
> // 表达式1?表达式2:表达式3;
> // name_1 = name_1 == undefined ? "大哥" : name_1;
> name_1 = name_1 ? name_1 : "大哥";
> 
> // name_1没有传值 undefined
> // undefined ？name_1："大哥";
> // false ？name_1："大哥";
> 
> // name_1 传入值 "张三"
> // "张三" ？name_1："大哥";
> // true?name_1："大哥";
> 
> // 严谨写法：三元表达式；
> name_2 = name_2 ? name_2 : "二哥";
> 
> 
> // 函数体；
> console.log("山上有庙");
> console.log("庙有" + name_1 + "," + name_2);
> console.log(name_1 + "说事");
> console.log(name_1 + "对" + name_2 + "说：");
> }
> ```
>
> 
>
 ### 04-函数-参数-形参与实参
>
> - 形参：形式上先参与函数内部逻辑的一些参数，没有调用时，不知道要传入什么；
> - 实参：真实传入数据，可以直接传数据，也可以传入外面已经定义好的变量；
> - 形参与实参：要传入的数据是**简单数据类型**数据，形参与实参相互不影响；
>
> ```js
> // 声明函数，没有执行；
> function demo(x, y) {
> x = x + y;
> console.log(x, y);
> }
> 
> // 调用时，函数执行
> var a = 10;
> var b = 20;
> 
> // a/b 背后代表的值传入了！！！
> demo(a, b);
> 
> // a，b 把值传入，传入后，和a,b没有任何关系；
> console.log(a, b);
> ```
>
> 
>
 ### 05-函数-返回值
>
> - 语法：
>
> ```js
> // 定义函数：参数，可以在内部参与运算
> // function qiu_he(x, y) {
> //   var sum = x + y;
> //   // console.log(sum);
> 
> //   // return:作用1：返回值，必须后面跟一个值；即将要作为函数执行完后，返回的值；
> //   return sum;
> // }
> 
> // 调用函数：传入实参
> // 想要获取到结果 
> // var sum = qiu_he(12, 12);
> // // 默认返回是undefined；
> // console.log(sum, '外面的函数返回值');
> 
> 
> // 作用2：终止函数的执行
> function demo() {
> console.log("1111111111111");
> console.log("2222222222222");
> // 终止函数的执行,函数内部下面的代码不执行了
> return;
> console.log("3333333333333");
> }
> var res = demo();
> // 看下：return后面没有值的时候，返回的是啥？
> console.log(res); // 返回undefined
> ```
>
> 
>
### 06-函数-案例-求n-m和
>
> - 语法：
>
> ```js
> // n-m数字的和;
> // 注意：
> // 比如：n>m
> // 比如：
> // 封装函数：
> function get_sum_2(n, m) {
> // 
> 
> // 内部定义的变量
> var sum = 0;
> for (var index = n; index <= m; index++) {
> sum += index;
> }
> // console.log(sum);
> return sum;
> }
> 
> // 会接受到函数的返回值；
> var res = get_sum_2(5, 6);
> console.log(res);
> ```
>
> 
>
> 
>
 ### 07-函数-参数-arguments
>
>- 语法：可以获取所有传入函数的实参，形成一个伪数组；本质是个对象，可以循环遍历；
>
>```JS
>function fn() {
>// arguments:函数内部的变量，
>// 不需要我们声明的；
>// console.log(arguments);
>
>// 伪数组：但是可以循环遍历的。
>for (var index = 0; index < arguments.length; index++) {
>console.log(arguments[index]);
>}
>}
>```
>
>
>
### 08-函数-函数表达式-匿名函数
>
> - 匿名函数：JS内不允许匿名函数单独存在；
>
> ```js
> // 函数表达式:声明函数的另外一种方式
> // get_sum：变量名；
> // 变量：储存的是函数，变量名就是以后的函数名；
> // var get_sum = function(a, b) {
> //   return a + b;
> // };
> 
> // 返回结果
> // var res = get_sum(1, 2);
> // console.log(res);
> 
> 
> // 匿名函数；JS不允许匿名函数单独出现，需要配合其他语法进行使用；
> //
> // function() {}  
> 
> 
> // 自执行函数：页面打开自己就执行；
> // function fn() {}
> // fn();
> (function() {
> // 
> console.log(1);
> 
> })();
> ```
>
> 
>
### 09-函数-函数类型-回调函数
>
> - 语法：
>
> ```js
> // 变量背后代表的是一个函数；
> // var fn = function() {
> //   console.log(1);
> // };
> 
> // 函数类型；返回function类型
> // console.log(typeof fn);
> 
> 
> // 回调函数：
> function demo_1(a, fn) {
> a = a + 1;
> 
> // 形参:需要传入一个函数；
> fn();
> }
> 
> // 声明个函数；
> var demo_2 = function() {
> console.log(1);
> }
> 
> // 当我们实参是有函数，传入，这个函数叫回调函数；
> demo_1(10, demo_2);
> 
> // 参数有函数传入，这个就叫回调函数；
> demo_1(20, function() {
> console.log("我是匿名函数，作为参数进行传入");
> })
> ```
>
> 
>
 ### 10-js-作用域
>
> - 全局作用域：
>
> ```JS
> // 全局作用域
> // 全局变量：在你声明的这个作用域内，任何地方都可以访问；
> // var a = 10;
> 
> // function demo() {
> //   console.log(a);
> // }
> 
> // demo();
> ```
>
> - 局部作用域：
>
> ```js
> // 局部作用域：声明的函数内部的范围；
> // function demo() {
> //   // 局部变量：只能在你的局部作用域访问；
> //   var b = 20;
> // }
> 
> // // 外面访问不到局部作用域内的变量；
> // console.log(b);
> ```
>
> 
>
 ### 11-js-预解析
>
> - 预解析，也叫变量提升：会把声明的变量和函数提升到你当前的作用域的最顶端；
> - 注意：你当前的作用域的是在哪？
>   - 是全局作用局
>   - 还是局部左右域；
> - 基础面试题：
>
> ```js
> // 观察下面的代码，说出执行结果
> var num = 10;
> fun();
> 
> function fun() {
> console.log(num);
> var num = 20;
> }
> 
> 
> // ------------------------------------------------------------变量提升的演示
> // 预解析：先把你声明变量、函数先全部提升到你当前的作用域的最顶端；
> var num;
> 
> function fun() {
> var num;
> console.log(num);
> num = 20;
> }
> 
> // 赋值；
> num = 10;
> // 函数调用；
> fun(); // 输出 undefined；
> ```
>
> 
>
 ### 13-总结
>
> - 参数：
>   - 形参：形式上参与函数内部逻辑的那个参数
>   - 实参：实际参与的运算的数据；
> - 返回值：设置return 数据；
> - arguments：
>   - 函数内部变量
>   - 获取所有传入的实参；
>   - 伪数组：可以遍历；
> - 作用域与预解析：把我们的声明的变量和声明的函数提升到  **当前作用域顶部**；
> - 当前作用域：局部作用域还是全局作用域；
>
> ```js
> function fn(){}
> 
> // 提升的只是 var fn；
> var fn = function(){}
> 
> ```
>
 ### git
>
> 
>
> ## 介绍
>
> - version
>
> - git：**做版本管理的；**
> - 版本管理：写代码，不是一次性把所有功能模块写完善的，或者写完的，代码和功能都是一点一点迭代出来，就是形成不同的版本；
> - 特点：
>   - **代码安全**：git这个工具，可以将我们写好的代码，备份到网络上面（比如：github），将来如果想要恢复，可以直接恢复；
>   - **团队开发**：在现在公司里面，绝大多数情况都是团队开发，如果没有一个可以协同的软件，人工进行代码的合并、管理是非常吃力的；
>   - **责任明确**：版本管理工具，是可以管理到出问题的代码是谁合并到一起的。
>   - **代码回滚**：之前有一个版本，是没有问题的，现在为了加新的功能，影响了原来的版本，就可以先把当前的版本进行撤销，恢复到上一个版本先进行使用。
> - **什么时候用？大家只要做个不小的项目，都要初始化一个git。**
>
> ## 安装
>
> - 官网下载对应电脑的版本：[git下载页面](https://www.git-scm.com/download/)
>
> - 就会得到一个安装文件,直接双击安装，无脑下一步安装即可。
>
> ## 配置
>
> - 配置个人信息：**用于追责用**；在任务位置右键，选择 `Git Bash Here`
>
> - 黑色的窗口，在窗口内输入：
>
> ```cmd
> git config --global user.email "你自己的邮箱"
> git config --global user.name "你自己的名字"
> 
> ```
>
> - 查看配置：
>
> ```
> git config --list
> 
> ```
>
> ## 使用
>
> - 其实，使用git这个黑色窗口使用命令行管理自己的代码是可以的，我们以后会学习，目前我们还是学习界面化操作；
> - 在vscode中，我们可以找到这个图标
> - 点击这个图标，就可以进行源代码管理，需要选择个我们要管理代码的目录初始化：

>
> - 初始化之后，会在当前要管理的文件夹下面有.git文件夹；之后当你的代码发生变量，都会在里面有提示；这个文件就是用于管理我们多个版本的文件夹；
>

> - 此时如果我们想保存一下当前这个版本的代码
>

> - 必须输入备注信息，标识该次提交的简单的备注；
>
> ## 查看

> - 上面只是对每次的修改做一次提交，每次提交就算是一个版本；
> - VSC下载**gitLens插件**查看每次提交的版本记录
>
> - 多次提交版本，只能看到与上次版本的对比，如果当前最新版本有问题，我们删除了当前版本的部分代码即可；
# JS-基础-五
### 对象

#### 00-介绍

- 核心概念：**万物皆对象**，我们在编程中，使用对象来描述万事万物。
- 对象：使用`属性`描述事物的`特征`，使用`方法`来描述`行为`， 就是对象这种语法。
- 对象**就是属性和方法的集合**；
- 对象描述扳手：
  - 属性(特征)：金属、银白色
  - 方法：能拧螺丝、防身等；

#### 01-语法

#### 02-创建

- 构造函数：

```javascript
var obj = new Object(); // 这是一个没有属性和方法的对象
console.log(obj);
```

- 字面量：

```javascript
var obj = {}; // 这也是一个没有属性和方法对象，其本质和构造函数创建的对象是一样的
console.log(obj,typeof obj);
```

#### 03-添加

- 如： 使用对象描述一个叫`狗蛋`的人，先字面量声明一个对象，再给对象上属性和方法赋值；

```javascript
var obj = {};


// 对象.属性 = 值;
obj.name = '狗蛋';// 名字是一个人的特征

// 对象.方法名 = function(){}
// 注意：该方法后面的的赋值为一个函数，函数在什么时候执行？调用的时候才会执行；
obj.sayName = function(){  // 人会说出自己的名字，也就是人有自己的行为
	console.log('你好，我叫' + obj.name);
}
```

- 通过字面量初始化对象时，初始化属性

```js
// 描述一个学生
var student = {
  name : '狗蛋',
  age : 12,
  gender : '男',
  sayName : function(){
    console.log(student.name);
  }
}
// 
```

- 一个属性和一个值叫**键值对**。多个键值之间使用逗号分隔，键的方式添加属性：

```js
// 对象[属性名]  属性名必须是String类型，里面可以写字符串；
var obj = {};
obj['name'] = '狗蛋';
obj['sayName'] = function(){
  console.log('你好，我叫' + obj['name']);
}
```



#### 04-获取

- 点属性访问

```javascript
// 得到对象的名字,属性可以当成变量使用
console.log(obj.name);
// 调用对象的方法，方法的本质是函数
obj.sayName();
```

- 以键的方式访问属性

```js
console.log(obj['name']);
obj['sayName']();
```



#### 04-遍历

- 数组可以遍历；对象也可以遍历；

```javascript
// key 就是obj这个对象中的每个键，obj就是要遍历的对象。
for(var key in obj){
}

var obj = {
  name : '狗蛋',
  age : 12,
  gender : '男'
};
for(var key in obj){
  console.log(key);
  // 只能通过键的方式获取值
  console.log(obj[key]);
}
```
# JS-基础-六
## 00-Math的用法
### 语法总结

| 方法                                                         | 用法                                                         |
| :----------------------------------------------------------- | ------------------------------------------------------------ |
| Math.random(x)；这个方法的作用是生成一个 [0,1) 之间的随机浮点数 | console.log(Math.random());//[0,1)                           |
| Math.floor(x)   把一个浮点数进行向下取整                     | console.log(Math.floor(3.1));//3                             |
| Math.round(x)  把一个浮点数进行四舍五入取整                  | console.log(Math.round(3.9));//4                             |
| Math.ceil(x)  把一个浮点数进行向上取整                       | console.log(Math.ceil(3.9));  // 4                           |
| Math.abs(x)  求一个数的绝对值 正数                           | console.log(Math.abs(3));  // 3                              |
| Math.max(x,y...)  求多个数字中的最大值，同理 Math.min(x,y...); | console.log(Math.max(10,20));//20  console.log(Math.min(10,20));  // 10 |
### 案例：刷新页面，页面中有盒子可以随机变颜色

```
    // 随机变颜色
    // 颜色：rgb（120,120,110）；
    // 0-255范围，需要求一个0-255随机整数
    // 先封装一个随机数的函数
    // 再封装一个由随机数构成的颜色函数；
    function get_color() {
        var res = Math.random() * 256;
        res = Math.floor(res);
        return res;
    }

    // var res=Math.random()*256;
    // res=Math.floor(res);

    function div_color() {
        return `rgb(${ get_color()},${ get_color()},${ get_color()})`;
    }
    // var color = `rgb(${ get_color()},${ get_color()},${ get_color()})`;
    // console.log(color);
    // 字符串拼接，     `rgb（120,120,110）`

    // document.write()页面显示
    document.write(`<div style='background:${div_color()}'></div>`);
    document.write(`<div style='background:${div_color()}'></div>`);
    document.write(`<div style='background:${div_color()}'></div>`);

```

## 01-Date的用法

### 语法

```js
var date = new Date(); // 得到的是当前时间的日期对象
console.log(date.getFullYear());// 年份
console.log(date.getMonth()); // 月份，从0开始

// 当前日 为什么不是getDay() 英语：日期date，day某天；
console.log(date.getDate()); 

console.log(date.getHours()); // 小时，0-23
console.log(date.getMinutes()); // 分钟 ， 0-59
console.log(date.getSeconds()); // 秒数 ， 0-59
console.log(date.getMilliseconds()); // 毫秒 0-999 ， 1秒 = 1000毫秒
```

### 时间戳

```js
//获取从1970年1月1日到现在的总毫秒数，**常说的时间戳
var date = new Date();

console.log(date.valueOf());
console.log(date.getTime());
console.log(1*date);

console.log(Date.now());
```

## 02-Array

### 02-01-对元素的操作

| 方法                                      | 举例                                                         | 返回值           |
| ----------------------------------------- | ------------------------------------------------------------ | ---------------- |
| arr.push 从数组后面推入一个元素或多个元素 | *var res = arr.push('abc', 'drf');             console.log(arr, res);* | 修改后数组的长度 |
| arr.pop删除数组最后一个元素               | *var res = arr.pop();*  console.log(res, arr);               | 返回被删除的元素 |
| arr.shift将数组的第一个元素移除           | var res = arr.shift(); console.log(arr, res);                | 返回被删除的元素 |
| arr.unshift 从数组前面添加一个或多个元素  | *var res = arr.unshift('abc');*console.log(arr, res);        | 返回新数组的长度 |

### 02-02-splice的用法

| 方法                | 作用                                               | 返回值               |
| ------------------- | -------------------------------------------------- | -------------------- |
| arr.splice(3,1);    | 从索引3开始，总共移除1个元素                       | 返回被移除数据的数组 |
| arr.splice(3,0,7,8) | 从索引3开始，移除0个元素，在索引3后插入7,8两个元素 | 返回一个空数组       |
| arr.splice(1,1,2)   | 从索引1开始，替换1个数据，用2进行替换（包含索引1） | 被替换数据的数组     |

### 02-03-查找元素(两种方法)

- indexOf：根据元素查找索引，如果这个元素在数组中，返回索引，否则返回-1，找元素在不在数组内部

  ```js
  var arr = [10,20,30]
  console.log(arr.indexOf(30));  // 2
  console.log(arr.indexOf(40));  // -1
  ```

  

- findIndex方法(需要回调函数)用于查找满足条件的第一个元素的索引，如果没有，则返回-1

```js
var arr = [10, 20, 30];
var res1 = arr.findIndex(function (item) {
  return item >= 20;
});
// 返回 满足条件的第一个元素的的索引
console.log(res1);  


var res2 = arr.findIndex(function (item) {
  return item >= 50;
});
// -1
console.log(res2);
```

### 02-04-遍历数组

#### 三种方法

- 方法一：for循环

- *方法二：forEach：需要一个回调函数，需要3个形参*

  ```js
  var arr = [1, 2, 4, 6, 5, 7, 9];
      // arr.forEach(function(item, index, arr) {
      //     console.log(item, index);
  
      // })
  ```

  

- *方法三：filter筛选数组中需要的数组*

  ```js
  
  	//item是数组中的每个元素，index是item对应的索引,arr代表当前的数组    
      // var res = arr.filter(function(item, index, arr) {
      // return 后面需要写条件表达式，需要Boolean值
      //当为false时不返回item值；
      //     return 0;
  
      // });
      // console.log(res);
      var arr = [0, 2, 4, 6, 5, 7, 9];
      var res = arr.filter(function(item, index, arr) {
          return 1;
  
      });
      console.log(res);
  ```

  

#### 案例：筛选出一个数组中索引为偶数的元素(两种方法)

```js
var arr = [1, 3, 5, 2, 4, 9, 6];
    // 需求：筛选索引为偶数的数据
    // 方法一：for循环
    var new_arr = [];
    for (var index = 0; index < arr.length; index++) {

        if (index % 2 == 0) {
            // 修改数组的长度arr.push()
            new_arr.push(arr[index]);
        }

    }
    console.log(new_arr);

    // 方法二：filter方法：
    // var res = arr.filter(function(item, index, arr) {

    //     return index % 2 == 0;
    // });
    // console.log(res);
```



### 02-05-拼接与截取

- 拼接：.concat

  ```js
   // concat拼接默认拼接在原数组的最后索引的后面，之后组成一个新的数组，不改变原来的数组
      var arr_1 = arr.concat('abc');
      console.log(arr_1, arr);
  
      var arr_2 = arr.concat(88, 33);
      console.log(arr_2);
  
      var arr_3 = arr.concat([12, 24]);
      console.log(arr_3);
  ```

  

- 截取

  ```js
  slice两个参数
      // 第一个参数：截取的左下标；（包括）
      // 第二个参数：截取的右下标；(不包括)
      var arr_4 = arr.slice(2, 5);
      console.log(arr_4);
  
      // 第二个参数省略，默认为数字的长度；
      var arr_5 = arr.slice(2);
      console.log(arr_5);
  
      // 两个参数全部省略，第一个默认为0，第二个默认为length
      var arr_6 = arr.slice();
      console.log(arr_6);
  ```

  

### 02-06-数组的复制（5种方法）

- 定义一个数组  var arr = [12, 36, 24, 45, 67];

```js
// 方法一：for循环
    // 遍历一遍，然后定义一个新的数组，把遍历的值赋给新的数组
    var new_arr = [];
    for (var index = 0; index < arr.length; index++) {
        new_arr[index] = arr[index];
    }
    console.log(new_arr);
    
// 方法二：forEach : 变量
    // 先把数组遍历之后，取出数组中的各个元素，把取出的元素塞进新定义的数组中即可
    var new_arr_1 = [];
    arr.forEach(function(item, index) {
        new_arr_1.push(item);
    });
    console.log(new_arr_1);
 // 方法三：filter:数组过滤：满足条件返出来，返每个元素，返到新数组；
    var new_arr_2 = arr.filter(function(item, index) {
        return true;
    })
    console.log(new_arr_2);

 // 方法四：concat: 不对原数组操作，返回是一个新的数组；
    var new_arr_3 = arr.concat();
    console.log(new_arr_3);

// 方法五：slice :截取 不对原数组操作，返回是一个新的数组；
    var new_arr_4 = arr.slice();
    console.log(new_arr_4);
```

### 02-06-数组与字符串的转化

#### 数组转字符串

```js
// 不指定分隔符时默认“，”
    // 数组转字符串
    // 语法：arr.join
    // var arr = [1, 3, 4, 2, 7];
    // var str = arr.join(',');
    // console.log(str, typeof str);
```



#### 字符串转数组

```js
语法：str.split
    var str = `a-b-f-d`;
    var arr = str.split('-');
    console.log(arr, typeof arr);
```



### 02-07-数组的求和(两种方法)

```js
 var arr = [1, 3, 5, 3, 6];
    var sum = 0;
    // 方法一：for循环
    // for (var index = 0; index < arr.length; index++) {
    //     sum += arr[index];

    // }
    // console.log(sum);


    //方法二： filter的方法
    arr.filter(function(item, index) {
        sum += item;
    })
    console.log(sum);
```



### 02-08-循环和遍历的区别

- 循环就是无限的循环下去，而遍历则是一个个的到最后一个元素就结束了；

## 03-String

### 03-01-查找

- indexOf  字符串中是否存在指定字符 存在就返回找到的下标，没有就-1；

```
// 这个方法用于查找某个字符串是否包含于另一个字符串
var str = '我爱中华人民共和国';
console.log(str.indexOf('中华'));
```

- lastIndexOf  用法和indexOf一样，只不过是从后面开始找
- charAt：

```js
// 这个方法用于获取字符串中位于指定位置的字符
var str = '我爱中华人民共和国';
console.log(str.charAt(2));
```

- charCodeAt

```js
// 这个方法用于获取字符串中位于指定位置的字符的ASCII码
var str = 'abcdef'
console.log(str.charCodeAt(0));
```

### 03-02-拼接与截取

- 拼接

```js
var str = `abcdefghkfffdsxv`;
    // 拼接------------------------------------------
    // 方法一：+
    // 方法二：concat返回新的字符串
    var str_1 = str.concat('dd');
    console.log(str_1, str, typeof str_1);
```

- 截取

```javascript

//方法一:substring有两个参数，都为索引，左闭右开
    var str_2 = str.substring(3, 8);
    console.log(str_2);

// slice:与第一种方法的区别是————slice可以设置负参数，出现负参数时要和字符串的长度进行相加

// substr:第一个为下标，第二个截取的长度；
    var str_3 = str.substr(2, 4);
    console.log(str_3);
```

## 04-Object

### 对象的浅拷贝(复制)

```js
 var obj = {
        name: '张三',
        age: 16,
        sayHi: function() {
            console.log(1);

        }
    };
    // 先定义一个新的对象,再进行对象的遍历
    var new_obj = {};
    for (var key in obj) {
        new_obj[key] = obj[key];
    }
    console.log(new_obj);
```

## 05-String-split（案例）

```js
    // 需求：解析b.com?name="张三"&age=16，我们最终想要得到var obj={name："张三"，age：16}；
    // 1.首先接受到一个String类型的数据
    var str = `b.com?name="张三"&age=16`;
    // console.log(str, typeof str);
    
    // 2.将得到的字符串以指定的符号分割成数组，先？作为分隔符
    var arr_1 = str.split('?');
    // console.log(arr_1, typeof arr_1);
    
    // 3.得到的为 ["b.com", "name="张三"&age=16"]的数组，接下来我们需要找到这个数组的最后一个元素；
    var str_1 = arr_1[arr_1.length - 1];
    // console.log(str_1, typeof str_1);
    
    // 4.得到的为字符串  name="张三"&age=16，接下来需要将字符串分割转为数组，以&为分隔符；
    var str_2 = str_1.split('&');
    // console.log(str_2, typeof str_2);
    
    // 5.得到数组["name="张三"", "age=16"]，遍历数组
    var obj = {};
    str_2.forEach(function(item, index) {
        // console.log(item, index);
        // 6.循环体内部，进行每个数据的再次分割
        // 比如：name="张三"", "age=16"
        // 分割后得到数组为["name","张三"]
        var res = item.split("=");
        // console.log(res);
        //得到两个长度为2的数组， ["name", ""张三""]， ["age", "16"]
        // 数组的第一个位置为键key,第二个位置为值value;
        var key = res[0];
        var value = res[1];
        // 给对象的属性赋值
        obj[key] = value;
    })
    console.log(obj);
```





# WebAPI-DOM

## 01-JS-组成

- js组成：

  * ES:前六天基础知识
  * DOM：文档对象模型，树状结构当做对象模型
    - DOM节点：HTML 标签（标签属性、标签内的文本）；

  * BOM：浏览器当做一个对象

## 02-获取元素对象（DOM节点）

### 02-01-通过方法获取

- 小括号里面：放入字符串；

| 方法                        | 语法                                                         |
| --------------------------- | ------------------------------------------------------------ |
| 通过id名                    | var search = document.getElementById('search');//返回的为单个DOM节点 |
| 通过标签名                  | var tagName = document.getElementsByTagName("input");//返回的为伪数组，可以遍历 |
| 通过类名                    | var ipt = document.getElementsByClassName('ipt');//返回的为伪数组，可以遍历 |
| 通过css选择器（单个选择器） | document.querySelector(css选择器);//返回的为单个DOM节点      |
| 通过css选择器（单个选择器） | document.querySelectorAll(css选择器1,css选择器2...);//返回的为一个伪数组，**这个伪数组可以用forEach循环遍历**。 |

### 02-02-通过属性获取

| 属性                                                         | 语法                          |
| ------------------------------------------------------------ | ----------------------------- |
| **获取子元素**：可以得到某个元素之下的所有的子元素的集合，一个伪数组 | 父元素.children();            |
| **获取父元素**：返回一个；                                   | 元素.parentNode();            |
| **获取兄弟元素**：得到下一个兄弟元素                         | 元素.nextElementSibling()     |
| **获取兄弟元素**：得到上一个兄弟元素                         | 元素.previousElementSibling() |
### 02-03-通过BOM方法获取DOM节点

- 语法：

  var res = window.getComputedStyle(元素对象，即DOM节点)；

  返回的为字符串；

  ```js
   // DOM.style.
    var box = document.querySelector(".box");
  
    // DOM节点 属性方式 只能获取行内样式；
    // console.log(box.style);
  
  
    // BOM:返回所有（无论是行内还是非行内）的样式集合，对象。
    var res = window.getComputedStyle(box);
    
    // 属性值：字符串； res.width res.fontSize
  ```

  

- **优点**：可以获得css的全部样式；

## 03-事件类型

- onclick：用于鼠标点击之后发生的响应。//必须先获取DOM节点，之后再进行注册事件

  ```js
  语法：
  DOM节点.onclick=function() {
      //函数体
      //用户点击之后才执行；
  }
  
  
  
  
  	//案例需求：一个按钮控制开关灯
      // 按开灯时：页面变白，按钮文字变为关灯
      //  按关灯时：页面变黑，按钮文字变为开灯
  
      // 获取DOM值
      var btn = document.getElementById("btn");
      var value;
      // 注册事件
      btn.onclick = function() {
          // 点击之后的效果
          value = btn.value;
          if (value == "开灯") {
              document.body.style.backgroundColor = "#fff";
              btn.value = "关灯";
          } else {
              document.body.style.backgroundColor = "#000";
              btn.value = "开灯";
          }
      }
  
  ```

- 下面的注册事件针对有光标的标签input textarea;

  

  * onbulr：无光标时，焦点消失

    ```js
    DOM节点名.onbulr=function() {
     //函数体
     //用户点击之后才执行；
    } 
    ```

    

    

    

  * onfocus：有光标时，获得焦点 

    ```js
    DOM节点名.onfocus=function() {
    //函数体
    //用户点击之后才执行；
    } 
    ```

- **鼠标的事件类型**

  | 鼠标事件类型                | 语法                |
  | --------------------------- | ------------------- |
  | mousedown：鼠标按下时触发   | DOM节点.onmousedown |
  | mousemove：鼠标移动时触发   | DOM节点.onmousemove |
  | mouseup：鼠标弹起的时候触发 | DOM节点.onmouseup   |
  | mouseover：鼠标移入时触发   | DOM节点.onmouseover |
  | mouseout：鼠标移出时触发    | DOM节点.onmouseout  |


- **键盘事件**

  | 键盘事件          | 语法              |
  | ----------------- | ----------------- |
  | 按键按下：keydown | DOM节点.onkeydown |
  | 按键弹起：keyup   | DOM节点.onkeyup   |


* **触摸事件**:推荐使用addEventListener的方式注册：有很多移动端的事件，都是后面h5或者c3才出现的，on的方式没有对应的属性

  | 触摸事件                                         |
  | ------------------------------------------------ |
  | touchstart - 会在手指触摸到屏幕的时候触发        |
  | touchmove - 会在手指触摸到屏幕，移动的过程中触发 |
  | touchend - 会在手指离开屏幕的瞬间触发            |

  - **事件对象属性：触摸点**

    ```js
    事件对象.touches - 屏上面的触摸点
    事件对象.targetouches - 元素上面的触摸点
    事件对象.changedTouches - 变化的触摸点
    ```

    

- 用于表单状态的改变事件：**onchange**

  - 触发满足的两个条件
    - 当前对象属性改变，并且是由键盘或鼠标事件激发的，脚本触发无效
    - 当前对象失去焦点
  - 可使用的元素：input，select，textarea

- **oninput**事件：只有当表单元素发生改变时调用，元素变化，立即触发方法

  - 可使用元素：

    ```js
    <input type="password">
    <input type="search">
    <input type="text">
    <textarea></textarea>
    ```

    

## 04-操作标准样式属性

- **标准属性**：标签中本身带的属性
  * 比如：img标签中的src、 input中的value属性、style属性
  * 这些属性都可以看做对象，后面可直接修改属性样式，用“ . ”的方式即可
  * 注意：**style属性只能获取行内样式，获取不到内嵌式和外链式对标签设置的样式**。

```js
//div为DOM节点名
// 获取：只能获取行内样式；
div.style.backgroundColor
// 设置
div.style.backgroundColor = ’#fff‘;
```

- **开关属性**：checked/selected/disabled ，这种只有两种状态的属性；

  * 赋值：两个状态的值，布尔类型；

  * 什么时候用？**当涉及到什么情况下执行某件事，什么情况下不执行时用**

  * 什么DOM节点时有这样的属性：<input type="checkbox" name="check" id="ck"  />

    ```js
    var ck = document.getElementById('ck');
    
    ck.checked = true;
    ck.checked = false;
    ```


## 05-操作类样式属性-className

- 类样式：DOM节点上的class属性；

- 操作类样式的效果：可以添加或修改我们已经写好的类名，方便的更换样式；

  ```js
  // 如果要修改类样式，只需要把className修改一下就行了；
  // 但是会直接覆盖
  box.className = '新的类名';
  
  // 解决：在原来的基础上进行添加类名
  box.className += '新的类名';
  ```

  

## 06-操作类样式对象-classList

- 对象：提供**多个方法**进行操作，操作更为简单；**比较好的方式解决上面的覆盖问题；**

- 操作什么：类名；

  ```js
   // 参数：多个类名，之间用逗号隔开
  //add：给元素对象添加一个或者多个类名，不会影响原来的类名；  
   
  box.classList.add(类名1,类名2...)；
                     
  // 参数：多个类名，可以是多个，多个之间用逗号隔开
  //remove： 给元素删除一个或者多个类名
  box.classList.remove(类名1,类名2...) 
                                       
   // 参数： 要切换的类名
   //toggle：切换类名，
  box.classList.toggle(类名)             
  
  
  ```

  

## 07-操作自定义属性

### 07-01-data-开头的自定义属性



- 如何获取自定义属性：

  * 自定义属性样式必须为：标签中：以**data-开头**

  * 获取时：DOM名.dataset

    ​              获取当个时：用下面的为力 input.data.src

    ```js
    命名: 在标签上已自定义属性 以 data-属性名
    <input type="button" value="美女1" data-src="./images/01.jpg" />
    ```

    

  * 返回的是对象，可以操作和修改样式

    

- this :事件执行函数：内部如何获取到DOM节点的自定义属性；可以通过标签，也可以通过this;

- 案例-切换不同图片

  ```js
  // 需求：不同的按钮，切换不同的图片
      // 获取所有DOM节点
      // 思路：先获取到所有的DOM节点，之后循环遍历；找到每个节点，对每个节点进行操作，操作的信息用自定义类名的方式提前存在DOM节点中
      var ipt = document.getElementsByClassName('ipt');
      var img = document.getElementById('img');
  
  
      // ipt为伪数组，可以循环遍历
      for (var i = 0; i < ipt.length; i++) {
          // 注册点击事件:点击不同的按钮，有不同的图片切换 
          ipt[i].onclick = function() {
              img.src = this.dataset.src;
          }
  
  
      }
  ```


### 07-02-自定义属性的灵活操作（推荐使用）

- 语法：自定义的属性名可以随便取

- 作用：根据属性名获取属性值

  ```js
      // 获取属性值
      // 获取自定义的属性值
      var id = document.getElementById('box');
      console.log(id.getAttribute('abc'));
      // 添加或修改属性名的值：需要两个参数
      // 添加
      id.setAttribute('ff', '你好');
      // 修改
      id.setAttribute('index', '你好');
  
      // 删除属性某个属性
      id.removeAttribute('index');
  ```

  

##  08-位置

### 08-01- 获取元素的实际宽度和高度



- 元素的实际宽高 = border+padding+content（width和height）

  ```js
  // 返回值：数值；
  
  // 只能进行获取；
  // 元素的实际宽度
  元素.offsetWidth 
  // 元素的实际高度
  元素.offsetHeight
  
  // 获取和设置
  dom.style.width；
  ```

  

### 08-02-获取元素对象 位置

- 元素对象的位置：获取到的是数值；

```js
// 得到的是某个元素距离他的offsetParent元素的水平距离
// 元素.offsetLeft = marginLeft + left
元素.offsetLeft 

// 得到的是某个元素距离他的offsetParent元素的垂直距离
// 元素.offsetTop = marginTop + top
元素.offsetTop 

// 找到一个有定位的父亲元素进行参考，如果亲生父亲没有定位，会一直往上找，直到找打有定位的父亲，或者body；
元素的offsetParent
```



## 09-全选和反选案例

```js
// 需求：全选和取消
    // 上面的盒子选中，子盒子选中
    // 上面的盒子取消，子盒子取消选中
    // 获取DOM节点
    var checkAll = document.getElementById('checkAll');
    var ck = document.getElementsByClassName('ck');


    checkAll.onclick = function() {
        // console.log(checkAll.checked);
        // 遍历子盒子
        for (let i = 0; i < ck.length; i++) {
            ck[i].checked = checkAll.checked;

        }

    }


    // 需求：反选
    // 下面的盒子都选中时，上面的盒子选中
    // 下面的盒子只要有一个没有选中，上面的盒子也就没有选中
    // 再遍历一遍子盒子
    for (var j = 0; j < ck.length; j++) {
        // 点击事件
        ck[j].onclick = function() {
            // 假设所有的子盒子都被选中，这时候需要设定一个变量区检验
            var flag = true;
            for (var k = 0; k < ck.length; k++) {
                //判断子盒子是否被选中
                if (ck[k].checked == false) {
                    flag = false;
                    break;
                }

            }

            // 循环结束后，判定flag的值
            if (flag == true) {
                checkAll.checked = true;
            } else {
                checkAll.checked = false;
            }
        }
    }
```

## 10-注册事件！！！

### 10-01-on事件名

- 本质相当于是把一个函数存储到 了 on 这个属性里面 ， 后面被重复赋值了，会覆盖；on的方式注册，
- 无法多次注册；团队协作时，有可能别人写的代码，会把你的覆盖了。

### 10-02-添加事件监听（推荐使用）

- 作用：addEventListener：添加事件监听，可以多次注册事件

- 语法：

  ```js
  DOM节点.addEventListener('事件类型'，function（) {
      
  });
  
  //语法：
  btn.addEventListener('click', function() {
          console.log(1);
  
   })；
  
  ```
## 11-事件对象！！！

### 11-01-事件对象

- 对象：属性和方法的集合；

- 属性：

  ```js
  // 鼠标位置
  
  // 可视区域坐标系 - 以浏览器的可视区域的左上角为原点的
  // 可视区域：就是元素用来显示内容的区域
  事件对象.clientX
  事件对象.clientY
  
  // 页面坐标系  -  以body的左上角作为原点
  事件对象.pageX
  事件对象.pageY
  
  
  // 事件的目标对象，点击谁用到谁上；
  事件对象.target
  
  // 事件的绑定对象，就是是绑定在哪个DOM节点上 和 this一样
  // 前面说的事件源
  e.currentTarget==this -----> true
  ```


- 方法：

  ```js
  // 阻止默认行为；
   var dom_a = document.querySelector("#box_a");
  dom_a.addEventListener('click', function(e) {
  //   // 阻止默认行为
     e.preventDefault();
   });
  
  
  // 阻止冒泡
  事件对象.stopPropagation();
  ```

### 11-02-阻止a标签转跳

  ```js
  // 阻止a标签转跳
  // 1 把a标签的href属性设置为 javascript:void(0);
  // 2 在a标签的点击事件里面，return false;
  // 3 使用事件对象.preventDefault();
  ```

  

## 12-事件三阶段

### 12-01-捕获和冒泡

- 捕获：从根部往目标DOM节点上，一层一层的找，捕获是用户点击了那个DOM节点；

  - 冒泡：从目标节点到跟接单；
  - 冒泡执行：**事件默认是在冒泡阶段执行；**当我们目标DOM节点注册了事件，冒泡往上的DOM节点也注册了同样的事件话，也会执行；

### 12-02-阻止冒泡

```js
 // 要阻止冒泡，需要先得到事件对象，给处理程序添加一个形参即可
  erzi.addEventListener('click', function(e) {
    // 调用阻止事件冒泡的方法进行阻止
    // x希望在哪儿阻止冒泡，就在哪儿添加形参，形参中有很多属性，相当于一个对象
    // 用形参自身的属性阻止e.stopPropagation()；
    e.stopPropagation();
    console.log('我是你儿子');
  });
```



- 注意：
  * 一定要传入形参e;
  * 方法写在函数里，位置无所谓；

## 13-获取元素对象位置

- 语法：获取元素距离参考父亲的左边和上边的值；

```js
// 得到的是某个元素距离他的offsetParent元素的水平距离
// 元素.offsetLeft = marginLeft + left
元素.offsetLeft 

// 得到的是某个元素距离他的offsetParent元素的垂直距离
// 元素.offsetTop = marginTop + top
元素.offsetTop 

// 找到一个有定位的父亲元素进行参考，如果亲生父亲没有定位，会一直往上找，直到找打有定位的父亲，或者body；
元素的offsetParent
```

## 14-事件解绑

- 案例：抽奖——开关思想
  * 在全局设置变量，初始化没有点击
  * 点击事件内部：
    - 如果没有点击：旋转下，点击的证明；
    - 点击过了：没有任何反应；
- 缺点：就是因为你设置的全局开关，在控制台可以获取到，可以重新赋值；
- 需要用到解绑：更为安全

```js
//两种方法：两种方法不能混用
//第一种
var btn = document.getElementById('btn');
btn.onclick = function(){
  btn.onclick = null;
  console.log('谢谢惠顾');
}
//第二种
var btn = document.getElementById('btn');
btn.addEventListener('click',function fn(){
  // 解绑 当前的函数
  btn.removeEventListener('click',fn);
  console.log('抽奖了');
})
```

## 15-事件委托

* 什么是事件委托？
  - 把事件注册在父级的元素身上，
  - 利用事件冒泡执行，当事件传播到已经注册了事件的父级元素身上，
  - 判断  触发事件的DOM  （e.target）节点是否是指定的元素，e.target.nodeName=="LI"
    - 如果是，就执行逻辑，
    - 否则什么都不管；

* **什么时候用？**

  *   **当我们需要给动态创建（不是一开始写死的，是后期可能会变的元素）的元素实现注册事件的效果的时候；**

* 把原理理解一下就行，不需要自己实现，还需要理解事件委托的使用场景，以后我们会在jq阶段学习一个别人封装好的事件委托;

* **注意**：

  - 解决：多次注册事件的问题；新增节点没有事件的问题；

  - 实现：通过在父级DOM节点注册事件，利用事件冒泡的执行机制，判断当前点击的对象是不是需要的节点；执行相应的逻辑；
  - 场景：给动态新增的DOM节点拥有相同的事件；

## 16-DOM节点的创建-修改-添加-删除

- 创建

  * innerHTML
  * document.write();
  * **document.creatElement('li');**

- 添加

  * 父节点.appendChild(新的DOM节点)：从后添加的DOM节点
  * 父节点.insertBefore(新的DOM节点,插入谁之前的DOM节点):有两个参数，在某个元素之前，添加新的DOM节点；

- 修改

  * innerHTML:结构

  * innerText：文本内容；

    

- 删除

  * 父亲节点.removeChild(被删除的节点)；



# WebAPI-BOM

## 01-BOM-window及onload

- BOM学习的对象：window上面的属性和方法；
- onload：等待静态资源加载完成后执行你的逻辑；

```js
  window.onload = function() {
    // 静态资源全部加载完成后，才执行这个函数；
    // 对图片进行操作
    // 等待图片下载完成后,才能进行操作;
  }
```





## 02-BOM-定时器-语法

```js
  // 语法: 一次性定时器;
  // es6:函数写法：() => {}
  // timeout：毫秒数

  // 作用：延迟一定时间执行；
  // var timer = setTimeout(function() {
  //   alert(1)
  // }, 3000);


  // 返回值；返回这个定时器的ID，用于清除定时器；
  // var btn = document.querySelector("#stop");
  // btn.onclick = function() {
  //   clearTimeout(timer);
  // };


  // 语法：永久定时器
  // 不是一瞬间执行，等待1000后，开启你的定时器；
  // 返回值：ID
  var timer = setInterval(function() {
    // document.write("123</br>")
    console.log(1);
  }, 1000);


  // 
  var btn = document.querySelector("#stop");
  btn.onclick = function() {
    clearInterval(timer);
  };
```

### 倒计时案例

- 实现：点击后
  - 按钮禁用；
  - 开启倒计时：
    - 间隔1秒才执行，需要在点击之后，立马执行一次；
    - 变量每次 miao--;
    - 当秒miao到了某个值的时候：清除定时器、去除按钮的禁用、恢复原来的文字；

```js
 btn.onclick = function() {
    // 3.点击之后有效果？
    // 3.1 按钮不能点了
    btn.disabled = true;

    // 3.2 开启倒计时
    var miaoshu = 5;

    // 立即执行；
    btn.value = `获取验证码【${miaoshu}】`;

    // 无限次定时器
    var timer = setInterval(function() {

      // 
      miaoshu--;

      // 当==1的时候
      btn.value = `获取验证码【${miaoshu}】`;

      // 判断：miaoshu到哪了？到达1的时候要清除定时器
      if (miaoshu == 0) {
        // 清除定时器
        clearInterval(timer);

        // 把禁用的属性关了
        btn.disabled = false;

        // 本身的文字恢复
        btn.value = "获取验证码";
      }

    }, 1000);

  }
```



## 03-BOM-location

- 语法：负责管理浏览器地址栏相关的行为和信息的对象；

```js
// 转跳你需要的地址；
    window.location.href = "http://www.baidu.com"
```

## 04-BOM-localStorage

- 作用：实现数据本地化，刷新后还在；

```js
  // 作用:可以使我们的数据本地化，刷新后还在；
  // 储存一条数据
  // localStorage.setItem("name", "张三");
  // localStorage.setItem("age", 12);
  // localStorage.setItem("zhiye", "前端工程师");


  // 获取刚才的数据：现在是直接读取浏览器数据
  // var a = localStorage.getItem("name");
  // console.log(a);

  // 没有的值的话，返回一个null;
  // var b = localStorage.getItem("age");
  // console.log(b);


  // 删除数据:某条数据
  // localStorage.removeItem("name");


  // 全部清除
  localStorage.clear();
```



## 05-BOM-JSON

- 作用：把对象类型转为JSON格式的字符串；
- JSOM上的**方法**：

```js
// 将对象转换为json格式的字符串
// 返回值：一个满足json格式的 字符串
JSON.stringify(对象);

// 将json格式的字符串转换为对象
// 返回值：依赖于你的json格式字符串，可能返回数组，或者是对象....
JSON.parse(json格式字符串);
```

## 06-本地化的步骤

- 第一步：将HTML结构中的数据抽象为一定格式的数组

- 第二步：将得到的数组存到本地

  - 1.转JSON格式：*var str = JSON.stringify(arr);*

  - 2.存储：*localStorage.setItem("list", str);*

  - 3.读取： var list = localStorage.getItem("list");

  - 4.转为约定的格式：JSON.parse(list)；

  - 注意：转格式和读取时必须用变量接收；

    

- 第三步：将HTML结构用渲染出来（列表初始化）

  * 新增DOM节点

  * 修改DOM节点内容（html结构）

  * 插入列表中

    

## 07-微博案例

- 列表初始化
- 新增微博

  - DOM操作：

    - 新增DOM节点

    - 修改新增DOM节点内容

    - 插入列表
  - 数据操作
- 删除微博
  - 事件委托----------DOM操作
  - 数据操作

   

```js
 function patchZero(v) {
        return v < 10 ? '0' + v : v;
    }

    function formatDate() {
        var now = new Date();
        var y = now.getFullYear();
        var m = now.getMonth() + 1;
        var d = now.getDate();
        var h = now.getHours();
        var mm = now.getMinutes();
        var s = now.getSeconds();
        return y + '-' + patchZero(m) + '-' + patchZero(d) + ' ' + patchZero(h) + ":" + patchZero(mm) + ':' + patchZero(s);
    }
    // ---------------------------列表初始化-------------------------------
    // 约定一个格式，数组里面包对象
    // 把写在HTML里的结构抽象为一个数组，格式如下：
    // var arr = [{
    //     content: "快来收了这九款用上就停不下来的应用吧！！",
    //     ID: ID,
    //     time: "2019-7-26 15:25:56",
    // }, {
    //     content: "快来收了这九款用上就停不下来的应用吧！！",
    //     ID: ID,
    //     time: "2019-7-26 15:25:56",
    // }, {
    //     content: "快来收了这九款用上就停不下来的应用吧！！",
    //     ID: ID,
    //     time: "2019-7-26 15:25:56",
    // }, ];
    // // // //本地初始化
    // // // // 第一步：转格式
    // var str = JSON.stringify(arr);
    // // // // 第二步：存储
    // localStorage.setItem("list", str);
    // 第三步：读取
    var list = localStorage.getItem("list");

    // 进行优化
    // 如果本地没有数据
    var ID = `${Date.now()}.${Math.random()}`;
    var arr;
    if (list == null) {
        arr = [];
    } else {
        arr = JSON.parse(list);
    };
    // ----------渲染-----------
    var ul = document.querySelector('.weibo-list');
    for (var i = 0; i < arr.length; i++) {
        //    新增DOM节点
        var li = document.createElement('li');
        // 修改DOM节点的内容
        li.innerHTML = `<p class="content">${arr[i].content}</p>
    <span class="del" ID=${arr[i].ID}>删除</span>
    <em class="time">${arr[i].time}</em>`;
        // 插入
        ul.appendChild(li);

    }



    // -----------------------------新增一条微博
    // 需求：点击发布时，文本域内容发布
    // 获取DOM节点
    var btn = document.querySelector('.weibo-btn');
    var textarea = document.querySelector('.weibo-text');


    // 注册事件
    btn.onclick = function() {
        // 先获取文本域的内容
        var value = textarea.value;
        var time = formatDate();

        // 优化
        if (value == "") {
            alert('输入的文本内容不能为空');
            return;
        }
        // 新增一个DOM节点
        var new_li = document.createElement('li');
        // 修改DOM节点的内容
        new_li.innerHTML = `<p class="content">${value}</p>
    <span class="del" ID=${ID}>删除</span>
    <em class="time">${time}</em>`;
        // 插入
        // 需要找一个参考位置
        var cankao = ul.children[0];
        ul.insertBefore(new_li, cankao);
        textarea.value = "";

        // --------------数据操作
        // 抽一条数据格式出来
        var obj = {
                ID: ID,
                content: value,
                time: time,
            }
            // 将选出来的数据插入原数组中
        arr.unshift(obj);
        // 转格式
        var str = JSON.stringify(arr);
        // 存储
        localStorage.setItem('list', str);

    }





    // 组合键发布---------------------
    textarea.onkeydown = function(e) {
        // 按下Ctrl和enter键发布
        if (e.ctrlKey && e.keyCode == 13) {
            btn.onclick();
        }
    }

    // ----------------------------删除------------------
    // 事件委托
    // 给ul做事件委托
    ul.onclick = function(e) {
        // 点谁是谁
        if (e.target.nodeName == "SPAN") {
            // 删除span所在的那一行
            // 需要找到它的父亲
            var parent = e.target.parentNode;
            // 删除
            ul.removeChild(parent);


            // 数据操作---------------------------------
            // 需求：需要找到要删除某个特定的元素，因此需要给要删除的元素进行唯一的标识
            // 获得自定义属性
            var ID = e.target.getAttribute('ID');

            // 筛选数据，一个一个的过
            for (var k = 0; k < arr.length; k++) {

                // 判断
                if (arr[k].ID == ID) {
                    // 数组的删除
                    arr.splice(k, 1);
                    break;

                }

            }
            // 存储
            var str = JSON.stringify(arr);
            localStorage.setItem('list', str);

        }
    }
```

## 08-轮播图流程

### 思想：排它思想

#### js中的操作

- 第一步：页面加载完成后执行

- 第二步：序号播放

- 第三步：左右按钮播放

- 第四步：左右联动序号

- 第五步：序号联动左右

- 第六步：自动播放和鼠标控制

  ```js
  // 介绍和序号轮播
      // 页面加载完成之后再执行
      window.onload = function() {
          // 需求：鼠标移入小圆点中时，图片切换,实际上是ul的位置在变化
          // 获取DOM节点
          var point = document.querySelectorAll('.list i');
          var ul = document.querySelector('#imglist');
          var imgWidth = ul.children[0].offsetWidth;
          var box = document.querySelector('#box');
  
          // 左右轮播
          // 需求：点击右边按钮时，图片切换
          // 获取DOM节点
          var right = document.querySelector('.arrow-right');
          var left = document.querySelector('.arrow-left');
  
          // 注册事件
          // 右边按钮
          var index = 0;
          right.onclick = function() {
              // 点击之后，图片切换
              index++;
              // 图片下标为0时，显示第一张图片
              // 图片下标为1时，显示第2张图片
              // 图片下标为2时，显示第3张图片
              // 图片下标为5时，显示第6张图片
              // 图片下标为6时，显示第1张图片
              if (index == ul.children.length) {
                  index = 0;
              }
              // 计算ul的位置
              var num = index * imgWidth;
              // 设置ul的偏移量,向左偏倚为负值
              ul.style.left = `-${num}px`;
              // 左右切换的index是全局的index，没有影响小圆点局部的index
              // index:0,小圆点的index：1
              // index:1,小圆点的index：2
              // index:2,小圆点的index：3
              for (var k = 0; k < point.length; k++) {
                  point[k].classList.remove('current');
              }
              point[index].classList.add('current');
          }
  
  
          // 左边按钮
          left.onclick = function() {
              index--;
              if (index == -1) {
                  index = ul.children.length - 1;
              }
              // 计算ul的位置
              var num = index * imgWidth;
              // 设置ul的偏移量,向左偏倚为负值
              ul.style.left = `-${num}px`;
  
              for (var k = 0; k < point.length; k++) {
                  point[k].classList.remove('current');
              }
              point[index].classList.add('current');
          }
  
          // 注册事件
          // 对小圆点的每一个进行操作，需要遍历循环
          for (var i = 0; i < point.length; i++) {
  
              // 需要提前将小圆点的下标存起来
              point[i].index = i;
              point[i].onmouseover = function() {
                  // 鼠标移入时图片切换
                  // 一个圆点对应一张图片
                  for (var j = 0; j < point.length; j++) {
                      // 排它思想
                      point[j].classList.remove('current');
  
                  }
                  this.classList.add('current');
                  // 计算ul的位置
                  // 下标为0时，往左挪动0个图片
                  // 下标为2时，往左挪动2个图片
                  // 下标为5时，往左挪动5个图片
                  // ul的挪动距离=下标*一个图片的宽度
                  // 需要获取一个图片的宽度
                  var num = this.index * imgWidth;
                  // 设置ul的偏移量,向左偏倚为负值
                  ul.style.left = `-${num}px`;
  
              }
  
          }
  
          // 自动轮播:自动往右点击
          // 设置定时器
          var timer = setInterval(function() {
              right.onclick();
          }, 1000);
  
          // 鼠标移入时，清除定时器
          box.onmouseover = function() {
                  clearInterval(timer);
              }
              // 鼠标移除时，开启定时器
          box.onmouseout = function() {
              timer = setInterval(function() {
                  right.onclick();
              }, 1000);
          }
      }
  ```

#### jQuery** **里面的排他思想**

- 想要多选一的效果，排他思想：当前元素设置样式，其余的兄弟元素清除样式。

 ## 09-zepto 类库

- 介绍
  - 对原生JS的极好的封装；
  - https://www.html.cn/doc/zeptojs_api/

## 10-swiper-插件

- 中文官网 ：https://www.swiper.com.cn/
- 以后如果找一个插件，去到人家提供下载和demo的地方，先看看demo，是不是你想要的效果；如果确定了这就是你想要的效果，看**教程开始**学习

# jQuery

## 00-入口函数

- 当script标签写在head中或者html结构之前时需要写入口函数

  ```js
  //第一种：
  $(function () {
      // 此处是页面 DOM 加载完成的入口
  })
  
  //第二种
  $(document).ready(function() {
      // 此处是页面 DOM 加载完成的入口
  })
  ```

  

-  一般推荐使用第一种

## 01-jQuery **对象和** **DOM** **对象**转化

- DOM对象==>jQuery 对象: $(DOM对象)
- jQuery 对象==>DOM对象:
  - $('div') [index]       index 是索引
  - $('div') .get(index)    index 是索引号  

​	

## 02-jQuery 常用API

### 02-01-选择器

-  **$(“选择器”)   // 里面选择器直接写 CSS 选择器即可，但是要加引号**     

```
$('#id')==》指定id元素

$('*')==》所有元素

$('.class')==》指定class元素

$('div')==》根据标签获取元素

$('div,p,li')==》获取多个

$('li.class')==>交集获取

$('ul>li')==>子代

$('ul li')==>后代
```

### 02-02-隐式迭代

- 遍历内部 DOM 元素（伪数组形式存储）的过程就叫做隐式迭代；

### 02-03-jQuery筛选选择器

```js
$('li:first')：第一个元素

$('li:last')：最后一个元素

$('li:eq(2)')==》索引为2【查找指定索引的元素】

$('li:odd')==》索引为奇数

$('li:even')==》索引为偶数

注意：索引是从0开始的
```

### 02-04-筛选方法

```js
$('li').parent()父级

$('ul').children('li');子集【儿子级】【如果不加参数，获取所有的，如果添加指定的元素，按照指定的找】

$('ul').find('li')后代【后代级】

$('li').siblings('li')兄弟

$('li'),nextAll();后面的

$('li').prevAll();前面的

判断是否具有某个类名：$('div').hasClass('aaa')

$('div').eq(index);指定索引方法【eq推荐用方法】
```

- 重要： parent() 、 children()  、find() 、 siblings() 、 eq()；

  

## 03-jQuery样式操作

### 03-01-操作CSS方式

- **语法**：$().css(“属性”)

  ​           $().css(“属性”，“属性值”)

- 里面可以写一个或者两个参数，一个参数为获取，两个参数为获取

### 03-02-设置类样式方法

- **添加类**：.addClass("类名")
- **删除类**：.removeClass("类名")
- **切换类**：.toogleClass("类名")
## 04-jQuery **效果**

- 参数：三个参数都可以省略

- speed：三种预定速度之一的字符串(“slow”,“normal”, or “fast”)或表示动画时长的毫秒数值(如：1000)

- easing：(Optional) 用来指定切换效果，默认是“swing”，可用参数“linear”

- fn：回调函数，表示在效果完成之后执行的函数

  

| 显示隐藏效果                   |
| ------------------------------ |
| .show([speed,[easing],[fn])    |
| .hide([speed,[easing],[fn])    |
| .toggle([speed,[easing],[fn]]) |

  

| 滑动效果                            |
| ----------------------------------- |
| .slideDown([speed,[easing],[fn]])   |
| .slideUp([speed,[easing],[fn]])     |
| .slideToggle([speed,[easing],[fn]]) |



| 淡入淡出效果                                                 |
| ------------------------------------------------------------ |
| fadeIn([speed,[easing],[fn]])                                |
| fadeOut([speed,[easing],[fn]])                               |
| fadeToggle([speed,[easing],[fn]])                            |
| fadeTo([[speed],opacity,[easing],[fn]])**【注意fadeTo必须写两个参数，speed和opacity】** |

- 事件切换:hover([over,]out)

  ```js
  （1）over:鼠标移到元素上要触发的函数（相当于mouseenter）
  mouseenter==mouseover
  （2）out:鼠标移出元素要触发的函数（相当于mouseleave）
  mouseleave==mouseout
  （3）如果只写一个函数，则鼠标经过和离开都会触发它
  ```

- 动画队列及其停止排队方法:在动画前面加**.stop**即可避免
- 自定义动画
  - 语法：animate(params,[speed],[easing],[fn])；
  - params: 想要更改的样式属性，以**对象**形式传递，必须写。 属性名可以不用带引号， 如果是复合属性则**需要采取驼峰命名法 **

## 05-jQuery -属性操作（2种）

### 05-01-固有属性

- 语法：.prop（“属性”）;

  ​           .prop（“属性”,"属性值"）;

- 里面可以写一个或者两个参数，一个参数为获取，两个参数为获取；

### 05-02-自定义属性

- 语法：.attr（“属性”）;

  ​           .attr（“属性”,"属性值"）;

- 里面可以写一个或者两个参数，一个参数为获取，两个参数为获取

### **05-03-数据缓存** **data()**【了解】

- 当做变量存储

-  **附加数据语法**

  data(''name'',''value'')   // 向被选元素附加数据   

  **获取数据语法**

  data(''name'')             //   向被选元素获取数据 

  ```js
  data() 方法可以在指定的元素上存取数据，并不会修改 DOM 元素结构，所以元素上无法查看。一旦页面刷新，之前存放的数据都将被移除。
  $('span').data('spanindex',3);
  
  console.log($('span').data('spanindex'));
  
  ```

  

## 06-jQuery内容文本值(3种)

### 06-01-普通元素内容

- 语法：.html（）;

  ​           .html（内容）;

- 里面可以写不写或者一个参数，没有参数为获取，一个参数为获取

### 06-02-普通元素文本内容

- 语法：.text（）;

  ​           .text（内容）;

- 里面可以写不写或者一个参数，没有参数为获取，一个参数为获取

### 06-03-表单的值val(）

- 语法：.val（）;

  ​           .val（内容）;

- 里面可以写不写或者一个参数，没有参数为获取，一个参数为获取

## 07-jQuery -元素操作

###  07-01-遍历：两种方法

- 第一种：$("div").each(function(index, Ele) { xxx; }）

  - **一般用于遍历元素**

  ```js
  	<div>1</div>
      <div>2</div>
      <div>3</div>
  var arr = ["red", "yellow", "blue"];
   $("div").each(function(i, elm) {
          //     // i索引值
          //     // elm为DOM元素，不能用.css的方法 
          //     $(elm).css("background", arr[i]);
   })
  ```

  

- 第二种：$.each(object，function(index, element){ xxx;}）

  - **一般用于遍历数据**

```js
var arr = ["red", "yellow", "blue"];
$.each(arr, function(i, elm) {
            console.log(i, elm);

        })
```

### 07-02-创建

- 语法：$(''<li></li>'');   

### 07-03-添加

- 内部添加
  - 从后添加 .append();
  - 从前添加 .prepend();
- 外部添加
  - 从后添加 .after();
  - 从前添加.before();

### 07-04-删除

- .remove()===>把元素本身删除包括html中的结构
- .empty()===>清空，页面上的内容没有了，但html结构还在
- .html()===>页面上的内容没有了，但html结构还在

## 08-jQuery **尺寸、位置操作**

### 08-01-尺寸

| 尺寸                                     | 备注                      |
| ---------------------------------------- | ------------------------- |
| .width()、       .height()               | 相当于获取的文本内容      |
| .innerWidth()、  .innerHeight()          | 包含padding               |
| .outerWidth()     .outerHeight()         | 包含padding+border        |
| .outerWidth(true)     .outerHeight(true) | 包含padding+border+margin |

- 以上参数为空，则是获取相应值，返回的是数字型。
  如果参数为数字，则是修改相应值。
  参数可以不必写单位。

### 08-02-位置（3种）

- offset():距离文档的距离

  - 两个属性：[left，top]；
  - 
    - offset().left
    - offset().top
  - 可以设置元素的偏移：offset({ top: 10, left: 30 });**设置时以对象形式传**
  - **返回的为对象**

- position()：相对于**带有定位的父级**偏移坐标，如果父级都没有定位，则以文档为准。

  - 两个属性：[left，top]；
    - position().left
    - position().top
  - 该方法只能获取，不能设置
  - 返回的为对象

- scroll()：被选元素被卷去的部分

  - 两个属性：[left，top]；

    - scroll().left
    - scroll().top

  - **scroll事件**

    - 谁有滚动条，注册给谁

    - 如果是浏览器有滚动条的话，注册事件格式为

      - $("body,,html").scrollTop(0);

    - 自定义效果只能加给元素，不能加给document

    - 一般用于回到顶部时的注册事件

      - $("body,html").animate({

        ​                scrollTop: 0

        ​            }, 1000)

    - 整个网页都有滚动条的话，滚动事件加给window



## 09-jQuery事件

### 09-01-on事件注册

- 注册的多个事件，处理程序相同时，格式为

  ```js
  $("div").on("click mouseover mouseout",function() {
      //处理程序相同
  })
  ```

- 注册的多个事件，处理程序不同时，格式为

  ```
  $("div").on({
      //属性名：属性值
      click:function() {},
      mouseover:function() {}
  })
  ```

​	

- **事件委托**

  - 在此之前有bind(), live()，delegate()等方法来处理事件绑定或者事件委派，最新版本的请用on替代他们。

    ```js
    $('ul').on('click', 'li', function() {
    
    ​    alert('hello world!');
    
    }); 
    ```

    

  - 动态创建的元素，click()没有办法绑定事件，on() 可以给动态生成的元素绑定事件

    ```js
    $(“div").on("click",”p”, function(){
    
    ​     alert("俺可以给动态生成的元素绑定事件")
    
     });
    ```

    

### 09-02-off()解绑事件(3种写法)

- 移除通过 on() 方法添加的事件处理程序。

```js
$("p").off() // 解绑p元素所有事件处理程序

$("p").off( "click")  // 解绑p元素上面的点击事件 后面的 foo 是侦听函数名

$("ul").off("click", "li");   // 解绑事件委托
```

- 如果有的事件只想触发一次， 可以使用**one()**来绑定事件。

### 09-03-自动触发事件trigger()-3种形式

- 语法：element.click()  // 第一种简写形式

  ​            element.trigger("type")//第二种自动触发模式

```js
$('p').click();

$("p").trigger("click"); // 此时自动触发点击事件，不需要鼠标点击

$('div').triggerHandler('click');// 自动触发事件【这种触发事件不会触发默认行为】
```



##  10-jQuery事件对象

- 事件被触发，就会有事件对象的产生

- 语法：element.on(events,[selector],function(event){})

  ```js
  阻止默认行为：event.preventDefault()   或者 return  false 
  
  阻止冒泡： event.stopPropagation()
  ```

  

## 11-jQuery其它方法

### 11-01-插件

- 常用网站
  -  jQuery 插件库  http://www.jq22.com/   
  -   jQuery 之家   http://www.htmleaf.com/  

### 11-02-图片懒加载

- BOOTSTRAP插件

  - https://www.bootcss.com/
  - - 引入CSS、引入JQ、引入JS
    - .container
    - 复制粘贴。

- 步骤：

  - 要引入JQuery
  - 插件JS【js引入文件和js调用必须写到 DOM元素（图片）最后面】
  - 将图片 src 替换为 data-lazy-src
  - 调用lazyLoadInit(）

  ​								

## 12-todolist案例

```js
 var str = localStorage.getItem('toDoList');
      // 判断本地是否有地方存储数据
      if (str == null) {
        // 向浏览器本地申请一个地方
        localStorage.setItem('toDoList', '[{"name":"吃饭","isOk":true},{"name":"睡觉","isOk":false}]');
        // 重新读取本地数据
        str = localStorage.getItem('toDoList');
      }
      // 把字符串数组 转换为 数组
      var arr = JSON.parse(str);
     // console.log(arr);[{"name":"吃饭","isOk":true},{"name":"睡觉","isOk":false}]
      // 循环遍历
      for (var i = 0; i < arr.length; i++) {
        // 取出一个对象
        var obj = arr[i]; // {name: "吃饭", isOk: true}
        // 判断
        if (obj.isOk == true) {
          // 完成
          $('<li></li>').attr('num',i).html('<span>' + obj.name + '</span>').appendTo('ul');
        } else {
          // 没完成
          $('<li></li>').attr('num',i).html('<input type="checkbox"><span>' + obj.name + '</span>').appendTo('ol');
        }
      }




      // 1、点击添加，创建li添加到ol
      // li里面有checkbox，有span，span里面放的就是输入的内容
      $('.add').click(function () {
        // 回去val值
        var zhi = $('.txt').val();
        // 创建li
        var li = $('<li></li>');
        // 设置        li.attr('num',arr.length);内容
        li.html('<input type="checkbox"><span>' + zhi + '</span>');
        // 放到ol里面
        $('ol').append(li);
        // 清空value
        $('.txt').val('');


        // 添加数据，保存
        
        // [
        //   {"name":"吃饭","isOk":true},
        //   {"name":"睡觉","isOk":false},
        //   {"name":zhi,"isOk":false} 
        // ]
        // 往数组里面添加内容
        arr.push( {"name":zhi,"isOk":false} );
        // console.log( arr );
        // 转成字符串
        str = JSON.stringify(arr);
        // 添加
        localStorage.setItem('toDoList',str);

      })

      // 2、点击checkbox，把这个li添加到下面ul
      $('ol').on('click','input',function () {

        // 获取li
        var li = $(this).parent();
        // 放到ul
        $('ul').append(li);
        // 把input
        $(this).hide();


        // 修改isOk改为true
        // 点击input，修改数组里面对象的isOk，改为true
        // arr = [
        //   {"name":"吃饭","isOk":true},==><li num=0>吃饭</li>
        //   {"name":"睡觉","isOk":false},==><li num=1>睡觉</li>
        //   {"name":"睡觉","isOk":false},==><li num=2>睡觉</li>
        //   {"name":zhi,"isOk":false},
        //   {"name":zhi,"isOk":false},
        //   {"name":zhi,"isOk":false} 
        // ]
        // arr[i].isOk = true;
        // 我们需要知道当前操作的这个li的索引值(num)，就知道了数组里面第几项需要改isOk
        // 获取当前点击li的num
        var i = li.attr('num');
        // 修改isOk
        arr[i].isOk = true;
        // 转换
        str = JSON.stringify(arr);
        // 保存
        localStorage.setItem('toDoList',str);

      });
```



