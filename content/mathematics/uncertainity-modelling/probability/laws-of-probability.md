[Home](1%20Introduction.md)

<div style="text-align: justify;">

# Laws of Probability

The theory of probability is a formalization of intuitive ways of describing uncertainties. Probability is a measure defined on a sample space $\mathbb{S}$, an event space $\mathcal{F}$ and σ-algebra. This leads to the following definition, 

> The probability of an event $\mathbb{E}$ in a sample space $\mathbb{S}$ is denoted by $P$, is the measure of the likelihood that $\mathbb{E}$ will occur on a single trial of the corresponding random experiment.

> The probability of an event $\mathbb{E}$ occurs is usually denoted by $P(\mathbb{R})$ or sometimes as $Pr(\mathbb{R})$.

In general, probability of a event is defined as a function which follows certain axioms. These are listed as the Laws of Probability or the Axioms of Probability. 

# Axioms

A probability function, $Pr:\mathcal{F} \rightarrow \mathbb{R}$ that satisfies,

> Normalization or Quantification axiom: $\forall$ $\mathbb{E} \in \mathcal{F}, 0 \leq Pr(\mathbb{E}) \leq 1$. So, the probability of an event is defined between 0 and 1 where $Pr(\mathbb{E})=0$ denotes that the event is improbable and $Pr(\mathbb{E})=1$ denotes that the event is certain. 

> $Pr(\mathbb{S}) = 1$ and $Pr(\emptyset) = 0$. If we think about this, the entire sample space can be also considered as a event.

> For any finite or countably infinite set of pairwise disjoint events, $\mathbb{E}_1, \mathbb{E}_2,...,\quad$ $Pr(\cup_{i\geq1}$ $\mathbb{E}_i) = \Sigma_{i\geq1}$ $Pr(\mathbb{E}_i)$

# Conditional Probability

Conditional probability is relevant when the occurrence of two events is dependent on each other. In simpler terms, it defines ``how the likelihood of one event changes given that another event has already occured``. It is denoted as $Pr(A|B)$, indicating the probability of event $A$ given the occurrence of event $B$. For instance, in the scenario where two dice are rolled, $Pr(\text{sum is even}|\text{first is odd})$ represents the probability that the sum of the outcomes of the two dice is even, given that the outcome of the first die is odd. ``A crucial aspect of conditional probability is that it introduces a specific condition, modifying the sample space for computing probabilities``. The probability calculation is based on the revised or constrained set of possible outcomes defined by the given condition.

When computing $P(A|B)$ for events $A$ and $B$ within the sample space $\mathbb{S}$, the sample space is restricted to include only those events in $\mathbb{S}$ where event $B$ has occurred. In other words, the probability calculation is performed within the subset of the sample space defined by the occurrence of event $B$.This gives the formal definition,
> $Pr(A|B) = Pr(A \cap B)/Pr(B)$

# Independence

Two events are said to be independent if the occurrence of one event does not influence the likelihood of the occurrence of the other event, and vice versa. Thus, an event $A$ does not depend on an event $B$ if and only if $Pr(A|B) = Pr(A)$. This gives the formal definition, 
> $Pr(A \cap B) = Pr(A) \cdot Pr(B)$. 

# Improbable vs Impossible

</div>
<br>
<div style="display: flex;justify-content: space-between; text-align: end;">
<div></div>
<div>

[Previous](Probability.md)</div>
<div style="text-align: end;">

[Next](distribution-and-density-functions.md)</div>
</div>