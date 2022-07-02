# 8-Week-SQL-Challenge
This repository contains case studies crafted from https://8weeksqlchallenge.com/

**Case Study #1: Danny's Diner**

<img width="500" alt="Screen Shot 2022-07-02 at 12 26 27 pm" src="https://user-images.githubusercontent.com/108335477/176983399-e001685a-20ae-4dbb-a2cb-622d38650350.png">

**Business Objective**

Danny wants to use the data to answer a few simple questions about his customers, especially about their visiting patterns, how much money they’ve spent and also which menu items are their favourite

**Entity Relationship Diagram**

![127271130-dca9aedd-4ca9-4ed8-b6ec-1e1920dca4a8](https://user-images.githubusercontent.com/108335477/176983497-ef4193af-664b-44ea-9e62-9ffdb962ad81.png)

**Case Study Questions**

1. What is the total amount each customer spent at the restaurant?
2. How many days has each customer visited the restaurant?
3. What was the first item from the menu purchased by each customer?
4. What is the most purchased item on the menu and how many times was it purchased by all customers?
5. Which item was the most popular for each customer?
6. Which item was purchased first by the customer after they became a member?
7. Which item was purchased just before the customer became a member?
8. What is the total items and amount spent for each member before they became a member?
9. If each $1 spent equates to 10 points and sushi has a 2x points multiplier - how many points would each customer have?
10. In the first week after a customer joins the program (including their join date) they earn 2x points on all items, not just sushi - how many points do customer A and B have at the end of January?

**Solution**

1. What is the total amount each customer spent at the restaurant?

<img width="433" alt="Screen Shot 2022-07-02 at 2 25 01 pm" src="https://user-images.githubusercontent.com/108335477/176986432-ca335274-a187-4c6d-87ae-7b9221597c95.png">

Thought Process:

-Use SUM and GROUP BY to find out the total_sales contributed by each customer. Note here I have renamed sum as 'total_sales'.

-Use JOIN to merge sales and menu tables as customer_id and price are from both tables.

<img width="269" alt="Screen Shot 2022-07-02 at 2 37 13 pm" src="https://user-images.githubusercontent.com/108335477/176986710-6c86decd-ce1a-4db5-ad1d-1eecf833e415.png">

