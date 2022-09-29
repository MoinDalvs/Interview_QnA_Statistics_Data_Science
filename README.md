# Data Science Statistics Interview Questions

## Q1. What is the Central Limit Theorem and why is it important?

An Introduction to the Central Limit Theorem
In a world full of data that seldom follows nice theoretical distributions, the Central Limit Theorem is a beacon of light. Often referred to as the cornerstone of statistics, it is an important concept to understand when performing any type of data analysis.

### Motivation
#### **`Suppose that we are interested in estimating the average height among all people. Collecting data for every person in the world is impractical, bordering on impossible. While we can’t obtain a height measurement from everyone in the population, we can still sample some people. The question now becomes, what can we say about the average height of the entire population given a single sample.`**

#### **`The Central Limit Theorem addresses this question exactly. Formally, it states that if we sample from a population using a sufficiently large sample size, the mean of the samples (also known as the sample population) will be normally distributed (assuming true random sampling). What’s especially important is that this will be true regardless of the distribution of the original population.`**

When I first read this description I did not completely understand what it meant. However, after visualizing a few examples it become more clear. Let’s look at an example of the Central Limit Theorem in action.

### Example
Suppose we have the following population distribution.

![image](https://user-images.githubusercontent.com/99672298/192943788-4e4521b9-56fb-4479-a891-79e994c36987.png)

I manually generated the above population by choosing numbers between 0 and 100, and plotted it as a histogram. The height of the histogram denotes the frequency of the number in the population. As we can see, the distribution is pretty ugly. It certainly isn’t normal, uniform, or any other commonly known distribution.

In order to sample from the above distribution, we need to define a sample size, referred to as N. This is the number of observations that we will sample at a time. Suppose that we choose N to be 3. This means that we will sample in groups of 3. So for the above population, we might sample groups such as [5, 20, 41], [60, 17, 82], [8, 13, 61], and so on.

Suppose that we gather 1,000 samples of 3 from the above population. For each sample, we can compute its average. If we do that, we will have 1,000 averages. This set of 1,000 averages is called a sampling distribution, and according to Central Limit Theorem, the sampling distribution will approach a normal distribution as the sample size N used to produce it increases. Here is what our sample distribution looks like for N = 3.

![image](https://user-images.githubusercontent.com/99672298/192943838-cbd059c6-8a46-4d4a-9591-dec993a67d45.png)

As we can see, it certainly looks uni-modal, though not necessarily normal. If we repeat the same process with a larger sample size, we should see the sampling distribution start to become more normal. Let’s repeat the same process again with N = 10. Here is the sampling distribution for that sample size.

![image](https://user-images.githubusercontent.com/99672298/192943882-b1201032-0cb9-4f71-a864-64963d6d839a.png)

This certainly looks more normal, and if we repeated this process one more time for N = 30 we observe this result.

![image](https://user-images.githubusercontent.com/99672298/192943912-58135add-1950-4ad5-9945-4045456475b4.png)

The above plots demonstrate that as the sample size N is increased, the resultant sample mean distribution becomes more normal. Further, the distribution variance also decreases. Keep in mind that the original population that we are sampling from was that weird ugly distribution above.

## Q2. What is sampling? How many sampling methods do you know?

#### **`Data sampling is a statistical analysis technique used to select, manipulate and analyze a representative subset of data points to identify patterns and trends in the larger data set being examined. It enables data scientists, predictive modelers and other data analysts to work with a small, manageable amount of data about a statistical population to build and run analytical models more quickly, while still producing accurate findings.`**

Sampling can be particularly useful with data sets that are too large to efficiently analyze in full – for
example, in big data analytics applications or surveys. Identifying and analyzing a representative sample
is more efficient and cost-effective than surveying the entirety of the data or population.
An important consideration, though, is the size of the required data sample and the possibility of
introducing a sampling error. In some cases, a small sample can reveal the most important information
about a data set. In others, using a larger sample can increase the likelihood of accurately representing
the data as a whole, even though the increased size of the sample may impede ease of manipulation and
interpretation.
There are many different methods for drawing samples from data; the ideal one depends on the data set
and situation. Sampling can be based on probability, an approach that uses random numbers that
correspond to points in the data set to ensure that there is no correlation between points chosen for the
sample.

#### Further variations in probability sampling include:

• **Simple random sampling:** Software is used to randomly select subjects from the whole population.

• **Stratified sampling:** Subsets of the data sets or population are created based on a common factor, and samples are randomly collected from each subgroup.

• **Cluster sampling:** The larger data set is divided into subsets (clusters) based on a defined factor, then a random sampling of clusters is analyzed.

• **Multistage sampling:** A more complicated form of cluster sampling, this method also involves dividing the larger population into a number of clusters. Second-stage clusters are then broken out based on a secondary factor, and those clusters are then sampled and analyzed. This staging could continue as multiple subsets are identified, clustered and analyzed.

• **Systematic sampling:** A sample is created by setting an interval at which to extract data from the larger population -- for example, selecting every 10th row in a spreadsheet of 200 items to create a sample size of 20 rows to analyze.

Sampling can also be based on non-probability, an approach in which a data sample is determined and
extracted based on the judgment of the analyst. As inclusion is determined by the analyst, it can be more
difficult to extrapolate whether the sample accurately represents the larger population than when
probability sampling is used.

![image](https://user-images.githubusercontent.com/99672298/192952665-855b8983-8fac-425d-8569-e79619b3ed19.png)

#### Non-probability data sampling methods include:

• **Convenience sampling:** Data is collected from an easily accessible and available group.

• **Consecutive sampling:** Data is collected from every subject that meets the criteria until the
predetermined sample size is met.

• **Purposive or judgmental sampling:** The researcher selects the data to sample based on predefined
criteria.

• **Quota sampling:** The researcher ensures equal representation within the sample for all subgroups
in the data set or population (random sampling is not used).

Once generated, a sample can be used for predictive analytics. For example, a retail business might use
data sampling to uncover patterns about customer behavior and predictive modeling to create more
effective sales strategies.
