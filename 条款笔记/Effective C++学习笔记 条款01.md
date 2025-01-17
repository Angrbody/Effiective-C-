﻿# Effective C++ 条款01：
# 视C++为一个语言联邦（view C++ as a federation of languages）
过往学习的理解：C++ = C + class， 即C加上了面向对象的设计，在写代码时设计了一些简单的类，使用了指针，但随着各种库函数的使用，已经涉及到了C++的各种扩展。
### 三大扩展

 1. 异常（exception）：
        	C++使用`try,catch,throw`关键字以及其他异常函数来处理程序执行期间产生的异常，如使用无效参数、错误的运算操作、内存越界、数学上/下溢等等，`std::exception`是所有标准C++异常的父类。
 2. 模板（template）：
        	泛型编程的基础，个人理解为当不知道函数需要处理什么样的数据类型时，可以通过设计template来实现“模糊输入”的函数模板，如一个返回二者较大值的函数既可以处理int输入，也可以应对double输入，只需要保证输入的两个参数类型相同即可。
        	模板的使用提高了代码的重复利用率。
 3. STL（Standard Template Lab）：
        	为C++带来前所未见的伸展性，极大扩充了C++的内容，主要包括以下三类：容器（Container）、算法（Algorithms）、迭代器（iterators）

### C++:多重范型编程语言（multiparadigm programing language）
   

 1. 过程形式(procedural)
　　即C++中保留了C的过程编程，设计应用各种函数，以自顶向下、逐步求精的核心概念完成一系列的任务，程序通过顺序、选择、循环三种基本控制语句来完成，形式比较贴近自然表达式。
 3. 面向对象形式(object-oriented)
　　即在C的基础上增加了类class的设计，通过设计不同的对象来实现不同功能，每个类包含数据和函数（方法），以此为基础扩展出继承和多态等类之间的复杂关系。
      

 4. 函数形式(functional)
　　函数式编程和声明式编程一样，核心思想是告诉计算机需要做什么，但不指定具体做法。在函数式编程中函数和其他数据类型一样出于平等低位，可以赋值给其他变量，也可以作为参数传入另一个函数，或者作为别的函数的返回值。
　　特点：一个函数相同的输入总会得到相同的输出，且不会对外部产生影响。
       

 5. 泛型形式(generic)
	　　泛型编程指在多种数据类型上皆可操作,和oop编程不同之处在于泛型编程并不要求额外的间接层来调用函数,而使用完全一般化并可重复使用的算法.
	STL就是泛型编程思想的实现,是一种泛型算法库.
       

 6. 元编程形式(metaprogramming)
　　元编程意图编写或者操控其他程序（或自身）作为它们的数据，或者在运行时完成部分本应在编译时完成的工作，其中编写元程序的语言为元语言，被操作的语言为目标语言．
　　最常用的元编程工具是编译器．
### C++联邦：4个次语言（sub language）
    

 1. C：C++的基础，包含区块、语句、预处理器、内置数据类型、数组、指针等
 2. Object-Oriented C++：C with Class，封装+继承+多态+virtual函数（动态绑定）
 3. Template C++：C++的泛型编程 -> 模板元编程（TMP）
 4. STL：template程序库，协调配合各种容器、迭代器、算法以及函数对象

　　四个次语言组成C++的联邦政府，各自有各自的规约，在次语言间进行转换时需要注意编程守则的改变。
   *记住：C++高效编程守则视状况而变化,取决于你使用C++的哪一部分*

