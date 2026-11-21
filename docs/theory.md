# Theory: Types of Overround

## Definitions

We have an event, with $n$ mutually exclusive outcomes, indexed by $i = 1, 2, \ldots, n$.

| <div style="width:100px">Symbol</div> | Meaning |
| --- | --- |
| $p_i$ | The true probability of outcome $i$ occurring. since mutually exclusive, $\displaystyle\sum_{i=1}^{n} p_i = 1$. Also, $p_i > 0$ for all $i$. |
| $o_i = \frac{1}{p_i}$ | The fair, decimal odds for outcome i. These will be modified in all kinds of ways in the different methods, to become $o_i'$. |
| $s_i$ | The total stake from all bettors, the BM receives on outcome $i$. |
| $o_i' = \frac{1}{p_i'}$ | The modified odds for outcome $i$, which may be different from the fair odds $o_i$, with their own implied probabilities $p_i' = 1 / o_i'$. |
| $B = \displaystyle\sum_{i=1}^{n} p_i'$ | The Booksum. |
| $B - 1$ | The overround. |

| <div style="width:100px">Abbreviations</div> | Meaning |
| --- | --- |
| BM | Bookmaker |

We will look at mainly these 2 expected values, each in the two variants "on outcome $i$" and "summed over the whole event".

| <div style="width:100px">Expected value</div> | on outcome $i$ | summed over the event |
| --- | --- | --- |
| $\mathbb{E}[\text{payout}]$ | $p_i \, s_i \, o_i'$ | $\displaystyle\sum_{i=1}^{n} p_i \, s_i \, o_i'$ |
| $\mathbb{E}[\text{profit for the BM}]$ | $s_i \left( 1 - p_i \, o_i' \right)$ | $\displaystyle\sum_{i=1}^{n} s_i \left( 1 - p_i \, o_i' \right)$ |


## Methods

### (0) Fair Odds

### (1) Multiplicative Overround



### (2) Additive Overround


$$
p_i' = p_i + m \qquad \text{with} \qquad 0 < m < 1 - \max_i p_i
$$


- => $o_{i, add}' = \dfrac{1}{p_i + m}$
- => $B = \sum_{i=1}^{n} (p_i + m) = 1 + n \, m$
- => $B - 1 = n \, m$


$$
\begin{aligned}
\mathbb{E}[\text{payout on event}] &= \sum_{i=1}^{n} p_i s_i o_i' = \sum_{i=1}^{n} \frac{p_i \, s_i}{p_i + m} = \sum_{i=1}^{n} \underbrace{\frac{s_i}{1 + \frac{m}{p_i}}}_{\le \, s_i} \\

&\implies \text{expected payout always smaller than stake }
\\

\mathbb{E}[\text{profit BM on event}] &= \sum_{i=1}^{n} s_i - \mathbb{E}[\text{payout on event}] = \sum_{i=1}^{n} s_i \left( 1 - \frac{p_i}{p_i + m} \right) = \sum_{i=1}^{n} s_i \, \frac{m}{p_i + m} \\

&\implies \text{expected profit always > 0 }
\end{aligned}
$$


### (3) Exponential Overround
