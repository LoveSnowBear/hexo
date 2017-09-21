---
title: log4j源码阅读学习一
date: 2017-09-20 20:34:05
tags:

---
####温馨提示
       该博客中记录的是作者的第一次看源码的学习历程,作者是Java初学者,编程水平仅限于Java se,在学习的道路上难免会遇到一些困难,对于知识的理解也会出现偏差,记录的目的是希望能够和大家交流进步,希望读者朋友能抱着怀疑的态度阅读,对于有疑问的地方希望您能停下脚步指点一二,望与君同进步!
###学习内容
1. 导入源码
2. 建立测试类
3. 跟踪getLogger方法

####1.1 导入源码
首先从github上找到Apache/log4j源码,下载到本地

	git clone https://github.com/apache/log4j.git

然后将log4j的源码引入到eclipse中建立java工程
	![ ](/home/snowbear/图片/log4j源码.png  "导入源码")
虽然导成了maven工程,pom文件会报错,但是不影响代码的调试,所以暂时没有解决这个问题(execution标签的问题)

####1.2 建立测试类
建立Begin.java

	package test.begin;

	import org.apache.log4j.Logger;

	public class Begin {

		public static void main(String[] args) {

			Logger logger = Logger.getLogger("Begin.class");
			logger.debug("begin");
		}

	}	

####1.3 跟踪调试代码
首先跟踪Logger.getLogger("Begin.class"); 跟中执行流程如下
	![ ](/home/snowbear/图片/2017-09-21_21-40-08log4j.png  "log4j(一)")
	
今天就只做到这一步,同时对每一次的方法调用内容有了一个了解,明天再进行具体分析和向下推进.

