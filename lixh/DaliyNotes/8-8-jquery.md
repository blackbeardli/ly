### 一.$.each() 与$().each()

#### jQuery.each()方法:  

* jQuery.each() 函数用于**遍历指定的对象和数组**;

* 语法:  `$.each( object, callback )`

  * **object**:  Object类型 指定需要遍历的对象或数组;

  * **callback**:   Function类型 指定的用于循环执行的函数:

    * function(index, value)
    * index:表示遍历的数组的下标;
    * value:表示下标对应的值;

    ```
    $(function () { 
        $.each([52, 97], function(index, value) {
        	alert(index + ': ' + value);
        });
    })
    //运行结果:
    0:52   1:97
    ```



#### jQuery each() 方法

* each() 方法为每个匹配元素规定要运行的函数。

* 语法:  `$(*selector*).each(function*(index,element)*)`

  * function*(index,element) *  必需。为每个匹配元素规定运行的函数;

  * *index* - 选择器的 index 位置;

  * *element* - 当前的元素（也可使用 "this" 选择器）。

    ```
    //html-------------------
    <button>输出每个列表项的值</button>
    <ul>
        <li>Coffee</li>
        <li>Milk</li>
        <li>Soda</li>
    </ul>
    //js---------------------
    $("button").click(function(){
        $("li").each(function(){
            alert($(this).text())
        });
    });
    //运行结果---------------
    //弹框依次弹出:  Coffee    Milk   Soda
    ```


### 二.json中获取数据两种方式:

### []  和.

##### var json={"name":"liming","age":"18"}

##### 想要得到liming ,以下为两种方法

* ##### json["name"];

* ##### json.name;

  

;







