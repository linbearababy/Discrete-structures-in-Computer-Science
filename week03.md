# Week 03 

# Sequences(序列）  ; cardinality（countable || uncountable）; matrices （矩阵）

# sequence 

Definition:

Geometric progression : ar^n

Arithmetic progression:  b, b+d, b+2d, b+3d,  …, b+nd

Strings:

A string is a finite sequence, often denoted a1a2...an
▪ The length of the string is the number of its terms.
▪ The empty string, denoted λ, is the string that has no terms. 
					
Summation :

▪ Consider the sequence {an}.

We define the following summation:					
  n j=m					
  
▪ Terminology:

  j is called the index of summation,

  m is the lower limit, 

  n is the upper limit. 
  
(6) summation of geometric  progression:
			
  Consider the arithmetic progression, for reals a and d: a, ar, ar2 ar3, ..., arn, ... 𝑛
					
  ◼ What is the sum of the first n + 1 terms, ෍ 𝑎𝑟𝑗 ? 𝑗=0
					
  S = a + ar + ar^2 + ... + ar^(n-1) + ar^n
					
  S–rS 		
  
	S = a(1-r^(n+1))/ (1-r)



(7)  useful summation:

  1+2+3+4+...+n :  k= (n+1)*n/2

  1^2+ 2^2+...+n^2 =  (n*(n+1)(2n+1))/6

  1^3 +2^3 + … + n^3 = n^2*(n+1)^2/4

  (等比数列）ar^k（sum) =  (ar^(n+1) -1)/(r-1)


(8) 	nested summation:	

To evaluate a nested summation, work from the inside out.					

▪ Example: first expand the inner summation and then compute the outer summation (like double integrals). 
				
		
(9) 题目： 求a(n); 证明（a(n)) (2.4.12);  找relation	

# cardinality 

(1)Cantor extended the Correspondence Principle to the infinite sets.

▪ Two sets A and B are defined to have the same cardinality (size) iff there is a bijection between them.

▪ A set is said to be countably infinite if it has the same size as N, the set of natural numbers.

▪ I.e., a set A is countably infinite iff there is a bijection (one-to-one and onto function) from N to A.

(2)A set is countable if it is finite or countably infinite. 

(3) so far, N, E, Z,  Q are countable.

(4) R IS

(5) 	
▪ The union of two countable sets is countable.
					
▪ A subset of a countable set is countable. ▪ If A is uncountable and A B then B is
					
uncountable. 

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-05-29%2000.15.34.png)


# matrix 矩阵

（1） 定义/概念： 

	乘法结合律： (AB)C=A(BC)．
	乘法左分配律：(A+B)C=AC+BC  
	乘法右分配律：C(A+B)=CA+CB  
	对数乘的结合性k(AB）=(kA)B=A(kB）．
	转置 (AB)T=BTAT．
	矩阵乘法一般不满足交换律 
	
（2） # 矩阵运算
![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-05-30%2010.56.07.png)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-05-30%2010.56.24.png)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-05-30%2010.56.35.png)

（3） AB != BA (交换律 不行）

     matrix multiplication is associative 结合律 （T) / commutative 交换律(F) 
     
(4)  BEST ORDER

找出做乘法运算最少的的顺序

ABC :

(AB)C = A(BC)

A= [aij] 20*30

B= [bij] 30*40

C= [cij] 40*10

(AB)C:

AB = 20*40 个元素， 每个元素经过30次乘法运算， 所以总共次数为 20*40*30

(AB)C = (AB) *C = 20*40 * 40*10 = 20*10 (个元素）， 每个元素经过40次运算，所以一共为

20*10*40 

所以一共：
（AB) + (AB)C = 20*30*40 + 20*10*40= 32000


A(BC) =  (BC) + A(BC) 次数

（BC) = 30*10 (个元素） 每一个元素经历了 40次， 所以共 30*10*40

A(BC) = 20*30 * 30*10 = 20*10 个元素， 每一个元素经历了30 次乘法运算，所以共 20*10*30

30*10*40 + 20*10*30 = 18000 

所以A(BC) is the best order

(5) identity matrix	

The identity matrix is a square matrix with all 1’s along the diagonal and 0’s elsewhere. 

(6) inverse matrix	

. Let A and B be nn matrices.
▪ If AB=BA=In then B is called the inverse of A,					
denoted B=A-1
					
(7)  solving linear equalities
 
2x + y =8    ------       2 1           x        8
-2x+y =4     ------       -2 1         y         4

(8) power of matrices		
Let A be an n ×n matrix. The powers of A are defined recursively:				

0th power of A: A0 = In 
				
kth power of A : Ak = A∙Ak −1, for k > 0
				
(9) zero - one matrices
						
All entries are 0 or 1.				
						
▪ Operations are Boolean operations: Let A = [aij] and B = [bij] be m ×n zero-one matrices. Then:
						
▪ The join of A and B, written A B, is the m ×n zero-one matrix [aij bij]. 
								
(10) boolean product

(11) boolean power


# summmary

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/IMG_7101.jpg)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/IMG_7103.jpg)
