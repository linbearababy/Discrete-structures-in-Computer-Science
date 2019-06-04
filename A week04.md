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

