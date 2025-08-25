# Addressing Membership Challenges: Insights and Strategies for Amour Beauty Box

Erdos UX Research - Spring 2025 - A/B testing

<b>Objective:</b>

Amour Beauty Box is a makeup company that offers membership-based services. Over the past three business quarters, Amour Beauty Box has been experiencing declining sign-ups but minimal cancellations, which suggests current members are satisfied, but the company is struggling to attract new customers. To determine whether internal or external factors cause this trend, we have proposed conducting A/B testing. As part of this process, we recommend surveying customers to gather insights. 

<h2 id="Table-of-Contents">Table of Contents</h2>

<ul>
    <li><a href="#Introduction">Introduction</a></li>
    <li><a href="#User-Journey">User Journey</a>
    <li><a href="#User-Survey">User Survey</a>
        <ul>
            <li><a href="#Section-1">Section 1: First Impressions</a></li>
            <li><a href="#Section-2">Section 2: Website & Sign-up Experience</a></li>
            <li><a href="#Section-3">Section 3: Offers & Incentives</a></li>
            <li><a href="#Section-4">Section 4: Decision-Making Drivers</a></li>
            <li><a href="#Section-5">Section 5: If You Didn't Subscribe</a></li>
            <li><a href="#Section-6">Section 6: Final Thoughts</a></li>
        </ul>
    <li><a href="#Survey-Result">Key Takeaways from Our Survey</a></li>
    <li><a href="#AB">A/B test experiment design</a>
        <ul>
            <li><a href="#Metric">Testing Metrics</a></li>
            <li><a href="#H0">Null hypotheses and Alternative hypotheses</a></li>
            <li><a href="#Min-Size">Minimum Sample Size</a></li>
            <li><a href="#Duration">Duration of the experiment</a></li>
        </ul>
    <li><a href="#Analysis">Data Analysis</a>
        <ul>
            <li><a href="#Dataset">Dataset</a></li>
            <li><a href="#Normality">Normality Check</a></li>
            <li><a href="#U-Test">Mann Whitney U Test</a></li>
        </ul>
    <li><a href="#Conclusion">Conclusion</a></li>
    <li><a href="#Code-Description">Code Description</a></li>
</ul>

---

<h3 id="Introduction">Introduction</h3>

Amour Beauty Box is a beauty subscription company with a clear mission: to be the go-to destination for trend-savvy, socially conscious makeup lovers. What sets Amour apart from other subscription services is its distinctive focus on indie and emerging beauty brands, combined with a deep responsiveness to TikTok and Instagram trends. This means subscribers aren't just getting mainstream products—they're discovering what’s next in beauty before it hits the shelves.

In line with its commitment to sustainability, Amour Beauty Box is also eco-friendly, using recyclable packaging and partnering with brands that prioritize clean ingredients and ethical sourcing. The brand resonates most strongly with Gen Z and young millennial consumers, who value both innovation and social responsibility in their beauty choices.
Subscribers receive curated boxes based on their personal preferences and skin type, ensuring that each delivery feels personalized and exciting. Each box includes exclusive promotions, free shipping, and access to premium products from popular and up-and-coming brands alike. 

Amour offers a versatile subscription model with three plans tailored to different budgets and preferences:

<li><b>Monthly Plan:</b> $19.99 for the first box, $29.99 for subsequent boxes</li>

<li><b>Quarterly Plan:</b> Three boxes for $79</li>

<li><b>Annual Plan:</b> Twelve boxes for $287</li>

---

<h3 id="User-Journey">User Journey</h3>

A typical user journey follows the diagram below. First, the user visits the `Homepage` of Amour Beauty Box, which includes an image with a "Join Now" button, a general description of subscriptions, and mentions of popular brands. Clicking "Join Now" takes the user to an `Overview` page that covers box curation and different subscription plans. After understanding the different plans, the user clicks "Subscribe Now", leading to the `Subscription Plans` page. The user selects the subscription plan that fits their needs, which then directs them to the `Account Creation` page. At this step, the user inputs their skin type and beauty preferences and creates an account. Upon completing this step, they are sent to the `Checkout` page to enter payment information and confirm their plan. After paying, the user is sent to the `Confirmation` page, which displays a thank-you message and triggers an email confirmation.

<p float="left">
  <img src="/Figure/user_journey.JPG" width="1000" />
</p>
<p align="center"><b>Figure 1. User journey diagram</b></p>

There are various paths in a user journey from visiting the website to subscription confirmation:
1. Visits Homepage → Exits
2. Visits Homepage → Overview → Exits
3. Visits Homepage → Overview → Subscription Plans → Exits
4. Visits Homepage → Overview → Subscription Plans → Account Creation → Exits
5. Visits Homepage → Overview → Subscription Plans → Account Creation → Checkout → Exits
6. Visits Homepage → Overview → Subscription Plans → Account Creation → Checkout → Confirmation

In addition, the user can cancel the plan at any time by accessing the Account page. Understanding the flow is a starting point for selecting key metrics for A/B testing.

---

<h3 id="User-Survey">User Survey</h3>

We're Amour Beauty Box - a beauty subscription designed to help you discover indie gems, clean beauty, and viral favorites (yes, the ones you keep seeing on TikTok). We're working on making our website and sign-up experience even better, and we’d love your input!
This short survey takes about 3–4 minutes and helps us shape the perfect subscription experience - from first click to first unboxing.
As a thank you, you'll be entered to win a $50 Amour Beauty Box shop credit.

<h4 id="Section-1">Section 1: First Impressions</h4>

1. What features of our membership stood out to you when you first visited our website? (Select all that apply)
- [x] Discounted products
- [ ] Free gifts
- [x] Early access to launches
- [x] Exclusive content
- [ ] Flexible cancellation
- [ ] None of the above

2. On your first visit, how easy was it to understand the membership includes?
- [ ] Very easy
- [ ] Easy
- [ ] Neutral
- [x] Difficult
- [ ] Very difficult

3. Which of the following caused confusion or hesitation while considering signing up?
- [ ] Lack of clear pricing
- [ ] No customer reviews/testimonials
- [x] Didn't know what was included
- [ ] Didn't trust the site
- [ ] Checkout process was too complicated
- [ ] Other (please specify): ___________________

<h4 id="Section-2">Section 2: Website & Sign-up Experience</h4>

4. How would you rate the length of the sign-up process?
- [ ] Very short
- [ ] Manageable
- [ ] Slightly long
- [x] I didn't complete it

5. Did you encounter any technical issues during the sign-up process?
- [ ] Yes
- [x] No
- [ ] Not sure

6. How would you prefer to set your beauty preferences and skin type?
- [x] A visual quiz with image examples
- [ ] A text-based form with dropdowns
- [ ] A quick "swipe right/ left" style interaction
- [ ] I don't want to set preferences - just surprise me!

7. Did seeing (or not seeing) a preview of what's in the first box affect your decision to sign up?
- [x] Yes - I was more likely to sign up after seeing a preview
- [ ] Yes - I wanted to see a preview but didn't find one
- [ ] No - A preview didn't matter to me
- [ ] I didn't notice whether a preview was shown or not

<h4 id="Section-3">Section 3: Offers & Incentives</h4>

8. Which of the following would make you more likely to sign up? (Select all that apply)
- [x] First-time member discount
- [x] Product previews
- [ ] Trust badges (e.g., "Secure checkout")
- [x] Verified customer reviews
- [x] Trial period
- [ ] Other (please specify): ___________________

9. What would motivate you to try a new beauty subscription box for the first time?
- [ ] A discounted first box
- [ ] A free bonus item from a trending brand
- [x] A personalized quiz to match products to me
- [ ] Seeking product previews on TikTok/Instagram
- [ ] Knowing it features eco-friendly or clean beauty brands 

10. What kind of message would most convince you to hit "Subscribe"?
- [ ] "Get TikTok's hottest products before they sell out"
- [ ] "Build your perfect box in under 2 minutes"
- [x] "First box just $9.99 - no commitment"
- [ ] "Curated clean beauty from emerging brands"
- [ ] "Join 100,000+ subscribers who love their boxes"

<h4 id="Section-4">Section 4: Decision-Making Drivers</h4>

11. When choosing a beauty subscription box, which of these is most important to you?
- [ ] The ability to discover new brands
- [ ] Getting the best value for my money
- [ ] Eco-conscious and sustainable practices
- [x] Personalization based on my skin type and preferences
- [ ] Following the latest beauty trends

12. When you're thinking about subscribing, what do you want to see before making the decision? (Select all that apply)
- [x] Real photos/videos of past boxes
- [ ] Clear pricing with no surprises
- [x] Brand names I recognize and trust
- [x] A way to customize or preview my box
- [ ] Reviews or social media feedback from others

13. How do you feel about the current subscription pricing and options?
- [x] Clear and easy to understand
- [ ] Too many choices - simplify it
- [ ] Needs more flexibility (e.g., pause or skip box options)
- [ ] I didn't notice the differences between plans

<h4 id="Section-5">Section 5: If You Didn't Subscribe</h4>

14. If you didn't complete your sign-up, what held you back? (Select all that apply)
- [x] I didn't understand what I was getting
- [ ] The sign-up process felt too long
- [x] I wasn't sure how personalized the box would be
- [ ] I didn't see enough customer feedback or social proof
- [x] I wanted to see product previews before subscribing

<h4 id="Section-6">Section 6: Final Thoughts</h4>

15. What would make the membership offer more compelling to you?  

16. Do you have any other comments about your experience on the website?

**Thank you so much for your feedback! It means the world to us - and to your future beauty hauls**

---

<h3 id="Survey-Result">Key Takeaways from Our Survey</h3>

Survey results from 312 responses revealed several key insights into user behavior and signup barriers. Many users found the "Join Now" button difficult to locate, which slowed down the signup process. Additionally, hesitation points centered around unclear pricing, the absence of customer reviews, and a lack of product previews, all of which contributed to lower engagement. However, incentives such as first-time discounts, prominently displayed customer reviews, and detailed product previews significantly increased the likelihood of signup, emphasizing the importance of transparency and user trust in driving conversions.

To optimize the signup process and enhance user engagement, the "Join Now" button should be centered and visually emphasized on key pages for better visibility. Introducing clear product previews and showcasing authentic customer reviews earlier in the signup journey will help build trust and transparency. Additionally, testing incentives such as first-time member discounts or bonus items can significantly improve acquisition rates. Streamlining the signup and account creation process with engaging elements—such as interactive visual quizzes—will create a more personalized and enjoyable experience, ultimately encouraging users to complete their registration.

---

<h3 id="AB">A/B test experiment design</h3>

<h4 id="Metric">Testing Metrics</h4>

There are two ways to conduct an A/B test, depending on the metric used:

- Conversion refers to any action taken online that aligns with a business's goals, such as filling out a form, making a purchase, or completing a survey. In this study, the conversion rate represents the proportion of people who sign up for the subscription.
- Revenue is a continuous metric that directly impacts the business's bottom line.

First, we consider `conversion rate`, which represents the number of conversions within a given timeframe and is typically expressed as a percentage. For example, if 100 visitors access a website and 10 make a purchase, the conversion rate is 10%. This metric helps businesses assess how effectively their website converts visitors into customers.

Secondly, we also conduct an A/B test on `revenue`, as a high conversion rate does not necessarily imply high revenue. For example, Amour Beauty Box may have more people signing up for the monthly box, resulting in a high conversion rate but lower revenue. Conversely, if fewer people sign up but opt for annual payments, it would yield a lower conversion rate but higher revenue.

<h4 id="H0">Null hypotheses and Alternative hypotheses</h4>

To evaluate the effectiveness of the proposed improvements to the signup flow at Amour Beauty Box, we carefully defined two sets of hypotheses: one addressing the conversion rate and the other examining revenue per user based on the position of the 'Join Now' button on the homepage. In the control design, the button had been placed in the top left corner, while in the variant design, it had been repositioned prominently in the center to enhance visibility and encourage user engagement.

<p float="left">
  <img src="/Figure/control.PNG" width="400" />
  <img src="/Figure/variant.PNG" width="400" /> 
</p>
<p align="center"><b>Figure 2. (Left)The control group, where the 'Join Now' button is positioned at the top left.</b></p>
    <p align="center"><b>(Right) The variant group, where the 'Join Now' button is positioned at the center.</b></p>

For `conversion rate`:

• **Null hypothesis ($$H_{01}$$)** asserted that the proportion of users signing up was the same between the control group and the variant group. That is, the change implemented in the variant group does not lead to a statistically significant increase in conversion rate.

• **Alternative hypothesis ($H_{11}$)** proposed that signup rates differed between the two groups, indicating that the implemented change has led to a statistically significant increase in conversion rate.

Similarly, for `revenue`: 

• **Null hypothesis ($H_{02}$)** posited that there was no difference in revenue per user between the control and variant groups 

• **Alternative hypothesis ($H_{12}$)** suggested that revenue differs across groups.


<h4 id="Min-Size">Minimum Sample Size</h4>

Last year, Amour Beauty Box reportedly had around 30,000 subscribers and received approximately 15,000 website visits per month, which averages to about 500 visits per day.
The estimated proportion is calculated as the number of subscribers divided by the total visits.

$$ p = \frac{30,000 \hspace{1mm} \text{subscribers}}{15,000 \hspace{1mm} \text{visits per month} \cdot 12 \hspace{1mm} \text{months per year}} \approx 0.167 $$

We want to construct a 95% confidence interval for p = 16.7% with a margin of error M = 1.3%. The minimum sample size is:

$$ n = \left( \frac{z}{M} \right)^2 \cdot p \cdot (1 - p) = \left( \frac{1.960}{0.013} \right)^2 \cdot 0.167 \cdot (1 - 0.167) \approx 3,162.2$$

We aimed to collect 3,162 samples for the control group and 3,162 samples for the variant group, totaling 6,324 samples. Additionally, we needed to account for duplicate users accessing the website, so our goal was to collect 10,000 samples.

<h4 id="Duration">Duration of the experiment</h4>

The duration of the experiment is calculated by dividing the number of samples that need to be collected by the number of daily visits.

$$\text{Duration} = \frac{10,000 \hspace{1mm} \text{samples}}{500 \hspace{1mm} \text{visits per day}} = 20 \hspace{1mm} \text{days} $$

We will test changes to the website and signup flow to evaluate their impact on conversion rates. The control and variant groups will each consist of 3,162 samples (6,324 total, accounting for duplicates, aiming for 10,000 samples overall). The test will run for approximately 20 days.

---

<h3 id="Analysis">Data Analysis</h3>

Perform an A/B test on the dataset [AB_Test_Results.csv](https://github.com/kpnguyen21/erdos-AB-testing/blob/main/Data/AB_Test_Results.csv). 

<h4 id="Dataset">Dataset</h4>

After 20 days, we successfully collected 10,000 samples for the experiment. The dataset consists of three variables:

- `USER_ID`: A unique identifier for each user who accessed the website.
- `VARIANT_NAME`: A nominal variable that represents either the "control" or "variant" group.
- `REVENUE`: A continuous metric, where 0 indicates that the user did not make a purchase, while a positive value represents a completed purchase.

We sorted the data and removed duplicate entries to maximize revenue retention. If the same users appeared in both the control and variant groups, the results would be inaccurate, as each user would be counted twice, skewing the data. Therefore, before conducting any analysis, we needed to remove duplicate users.

Next, we added the columns `RANK_REVENUE` and `RANK_CONVERSION`, which represent the average ranks of `REVENUE` and `BUY`, respectively.  This step prepares the dataset for the Mann-Whitney U test, if necessary.

We generated exploratory data analysis (EDA) plots to examine the revenue distribution and conversion rates across the two groups. These visualizations provide insights into spending patterns, highlight differences in purchasing behavior, and help identify potential trends or anomalies that may influence overall performance.

<p float="left">
  <img src="/Figure/revenue_distribution.jpg" width="800" />
</p>
<p align="center"><b>Figure 3. Revenue distribution between the control and variant groups.</b></p>

The revenue distributions for both the control and variant groups are heavily concentrated at the lower end, suggesting that a significant portion of individuals either did not make a purchase or opted for lower-value transactions. This trend indicates a potential barrier to higher spending, possibly influenced by factors such as pricing, consumer preferences, or product appeal.

<p float="left">
  <img src="/Figure/membership_signups.jpg" width="800" />
</p>
<p align="center"><b>Figure 4. Comparison of new sign-ups versus non-sign-ups for new membership between the control and variant groups.</b></p>

In both the control and variant groups, a significantly larger number of individuals chose not to sign up for the membership. Additionally, the variant group exhibited an even higher non-signup rate and a lower number of sign-ups compared to the control group. This suggested that the change we implemented may have had little to no impact on revenue or conversion rates. To confirm this observation, we conducted statistical tests to determine whether these differences were statistically significant.

<h4 id="Normality">Normality Check</h4>

Since our sample size was large, we chose not to use the T-test. There were several options for conducting an A/B test, depending on whether the data was normally distributed. If the conversion rate or revenue had followed a Gaussian distribution, we would have performed a Z-test. Otherwise, we recommended using the Mann-Whitney U test, a non-parametric method that did not require the assumption of normality. Therefore, our first step was to test for normality.

• **Null hypothesis ($$H_0$$):** The population (`conversion rate` or `revenue`) from which the sample is drawn is normally distributed.

• **Alternative hypothesis ($$H_1$$):**  The population (`conversion rate` or `revenue`) from which the sample is drawn is not normally distributed. 

<table>
  <tr>
    <th rowspan="2"></th>
    <th colspan="2">Conversion Rate</th>
    <th colspan="2">Revenue</th>
  </tr>
  <tr>
    <th>Control</th>
      <th>Variant</th>
    <th>Control</th>
      <th>Variant</th>
</tr>
    <tr>
        <td>Statistics</td>
        <td>3490.598</td>
        <td>3781.952</td>
        <td>9552.712</td>
        <td>8273.628</td>
    </tr>
    <tr>
        <td>p-value</td>
        <td>$\approx 0$</td>
        <td>$\approx 0$</td>
        <td>$\approx 0$</td>
        <td>$\approx 0$</td>
    </tr>
</table>

Using D'Agostino's K-squared Test (`normaltest` from Python's SciPy library), we rejected the null hypothesis for both the control and variant groups in terms of `conversion rate` and `revenue`. Since neither `conversion rate` nor `revenue` followed a Gaussian distribution, normality could not be assumed. Therefore, we opted for the Mann-Whitney U test—a non-parametric statistical method—to compare the two groups in our A/B testing.

<h4 id="U-Test">Mann Whitney U Test</h4>

The Mann-Whitney U test is equivalent to an independent t-test. It does not assume normality and works well with small sample sizes.

Steps for Mann Whitney U Test:

1. Collect two independent samples.
2. Rank the data from smallest to largest across both groups. If two observations have the same value, assign them the average rank.
3. Sum the ranks for each sample (denoted as $R_1$ and $R_2$)
4. Calculate the U-statistics:

$$ U_1 = n_1 n_2 + \frac{n_1(n_1 + 1)}{2} - R_1 $$

$$ U_2 = n_1 n_2 + \frac{n_2(n_2 + 1)}{2} - R_2 $$

where 
- $n_1$ and $n_2$ are sample sizes for the two groups
- $R_1$ and $R_2$ are the rank sums of each group

The final U-statistics is the smallest value of $U_1$ and $U_2$.

5. Compare U to the critical value from the Mann-Whitney U Table at the chosen significance level (e.g. 0.05)

For small sample sizes, the exact distribution of U can be calculated, and the p-value can be determined directly from the CDF. However, for larger sample sizes, the distribution of U can be approximated by a normal distribution, and the p-value can be calculated using the standard normal CDF.

Expected value of U:

$$\mu_U = \frac{n_1 \cdot n_2}{2}$$

Standard error of U:

$$\sigma_U = \sqrt{\frac{n_1 \cdot n_2 \cdot (n_1 + n_2 + 1)}{12}}$$

z-value is:

$$z = \frac{U - \mu_U}{\sigma_U}$$

The p-value for the U statistic can be obtained by computing the p-value of the corresponding z-score.

<table>
  <tr>
    <th rowspan="1"></th>
    <th colspan="1">Conversion Rate</th>
    <th colspan="1">Revenue</th>
  </tr>
    <tr>
        <td>Statistics</td>
        <td>4980184.0</td>
        <td>4979759.0</td>
    </tr>
    <tr>
        <td>p-value</td>
        <td>$\approx 0.5998$</td>
        <td>$\approx 0.6021$</td>
    </tr>
</table>

Our results indicated that the p-values for U-statistics in both conversion rate and revenue exceeded the significance level of 0.05. As a result, we failed to reject both null hypotheses. 

---

<h3 id="Conclusion">Conclusion</h3>

We failed to reject the null hypothesis for the conversion rate, indicating that the implemented change did not lead to a statistically significant increase in sign-ups. In other words, the adjustment had little to no impact on user behavior, suggesting that additional factors may be influencing conversion rates. This outcome highlights the need for further analysis to explore elements such as user preferences, market conditions, and potential website optimizations that could enhance engagement and drive sign-ups.

Similarly, we failed to reject the second null hypothesis, meaning the change did not result in a statistically significant increase in revenue. The modification did not contribute to higher earnings, implying that user spending and purchasing behavior remained largely unaffected. This finding underscores the importance of further investigation into potential revenue-driving factors, including pricing strategies, customer retention efforts, and external market dynamics that may support financial growth.

---

<h3 id="Code-Description">Code Description</h3>

[AB_Test_Results.csv](https://github.com/kpnguyen21/erdos-AB-testing/blob/main/Data/AB_Test_Results.csv): This dataset is from [Kaggle](https://www.kaggle.com/datasets/sergylog/ab-test-data).


[AB_test.ipynb](https://github.com/kpnguyen21/erdos-AB-testing/blob/main/AB_test.ipynb): I analyzed the dataset by performing a normality check and applying the Mann-Whitney U test to the dataset.
