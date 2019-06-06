# Asymptotic Notation
Big -O notation		
					
𝑓(𝑛) = 𝑂(𝑔(𝑛)) iff there exists ▪ Constant 𝑐 > 0					
▪ Constant 𝑛0
▪ Such that 𝑓 𝑛 ≤ 𝑐 ⋅ 𝑔(𝑛) for all 𝑛 ≥ 𝑛0					
▪ Eventually, 𝑓(𝑛) is always smaller than 𝑐 ⋅ 𝑔(𝑛)	
Note properly it is 𝑓 𝑛 ∈ 𝑂(𝑔 𝑛 ) but everyone		
abuses notation this way 

	 	 	 		
Example : 			
				
					
We said we need 4 𝑛 − 1 2 operations for BubbleSort
					
▪4 𝑛−1 2 =4𝑛2 −8𝑛+4≤4𝑛2 +4 ▪ Also 4𝑛2 + 4 ≤ 8𝑛2 if 𝑛 ≥ 1
▪Thus4 𝑛−1 2 =𝑂(𝑛2)
					
▪ Assuming the number of operations is roughly proportional to the time required, we say that BubbleSort requires 𝑂(𝑛2) (or quadratic) time. 

Tricks for proving f(n) = O(g(n)) 			
▪ Observe the highest order term
▪ Highest term in f(n) must be ≤ that of g(n)
					
▪ Try fixing c first, then find n0.
▪ Let a be the coefficient of the highest term in f(n) Try
					
to let c = a, a+1, etc.
▪ Or let c = sum of all coefficients 

(2) Big-omega Notation (Asymptotic lower bound) 		
𝑓(𝑛) = Ω(𝑔(𝑛)) iff there exists ▪ Constant 𝑐 > 0
					
▪ Constant 𝑛0
▪ Such that 𝑓 𝑛 ≥ 𝑐 ⋅ 𝑔(𝑛) for all 𝑛 ≥ 𝑛0
					
▪ Eventually, 𝑓(𝑛) is always bigger than 𝑐 ⋅ 𝑔(𝑛) ▪ Reverse of 𝑂(𝑔(𝑛)) 
				
（3)Big-theta (Asymptotic tight bound) 
			
▪ 𝑓(𝑛) = Θ(𝑔(𝑛)) iff ▪ 𝑓(𝑛) = 𝑂(𝑔(𝑛)) and ▪ 𝑓(𝑛) = Ω(𝑔(𝑛)) 
				
（4）			
P = NP 			 							
A problem is said to be in the set P if there is an algorithm that solves it that runs in 𝑂(𝑛𝑘) time for some integer 𝑘
					 							
▪  A problem is said to be in the set NP if an answer can be verified in 𝑂(𝑛𝑘) time
 							
▪ Whether these two sets are the same is unknown 

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-04%2019.46.22.png)

# 	Divisibility and Modular Arithmetic 
(1)	
Division :				
▪ Definition: If a and b are integers with a ≠ 0, then a divides b if there exists an integer c such that
b = ac.
▪  When a divides b we say that a is a factor of b, or a is a divisor of b and that b is a multiple of a.
▪  The notation a | b denotes that a divides b.
 					
▪  If a | b, then b/a is an integer.
 			
▪  If a does not divide b, we write a ∤ b.
(2) 
Properties of divisibility			
▪ Theorem 1: Let a, b, and c be integers, where a ≠ 0.			
						 
If a | b and a | c, then a | (b + c);
 						
						 							
If a | b, then a | (bc) for all integers c;
 						
						 							
If a | b and b | c, then a | c.			 					
◼ Proof:
(i) Supposea|banda|c.
					
Then there are integers s and t with b = as and c = at. Hence, b + c = as + at = a(s + t).
It follows that a | (b + c).
Hence, if a | b and a | c, then a | (b + c).
					
(ii), (iii) : Exercise (the proofs are similar to the proof above). 
			
▪ Lemma: If n is a positive integer and a is a positive factor of n, then 1 ≤ a ≤ n.
					
▪ Proof:
Assume n is a positive integer and a is a positive factor of n.
					
Then n = ab, for some integer b.
Moreover, b must be positive since both n and a are. Hence b ≥ 1.
From this inequality we get: n = ab ≥ a ∙1 = a.
Additionally, the assumption that a is positive implies a ≥ 1.
					
Thus, 1 ≤ a ≤ n.

(3) Division algorithm	
		
Division Algorithm (Theorem): If a is an integer and d is a positive integer, then there are unique integers q and r, with 0 ≤ r < d, such that a = dq + r.
					
▪ d is called the divisor.
▪ a is called the dividend. ▪ q is called the quotient.
▪ r is called the remainder 
			
Definitions of div and mod: 
					
q = a div d
 r = a mod d 
					
(4) Congruence relation			
					
Definition: If a and b are integers and m is a positive integer, then a is congruent to b modulo m iff m | (a – b).
	
▪  We write a ≡ b (mod m) to say that a is congruent to b modulo m.
	
▪  Two integers are congruent mod m if and only if they have the same
 							
remainder when divided by m.

▪  We write a ≢ b (mod m) to say a is not congruent to b modulo m. 
 						
More: 
			
▪ Theorem 4: Let m be a positive integer. The integers a and b are congruent modulo m if and only if there is an integer k such that a = b + km.

▪ Proof:	
▪  (=>) Assume a ≡ b (mod m)
 							
Then m | (a – b).
 Hence, there is an integer k such that (a – b) = km. But then a = b + km.
	
▪  (<=) Assume there is an integer k such that a = b + km, Then km = a – b.
 Hence, m | (a – b).
 Thus, a ≡ b (mod m). 
 						
(5) Notation Hazard: (mod m) v.s. mod
						
▪ The “mod” in a ≡ b (mod m) and a mod m = b are
					
different.
					
▪ a ≡ b (mod m) is a relation on the set of integers.
					
▪ In a mod m, the notation mod denotes a binary operation (function).
					
▪ Theorem 3: Let a and b be integers, and let m be a positive integer. Then a ≡ b (mod m) if and only if a mod m = b mod m. (Proof in the exercises) 
				
(6) 	Congruences of Sums and Products 
								
▪ Theorem 5: Let m be a positive integer. If a ≡ b (mod m) and c ≡ d (mod m), then a + c ≡ b + d (mod m) and
ac ≡ bd(modm).
					
▪ Proof:					 							
▪  Assume a ≡ b(modm) andc ≡ d(modm).
					 							
▪  Then, by Theorem 4, there are integers s and t with b = a + sm and d = c + tm.
 				
▪  Therefore,
 b + d = (a + sm) + (c + tm) = (a + c) + m(s + t) and bd = (a + sm) (c + tm) = ac + m(at + cs + stm).
	
▪  Hence,by Theorem 4, a+c ≡ b+d(modm)andac ≡ bd(modm). ▪ Example: Because 7 ≡ 2 (mod 5) and 11 ≡ 1 (mod 5) , it follows that 18 = 3 (mod 5) and 77 = 2 (mod 5) 

▪ Proof:	
▪  (=>) Assume a ≡ b (mod m)
 							
Then m | (a – b).
 Hence, there is an integer k such that (a – b) = km. But then a = b + km.
	
▪  (<=) Assume there is an integer k such that a = b + km, Then km = a – b.
 Hence, m | (a – b).
 Thus, a ≡ b (mod m). 
 						
(5) Notation Hazard: (mod m) v.s. mod
						
▪ The “mod” in a ≡ b (mod m) and a mod m = b are
					
different.
					
▪ a ≡ b (mod m) is a relation on the set of integers.
					
▪ In a mod m, the notation mod denotes a binary operation (function).
					
▪ Theorem 3: Let a and b be integers, and let m be a positive integer. Then a ≡ b (mod m) if and only if a mod m = b mod m. (Proof in the exercises) 
				
(6) 	Congruences of Sums and Products 
								
▪ Theorem 5: Let m be a positive integer. If a ≡ b (mod m) and c ≡ d (mod m), then a + c ≡ b + d (mod m) and
ac ≡ bd(modm).
					
▪ Proof:					 							
▪  Assume a ≡ b(modm) andc ≡ d(modm).
					 							
▪  Then, by Theorem 4, there are integers s and t with b = a + sm and d = c + tm.
 				
▪  Therefore,
 b + d = (a + sm) + (c + tm) = (a + c) + m(s + t) and bd = (a + sm) (c + tm) = ac + m(at + cs + stm).
	
▪  Hence,by Theorem 4, a+c ≡ b+d(modm)andac ≡ bd(modm). ▪ Example: Because 7 ≡ 2 (mod 5) and 11 ≡ 1 (mod 5) , it follows that 18 = 3 (mod 5) and 77 = 2 (mod 5) 

Solution: Using the definitions above: 7 +11 9 = (7 + 9) mod 11 = 16 mod 11 = 5
7 ∙11 9 = (7 ∙ 9) mod 11 = 63 mod 11 = 8 
								
▪ The operations +m and ∙m satisfy many of the same
					
properties as ordinary addition and multiplication. ▪ Closure: If a and b belong to Zm , then a +m b and a ∙m b
					
belong to Zm .
		
▪  Associativity: If a, b, and c belong to Zm , then (a +m b) +m c = a +m (b +m c) and
 (a ∙m b) ∙m c = a ∙m (b ∙m c).
 						
▪  Commutativity: If a and b belong to Zm , then a +m b = b +m a and a ∙m b = b ∙m a.
 							
▪ Identity elements: If a belongs to Zm , then a +m 0 = a
				
and a ∙m 1 = a.
			
▪ Additive inverses: If a ≠ 0 belongs to Zm , then m − a is the additive
					
inverse of a modulo m and 0 is its own additive inverse. • a+m(m−a) =0and0+m0 =0
					
▪ Distributivity: If a, b, and c belong to Zm , then
• a∙m(b+mc)= (a∙mb)+m (a∙mc) and (a
					
(a+mb)∙m c =(a∙mc)+m(b∙mc). ▪ Proofs are exercises.
					
▪ Multiplicative inverses have not been included since they do not always exist. For example, there is no multiplicative inverse of 2 modulo 6.
					
▪ (optional) Using the terminology of abstract algebra, Zm with +m is a commutative group and Zm with +m and ∙m is a commutative ring. 

(10) primes				
▪ Definition: A positive integer p greater than 1 is prime if the only positive factors of p are 1 and p.
					
▪ A positive integer that is greater than 1 and is not prime is called composite. 
				
(11)THE Fundamental Theorem of Arithmetic 	

▪ Theorem: Every positive integer greater than 1 can be written as a prime or as the product of two or more primes; this representation is unique if the prime factors are written in order of non-decreasing size.
					
▪ Examples:
▪ 100 = 2 ∙ 2 ∙ 5 ∙ 5 = 22 ∙ 52
					
▪ 641 = 641
					
▪ 999 = 3 ∙ 3 ∙ 3 ∙ 37 = 33 ∙ 37 

(12)	The Sieve of Erastosthenes 
						
A method for finding all primes that do not exceed a given positive integer, n.
					
▪  List all of the integers from 2 to n in increasing order.
	
▪  Mark the first unmarked element of the list as “prime”.

▪  Delete all the unmarked integers that are divisible by the last element that was marked as “prime”.
						 							
▪  Repeat the previous two steps until only marked integers 
 
(13)Greatest common divisor			
					
▪ Definition: Let a and b be integers, not both zero. The largest integer d such that d | a and also d | b is called the greatest common divisor of a and b. It is denoted by gcd(a,b). 
									
▪ Definition: The integers a and b are relatively prime if their greatest common divisor is 1.
					
▪ Example: 17 and 22
▪ Definition: The integers a1, a2, ..., an are pairwise relatively
					
prime if gcd(ai, aj)= 1 whenever 1 ≤ i < j ≤ n 

*1 find gcd
					
▪ Suppose the prime factorizations of a and b are:
					
where each exponent is a nonnegative integer, and where all primes occurring in either prime factorization are included in both. Then:
			
▪ Example:
▪120= 23 ∙3∙5 
				
(14) 	Euclidean Algorithm 

▪  The Euclidian algorithm is an efficient method for computing the greatest common divisor of two integers.

▪  It is based on the fact that, if a > b, then gcd(a, b) = gcd(b, a mod b).
 							
▪ Example: Find gcd(91, 287):
 ▪ 287 mod 91 = 14, so gcd(91, 287) = gcd(91, 14)
 							
▪ 91 mod 14 = 7, so gcd(91, 14) = gcd(14, 7)
 							
▪ 14 mod 7 = 0, so gcd(14, 7) = gcd(7, 0)
 							
▪ gcd(7, 0) = 7 
 						
SO gcd(91,287) = 7

SO gcd(91,287) = 7       ; M=91   N= 287
E:                                                 B:
287 = 3*91+14                              ( N= 3*M+  14  )           14 = N-3M
91 =   6*14 + 7            M = 6* (N-3M) +7     ---- 7 = M- 6*(N-3M) -- 7 = 19M -6N (= 19*91- 6*287)
14= 2*7 +0                                   S =19; T=-6

B: 

m=91, n=287  





($) gcd (252, 198)  N =252, M=198
252 = 1*198+54   54=N-M  36= M-3(N-M) 18=(N-M)-(M-3(N-M))=N-M-M+3N-3M=4N-5M S=4 T=-5
198 = 3*54+36
54= 1*36+18
36= 2*18+0
Gcd = 18


(15)	least Common Multiple 
					
▪ Definition: The least common multiple of the positive integers a and b is the smallest positive integer that is divisible by both a and b. It is denoted by lcm(a,b).
					
▪ The least common multiple can also be computed from the prime factorizations: If the prime factorizations of a and b are: 
				
where each exponent is a nonnegative integer, and where all primes occurring in either prime factorization are included in both. 
				
		
#  congruence
					
(1)Bézout’s Theorem 
			
▪ If 𝑎 and 𝑏 are positive integers, then there exists integers 𝑠 and 𝑡 such that gcd 𝑎,𝑏 =𝑠𝑎+𝑡𝑏
					
▪ The coefficients 𝑠 and 𝑡 are called Bézout’s coefficients ▪ Named after Etienne Bézout
					
▪ We can find these coefficients using a modified form of the Euclidean algorithm 
			
(2) Finding Bézout’s coefficients 			
					
▪gcd (252,198) =18 
▪ 252 = 1 ⋅ 198 + 54				
▪ 198 = 3 ⋅ 54 + 36 
▪ 54 = 1 ⋅ 36 + 18 
▪ 36 = 2 ⋅ 18 

(3)				
Linear Congruence 
					
▪Hastheform𝑎𝑥≡𝑏 𝑚𝑜𝑑𝑚 ▪ 𝑚 ∈ Z+
					
▪ 𝑎, 𝑏 ∈ Z
▪ 𝑥 is an integer variable
					
▪ Can solve for 𝑥 using 𝑎ത𝑎 ≡ 1 (𝑚𝑜𝑑 𝑚) ▪ 𝑎ത is the inverse of 𝑎
					
▪ Requires 𝑎 and 𝑚 to be relatively prime ▪ Otherwise there may not be a solution 

PROOF
				
▪Letgcd𝑎,𝑚 =1
▪ Then 𝑠𝑎 + 𝑡𝑚 = 1 or 𝑠𝑎 + 𝑡𝑚 ≡ 1 (𝑚𝑜𝑑 𝑚) ▪ But 𝑡𝑚 ≡ 0 (𝑚𝑜𝑑 𝑚)
▪ Thus 𝑠𝑎 ≡ 1 (𝑚𝑜𝑑 𝑚) and 𝑠 is an inverse of 𝑎 

(4) Solving a linear congruence 
					
▪ To solve 𝑎𝑥 ≡ 𝑏 (𝑚𝑜𝑑 𝑚)
▪ Find the Bézout coefficients 𝑠 and 𝑡 for sa + t𝑚 = 1
					
▪ Multiply both sides by 𝑠
▪ 𝑠𝑎 reduce to 1 leaving 𝑥 ≡ 𝑠𝑏 (𝑚𝑜𝑑 𝑚) 
				
		 	 	 		
			
				
					
▪ Solve 3𝑥 ≡ 4 (𝑚𝑜𝑑 7)
					
▪ Find the Bézout coefficients of 3 and 7
 ▪7=2⋅3+1
					
▪ 1 = −2 ⋅ 3 + 1 ⋅ 7
 ▪ 𝑎’ = − 2
					
▪ Multiply by 𝑎’

 ▪−2⋅3𝑥≡−2⋅4 𝑚𝑜𝑑7 
▪ 𝑥 ≡ −8 ≡ 6 (𝑚𝑜𝑑 7) 
				
(5) 				
Fermat’s Little Theorem 
				
▪ If 𝑝 is prime and 𝑎 is an integer not divisible by 𝑝 then ▪𝑎𝑝−1 ≡1(𝑚𝑜𝑑𝑝)
▪𝑎𝑝 ≡𝑎(𝑚𝑜𝑑𝑝)
					
▪ Note that this doesn’t say anything about what happens if 𝑝 is composite
					
▪ The proof is outlined in Exercise 4.4.19
					
▪ Don’t confuse this with Fermat’s Last Theorem

▪ 𝑎𝑛 + 𝑏𝑛 = 𝑐𝑛 has positive integer solutions only when 𝑛 = 1 or 𝑛 = 2 

EG: 			
▪ Find 7^(222) 𝑚𝑜𝑑 11		
					
▪ Note that 7^(10) ≡ 1 (𝑚𝑜𝑑 11)
							
222 10⋅22+2 10 22 2 22

▪7^(222)=7^(10*22+2)  =(7^(10))^22* 7 ^2 = 1^22 *7^2 = 49 ≡1⋅49≡5(𝑚𝑜𝑑11) 

(7^(10))^k = 1 (mod  11) 

				
#a*n = 1 ( mod m) 
 inverse  n,m 互为质数是inverse


# n*a = k(mod m) 
coungruence     n,m 互为质数有解，否则无解
			
		
# number representations 
				
▪ Integer Representations ▪ Base b Expansions
					
▪ Binary Expansions

▪ Octal Expansions

▪ Hexadecimal Expansions
					
▪ Base Conversion Algorithm

▪ Algorithms for Integer Operations 
				
（1） binary 				
▪ The binary, or base 2, expansion, uses the digits 0 and 1 only. 
			
▪ (1 0101 1111)2 =
1∙28 + 0∙27 + 1∙26 + 0∙25 + 1∙24 + 1∙23 + 1∙22 + 1∙21 + 1∙20 =351. 
				
(2) octal			
					
▪ The octal expansion (base 8) uses the digits {0,1,2,3,4,5,6,7}.
					
▪ Exercise: What decimal number equals (7016)8? ▪ 7∙83 + 0∙82 + 1∙81 + 6∙80 = 3598 
				
(3) hexadecimal 			
					
▪ The hexadecimal, or base 16, expansion uses {0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F} for digits.
					
▪ (A)16 through (F)16 represent (10)10 through (15)10.
▪ Exercise: What decimal number equals (2AE0B)16 ?
					
▪ 2∙164 + 10∙163 + 14∙162 + 0∙161 + 11∙160 =175627
				
			
(4) convert
		
▪ Binary to octal: replace 3-bit blocks with octal digit
 ▪ Example:
					
(11111010111100)2 

 (011 111 010 111 100)2      
  			
( 3 7 2 7 4)8 	
					
▪ Octal to binary: replace octal digit with 3-bit binary equivalent		
					
▪ Example: 
(37274)8
			
( 3 7 2 7 4)8 

(011 111 010 111 100)2 
				
▪ Binary to hexidecimal: replace 4-bit blocks with hexidecimal digit

▪ Example:

(11111010111100)2 

(0011 1110 1011 1100)2
					
( 3 E B C)16 
					
▪ Hexidecimal to binary: replace hexidecimal digit with 4-bit blocks with binary block
					
▪ Example:
(3EBC)16 

( 3 E B C )16
					
(0011 1110 1011 1100)2 
				
(5) 加减 乘除

二进制

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2020.43.26.png)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2020.46.57.png)
				
			
八进制

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2020.44.28.png)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2020.47.24.png)


十六进制

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2020.45.09.png)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2020.47.53.png)		
			
		
	
# 代表题：

notation （ big-oh , big- omega, big- theta) 

(a)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2022.33.04.png)

(b)
![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2022.33.15.png)

(c) 
![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2022.33.51.png)

E 方法 + B 方法 + linear congruence 方法

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2021.38.38.png)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-06-05%2021.38.48.png)

![](https://github.com/linbearababy/Discrete-structures-in-Computer-Science/blob/master/PICTURE/IMG_7119.jpg)

# summary： 

大题：				
Practice 卷子  （抄题 因为这次的大题类型不变，而且选择题也会很有用）
> 二进制，八进制，十六进制，是进制的相互转换；以及他们的加减和相乘
>证明是big-theata
>用E和B方法找gcd
>linear congruence 
作业题（题型）

选择： 
概念：
 
	（1）  big-oh: 
                  ▪ Such that 𝑓 𝑛 ≤ 𝑐 ⋅ 𝑔(𝑛) for all 𝑛 ≥ 𝑛0	

 		Big-omega
		     ▪ Such that 𝑓 𝑛 >= 𝑐 ⋅ 𝑔(𝑛) for all 𝑛 ≥ 𝑛0	

		Big- theta 
      		     ▪ 𝑓(𝑛) = Θ(𝑔(𝑛)) iff ▪ 𝑓(𝑛) = 𝑂(𝑔(𝑛)) and ▪ 𝑓(𝑛) = Ω(𝑔(𝑛))  n>= k , c1,c2


(2) inverse & Congruence

		#a*n = 1 ( mod m) 
		 inverse  n,m 互为质数是inverse


		# n*a = k(mod m) 
		coungruence     n,m 互为质数有解，否则无解


(3) 	mod （余数 c = a mod b 且 余数c 不能是负数） 
	vs modula (mod m) ( a=b(mod m) a-b = k*m)	这两个不是一个概念

另外： a = b (mod m ) ------- a -b = k*m (看有没有k存在） ----------- a mod m = b  mod m  看等号两边是否相等）

		Eg: 
		22 = 67 （mod 5) 
		相当于 22 mod 5 = 67 mod 5

(4) 判断二进制， 八进制， 十六进制

	▪ The binary, or base 2, expansion, uses the digits 0 and 1 only. 

	▪ The octal expansion (base 8) uses the digits {0,1,2,3,4,5,6,7}.

	▪ The hexadecimal, or base 16, expansion uses {0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F} for digits.


(5) 整除的概念： （ | ）	

	▪ Definition: If a and b are integers with a ≠ 0, then a divides b if there exists an integer c such that b = ac.
	▪  When a divides b we say that a is a factor of b, or a is a divisor of b and that b is a multiple of a.
	▪  The notation a | b denotes that a divides b.
 					
▪  If a | b, then b/a is an integer.
 			
▪  If a does not divide b, we write a ∤ b.

						 
If a | b and a | c, then a | (b + c);
 						
						 							
If a | b, then a | (bc) for all integers c;
 						
						 							
If a | b and b | c, then a | c.
If a not | b ,and a not | c, then a  not  | bc (false) 

If a not | b, then gcd (a,b) =1. (false)				
			
		
(6) 
If 2^(n -1) is not prime then n is not prime (false) 				
			
		
(7) 7^(10001) = 1 ( mod 11)		
			
	Note that 7^(10) ≡ 1 (𝑚𝑜𝑑 11)
	▪𝑎^(𝑝−1) ≡1(𝑚𝑜𝑑𝑝)
	▪𝑎^𝑝 ≡𝑎(𝑚𝑜𝑑𝑝)


