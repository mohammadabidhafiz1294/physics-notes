***Q:*** Find the secret string s if 

    f(00)=0  
    f(01)=1  
    f(10)=1  
    f(11)=0.

Write your answer directly without any quotation mark etc. Ex: 00

*Solutions*:
	To find the secret string \( s \) in the context of the Bernstein-Vazirani algorithm, we need to understand that \( f(x) \) is given by:

$f(x) = s \cdot x \mod 2$

where \( s \) is the secret \( n \)-bit string, and $\cdot$ denotes the bitwise dot product.

Given the function values:

- \( f(00) = 0 \)
- \( f(01) = 1 \)
- \( f(10) = 1 \)
- \( f(11) = 0 \)

We can set up equations to determine \( s \). Let's denote the bits of \( s \) as \( s = $s_1s_0$ \).

1. For \( x = 00 \):
   $$f(00) = s_1 \cdot 0 + s_0 \cdot 0 = 0$$ 
   This equation doesn't give any information about \( $s_1$ \) and \( $s_0$ \).

2. For \( x = 01 \):
    $$f(01) = s_1 \cdot 0 + s_0 \cdot 1 = s_0 \equiv 1 \mod 2$$
   Thus, \( $s_0$ = 1 \).

3. For \( x = 10 \):
   $$f(10) = s_1 \cdot 1 + s_0 \cdot 0 = s_1 \equiv 1 \mod 2$$
   Thus, \( $s_1$ = 1 \).

4. For \( x = 11 \):
	$$f(11) = s_1 \cdot 1 + s_0 \cdot 1 = s_1 + s_0 \equiv 0 \mod 2$$ 
   Given that \( $s_0$ = 1 \) and \( $s_1$ = 1 \), we have:
   \[ 1 + 1 \equiv 0 \mod 2 \]
   This equation is satisfied and consistent with \( $s_0$ = 1 \) and \( $s_1$ = 1 \).

Hence, the secret string \( s \) is \( $11$ \).

The secret string \( s \) is:

\[ $s = 11$ \]

This matches the given function values for ( $f(x)$).