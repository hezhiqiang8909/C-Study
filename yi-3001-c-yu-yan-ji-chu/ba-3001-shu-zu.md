###1、数组
数组是相同类型的有限集合

**语法格式：**`存储类型    数据类型     标识符[数量];`

    例如：static int array[10];

数组的初始化：数组在定义的同时可以整体赋值，此时称为初始化。

    例如：int a[5]={1,2,3,4,5}

如果未完全赋满所有值，则未赋值的元素将清零。

    例如：
    
    int a[5] ={1,2,3,4}
    此时 a[0] = 1, a[1]=2,a[2]=3,a[4]=0
    
    常见初始化为空 a[5]={}

数组在定义之后不可以整体赋值或取值，需要依次用下标表示

    例如：

    a[0] = 10;
    a[3] = 30;
    
拥有N个元素的数组下标范围是0 ~ N-1

    例如：

    int a[5]
    有效的元素为：a[0] a[1] a[2] a[3] a[4]
    a[5]不是有效元素，也许恰巧有脏值，但是此时访问已经算内存越位
    
        