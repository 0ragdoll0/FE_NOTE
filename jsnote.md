# 对象属性
## 属性值
属性值必须是字符串，字符串，字符串！
在定义或获取时会将不是字符串的类型强制转换成字符串！
### 属性值为对象时，强行调用toString()
![](https://github.com/0ragdoll0/FE_NOTE/blob/master/pics/props.PNG)
## 遍历
### 1.for ... in
只遍历可枚举属性，遍历所有实例和原型链上的属性
var obj={name:"niel",age:22}
for(let k in obj){
  console.log(k);
}

### 2.Object.keys()
返回所有实例自有的可枚举属性的数组，原型链上的不返回
var propsArray=Object.keys(obj);

### 3.Object.getOwnPropertyNames()
返回所有实例自有的属性的数组，包括可枚举和不可枚举的
var props=Object.getOwnPropertyNames(obj);
