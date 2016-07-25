#布尔类型
1. 声明定义一个布尔值，使用关键字 FALSE(false) 和 TRUE(true)

######语法
    
        ```
        <?php
                 $flag1 = false;
                 $flag2 = true;
           ?>
        ```
2. 关于类型转换时的注意点

    2.1 以下的值会被转换为false
      - 布尔值 FALSE 本身
      - 整形值 0
      - 浮点型的值 0.0
      - 空字符串
      - 不包含任何元素的数组
      - 不包含任何成员变量的对象(仅PHP4.0适用)
      - 特许类型NULL（包括未赋值的变量）
      - 空标记生成SimpleXml对象

     2.1.1 验证2.1的代码如下
         ```
         $flag1 = false;
            var_dump($flag1);     // boolean false
            $flag2 = (boolean)0;
            var_dump($flag2);     //boolean false
            $flag3 = (boolean)0.0;
            var_dump($flag3);     //boolean false
            $flag4 = (boolean)'';
            var_dump($flag4);     //boolean false
            $flag5 = (boolean)array();
            var_dump($flag5);     //boolean false
            class foo{
            }
            $flag6 = (boolean)new foo();
            var_dump($flag6);     //boolean false
            $flag7 = (boolean)NULL;
            var_dump($flag7);     //boolean false
            $flag7;
            var_dump($flag7);    //boolean false
        ```
    2.1.2  提示
    > -1 和其它非零值（不论正负）一样，被认为是 TRUE ！



