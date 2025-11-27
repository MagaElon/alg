# alg
algorithm

---


**2- Consider functions** ( f_1, f_2, g : \mathbb{N} \to \mathbb{R} ) **which are asymptotically positive.
Show that if** ( f_1 = O(f_2) ) **then** ( f_1 + f_2 = \Theta(f_2). )

We must find (1) ( c > 0, n_0 \in \mathbb{N} ) such that
( f_1(n) + f_2(n) \le c , f_2(n) ) for all ( n \ge n_0 )
and (2) ( c' > 0, n_0' \in \mathbb{N} ) such that
( f_1(n) + f_2(n) \ge c' , n , f_2(n) ) for all ( n \ge n_0'. )

---

### (1)

Since ( f_1 = O(f_2) ) we have that
( f_1(n) \le c , f_2(n), n \ge \hat{n} ) for some ( c, \hat{n} ).
Therefore, we have:

[
f_1(n) + f_2(n) \le c f_2(n) + f_2(n) = (c + 1) f_2(n).
]

We can take ( c = \hat{c} + 1 ) and ( n_0 = \hat{n}. )

---

### (2)

We have again by assumption ( f_1(n) \le c , f_2(n), n \ge \hat{n} ),
which implies ( f_2(n) \ge \frac{1}{c} f_1(n) ).

Then:

[
f_1(n) + f_2(n) \ge \frac{1}{c} f_1(n)
]

for some ( n ) large enough since ( f_1(n) ) is asymptotically positive.
We thus take ( n_0' ) to be the max of ( \hat{n} ) and ( n_1 )
such that ( f_1(n) \ge 0 ) for ( n \ge n_1 ).
We take ( c' = \frac{1}{c}. )

---


**c. By iteration we obtain:**

[
T(n) = 2 T\left(\frac{n}{2}\right) + 1
]

[
T(n) = 2\left( 2 T\left( \frac{n}{2^2} \right) + 1 \right) = 2^2 T\left( \frac{n}{2^2} \right) + 2
]

[
T(n) = 2^2\left( 2 T\left( \frac{n}{2^3} \right) + 1 \right)
= 2^3 T\left( \frac{n}{2^3} \right) + 3
]

Continuing like this until:

[
\frac{n}{2^i} = 1
]

which implies ( i = \lg(n) ).

Therefore after ( \lg(n) ) iterations we have:

[
T(n) = 2^{\lg(n)} T(1) + \lg(n)
= n \cdot 1 + \lg(n)
]

The runtime of the algorithm is therefore:

[
T(n) = \Theta(n).
]

---

If you want, I can also turn these into **LaTeX**, **typed homework format**, or **clean notes** for studying.
