## Lec 1

### preference lists
properties:
1. completeness
2. transitivity

### Utility Functions
We usually assume each agent has a utility function that assigns a *payoff (utility)* to each outcome.

### Rationality
The central assumption of game theory and economics is that an agent seeks to maximize its utility; such agents are called rational.

### Nash Equilibria
If every agent plays a best response to the other agents' strategies then we are at a **Nash Equilibria**.
- So Nash Equilibria correspond to a **mutual best responses**. (No one has an incentive to change strategy.)
- Because of this stability property, a Nash Equilibria is typically considered to be the natural outcome of the game.

### Mixed strategies
In a mixed strategy, Alice plays a probability distribution $p$ on the rows. Similarly, Bob plays a probability distribution $q$ on the columns.

### Nash Existence Theorem
Any finite game has a Nash Equilibrium.

---

## Lec 2

### Consistency/IIA
Given a feasible set $S$ in $O$, an agent chooses the outcome $f(S)$ in $S$. Then $f$ satisfies the independence of irrelevant alternatives (consistency) condition if:
$$
\forall S'\subset S \subseteq O,
\\ if: f(S) \in S' \subseteq O
\\ then: f(S') = f(S)
$$
If we choose $x$ in $S'$ when given $S$ we must choose $x$ if we are given the smaller set $S'$ instead.

### Rationality Theorem
An agent is rational if and only if its choice function $f$ satisfies the Independence of the Irrelevant Alternatives condition.

### Anchoring
In human decision-making there is a bias to rely (anchor) on one specific piece of information.

---

## Lec 3

### Social Choice theory
The goal of social choice theory is to combine these individual preferences to form a collective set of preferences.

### Social Functions
Typically we want to combine the individual preferences lists to select either a **single winner** or **a complete ordering of the candidates**.

#### Social Choice Function. *[Single Winner]*

#### Social Welfare Function. *[Complete Ordering]*

### Condorcet winner
The Condorcet winner is a candidate that would win in a *pairwise vote with every other candidate*.

### Strategic Manipulable Elections
A social function $f$ is **strategically manipulable** if, for some set $\{\succ_1, \succ_2, ..., \succ_n\}$ of preferences, there is a $\succ_i'$ such that:
$$
f(\succ_1, ..., \succ_i, ..., \succ_n) = a
\\
f(\succ_1, ..., \succ_i', ..., \succ_n) = b
\\
b \succ_i a
$$
So voter $i$ prefers $b$ over $a$, so voter $i$ has in **incentive** to lie.

### Incentive Compatibility
A social choice function that is not manipulable is called incentive compatible. *(Truthtelling is always the best policy (DSIC))*
- Dictatorship
- There isn't other non-manipulable electoral systems.

### Gibbard-Satterthwaite Theorm
Any incentive compatible social choice function is a dictatorship. (If there are least 3 candidates receiving a vote.)

### Arrow's Impossibility Theorem
#### Social Welfare Functions
Two properties we may desire from a social welfare function $g$:
1. **Unanimity**: If every voter prefers $a$ to $b$ then $g$ should output $a$ to $b$.
2. **Consistency/IIA**: The relative position of $a$ and $b$ depends only upon the relative positions of $a$ and $b$ in the voters' preference lists.

#### Theorem
Any social welfare function that satisfies **unanimity** and **IIA** is a dictatorship.

[Proof from the Web](https://en.wikipedia.org/wiki/Arrow%27s_impossibility_theorem#Informal_proof)

---

## Lec 4

### Gibbard-Satterthwaite Theorem
Any incentive compatible social choice function is a dictatorship. (If there are least 3 candidates receiving a vote.)

---

## Lec 5
### The model
- There is a set of potential outcomes $O=\{S_1, S_2, S_3,...\}$.
- Instead of a preference list $\succ_i$ over the outcomes, each agent $i$ has a **monetary value $v_i(S)$** for each outcome $S$ in $O$.
- Each agent $i$ declares a **bid value $b_i(S)$** on each outcome $S$ in $O$.
- Given the bids they selects an outcome.
- Transfer payments are allowed between the agents and the mechanism: agent $i$ pays a price $p_i$. *(Thsi price may be negative)*
- Objectives
    - One natural objective is to **maximize social welfare**, the sum of the utilities of all participants. **maximize social welfare**, the sum of the utilities of all participants.
    - Another natural objective is to **maximize economic efficiency**, the sum of the valuations each participant has for the outcome. **maximize economic efficiency**, the sum of the valuations each participant has for the outcome.
    - These two are the same.

### Multi-Parameter Mechanisms

#### Three Interpretations
1. The utility of a bidder is its marginal contribution to social welfare.
2. The price a bidder pays is the damage it does to others by participating.
3. The price a bidder pays is the lowest bid (best lie) the bidder could have made and still won her assigned package.

### The VCG Mechanism
Given the bids $b$ the mechanism selects the outcome $S^\star$ of maximum welfare:
$$
S^\star(b) = argmax_{S\in O}\sum_j b_j(S)
$$
The mechanism then charges prices such that:
1. The utility of a bidder is its marginal contribution to social welfare.
2. The price a bidder pays is the damage it does to the others by participating.
3. The price a bidder pays is the lowest bid the bidder could have made and still won her assigned package.

---

## Lec 6
#### Example: Bilateral Trade
- There is one seller, values the item as $v_s$.
- There is one buyer, values the item at $v_b$
- The potential outcomes are $O=\{no-trade, trade\}$
- the welfare-maximizing decision is made, they trade if and only if $v_b \geq v_s$
- **Case 1**: $v_b \geq v_s$
Mechanism selects outcome "trade". Social-welfare $W=v_b$
- **Case 2**: $v_b < v_s$
Mechanism selects outcome "no-trade". Social-welfare $W=v_s$
- *So what are the VCG prices?*

##### Method #1 The prices are such that utility of a bidder equals its marginal contribution

###### Case 1 [Trade]
seller:
- $W=v_b$
- $W_{-s}=0$
- $c_s = v_b-0=v_b$
- So the price is:
    - $0-p_s=c_s$
    - $p_s = -v_b$

buyer:
- $W=v_b$
- $W_{-b}=v_s$
- $c_b=v_b-v_s$
- So the price is:
    - $v_b-p_b=v_b-v_s$
    - $p_b=v_s$

##### Method #2 The price equals opportunity cost - the damage caused to others

###### Case 1 [Trade]
seller:
- With the seller, the buyer gets the item of value $v_b$
- Without the seller, the buyer gets nothing.
- So, by participating the seller does $0-v_b=-v_b$ of damage.
- So $p_s=-v_b$

buyer:
- With the buyer, the seller does not keep the item so has zero value.
- Without the buyer, the seller keeps the item keeps the item of value $v_s$.
- So, by participating, the buyer does $v_s-0=v_s$ of damage.
- So $p_b=v_s$

---

## Lec 7

### Mixed Strategy Nash Equilibria (MSNE)
In a MSNE, **every** pure strategy in the support of the mixed strategy of an agent must be a pure best response to the mixed strategies of the other agents.

---

## Lec 8
### Correlated Equilibrium
Given a Nash Equilibrium has been recommended, if you believe the other agents will obey the signal, then it is a best response for you to do so too. This is called a correlated equilibrium.

So the correlated equilibria are given by a set of linear constraints.
The mechanism can optimize over these constraints via a linear program.

The linear constraints imply that correlated equilibrium can generate the larger space of expected payoffs.

---

## Lec 9

---

## Lec 10
