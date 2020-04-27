# javaBase
## 一、实验目的
（1）掌握字符串String及方法的使用  
（2）学会关于异常结构的处理  
（3）掌握GUI窗体及其组件的使用  
（4）学会组建的布局

## 二、实验任务
利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，达到如下功能：   
1.每 7 个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”   
2.允许提供输入参数，统计古诗中某个字或词出现的次数   
3.考虑操作中可能出现的异常，在程序中设计异常处理程序  

## 三．实验核心方法
```java
public static void print(String str) {// 字符串转数组
		char[] strs = str.toCharArray();
		int line = 0;
		// 每 7 个汉字加入一个标点符号
		int sep = 7;
		// 字符串总长度
		int len = strs.length;
		// 不足长度的去掉
		int stop = len % sep;
		String content = "";
		for (int i = 0; i < len - stop; i++) {
			if (i % sep == 0) {
				// 偶数时加“。”
				String r = str.substring(line * sep, (line + 1) * sep);
				if (line % 2 == 1) {
					System.out.println(r + "。");
					content += r + "。\n";
				} else {
					// 奇数时加“，”，
					content += r + "，";
					System.out.print(r + "，");
				}
				line++;
			}
		}
		writeFile("out.txt", content);
```

## 四、实验流程图
> 定义一个类→定义count方法统计字符串出现个数→for循环中嵌入if...else..语句来判断加入的标点符号
→编写控制选择的菜单→运行程序的主菜单→将字符串写入文件中捕获异常→运行 

## 五、运行截图

## 六、实验结果和收获
&nbsp;&nbsp;&nbsp;&nbsp;这次编程的内容是关于String字符串的应用及GUI窗体的使用，String字符串属于java中的字符串型。通过这次的实验，我了解到了关于字符串的基本操作、存储结构和定位结构，实验中主要可以分为五个部分，其中也运用到了许多基础的选择和循环结构，流程并不复杂，但是有一定的逻辑性，编程过程中也遇到了不少问题，多次查改后再修改，所以我觉得在以后的学习中，我会更加注重实践，多加积累、练习。
