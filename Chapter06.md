第6章习题答案
=
#####6.1-1 高度为h的堆，元素个数最多、最少是多少？  
最小：(∑(i from 0 to h-1)2^h-1) + 1 = 2^h  
最大：∑(i from 0 to h)2^h = 2^(h+1) - 1  

#####6.1-4 一个所有元素都不相同的最大堆，该堆的最小元素在哪里？  
在全部叶子节点中的一个。  

#####6.1-5 已排序的数组是最小堆吗？  
是。  

#####6.1-6 数组⟨23,17,14,6,13,10,1,5,7,12⟩ 是不是最大堆?  
不是。数组元素6和7违反定义。  

#####6.2-1  描述过程：MAX-HEAPIFY(A, 3) on the array A=⟨27,17,3,16,13,10,1,5,7,12,4,8,9,0⟩.  
3和10交换，再和9交换。  

#####6.2-2 最小堆伪代码，并和最大堆运行时间比较  
代码见[Prac622_Min_Heapify.java](https://github.com/zhuxiuwei/CLRS/blob/master/src/chap06/Prac622_Min_Heapify.java)  
运行时间和最大堆一样， 0(lgn)  

#####6.2-3  A[i]比所有孩子都大，调用max-heapify(A, i)的后果是？  
没有效果，已符合最大堆定义  

#####6.2-5  递归效率可能导致某些编译器产生低效代码，重写 max-heapify用循环替代递归  
代码见[Prac625_Max_Heapify_NoRescursive.java](https://github.com/zhuxiuwei/CLRS/blob/master/src/chap06/Prac625_Max_Heapify_NoRescursive.java)  

#####6.3-2  为什么建堆算法，是从最后一个非叶节点递减，而不是从第一个非叶节点递增  
递增的话，逻辑不对可能导致结果不对。因为子节点的调整可能破坏大根堆的性质。简单地例子：
4 1 3 10，从根节点4调整的话，最终结果就是错误的4 10 3 1。（期望值：10 4 3 1）  

#####6.5-1  
结果：13 12 9 5 6 8 7 4 0 1 2，15移除。  

#####6.5-2  
结果： 15 13 10 5 12 9 7 4 0 6 2 1 8  

#####6.5-3 用最小堆实现最小优先队列。  
代码见[PriorityQueueMinHeap](https://github.com/zhuxiuwei/CLRS/blob/master/src/chap06/Prac653_PriorityQueueMinHeap.java)  



###-------- 思考题 ----------  