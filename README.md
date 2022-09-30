# Data Science Statistics Interview Questions

## Q1. What is the Central Limit Theorem and why is it important?

An Introduction to the Central Limit Theorem
In a world full of data that seldom follows nice theoretical distributions, the Central Limit Theorem is a beacon of light. Often referred to as the cornerstone of statistics, it is an important concept to understand when performing any type of data analysis.

#### **`Suppose that we are interested in estimating the average height among all people. Collecting data for every person in the world is impractical, bordering on impossible. While we can’t obtain a height measurement from everyone in the population, we can still sample some people. The question now becomes, what can we say about the average height of the entire population given a single sample.`**

#### **`The Central Limit Theorem addresses this question exactly. Formally, it states that if we sample from a population using a sufficiently large sample size, the mean of the samples (also known as the sample population) will be normally distributed (assuming true random sampling). What’s especially important is that this will be true regardless of the distribution of the original population.`**

When I first read this description I did not completely understand what it meant. However, after visualizing a few examples it become more clear. Let’s look at an example of the Central Limit Theorem in action.

### Example
Suppose we have the following population distribution.

![image](https://user-images.githubusercontent.com/99672298/192943788-4e4521b9-56fb-4479-a891-79e994c36987.png)

I manually generated the above population by choosing numbers between 0 and 100, and plotted it as a histogram. The height of the histogram denotes the frequency of the number in the population. As we can see, the distribution is pretty ugly. It certainly isn’t normal, uniform, or any other commonly known distribution.

In order to sample from the above distribution, we need to define a sample size, referred to as N. This is the number of observations that we will sample at a time. Suppose that we choose N to be 3. This means that we will sample in groups of 3. So for the above population, we might sample groups such as [5, 20, 41], [60, 17, 82], [8, 13, 61], and so on.

Suppose that we gather 1,000 samples of 3 from the above population. For each sample, we can compute its average. If we do that, we will have 1,000 averages. This set of 1,000 averages is called a sampling distribution, and according to Central Limit Theorem, the sampling distribution will approach a normal distribution as the sample size N used to produce it increases. Here is what our sample distribution looks like for N = 3.

![image](https://user-images.githubusercontent.com/99672298/192962069-c51e2340-8ef5-4865-9f88-e5747cd6b8e5.png)
![image](https://user-images.githubusercontent.com/99672298/192962310-d002d2b0-46ac-4c41-a161-357dc882e456.png)
![image](https://user-images.githubusercontent.com/99672298/192962343-13872cbc-f1a3-42ad-aba1-668838f8e9b7.png)




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

    o EX: In the image below, let's say you need a sample size of 6. Two members from each
      group (yellow, red, and blue) are selected randomly. Make sure to sample proportionally:
      In this simple example, 1/3 of each group (2/6 yellow, 2/6 red and 2/6 blue) has been
      sampled. If you have one group that's a different size, make sure to adjust your
      proportions. For example, if you had 9 yellow, 3 red and 3 blue, a 5-item sample would
      consist of 3/9 yellow (i.e. one third), 1/3 red and 1/3 blue.

• **Cluster sampling:** The larger data set is divided into subsets (clusters) based on a defined factor, then a random sampling of clusters is analyzed.

    o EX: In the image below, the strata are natural groupings by head color (yellow, red, blue).
      A sample size of 6 is needed, so two of the complete strata are selected randomly (in this
      example, groups 2 and 4 are chosen).

![image](https://user-images.githubusercontent.com/99672298/192953627-72da4a4a-fc05-4e04-bff2-e9aaebad6c07.png)
![image](https://user-images.githubusercontent.com/99672298/192953662-e0cd5e9b-a4d3-4d6d-a850-7e327bcfc968.png)

#### What is cluster sampling?
Cluster sampling is a probability sampling technique where researchers divide the population into multiple groups (clusters) for research. Researchers then select random groups with a simple random or systematic random sampling technique for data collection and data analysis.

            Example: A researcher wants to conduct a study to judge the performance of sophomore’s in business education across the U.S. 
            It is impossible to conduct a research study that involves a student in every university. Instead, by using cluster sampling, 
            the researcher can club the universities            from each city into one cluster. These clusters then define all the sophomore 
            student population in the U.S. Next, either using simple random sampling or systematic random sampling and randomly pick clusters 
            for the research study. Subsequently, by using simple or systematic sampling, the sophomore’s from each of these selected 
            clusters can be chosen on whom to conduct the research study.

In this sampling technique, researchers analyze a sample that consists of multiple sample parameters such as demographics, habits, background – or any other population attribute, which may be the focus of conducted research. This method is usually conducted when groups that are similar yet internally diverse form a statistical population. Instead of selecting the entire population, cluster sampling allows the researchers to collect data by bifurcating the data into small, more productive groups.

#### Cluster sampling definition
Cluster sampling is defined as a sampling method where the researcher creates multiple clusters of people from a population where they are indicative of homogeneous characteristics and have an equal chance of being a part of the sample.

Example: Consider a scenario where an organization is looking to survey the performance of smartphones across Germany. They can divide the entire country’s population into cities (clusters) and select further towns with the highest population and also filter those using mobile devices.

##### Types of cluster sampling
There are two ways to classify this sampling technique. The first way is based on the number of stages followed to obtain the cluster sample, and the second way is the representation of the groups in the entire cluster analysis. In most cases, sampling by clusters happens over multiple stages. A stage is considered to be the step taken to get to the desired sample. We can divide this technique into single-stage, two-stage, and multiple stages.

##### Single-stage cluster sampling: 
As the name suggests, sampling is done just once. An example of single-stage cluster sampling – An NGO wants to create a sample of girls across five neighboring towns to provide education. Using single-stage sampling, the NGO randomly selects towns (clusters) to form a sample and extend help to the girls deprived of education in those towns.

##### Two-stage cluster sampling: 
Here, instead of selecting all the elements of a cluster, only a handful of members are chosen from each group by implementing systematic or simple random sampling. An example of two-stage cluster sampling – A business owner wants to explore the performance of his/her plants that are spread across various parts of the U.S. The owner creates clusters of the plants. He/she then selects random samples from these clusters to conduct research.

##### Multiple stage cluster sampling: 
Multiple-stage cluster sampling takes a step or a few steps further than two-stage sampling.

For conducting effective research across multiple geographies, one needs to form complicated clusters that can be achieved only using the multiple-stage sampling technique. An example of Multiple stage sampling by clusters – An organization intends to survey to analyze the performance of smartphones across Germany. They can divide the entire country’s population into cities (clusters) and select cities with the highest population and also filter those using mobile devices.

• **Multistage sampling:** A more complicated form of cluster sampling, this method also involves dividing the larger population into a number of clusters. Second-stage clusters are then broken out based on a secondary factor, and those clusters are then sampled and analyzed. This staging could continue as multiple subsets are identified, clustered and analyzed.

• **Systematic sampling:** A sample is created by setting an interval at which to extract data from the larger population -- for example, selecting every 10th row in a spreadsheet of 200 items to create a sample size of 20 rows to analyze.

Sampling can also be based on non-probability, an approach in which a data sample is determined and
extracted based on the judgment of the analyst. As inclusion is determined by the analyst, it can be more
difficult to extrapolate whether the sample accurately represents the larger population than when
probability sampling is used.

![image](https://user-images.githubusercontent.com/99672298/192952665-855b8983-8fac-425d-8569-e79619b3ed19.png)
![image](https://user-images.githubusercontent.com/99672298/192960298-567a388d-945b-41c1-b97b-ff2c7cf11d5e.png)

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

## Q3. What is the difference between type I vs type II error?

Is Ha(Alternate Hypothesis) true? No, H0(Null Hypothesis) is True (Ha is Negative: TN); Yes, H0 is False (Ha is Positive: TP).

+ A type I error occurs when the null hypothesis is true but it gets rejected. 
+ A type II error occurs when the null it is actually false but we failed to reject it.

![image](https://user-images.githubusercontent.com/99672298/192961828-89b200c7-4145-4418-bf8c-d32609ef4168.png)

## Q4. What is linear regression? What do the terms p-value, coefficient, and rsquared value mean? What is the significance of each of these components?

Imagine you want to predict the price of a house. That will depend on some factors, called independent
variables, such as location, size, year of construction… if we assume there is a linear relationship between
these variables and the price (our dependent variable), then our price is predicted by the following
function:

![image](https://user-images.githubusercontent.com/99672298/192962967-52a3146f-2ec8-418c-ba98-80f1e78ba027.png)

The p-value in the table is the minimum $\alpha$ (the significance level) at which the coefficient is relevant. The
lower the p-value, the more important is the variable in predicting the price. Usually we set a 5% level, so
that we have a 95% confidentiality that our variable is relevant.

The p-value is used as an alternative to rejection points to provide the smallest level of significance at
which the null hypothesis would be rejected. A smaller p-value means that there is stronger evidence in
favor of the alternative hypothesis.

The coefficient value signifies how much the mean of the dependent variable changes given a one-unit
shift in the independent variable while holding other variables in the model constant. This property of
holding the other variables constant is crucial because it allows you to assess the effect of each variable
in isolation from the others.

R squared ( $R^2$ ) is a statistical measure that represents the proportion of the variance for a dependent
variable that's explained by an independent variable or variables in a regression model.

## Q5. What are the assumptions required for linear regression?

#### There should be linear relationship betweent the independent and dependent variables, either there can be a positive correlation or negative correlation.

#### The Errors or residuals of the data to be Normally distributed ND~(0,1) and the variance of it should have homoscedasticity for any value of Independent Variable. There should be no autocorrelation among the errors nor postive or negative. There should be no relation between the Errors or any Independent Variable (also covers in Homoscedasticity of Error)

#### Homoscedasticity. This means the variance around the regression line is the same for all values of the predictor variable.

#### All The Variables should be Normally Distributed

#### The Variables Independent or Dependent should be Normally Distributed
