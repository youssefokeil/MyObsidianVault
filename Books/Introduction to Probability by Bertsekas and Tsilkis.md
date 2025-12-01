Author: [[Bertsekas & Tsilkis]]
Type: #TextBook 
Fields: #probability 
# Introduction to Probability by Bertsekas and Tsilkis 📚

## Chapter 1

### Probabilistic Models:
- **sample space $\Omega$** : set of all possible outcomes of an experiment
- **probability law**: assigns to a set $A$ of possible outcomes (called an **event**) a non-negative number $P(A)$ called the probability of $A$.

Every probabilistic model has an underlying process called an *experiment*, the set of all possible outcomes of said experiment is what we call the *sample space* and a subset of the sample space is called an *event*.
> NB: different elements of sample space should be *mutually exclusive* and *collectively exhaustive*. Meaning you can neither have an outcome from a die that is "1 or 3" nor that is outside of the sample space like 7. 

#### Sequential Models
Many experiments have a sequential character, such as tossing a coin two or three times. 

![[Pasted image 20251013125541.png]]

### Probability Law
specifies the likelihood of an outcome or any set of possible outcomes. It assigns to every event $A$ a number called $P(A)$, called probability of $A$ satisfying those axioms.

**Probability Axioms:**
1. *(Nonnegativity)* $P(A) \geq 0$, for every event A
2. *(Additivity)* If $A$ and $B$ are two disjoint events, then probability of their union is $P(A \cup B)= P(A) + P(B)$ 
3. *(Normalization)* the probability of entire sample space $\Omega$ is equal to 1 $P(\Omega)=1$

> NB: you usually use common sense assumptions about a model, like that heads and tails are "equally likely".

### Properties of Probability Laws:
(a) If $A \subset B$, then $\mathbf{P}(A) \leq \mathbf{P}(B)$.
(b) $\mathbf{P}(A \cup B)=\mathbf{P}(A)+\mathbf{P}(B)-\mathbf{P}(A \cap B)$.
(c) $\mathbf{P}(A \cup B) \leq \mathbf{P}(A)+\mathbf{P}(B)$.
(d) $\mathbf{P}(A \cup B \cup C)=\mathbf{P}(A)+\mathbf{P}\left(A^c \cap B\right)+\mathbf{P}\left(A^c \cap B^c \cap C\right)$.
### Discrete Probability Law
If the sample space consist of finite number of possible outcomes, then probability law is specified by probabilities the events that consist of a  single element. The probability of any event $\{s_1, s_2, \ldots, s_n\}$ is the sum of probabilities of its elements.  
 $$\mathbf{P}\left(\left\{s_1, s_2, \ldots, s_n\right\}\right)=\mathbf{P}\left(\left\{s_1\right\}\right)+\mathbf{P}\left(\left\{s_2\right\}\right)+\cdots+\mathbf{P}\left(\left\{s_n\right\}\right)$$

#### Discrete Uniform Probability Law
If the sample space consists of $n$ possible outcomes which are equally-likely.
$$P(A)=\frac{\text{Number of elements of A}}{n}$$ 

### Continuous Probability Law
here the probability of single-element events aren't sufficient to characterize a probability law.

### Conditional Probability
provides way to reason the outcome of an experiment based on *partial information*. 

Concretely, for a given sample space, if we know that the outcome belongs to event $B$. What is the likelihood that the outcome also belongs to event $A$. 
Denoted by $P(A|B)$.

$$P(A|B)=\frac{P(A \cap B)}{P(B)}$$
> Conditional probabilities can be viewed as probability law on a new universe $B$, because all of the conditional probability is concentrated on $B$.

> It is often convenient to use conditional probabilities first to determine unconditional probabilities using $P(A \cap B)=P(B)P(A|B)$, when the problem has a sequential manner.

### Total Probability Theorem & Bayes' Rule
#### The Total Probability Theorem
For partitions $A_{1}, A_{2}, \ldots , A_n$ that span the whole sample space (each outcome is one and only one of the disjoint events), the probability of $B$ is given by.

$\begin{aligned} \mathbf{P}(B) & =\mathbf{P}\left(A_1 \cap B\right)+\cdots+\mathbf{P}\left(A_n \cap B\right) \\ & =\mathbf{P}\left(A_1\right) \mathbf{P}\left(B \mid A_1\right)+\cdots+\mathbf{P}\left(A_n\right) \mathbf{P}\left(B \mid A_n\right) .\end{aligned}$

![[Pasted image 20251013151553.png]]
*Visualization of The Total Probability Theorem*

#### Bayes' Rule
using $A_{1}, A_{2}, \ldots , A_n$ partitions of the sample space, for any event B we have 

$\begin{aligned} \mathbf{P}\left(A_i \mid B\right) & =\frac{\mathbf{P}\left(A_i\right) \mathbf{P}\left(B \mid A_i\right)}{\mathbf{P}(B)} \\ & =\frac{\mathbf{P}\left(A_i\right) \mathbf{P}\left(B \mid A_i\right)}{\mathbf{P}\left(A_1\right) \mathbf{P}\left(B \mid A_1\right)+\cdots+\mathbf{P}\left(A_n\right) \mathbf{P}\left(B \mid A_n\right)}\end{aligned}$

> Bayes' Rule is used for *inference*, we have a lot of "causes" that lead to "effects". By getting the effect, we wish to find the possible cause. 
> 
> For the effect $B$ and possible causes $A_{1}, A_{2}, \ldots , A_n$. We have $P(B|A_i)$ as the probability the effect $B$ will be observed given this cause $A_i$, we then run the above equation for every $A_i$ for $i=1,2,3, \dots$ we infer the probability the cause $A_i$ happened, given that effect $B$ was observed --> $P(A_i|B)$.

### Independence
> When the occurrence of $B$, provides no information and doesn't alter the probability that $A$ has occurred.

$$P(A|B)=P(A)$$
We say that $A$ and $B$ are *independent events*, if and only if:
$$P(A \cap B)=P(A)P(B)$$
#### Conditional Independence
Conditional probabilities of events, meaning that given an event $C$, the events $A$ and $B$ are called conditionally independent if.

$$
\mathbf{P}(A \cap B \mid C)=\mathbf{P}(A \mid C) \mathbf{P}(B \mid C)
$$

The definition of the conditional probability and the multiplication rule yield
$$
\begin{aligned}
\mathbf{P}(A \cap B \mid C) & =\frac{\mathbf{P}(A \cap B \cap C)}{\mathbf{P}(C)} \\
& =\frac{\mathbf{P}(C) \mathbf{P}(B \mid C) \mathbf{P}(A \mid B \cap C)}{\mathbf{P}(C)} \\
& =\mathbf{P}(B \mid C) \mathbf{P}(A \mid B \cap C) .
\end{aligned}
$$
This yields
$$P(A|B \cap C) = P(A|C) $$
Meaning that if we know that $C$ occurred and we exist in a universe where $C$ occurred, then the knowledge about the existence of $B$ doesn't change the probability of the occurrence of $A$.
> If $A$ and $B$ are independent, so are $A$ and $B^c$

#### Independence of a Collection of Events:
$\mathbf{P}\left(\bigcap_{i \in S} A_i\right)=\prod_{i \in S} \mathbf{P}\left(A_i\right)$
for every subset $S$ of $\{1,2, \ldots, n\}$.

If we have a collection of three events, $A_1, A_2$, and $A_3$, independence amounts to satisfying the four conditions
$$
\begin{aligned}
\mathbf{P}\left(A_1 \cap A_2\right) & =\mathbf{P}\left(A_1\right) \mathbf{P}\left(A_2\right), \\
\mathbf{P}\left(A_1 \cap A_3\right) & =\mathbf{P}\left(A_1\right) \mathbf{P}\left(A_3\right), \\
\mathbf{P}\left(A_2 \cap A_3\right) & =\mathbf{P}\left(A_2\right) \mathbf{P}\left(A_3\right), \\
\mathbf{P}\left(A_1 \cap A_2 \cap A_3\right) & =\mathbf{P}\left(A_1\right) \mathbf{P}\left(A_2\right) \mathbf{P}\left(A_3\right) .
\end{aligned}
$$
The first three laws are called *pairwise independence*, and they don't imply the third.

This implies that knowledge of any event doesn't change our initial beliefs about the other two events. Given the independence of 4 events we obtain:
$$ \mathbf{P}\left(A_1 \cup A_2 \mid A_3 \cap A_4\right)=\mathbf{P}\left(A_1 \cup A_2\right) $$ or $$ \mathbf{P}\left(A_1 \cup A_2^c \mid A_3^c \cap A_4\right)=\mathbf{P}\left(A_1 \cup A_2^c\right) ; $$
### (Applications) Reliability
To analyze and model complex systems, it's often easier to assume the independence of the components. For example for *network components* with the following:
![[Pasted image 20251013172859.png]]\
for each component $i=1,2,\ldots$ the probability of success is $p_i$.
**For series connection**
probability of success means that every component is successful in the series connection
$$P(\text{series subsystem})=p_1p_{2}\dots p_m$$
**For parallel connection**
probability of success is the probability that any of the components succeeds
$$P(\text{parallel subsystem succeeds})= 1 - (1-p_1)(1-p_{2})\ldots(1-p_m)$$
Meaning its the converse of the probability of all components failing.

### Independent Trials and Bernoulli Trials
When the experiment is a sequence of independent but identical stages we have what we call *independent trials*, in the case where there is only two outcomes possible for each trial we have what we call *Bernoulli trials*.
$$p(k)=\binom{n}{k} p^k(1-p)^{n-k}$$
the $\binom{n}{k}$ is called *binomial coefficients* and $p(k)$ are called *binomial probabilities*.
#### The binomial formula
we know that $p(k)$ for every $k$ must add to 1, so we yield

$$\sum_{k=0}^{n} \binom{n}{k} p^k(1-p)^{n-k}=1$$
### Counting
I am very familiar of the counting principles of probability, so here's a simple summary.
- Permutations of $n$ objects: $n!$
- $k-$permutations of $n$ objects: $\Large{\frac{n!}{(n-k)!}}$
- combinations of $k$ out of $n$ objects, also called *binomial coefficient*: $\Large\binom{n}{k}= \frac{n!}{k!(n-k!)}$
- Partitions of $n$ objects  into $r$ disjoint groups with $i^{th}$ group having $n_i$ objects, also called the *multi-nomial coefficient* $\Large\binom{n}{n_1,n_2,\ldots,n_{r}}= \frac{n!}{n_{1}!n_{2}! \cdots n_{r}!}$
--------
## Chapter 2: Discrete Random Variable

### Random Variable
is a real-valued *function* of the experimental outcome.
- A discrete random variable has an associated *probability mass function (PMF)*, which gives the probability of every numerical value.
- A *function of a random variable* defines another random variable, whose PMF can be obtained from the PMF of the original random variable.
**Examples**
1. in an experiment involving two rolls of a die, it is the sum of two rolls.
2. In an experiment of 5 tosses of a coin, the number of heads in sequence is a random variable.
### Probability Mass Function
probability mass of $x$: $p_{x}(x) = P({X=x})$ is probability of event where all outcomes give rise to $X$ equal to $x$.

### Bernoulli Random Variable:
takes two values 1 and 0, one with the probability $p$ and the other with probability $(1-p)$.
**For heads or tails experiment:**
$$
X = \begin{cases} 1 & \text{if a head,} \\ 0 & \text{if a tail.} \end{cases}
$$
$$
p_X(x) = \begin{cases} p & \text{if } x=1, \\ 1-p & \text{if } x=0. \end{cases}
$$
### The Geometric Random Variable
The geometric random variable is the number X of tosses needed for a head to come up for the first time. Its PMF is given by
$$
p_X(k) = (1-p)^{k-1}p, \quad k=1, 2, \dots
$$
Why? because the first $k-1$ trials must yield tails, so that the $k^{th}$ trial would yield a head for the first time.
> Generally it's the repeated independent trials until the *first "success"*. Each trial has a probability of success $p$.

### Poisson Random Variable
>Poisson random variables are binomial random variables with very small $p$ and very large $n$. 

Like number of cars involved in an accident, number of typos in a book. You can model a mistyped word as a coin that is heads when a typo happens.
$$
\sum_{k=0}^{\infty} e^{-\lambda} \frac{\lambda^k}{k!} = e^{-\lambda} \left(1 + \lambda + \frac{\lambda^2}{2!} + \frac{\lambda^3}{3!} + \dots\right) = e^{-\lambda} e^{\lambda} = 1.
$$
>More precisely, a Poisson PMF with parameter $\lambda$, is a good approximation of $\lambda=np$ for *very large n* and *very small p*. 
$$
e^{-\lambda} \frac{\lambda^k}{k!} \approx \frac{n!}{(n-k)!k!} p^k (1-p)^{n-k}, \quad k = 0, 1, \dots, n.
$$
### Expectation, Mean & Variance
> *Expectation/Mean:* a weighted (in proportion to probabilities) average of possible values of $X$.

Think of spinning the wheel, you've got probabilities for every part of the wheel with a value associated to every probability. The *expected value* is the value you'll get on average if you spin the wheel multiple times and average the results.

#### Center of Gravity interpretation
There is a pretty intuitive way to understand *expectations* by imagining it as center of gravity. 

![[Pasted image 20251019145821.png|600, c]]

> *Variance:* provides a measure of dispersion of $X$ around its mean. It's defined as the expected value of random variable $(X-E[X])^2$ 
$$var(X)=E[(X-E[X])^2]$$
> NB: *Vartiance in Terms of Moments Expression*, is a convenient formula for variance of random variable $X$.
$$var(X)=E[X^2]-(E[X])^2$$
> *Standard Deviation:* is another measure of dispersion, defined below. Is easier to interpret, because it has same units as $X$.
$$
\sigma_X = \sqrt{\text{var}(X)}.
$$
### Joint PMFs
Multiple random variables and their joint and conditional PMFs, and associated expected values. 

1. *Joint PMF*: 
	determines the probability of any random variable specified by $X$ and $Y$
$$p_{X,Y}(x,y)=p_{y}(y)p_{X|Y}(x|y)$$
can be extended further to three or more random variables 
$$p_{X,Y,Z}(x,y,z)=p_{Y}(y)p_{Y|Z}(y|z)p_{X|Y,Z}(x|y,z)$$
2. *Marginal PMF*
$$
p_x(x)=\sum\limits_{y}p_{X,Y}(x,y)
$$
$$
p_y(y)=\sum\limits_{x}p_{X,Y}(x,y)
$$
![[Pasted image 20251101170654.png]]
## Chapter 3: Continuous Random Variables
A random variable $X$ is called **continuous** if its probability law can be described in terms of a non-negative function $f_X$, called the **probability density function** of $X$, or PDF for short, which satisfies
$$
\mathbf{P}(X \in B) = \int_B f_X(x) \,dx,
$$
For any single value a, we get $$
\mathbf{P}(X=a) = \int_{a}^{a} f_X(x) dx = 0.
$$
> To qualify as a PDF, the function must be non-negative $f(x)\geq 0$ for every $x$ and must satisfy the normalization constraint:
> $$\int_{-\infty}^{\infty} f_X(x) dx = 1$$ 

To interpret the PDF, we get  
$$\int_{x}^{x+\delta} f_X(t) dt \simeq f_X(x).\delta$$
### Expectation
The expectation of $X$ is:
 $$E[X]=\int_{-\infty}^{\infty} xf_X(x) dx $$
 The expectation of $g(X)$ has the form:
  $$E[g(X)]=\int_{-\infty}^{\infty} g(x)f_X(x) dx $$
 The variance is calculated by:
 $$\operatorname{var}(X)=\mathbf{E}\left[(X-\mathbf{E}[X])^2\right]=\int_{-\infty}^{\infty}(x-\mathbf{E}[X])^2 f_X(x) d x$$ 

### The Exponential Random Variable
The exponential random variable takes the form:
$$f_X(x)= \begin{cases}\lambda e^{-\lambda x} & \text { if } x \geq 0 \\ 0 & \text { otherwise }\end{cases}$$
It can be a very good model for the amount of time until *equipment breaks down*, until a *light bulb burns out* or an accident occurring.

### Cumulative Distribution Functions:
$F_X(x)=\mathbf{P}(X \leq x)= \begin{cases}\sum_{k \leq x} p_X(k) & X: \text { discrete } \\ \int_{-\infty}^x f_X(t) d t & X: \text { continuous }\end{cases}$
To describe all kinds of random variables with a single mathematical concept. It "accumulates" probability up to a value of $x$.

#### PMF from CDF
$p_X(k)=\mathbf{P}(X \leq k)-\mathbf{P}(X \leq k-1)=F_X(k)-F_X(k-1)$

#### PDF from CDF
$\begin{aligned} F_X(x) & =\int_{-\infty}^x f_X(t) d t \\ f_X(x) & =\frac{d F_X}{d x}(x)\end{aligned}$

>Sometimes, in order to calculate the PMF or PDF of a discrete or continuous random variable, respectively, it is more convenient to first calculate the CDF and then use the preceding relations.