---
layout: post
bigtitle:  'Fundraiser for Childhood Cancer: Reflection on Web App Improvement'
subtitle:   
categories:
    - project
    - side-projects
tags:
    - side-projects
published: true
---

# Fundraiser for Childhood Cancer: Reflection on Web App Improvement

---
>"I have a dream that one day I can play soccer with my friends"

A five-year-old boy said with a hopeful smile upon his lips.


Each year, the parents of approximately 15,300 kids will hear the words "your child has cancer." Across all ages, ethnic groups and socio-economic statuses, this disease remains the number one cause of death by disease in children. Despite major advances -- from an overall survival rate of 10 percent just fifty years ago to nearly 90 percent today, the survival rate is much lower for many rare cancers. Furthermore, the number of diagnosed cases annually has not declined in nearly 20 years.


Here are some quick statistics on Childhood Cancer:

Each day, 43 children are diagnosed with cancer.

12% of children diagnosed with cancer do not survive.

Children's cancer affects all ethnic, gender, and socio-economic groups.

The average age of children diagnosed is six.

More than 40,000 children undergo treatment for cancer each year.

60% of children who survive cancer suffer late-effects, such as infertility, heart failure, and secondary cancers.

There are approximately 375,000 adult survivors of children's cancer in the United States.

---
### Why not help them ourselves?

When I studied in Korea as a visiting student , I had an opportunity to host a fundraising event for children with childhood cancer. Inspired by the viral Youtube channel called Shoot for Love, three of my friends and I gathered to plan a fundraising event during 3-day-long school Fall Festival.


The concept was simple:

Anyone at the festival could participate in kicking a ball to a target by paying 500 won (50 cents).

The participant's score is saved in the system.

People have access to the overall standings scoreboard and see where they are ranked.

To promote the fundraising event, we posted videos on Facebook and asked participants to share videos and comment their friends to participate in a meaningful and heartwarming event together.

Below is a  photo and the pamphlet from the fundraising event:

<br>

<div class="me">
    <div><img src= "/assets/img/project/Fundraiser/1.jpg"></div>
    <div><img src= "/assets/img/project/Fundraiser/2.jpg"></div>
    <div><img src= "/assets/img/project/Fundraiser/3.jpg"></div>
    <div><img src= "/assets/img/project/Fundraiser/4.jpg"></div>
    <div><img src= "/assets/img/project/Fundraiser/5.jpg"></div>
    <div><img src= "/assets/img/project/Fundraiser/6.jpg"></div>
</div>

  <script>
    $(document).ready(function(){
      $('.me').slick();
    });
  </script>


In result, the fundraising event ended with great success:

900+ participants

Raised 764,630 won (260% more than goal)

We donated all collection as well as the soccer balls we used during the event to the Korean Childhood Cancer Ass.


It is always a phenomenal feeling to cooperate and help others in needs in any possible ways we can!

---
## Engaging more participants by building a new application

After the fundraising event ended with great success, I reflected on what else we could have done better. I thought it would be more engaging and therefore attract more participants if the website had visualization. The website we used for the event only showed  the overall standings scoreboard as shown below:

![5](/assets/img/project/Fundraiser/8.png)

The original app was not attractive

So I developed a new web application using shiny.

![5](/assets/img/project/Fundraiser/9.png)

The new shiny app promotes a sense of competition.

Here is a quick video of the shiny application I built.

[![IMAGE ALT TEXT](/assets/img/project/Fundraiser/11.png)](https://www.youtube.com/watch?v=tKa5p1ybGSE "Shiny Web App Demo__Fundraiser for Childhood Cancer")

I added the following features:

Gauge bar: To display how much collection has been raised to reach the goal (top-left)

Tabs: To display visualizations (bar charts), information about childhood cancer, row deletion, etc.

Bar charts: To promote a sense of competition across different colleges, departments, and teams


It was a blast building this shiny app as I knew this could not only contribute to help children receive more medical care, but the fundraising event as a whole would give a sense of warm community to the participants, not to mention the children :)
