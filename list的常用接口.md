# 一、认识list

大家在看该篇文章之前肯定都学过数据结构吧，

数据结构中有 线性表，链表，二叉树等等，我们的list就是一个双向链表

那么什么是双向链表呢，

定义（自己理解的不是官方的）

每一个节点都有两个指针域，分别为 prev和next  其中 prev指向上一个节点，next指向下一个节点， 这样可以使尾插头插，。尾删和头删的时间复杂度均为常量级别的

**list** 是支持常数时间从容器任何位置插入和移除元素的容器

list 支持模板 数值域可以为任意类型

# 二、常用接口

## 1、创建一个list对象

### ①、使用默认构造函数

语法

```C++
list<int> l1;
```

作用，在栈区创建一个l1对象

### ②、有参构造

语法

```C++
list( size_type count,const T& value, const Allocator& alloc = Allocator());
```

用法

```C++
list<int> l2(5, 3);
```

作用

给l2 对象写入五个3；

### ③、拷贝构造

```C++
list<int> l3(l1);
```

作用： 讲l1中的数据拷贝到l3中，这里新创建空间，不是深拷贝

## 2、list打印方法

### ①、 迭代器的方法打印

```C++
	while (it != l2.end())
	{
		cout << *it << " ";
		it++;
	}
```

### ②、范围for的方法打印

```C++
	for (auto li : l2)
	{
		cout << li << " ";
	}
```

## 3、给list赋值 assign

语法

```C++
  void assign( input_iterator start, input_iterator end );
  void assign( size_type num, const TYPE &val )；
```

作用

1. assign()函数以迭代器start和end指示的范围为list赋值
2. 为list赋值num个以val为值的元素。

## 4、返回最后一个元素 back()



