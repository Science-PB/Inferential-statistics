# Inferential-statistics
Two Sample T-Test, Test of Equal or Given Proportions, F-Test

# Introduction

Inferential statistics is a popular extension of descriptive statistics, where the objective is to explore and
find conclusions that go beyond the current data at hand. A common example of inferential statistics is
when a statistician tests a population mean based on sample data collected from the given population
to make a conjecture (Trochim, 2020). This type of example is referred to as hypothesis testing.
Hypothesis testing is composed of many statistical techniques and methods, such as the t-test,
proportion test and f-test that evaluate different claims based on the hypotheses established. This
paper will evaluate the three aforementioned tests to showcase various decisions that can be made
from a dataset on chick weight.

# Inferential Statistics

Hypothesis testing, as a component of inferential statistics, is a process with the intention to
make conjectures about a dataset. Heavy emphasis needs to be placed on the fact that the results from
hypothesis testing are not irrefutable facts but rather a decision-making aid to help make predictions
about how data will behave in a population. A primary component of hypothesis testing is the
development of a null and alternative hypothesis. Essentially, the intent is to receive results from
running a specific test to make a decision on whether to accept or reject a claim, i.e. accept or reject
the null hypothesis. A significant factor in this decision is how a derived probability value, or p-value,
compares to the significance level utilized. The level of significance is the maximum probability of
committing the error of rejecting the null hypothesis when it is true, i.e. a type I error (Bluman, 2018, p.
418-419)
In order to showcase the use of inferential statistics, specifically hypothesis testing, the use of a
two-sample t-test, a test of equal or given proportions and a f-test will all be applied to the R dataset
“ChickWeight” from the package “MASS”. The data contained within “ChickWeight” is a record of the
weight of 50 chicks with different types of dietary nutrition over the course of 21 days. The overall intent
of the experiment was to determine the effect of diet on the early stages of a chick’s life. The
experiment itself aligns well to the objective of determining claims through the use of hypothesis tests.

# Two Sample T-Test

A two-sample t-test incorporates sample data from two independent groups to reach a
conclusion on whether to accept or reject a hypothesis based on the means of the groups (Minitab,
2016). For the purposes of the “ChickWeight” dataset the t-test will take into account two different diets
and the effect they have on the average weight of chicks. The use of different diets is what effectively
appoints this to a two-sample test.
Since the dataset in general is poised to understand if diet makes a difference in early chick life,
the two-sample t-test will be used to make a decision on if the weight of chicks varies between “Diet 1” and “Diet 2” at the 21 day mark. Figure 1 provides the R-code utilized along with the results of running
a two-sample t-test.

<img width="740" alt="Screen Shot 2020-11-16 at 8 27 21 PM" src="https://user-images.githubusercontent.com/66921930/99328951-1f6fa200-284b-11eb-8be5-df43e5243824.png">


<img width="706" alt="Screen Shot 2020-11-16 at 8 31 57 PM" src="https://user-images.githubusercontent.com/66921930/99328954-20083880-284b-11eb-91d7-80f8af871edc.png">

The results, as seen in Figure 1, provide the hypotheses used to run the test. In plain terms, the
null hypothesis claims that there is no statistical difference between the mean weight of chicks who
were on “Diet 1” versus “Diet 2”. The alternative hypothesis states that there is a difference in the
mean weight of chicks who were on different diets. The p-value obtained from running this test is 0.22
which is significantly larger than the established significance value of 0.05. This supports the null
hypothesis. Therefore, in this example there is not enough evidence to reject the claim that there is not
a statistical difference between the mean weight of chicks on “Diet 1” versus “Diet 2” at the 21-day
mark.

# Test of Equal or Given Proportions

In hypothesis testing the proportion test is a statistical test to determine whether the proportions
between two groups are equal to each other. Proportions are defined as the probability of success of a
given event. The “ChickWeight” dataset did not at first readily lend itself to supporting an event to determine a probability of “success”. With extra efforts taken it was determined that a parameter could
be created to evaluate a success ratio based on the weight of chicks to determine if different diets had
different success rates. The condition utilized for the proportion was that a gain of 100g or more during
the 21-day span of the experiment would be considered a success. Based on this condition a
calculation was made to record how much a chick had grown based on which diet it was receiving.
Successful, i.e. 100g or more, was recorded as “TRUE, with the remainder labeled “FALSE”. The R-code
used to build out this condition can be found in Figure 2.

<img width="728" alt="Screen Shot 2020-11-16 at 8 30 47 PM" src="https://user-images.githubusercontent.com/66921930/99328952-20083880-284b-11eb-94cb-992eea3e1470.png">

Based on the condition being established, a proportion test could then be utilized to make an
assessment. In this case, a null hypothesis was established that there is no statistical difference
between the proportion in weight of chicks on “Diet 1” versus “Diet 2”, with an alternative hypothesis
that there is a statistical difference between the proportions. Figure 3 shows the R-code and results
from running this proportion test.

<img width="744" alt="Screen Shot 2020-11-16 at 8 31 06 PM" src="https://user-images.githubusercontent.com/66921930/99328953-20083880-284b-11eb-9c20-01965d082cbc.png">

The proportions from the samples of “Diet 1” and “Diet 2, resulted in 0.78 and 0.89
respectively. A p-value of 1 was established against a 0.05 alpha, or significance. While a different test,
the result came out to the p-value again being well above that of the predetermined significance level.
According to the results, the decision is made to not reject the null hypothesis. There is not enough
evidence to reject the claim that the proportions are the same between chicks on “Diet 1” and “Diet 2”.

# F-Test
Rounding out the evaluations of diet on the weight of chicks, a final f-test is performed. An f-test
is a statistical test to determine whether the variances between two groups are equal to one another.
This is a useful method in determining how variability in data changes between two different
measurement methods (STHDA, n.d.). In regards to the “ChickWeight” dataset, weight is utilized as the
comparison variable. The effect of the diet type is compared to the weight of the chick at the end of the
21-day experiment. A null hypothesis is set that there is not a statistical difference between the
variance of “Diet 1” and “Diet 2” on chick weight at the 21-day mark. The alternative is that there is a
statistical difference between the proportions at those same markers. R-code and output can be seen
in Figure 4.

<img width="706" alt="Screen Shot 2020-11-16 at 8 31 57 PM" src="https://user-images.githubusercontent.com/66921930/99328954-20083880-284b-11eb-91d7-80f8af871edc.png">

The output of running an f-test on this dataset resulted in another larger p-value, 0.31, from our
significance level of 0.05. Basing a decision on the p-value the determination would be to accept the
null hypothesis. There is not enough evidence to reject the claim that there is not a statistical difference
between the variance of “Diet 1” and “Diet 2” on chick weight at 21 days. From a scientific point of
view, it is interesting to note that there does appear to be a difference based on the ratio of variance
being 0.56. If variances are equal, it is expected that the ratio of variances will be equal to 1 (Statistics
How To, 2020). Knowing this, the question of the effectiveness and viability of hypothesis testing,
becomes a more prominent query.

# Conclusion

As statistical methods and techniques build on each other, confidence in the conclusions and
answers being derived from experiments should continue to grow exponentially. By using different
sample groups and statistical tests, statisticians and analysts should gain the perspective needed to
execute and determine reliable assumptions based on the data at hand. However, there are certain
limitations that exist in the environment. For one, it is crucial to determine and be aware of statistical
bias before conducting any test. The null and alternative hypothesis developed in the beginning of a test
should be considered fully along with the determination of a significance level, so that the results are
not later changed to meet an initially expected outcome. In regards to the tests performed in this report
it is important to note that they do not show the magnitude of how different or similar two groups are,
merely the acceptance of the claim in each case that diet type did not create a statistical difference in
chicks at the 21-day mark. Even with limitations, the use of hypothesis testing is a valuable tool in the
understanding and applicability of the use of inferential statistics in today’s modern-day analytics.

# References

Minitab. (2016, May). Understanding t-Tests: 1-sample, 2-sample, and Paired t-Tests. The Minitab Blog.

Retrieved from: https://blog.minitab.com/blog/adventures-in-statistics-2/understanding-analysis-of-
variance-anova-and-the-f-test

Trochim, W. (2020, March). Inferential Statistics. Conjoint.ly. Retrieved from:
https://conjointly.com/kb/inferential-statistics/

Bluman, A. (2018). Elementary Statistics: A Step by Step Approach (10th ed.). New York, NY: McGraw-
Hill Education.

STHDA. (n.d.). F-Test: Compare Two Variances in R. STHDA. Retrieved from:
http://www.sthda.com/english/wiki/f-test-compare-two-variances-in-r#compute-f-test-in-r

Statistics How To. (2020). F-Test. Statistics How To. Retrieved from:
https://www.statisticshowto.com/probability-and-statistics/hypothesis-testing/f-test/
