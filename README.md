# 8-Week-SQL-Challenge
This repository contains case studies crafted from https://8weeksqlchallenge.com/

Tool Used: PgAmin 4

**Case Study #1: Danny's Diner**

<img width="500" alt="Screen Shot 2022-07-02 at 12 26 27 pm" src="https://user-images.githubusercontent.com/108335477/176983399-e001685a-20ae-4dbb-a2cb-622d38650350.png">

**Business Objective**

Danny wants to use the data to answer a few simple questions about his customers, especially about their visiting patterns, how much money they’ve spent and also which menu items are their favourite

**Entity Relationship Diagram**

![127271130-dca9aedd-4ca9-4ed8-b6ec-1e1920dca4a8](https://user-images.githubusercontent.com/108335477/176983497-ef4193af-664b-44ea-9e62-9ffdb962ad81.png)

**Case Study Questions**

1. What is the total amount each customer spent at the restaurant?
2. How many days has each customer visited the restaurant?
3. What was the first item from the menu purchased by each customer? (_working in progress_)
4. What is the most purchased item on the menu and how many times was it purchased by all customers?
5. Which item was the most popular for each customer?
6. Which item was purchased first by the customer after they became a member?
7. Which item was purchased just before the customer became a member?
8. What is the total items and amount spent for each member before they became a member?
9. If each $1 spent equates to 10 points and sushi has a 2x points multiplier - how many points would each customer have?
10. In the first week after a customer joins the program (including their join date) they earn 2x points on all items, not just sushi - how many points do customer A and B have at the end of January?

**Solution**

**1. What is the total amount each customer spent at the restaurant?**

<img width="433" alt="Screen Shot 2022-07-02 at 2 25 01 pm" src="https://user-images.githubusercontent.com/108335477/176986432-ca335274-a187-4c6d-87ae-7b9221597c95.png">

Thought Process:

-Use SUM and GROUP BY to find out the total_sales contributed by each customer. Note here I have renamed sum as 'total_sales'.

-Use INNER JOIN to merge sales and menu tables as customer_id and price are from both tables.

<img width="269" alt="Screen Shot 2022-07-02 at 2 37 13 pm" src="https://user-images.githubusercontent.com/108335477/176986710-6c86decd-ce1a-4db5-ad1d-1eecf833e415.png">

**2. How many days has each customer visited the restaurant?**

<img width="617" alt="Screen Shot 2022-07-02 at 2 46 45 pm" src="https://user-images.githubusercontent.com/108335477/176986902-bb2134c1-a497-4692-9c53-7b388d3bb499.png">

Thought Process:

-Use DISTINCT and COUNT to avoid duplicates and count the customer's visit. 

<img width="263" alt="Screen Shot 2022-07-02 at 2 51 38 pm" src="https://user-images.githubusercontent.com/108335477/176986989-7a26c6d8-e18c-4ffc-aecd-8439cc7b4476.png">

**3. What was the first item from the menu purchased by each customer? (working in progress)**

**4. What is the most purchased item on the menu and how many times was it purchased by all customers?**

<img width="601" alt="Screen Shot 2022-07-03 at 4 22 00 pm" src="https://user-images.githubusercontent.com/108335477/177027671-0e04258d-a8d1-47ed-abc3-8aaec1c527db.png">

Thought Process:

-Use COUNT number of product_id and ORDER BY most_purchased (renamed) by descending order.

<img width="301" alt="Screen Shot 2022-07-03 at 4 22 09 pm" src="https://user-images.githubusercontent.com/108335477/177027746-cc1eb533-61f1-41fc-8bc5-1793f3e69a95.png">



