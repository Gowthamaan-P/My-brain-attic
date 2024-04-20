[Home](../Uncertainity%20Modelling.md)

<div style="text-align: justify;">

# Probability

The theory of probability is a formalization of intuitive ways of describing uncertainties.Uncertainty is one of the inescapable truths in the analysis of processes and measurements. The sources of uncertainty in data-driven modeling are primarily 

* Insufficient understanding of the process (modeling errors)
* Measurement errors
* Effects of unmeasured causes. 

The second source, is in fact, a manifestation of our inability to perfectly design and understand the instrumentation and its characteristics. All sources of uncertainty in a process lead to the same repercussion - that it is not possible to accurately predict  that process. Then we have what is known as a random process. To complement this  definition, it is useful to define, a perfectly predictable process (within the walls of theoretical analysis), known as the deterministic process that generates a deterministic signal. Strictly such processes are never encountered in practice. However, the  conception is useful in handling situations where the measured response is due to a mix  of known and unknown causes, such as in system identification.

The goal of probability theory and random process modeling is essentially to exploit the predictability of a random process to the maximum extent possible. With uncertainty reining the workhorses of prediction, the simplest recourse is to list all possible predictions (outcomes) and postulate the chance of each of those outcomes.

# Experiment or Trail 

An experiment is an activity that

- can be performed or repeated infinitely (ideally under same conditions)
- has a well-defined set of outcomes
- each repetition leads to exactly one outcome chosen by nature

> The set of all possible outcomes of an experiment, $\Omega$ or $\mathbb{S}$ is called the Sample space or Outcome space.

> An event $\mathbb{E}$, of an experiment is a specific outcome or a combination of outcomes that are of interest. 

When the number of possible outcomes shrinks to unity or the size of the sample space is one, the experiment ceases to be random/probabilistic and is termed as deterministic. The prime characteristic of a probabilistic phenomenon is that a specific outcome cannot be predicted because the underlying process is not properly understood. ``So, if a variable is considered random, it implies that it can take on various values from a set of possible outcomes, with the variable assuming a single value at any given instance.`` In dealing with uncertain events, the nature of the outcomes can be qualitative (e.g.,good / bad),or quantitative (e.g., sensor reading). In order to have a unified setup, the random variable is defined to take on only numeric values. This leads to the following formal definition.

# Random Variable

> A random variable X is a mapping (or point function) from the sample space $\mathbb{S}$ onto the real line such that to each element s $\sub$ $\mathbb{S}$ there corresponds a unique real number.

Conventionally, the RV is denoted by an uppercase variable X. The value that it takes on is denoted by a lowercase variable x. A random variable can be continuous or discrete.

Remarks:
- In constructing a random variable, we effectively replace our original (abstract) sample space by a new (concrete) sample space. Eg: outcomes of a game, head and tail of a toss are mapped to [1; 0].
- If the experiment itself yields some physical quantity that is real valued, then no further mapping is required.
- In practice, the term random variable is restricted to measurable functions only, i.e., those for which the probabilities in the sample space are defined.
- Random variables can be continuous or discrete values.

# Sample space vs Event Space

**Sample Space**
   - The sample space, often denoted by $\mathbb{S}$ or $\Omega$, is the set of all possible outcomes of a random experiment or process.
   - It represents the entire range of possible results that could occur.
   - Each individual outcome in the sample space is called an "element" or "sample point."

**Event Space**
   - The event space, often denoted by $\mathcal{F}$ is a subset of the sample space, containing one or more outcomes.
   - It consists of all possible events or combinations of outcomes that are of interest in a particular context.
   - Events can be simple (a single outcome) or compound (multiple outcomes).

**Example**

Consider a fair six-sided die, the 
- Sample Space ($\mathbb{S}$): $\{1, 2, 3, 4, 5, 6\}$ represents all possible outcomes when rolling the fair die.
- Event Space ($\mathcal{F}$): The event space is the collection of all possible events that can occur when rolling the die. It includes all subsets of the sample space, ranging from individual outcomes to combinations of outcomes. Eg. $\{1\}$, $\{2\}$, $\{1,2\}$, $\{1,3\}$, $\{1,2,3\}$, etc.

**FAQ**

<details>
  <summary>If combination of outcomes are considered, why they are not listed in the sample space?</summary>
  
  When combinations of outcomes are considered, those combinations are still elements of the sample space. The sample space $\mathbb{S}$ is the set of all possible outcomes of a random experiment. Combinations of outcomes, when taken together, form subsets of the sample space.

  For example, let's consider a fair six-sided die: $S = \{1, 2, 3, 4, 5, 6\}$. Now, let's look at a few events, which are subsets of the sample space:
  
  1. Event $A = \{1, 2\}$ - This is a subset of the sample space and a valid event.
  2. Event $B = \{1, 3\}$ - Another subset of the sample space and a valid event.
  
  The combination of outcomes is still within the sample space, and events are essentially specific subsets of the sample space that represent certain occurrences or combinations of outcomes that are of interest.
</details>

<details>
  <summary>Does combination of outcomes imply that the experiment has been repeated multiple times</summary>
  
  No, the term "combination of outcomes" doesn't necessarily imply conducting the experiment multiple times. When we talk about combinations of outcomes, we are referring to different sets or groups of individual outcomes within a single experiment or trial.
  
  For example, if you roll a fair six-sided die once, the sample space is $\{1, 2, 3, 4, 5, 6\}$, and the outcomes of a single experiment might be any one of these numbers. Now, if you consider an event like $A = \{1, 2\}$, it represents a combination of outcomes within that single roll – specifically, the event where the outcome is either 1 or 2. So, "combination of outcomes" refers to the grouping or selection of specific outcomes within a single instance of the experiment. It does not necessarily imply conducting the experiment multiple times. Each combination represents a possible scenario or event within a single trial of the experiment.
</details>
<br>

# Probability Approach
> Probability theory is used in expressing both ``“frequency”`` and ``“belief”`` of occurrence.  

Probability theory provides a mathematical framework for dealing with uncertainty and randomness. The frequentist and Bayesian approaches are two fundamental perspectives on how to interpret and apply probability.

1. **Frequentist Approach:**
   - Focuses on the ``long-run frequency`` or proportion of events in a large number of trials.
   - Probability is seen as the ``limit of the relative frequency`` of an event occurring.
   - It relies on objective, observable data and considers probabilities as properties of the data-generating process.
   - Commonly used in classical statistics and hypothesis testing.

2. **Bayesian Approach:**
   - Involves ``updating probabilities based on prior knowledge`` and incorporating new evidence as it becomes available.
   - Probability is interpreted as a ``measure of belief or confidence`` in the occurrence of an event, incorporating prior information and updating it using Bayes' theorem.
   - Emphasizes subjective probabilities that reflect an individual's degree of belief in an event.
   - Commonly used in Bayesian statistics and machine learning, particularly in situations with limited data.

In summary, the frequentist approach is more focused on objective, long-term frequencies and properties of data, while the Bayesian approach incorporates subjective beliefs and updates probabilities based on both prior information and new evidence. Both approaches have their strengths and are applied in different contexts depending on the nature of the problem and the available information.

# Population vs Sample
- **Population**: The entire group of individuals or instances about whom we want to draw conclusions. The population is the complete set and is often denoted by $N$, which can be very large and, in some cases, infinite.

- **Sample**: A subset of the population that is selected for the actual study. ``The sample is the observed set``, and its size is denoted by $n$. 

> The goal of taking a sample is to make inferences about the population based on the characteristics observed in the sample.

The process of selecting a sample from a population is crucial in statistical analysis, as it allows researchers to draw conclusions about the entire population without having to study every individual within it. 

> Probability deals with the population, while statistics focuses on a sample of that population to make inferences.

Let's detail this succinct summary,

- **Probability**: Probability theory deals with the likelihood of different outcomes in various situations. It is concerned with the study of random events and provides a mathematical framework for describing and analyzing uncertainty. Probability is often used to model the behavior of a population and the likelihood of different events occurring within that population.

- **Statistics**: Statistics, on the other hand, involves the collection, analysis, interpretation, presentation, and organization of data. While probability deals with the theoretical aspects of uncertainty, statistics deals with the practical application of this theory to make inferences about a population based on data collected from a sample.

In summary, probability is more concerned with theoretical concepts related to uncertainty and randomness, often applied to the entire population, while statistics deals with practical aspects of data analysis, typically focusing on samples from the population to draw conclusions about the population itself.

# Emprical estimation

As stated earlier, we define probability of an event to be its long run relative frequency. 

> $Pr(outcome) = \frac{\text{Number of trials producing the desired outcome}}{\text{Total number of trials}}$

The above definition replaced the long-held classical thought of uniform (equally likely) probability for phenomena that had natural symmetry in them (e.g., six-faced die without any imperfections). ``An inherent assumption is that the trials above have covered the entire outcome space, also known as the ensemble``, without introducing any deliberate prejudice (systematic error) towards one or more outcomes.
</div>
<br>
<div style="display: flex;justify-content: space-between; text-align: end;">
<div></div>
<div>

[Previous](../shared/prerequisite.md)</div>
<div style="text-align: end;">

[Next](laws-of-probability.md)</div>
</div>

