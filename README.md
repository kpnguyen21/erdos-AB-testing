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

We’re Amour Beauty Box - a beauty subscription designed to help you discover indie gems, clean beauty, and viral favorites (yes, the ones you keep seeing on TikTok). We're working on making our website and sign-up experience even better, and we’d love your input!
This short survey takes about 3–4 minutes and helps us shape the perfect subscription experience - from first click to first unboxing.
As a thank you, you'll be entered to win a $50 Amour Beauty Box shop credit.

<h4 id="Section-1">Section 1: First Impressions</h4>

1. What features of our membership stood out to you when you first visited our website? (Select all that apply)
- [x] Discounted products
- [ ] Free gifts
- [x] Early access to launches
- [x] Exclusive content
- [ ] Flexible cancellatin
- [ ] None of the above

2. On your first visit, how easu was it to understand the membership includes?
- [ ] Very easy
- [ ] Easy
- [ ] Neutral
- [x] Difficult
- [ ] Very difficult

3. Which of the following caused confusion or hesitation while considering signing up?
- [ ] Lack of clear pricing
- [ ] No customer reviews/ testimonials
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

6. How would you prefer to set your beauty preference and skin type?
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
- [ ] Trust badges (e.g., "secure checkout")
- [x] Verified customer reviews
- [x] Trial period
- [ ] Other (please specify): ___________________

9. What would motivate you to try a new beauty subscription box for the first time?
- [ ] A discounted first box
- [ ] A free bonus item from a trending brand
- [x] A personalized quiz to match products to me
- [ ] Seeking product previews on TikTok/ Instagram
- [ ] Knowing it features eco-friendly or clean beauty brands 

10. What kind of message would most convince you to hit "Subscribe"?
- [ ] "Get TikTok's hottest products before they sell out"
- [ ] "Build your prefect box in under 2 minutes"
- [x] "First box just $9.99 - no commitment"
- [ ] "Curated clean beauty from emerging brands"
- [ ] "Join 100,000+ subscribers who love their boxes"

<h4 id="Section-4">Section 4: Decision-Making Drivers</h4>

11. When choosing a beauty subscription box, which of these is most important to you?
- [ ] The ability to discover new brands
- [ ] Getting the best value for my money
- [ ] Eco-conscious and sustainable practices
- [x] Personalization to my skin type and preferences
- [ ] Following the latest beauty trends

12. When you're thinking about subscribing, what do you want to see before making the decision? (Select all the apply)
- [x] Real photos/ videos of past boxes
- [ ] Clear pricing with no surprises
- [x] Brand names I recognize and trust
- [x] A way to customize or preview my box
- [ ] Reviews or social media feedback from others

13. How do you feel about the current subscription pricing and options?
- [x] Clear and easy to understand
- [ ] Too many choices - simplify it
- [ ] Needs more flexibitlity (e.g., pause or skip box options)
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

- Conversion refers to any action taken online that aligns with a business’s goals, such as filling out a form, making a purchase, or completing a survey. In this study, the conversion rate represents the proportion of people who sign up for the subscription.
- Revenue is a continuous metric that directly impacts the business's bottom line.

First, we consider conversion rate, which represents the number of conversions within a given timeframe and is typically expressed as a percentage. For example, if 100 visitors access a website and 10 make a purchase, the conversion rate is 10%. This metric helps businesses assess how effectively their website converts visitors into customers.

Secondly, we also conduct an A/B test on revenue, as a high conversion rate does not necessarily imply high revenue. For example, Amour Beauty Box may have more people signing up for the monthly box, resulting in a high conversion rate but lower revenue. Conversely, if fewer people sign up but opt for annual payments, it would yield a lower conversion rate but higher revenue.

<h4 id="H0">Null hypotheses and Alternative hypotheses</h4>

<p float="left">
  <img src="/Figure/control.PNG" width="400" />
  <img src="/Figure/variant.PNG" width="400" /> 
</p>



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
