notation

⇒

⇔ - If and only if - shortened to iff

A⇒B conitional

B⇒A Inverse not neccesarily true

A'⇒B' 

B'⇒A' : Always true


# Types of Proofs
 
## Proof by Deduction

## Proof by Exhaustion

## Proof by Induction
Eg.
assuming its trueto prove true
$$\Sigma_{k=1}^n = \frac{k(k+1)(2k+1)}{6}$$
Base case: let n=1
$$ \text{for } n = 1\text{, } left = 1^2-1= 1\text{, } right = \frac{1*2*3}{6} = 1$$

assume true for n = k
shows true for n + k + 1 -> want to show that sum of n^2 for 

let n = k+1
we are proving that this is true
$$\Sigma ^{k+1}_{n=1}n^2 = \Sigma ^{k}_{n=1}n^2+(k+1)^2$$
$$=\frac{k(k+1)(2k+1)}{6}+(k+1)^2$$
 $$=\frac{1}{6}(k+1)(k(2k+1)+6(n+1))$$
 $$=\frac{1}{6}(k+1)(2k+3)(k+3)$$
	since 
$$\Sigma ^{k+1}_{n=1}n^2 = \frac{(k+1)((k+1)+1)(2(k+1)+1)}{6} = \frac{1}{6}(k+1)(2k+3)(k+3)$$
	therefore
$$=\frac{1}{6}(k+1)(2k+3)(k+3)\equiv\Sigma ^{k+1}_{n=1}n^2$$ therefore 
conclusion