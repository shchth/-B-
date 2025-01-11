# -B-
2024秋 闫宏飞老师计算概论B（python）课程，作为学生的经验
自己是0基础小白，最开始听说闫老师给分好才选的这门课，一学期下来也是认真对待，学了很多很多算法，投入了大量时间和精力，有自己独立解决一道题目的成就感，看着曾经难如登天的题目被轻松用学过的算法实现的快感，窥一隅而深感计算机算法科学之广博，只可惜结果不如人意，并没有取得很好的成绩，应大作业的要求记述一下自己学习这门课的经验，仅供参考。

## 学习方法：
刚接触这门课时学习方法明显有问题，为了解决每日选做耗费了大量时间结果收效甚微，总结下来并没有太多能力的增长，现在来看，我认为刚刚开始学习时一定不要为了解决问题而解决问题，题目的思考过程和算法是核心，每日选做可以放在一周固定的一个或两个时间段集中精力攻克，此外一定重视答案，做好笔记
课程学到后期就是各种算法轮番轰炸，看透PPT上要求掌握的内容，学扎实即可。离期末还有一个多月时候就要多刷题了，可以看看老师同学们都推荐做那些题目

##自己做的题目：

1.所有每日选做

2.Openjudge上部分额外题目（主要是群里同学做的题）

3.Leetcode动态规划（基础版）大部分和Leetcode热题100大约1/5 leetcode其他的部分题目

# Cheat-Sheet精华部分

不同于其他CheatSheet中各种算法的模板，这里的所谓“精华部分”是自己认为比较重要的一些内容

同时也是做题得到的经验，这里不摘录算法模板，因为大家基本都已经熟知或是在其他的地方见过


## 1.区间问题

a  区间合并 合并所有有交集区间                                   左  

b  选择不相交区间 选尽量多区间使之互不相交 可选最大数量            右

c  区间选点 选尽量少的点，使每个区间内至少有一个点                 右

d  最少区间覆盖 给一系列区间和目标区间，问最少选多少可以覆盖目标    左

e  区间分组 最少可分成几组使组内无交                              左

详见https://zhuanlan.zhihu.com/p/446371757
知乎     一文读懂五类常见区间问题





## 2.动态规划初始值设定

            不合法状态设置为                                   openjudge例题

求   min            +∞            不超过 j     dpij=0

     max            -∞            恰好为 j     dpj0=0    -∞     健身房
     
     方案数          0             至少为 j     dp00=0    -∞    最佳凑单
     






## 3.二分查找保姆级教程
在类似openjudge畜栏保留问题和leetcode1552  两球之间的磁力时，我们经常会用到贪心算法加二分查找
二分查找怎么写不会出错是一个很大的困扰，这是我看Leetcode上的一个解答中的做法，具体是哪个解答已经不记得了
建议做一下这两个题目再来看我这个笔记
划分一个数组

check是检查函数


### A  使划分的最小值最大

  while left<right:
  
    mid=(left+right+1)//2
    
    if check(mid):
    
      left=mid
      
    else:
    
      right=mid-1


### B  使划分的最大值最小

  while left<right:
  
    mid=(left+right)//2
    
    if check(mid):
    
      right=mid
      
    else:
    
      left=mid+1
