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
