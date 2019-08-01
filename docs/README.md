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





