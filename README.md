# Addressing Membership Challenges: Insights and Strategies for Amour Beauty Box

Erdos UX Research - Spring 2025 - A/B testing

<b>Objective:</b>

Amour Beauty Box is a makeup company that offers membership-based services. Over the past three business quarters, Amour Beauty Box has been experiencing declining sign-ups but minimal cancellations, which suggests current members are satisfied, but the company is struggling to attract new customers. To determine whether internal or external factors cause this trend, we have proposed conducting A/B testing. As part of this process, we recommend surveying customers to gather insights. 

<h2 id="Table-of-Contents">Table of Contents</h2>

<ul>
    <li><a href="#Introduction">Introduction</a></li>
    <li><a href="#User-Journey">User Journey</a>
    <li><a href="#User-Survey">User Survey</a>
    <li><a href="#Survey-Result">Key Takeaways from Our Survey</a></li>
    <li><a href="#Sample">Minimum Sample Size and Duration for Reliable Results</a>
        <ul>
            <li><a href="#Min-Size">Minimum Sample Size</a></li>
            <li><a href="#Duration">Duration of the experiment</a></li>
        </ul>
    <li><a href="#Conclusion">Conclusion</a></li>
    <li><a href="#Resource">Resource</a></li>
    <li><a href="#Code-Description">Code Description</a></li>
</ul>

---

<h3 id="Introduction">Introduction</h3>

Amour Beauty Box is a beauty subscription company with a clear mission: to be the go-to destination for trend-savvy, socially conscious makeup lovers. What sets Amour apart from other subscription services is its distinctive focus on indie and emerging beauty brands, combined with a deep responsiveness to TikTok and Instagram trends. This means subscribers aren't just getting mainstream products—they’re discovering what’s next in beauty before it hits the shelves.

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

We’re Amour Beauty Box — a beauty subscription designed to help you discover indie gems, clean beauty, and viral favorites (yes, the ones you keep seeing on TikTok). We're working on making our website and sign-up experience even better, and we’d love your input!
This short survey takes about 3–4 minutes and helps us shape the perfect subscription experience — from first click to first unboxing.
As a thank you, you'll be entered to win a $50 Amour Beauty Box shop credit.

---

<h3 id="Survey-Result">Key Takeaways from Our Survey</h3>

Survey results from 312 responses revealed several key insights into user behavior and signup barriers. Many users found the "Join Now" button difficult to locate, which slowed down the signup process. Additionally, hesitation points centered around unclear pricing, the absence of customer reviews, and a lack of product previews, all of which contributed to lower engagement. However, incentives such as first-time discounts, prominently displayed customer reviews, and detailed product previews significantly increased the likelihood of signup, emphasizing the importance of transparency and user trust in driving conversions.

To optimize the signup process and enhance user engagement, the "Join Now" button should be centered and visually emphasized on key pages for better visibility. Introducing clear product previews and showcasing authentic customer reviews earlier in the signup journey will help build trust and transparency. Additionally, testing incentives such as first-time member discounts or bonus items can significantly improve acquisition rates. Streamlining the signup and account creation process with engaging elements—such as interactive visual quizzes—will create a more personalized and enjoyable experience, ultimately encouraging users to complete their registration.

---

<h3 id="Sample">Minimum Sample Size and Duration for Reliable Results</h3>

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

Therefore, we will conduct the A/B experiment in 20 days.
