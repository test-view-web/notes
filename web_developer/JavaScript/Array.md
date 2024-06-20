
[# 一分钟掌握Javascript中的map方法](https://www.bilibili.com/video/BV1QA4y1S7zA/?spm_id_from=333.337.search-card.all.click&vd_source=54c4bb63799ad696ed0571b9fe25e6e0)
# JavaScript Array map() 方法
## 定义和用法

`map()` 方法使用为每个数组元素调用函数的结果创建新数组。

`map()` 方法按顺序为数组中的每个元素调用一次提供的函数。

注释：`map()` 对没有值的数组元素不执行函数。

注释：`map()` 不会改变原始数组。

## 实例

### 例子 1

返回原始数组中所有值的平方根的数组：

var numbers = [4, 9, 16, 25];
var x = numbers.map(Math.sqrt)
document.getElementById("demo").innerHTML = x;
## Math 对象

Math 对象允许您执行数学任务。

Math 不是构造函数。Math 的所有属性/方法都可以通过使用 Math 作为对象来调用，而无需创建它：

var x = Math.PI;            // 返回 PI
var y = Math.sqrt(16);      // 返回 16 的平方根