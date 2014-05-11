<script type="text/x-mathjax-config">
MathJax.Hub.Config({
tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}
});
</script>


---
layout: post
title: "算法导论--第二章习题"
date: 2014-05-11 18:04:00 +0800
comments: true
categories: 
---

**2.1-2 重写过程INSERTION-SORT,使之按非升序（而不是按非降序）排序。**

对数组A进行非升序排序：

	void InsertionSort(int[] Unsorted, int size)
	{
		for(j = 2; j < size; j++ )
		{
			int key = Unsorted[j];
			int i = j -1;
			
			while(i > 0 && Unsored[i] < key)
			{
				Unsorted[i+1] = Unsotred[i];
				i = i-1;
			}
			
			Unsorted[i+1] = key;
		
		}
	}


**2.2-1 用$\theta$形式表示对函数$n^3/1000-100n^2-100n+3$.**

答：$\theta(3)$



**2.2-2写出选择排序的代码，以及它的最佳和最坏情况下的运行时间**

答:最佳时间$\theta(n)$. 最坏时间$\theta(n^2)$.

选择排序代码：
	
	void SelectionSort(int[] Unsorted, int size)
	{
		for(int i =0; i < size; i++)
		{
			int min = Unsorted[i];
			int minIndex = i;
			//找到最小数
			for(int j=i; j<size; j++)
			{
				if(Unsorted[j]<min)
				{
					min = Unsorted[j];
					minIndex = j;	
				}
			}		
			
			if(min_index!=i)
			{
				//交换最小的数和第n个数
				int temp = Unsorted[i];
				Unsorted[i] = Unsorted[minIndex];
				 Unsorted[minIndex] = temp;
			}
				
		}
	
	}
	
	
**2.3-1以图2-4为模型，说明合并排序在输入数组A={3,41,52,26,38,57,9,49}上的执行过程.**






