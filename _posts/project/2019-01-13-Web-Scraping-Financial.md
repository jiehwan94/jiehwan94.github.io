---
layout: post
bigtitle:  '[Finance] Web Scraping Financial Data'
subtitle:   
categories:
    - project
    - side-projects
tags:
    - finance
    - side-projects
related_posts:
    - _posts/project/2019-02-02-Stock-Comparison-Tool.md
    - _posts/project/2019-04-05-Tech-Analysis-Tool.md
published: true
---


# Web Scraping Financial Data

## Motivation

I recently read a book, Rich Dad Poor Dad, written by Robert Kiyosaki in which the author advocates the importance of "financial literacy" and building wealth through investing in assets, real estate investing, and even starting and owning businesses. Although I don't have a good wealth of money now, his book solidified my vision of financial freedom and triggered me to seriously think about and reframe my economic perspective. So I started reading books related to stock investment.

After reading recommended books on stock investment, I learned that there are mainly two methodologies of investment analysis: fundamental and technical analysis. Although I developed a simple Stock Explorer using technical analysis, I found the technical analysis way too complicated and out of my league. On the other hand, I agreed with the idea of fundamental analysis that the stock price is simply a mirror of the health of the company. In terms of company evaluation, I can focus on the financial statements of companies including revenues, earnings, future growth, return on equity, profit margins, etc, which are already available on Yahoo Finance as shown below:

![2](/assets/img/project/Finance/Web_Scraping/2.png)
---

## Data Gathering

Yahoo Finance offers plenty of good information on its website. Fortunately, a little of bit research led me to get a clean json format of yahoo finance data as shown below:

![3](/assets/img/project/Finance/Web_Scraping/3.png)

From the nicely parsed json data, I searched a list of company stock code (called tickers) and ran a for loop to scrape each company's financial information by writing an R script as shown below:


![4](/assets/img/project/Finance/Web_Scraping/4.png)

Here is a snapshot of the scraped excel file:
![5](/assets/img/project/Finance/Web_Scraping/5.png)

---
## Data Cleansing
After scraping, I went through the scraped data and found that some variables are meaningless. I had to think about how to deal with Null values. In regards to handling missing data from my experience, I understand that there is NO good way to deal with missing data. Even a relatively small amount of absent observations on some variables can dramatically shrink the sample size-- resulting in lower precision of confidence intervals, weaker statistical power, and biased parameter estimates. Before jumping to data imputation, I first have to understand the reason why data go missing which generally falls in the following categories:

- **Missing at Random**: data point missing is not related to the missing data, but it is related to some of the observed data.

- **Missing Completely at Random**: Missing data have nothing to do with its hypothetical value and with the values of other variables.

- **Missing not at Random**: Two possible reasons are that the missing value depends on the hypothetical value (e.g. People with high salaries generally don't want to reveal their incomes in surveys) or missing value is dependent on some other variable's value (e.g. In an assumption that females generally don't want to reveal their ages, the missing value in age variable is impacted by gender variable).

In the first two cases, it is safe to remove the data with missing values depending upon their occurrences, while in the third case removing observations with missing values can produce a bias in the model. So we have to be really careful before removing observations. There are also different methods for deletion of data:

- Listwise: removes all data for an observation that has one or more missing values. It is often disadvantageous to use listwise deletion method as it produces biased parameters and estiamtes.

- Pariwise: analyzes all cases in which the variables of interest are present and thus maximizes all data available by an analysis basis.

- Dropping variables: I personally believe that it is always better to keep data than to discard it. Sometimes you can drop variables if the data is missing for more than 60% of observations but only if that variable is insignificant. Having said that, I prefer imputation over dropping variables.

The scraped financial data had 5 variables with more than 60% of observations missing, so I dropped those variables. For other variables with missing values, I utilized the mean imputation method, bearing in mind that it may reduce variance in the data set.

---
## Stay tuned!
There are companies that sell well-structured financial data for a significant amount of money. I am glad that I was able to do it my own way at no cost. Although it was quiet demanding at times, I am very thrilled about the follow-up side-projects I will be able to create with this gem!
