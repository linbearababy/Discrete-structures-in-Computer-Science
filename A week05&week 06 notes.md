			
#  mathematical induction 
		
Definition 


▪ Let P(n) be some propositional function involving natural number n.
					
▪To prove that P(n) is true for all n ≥ 0, we can do the following:
					
▪ Basis Step: Prove that P(0) is true.
					
▪ Induction Step:
					
Prove that, for any arbitrary k,
					
k ≥ 0, P(k) logically implies P(k + 1).


(2)				
		
To show P(n) for any n ≥ b :
					
▪ Basis: prove P(b) is true.
					
▪ Induction Step:
Assume that k ≥ b and that P(k) is true (IH).
					
Establish that then P(k +1) is also true. 
				
		 	 	 		
			
Example：
				
（1）					
Claim: 2^𝑛 > 𝑛^3 for all 𝑛 ≥ 10 
					
Proof:
					
Basis: 

n=10: 

2^10 = 1024 > 1000 = 10^3. Thus the claim is true for 𝑛 = 10.
					
Induction Step:

Assume𝑘≥10and2^𝑘 >𝑘^3 (IH)

We need to show that IH implies 2^(𝑘+1 )> (𝑘 + 1) 3 .
				
			
			 			
				
					
(𝑘+1)^ 3 = (1+1/ 𝑘)^3              (arithmetic) 
					
< (1+1/𝑘)^3  * (2k)        (IH)
					
≤ (1 + 1/10)^ 3  * (2𝑘)  (arithmetic, since 𝑘 ≥ 10)
					
< 2 (2^𝑘) = 2^(𝑘+1) (arithmetic) 
				
				
（2）证明求和式子 (改变项数个数的字母为研究对象）

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/IMG_7140.jpg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/IMG_7143.jpg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/IMG_7144.jpg)
（3） 				 							
▪  Problem: Show that you can make up any postage of 8 cents or higher using just 3-cent stamps and 5-cent stamps.
 						
▪  Let P(n): “You can make up postage of n cents using just 3-cent stamps and 5-cent stamps.”
 							
▪ Basis: P(8) is true since you can make up postage of 8 cents using one 3-cent stamp and one 5-cent stamp. 
				
▪ Let P(n): “You can make up postage of n cents using just 3-cent stamps and 5-cent stamps.”
					
▪ Induction Step: Assume k ≥ 8 and P(k) is true, i.e, that you can make up postage of k cents ... (IH).
					
Then, k = 3m + 5n, for some natural numbers n and m.
					
If n > 0, then you can replace one of the 5-cent stamps with two 3-cent stamps to make up a postage of
3(m + 2) + 5(n −1) = 3m + 5n + 1 = k + 1.
					
On the other hand, if n = 0, then k = 3m.
					
In this case, since k ≥ 8, it must be that m > 3, which means we can replace three of the 3-cent stamps with two 5-cent stamps to make up a postage of
3(m −3) + 10 = 3m + 1 = k + 1.
					
In both cases, therefore, we conclude that P(k + 1) is true. 
				
			
(3) strong inducton
				
▪ To prove that P(k+1) holds, we may use any of the following assumptions: 
				
		 	 	 		
			
Strong Induction Hypothesis 				
					
▪ P(k) is true
▪ P(k – 1) is true
▪ P(k – 2) is true 
▪ P(1) is true 

				
▪ We must make sure that all the “assumptions” are in fact true for the induction “engine” to start. 
				
#Principal of strong induction:
	
▪ Claim: P(n) is true for all natural numbers n:
					
▪ Proof by (strong) mathematical induction: ▪ Basis: Prove that P(0) is true.
▪ Induction step:
					
Assume k ≥ 0, P(0), P(1), ..., P(k) are all true (SIH). Show that SIH logically implies P(k+1). 
				
		
				
					
We want to show that
					
[P(0)k((k≥0)P(k))→P(k+1))] ⇒ nP(n) 

where the universe is the natural numbers.
					
Proof is done by contradiction 

1.¬ n P(n)     Contrary assumption

2.x ¬ P(x)                        1, De Morgan’s

3.¬ P(r)                          2, EI, select smallest r

4.P(r -1)                         3, choice of r as smallest 

5.P(0)                            Premise
				
6.r > 0		                        r is positive (by choice in 4) & 5 
				
7.k ((k ≥ 1) P(k))→ p(k+1))         Premise			
					
8.((r-1 ≥ 0) P(r-1)) → p(r)            UI, k=r-1

9. P(r)                                       4, 6 & 8, modus ponens

10.Contradiction		                     3 & 9		



# week 06 

# week 06   因为relation没讲完，所以重头在 前三个


# counting1&2 ； probability 可以看做一类， 他们放在一起考
# Mainly : 排列组合 (主要考做题）

（1）一件事完成一共有几种方法：

Product rule : 相乘 （每一种有多少种）

Sum rule ： 相加 （一共有几种） 

比如：从A -> B 可以做公交车和火车， 公交车可以有6种路线， 火车两种：
总共有 ： 6*1 + 2*1

%%作业（6.1）着重体会 6.1.32 
6.2.4

（2）

有顺序的（permutation) :

p(n ,r ) = n! / (n-r)!  （string / letter）

无顺序的 (combination)： 

c(n,r ) = p(n , r) / r! = n! / ( (n-r)! * r!)

（n)
    r
题型： （一般来说考无顺序的比较多）

有序：

String/ 字母



无顺序： 

扑克牌： 


%%作业6.3 & 6.4 
6.5 是独立的一种题型





7.1&7.2 &8.5 是概率



		 	 	 		
			
				
					
						
Then the total number of objects would be at most k. This is a contradiction, because there are at least k + 1 objects. 
					
(1)  red & blue :

At least 3 balls 一样的颜色 (可能是红或者蓝）

X = （k+1）奇数
x/2 = 3 -----------》 x= 5

(2) 至少3个是蓝色

3 + 10 =13			
			
（2） pascal identity

Pascal trangle

每一行是  C（	n,k) 

	
		 	 	 		
			
				
6.4.21	类型			
						 										
					 				
			
		











#  relations （自己是一类）

%%作业 	9.1 & 9.3

区分概念： 



# summary
		
![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/fullsizeoutput_6b7.jpeg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/fullsizeoutput_6b8.jpeg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/fullsizeoutput_6b9.jpeg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/fullsizeoutput_6ba.jpeg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/fullsizeoutput_6bb.jpeg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/fullsizeoutput_6bc.jpeg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/fullsizeoutput_6bd.jpeg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/fullsizeoutput_6bc.jpeg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/fullsizeoutput_6bf.jpeg)

