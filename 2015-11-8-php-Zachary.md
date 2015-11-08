#PHP基础入门

##主要内容
1. PHP简介
2. 开发环境配置
3. 基本语法

##简介
1. PHP: Hypertext Preprocessor
2. 运行在服务器上的脚本语言
3. 可以嵌入在HTML代码中
4. 简单，易学

##预备知识：
1. PHP文件能包含什么内容？  
	文本，HTML，CSS，PHP代码...等等
2. PHP文件执行的方式？  
	在服务器上执行，最后执行的结果可以输出返回（以纯文本的方式返回）
3. 后缀名？  
	.PHP
	
##开发环境

XAMPP：
PHP、MySQL、Tomcat等

##基本语法
1. 脚本的插入  
以`<?php` 开头， 以`?>`结尾
```
<?php
//此处为PHP代码
echo "Hello PHP!";
?>
```
可以嵌入在HTML代码中：  
```
<!DOCTYPE html>
<html>
<head>
	<title>My First PHP page!</title>
<head>
<body>
<?php
//此处为PHP代码
echo "<h1>Hello PHP!</h1>";
?>
</body>
</html>
```

2. 注释  
	1. `//这是单行注释`
	2. `#这也是单行注释`
	3. `/*这种是多行注释*/`

3. 变量与大小写  
所有的变量名都以`$`开头，例如`$msg`, `$_POST`, `$hehe_123`等等，后半部分命名规则可参考C语言。  
###大小写：
	1. 变量名区分大小写
	2. 常量名默认区分大小写
	3. 函数名、方法名、类名 **不区分**大小写
	4. NULL、TRUE、FALSE不区分大小写  	
###建议：
常量名大写；  
函数名，方法名，类名 使用与定义时相同的名字

4. 变量作用域
local、global、static  
在函数**之外**声明的变量是global的作用域，只能在函数以外进行访问  
在函数**内部**声明的变量是local的作用域，只能在函数内部进行访问  
global关键字
`gloabl $x;`  
`$GLOBALS[index]`数组

5. 输出  
echo 和 print  

6. if...else for while do...while 分支、循环  
foreach  
```
foreach($array as $value) {
	echo $value;
}
```
7. 数组  
索引数组、关联数组  
`array();`创建数组  
索引数组：
```
$arr = array('hello', 'world', 'php');
echo $arr[0];
echo $arr[1];
$arr[1] = '欢爷！';
echo $arr[1];
```
关联数组：
```
$age = array('Peter'=>25, 'Tom'=>40, 'John'=>20);
$age['欢爷']=>18;
echo $age['Peter'];
echo $age['欢爷'];
```
遍历：
```
foreach($age as $name=>$value){
	echo "key=" . $name . ", value=" . $value;
}	
```