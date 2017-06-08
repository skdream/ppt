http://thatjsdude.com/interview/index.html

http://thatjsdude.com/interview/js2.html


## Scope and hoisting
Question: console.log输出的值是什么?

A:function a(){}
B:1;
C:10;
D:undefined


var a = 1; 
function b() {
    a = 10; 
    return; 
    function a() {} 
}
b(); 
console.log(a);          
        
		
		

Pass by value or by reference
Question: Does JavaScript pass parameter by value or by reference?

Answer: Primitive type (string, number, etc.) are passed by value and objects are passed by reference. If you change a property of the passed object, the change will be affected. However, you assign a new object to the passed object, the changes will not be reflected.


var num = 10,
    name = "Addy Osmani",
    obj1 = {
      value: "first value"
    },
    obj2 = {
     value: "second value"
    },
    obj3 = obj2;
 
function change(num, name, obj1, obj2) {
    num = num * 10;
    name = "Paul Irish";
    obj1 = obj2;
    obj2.value = "new value";
}
 
change(num, name, obj1, obj2);


console.log(num,name,obj1.value,obj2.value,obj3.value)正确的输出为？
 
console.log(num); // 10
console.log(name);// "Addy Osmani"
console.log(obj1.value);//"first value"
console.log(obj2.value);//"new value"
console.log(obj3.value);//"new value" 



