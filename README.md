Download Link: https://assignmentchef.com/product/solved-int2005-lab04
<br>
Database Management System

<strong> </strong>

<h1> View</h1>




<strong>What is a View?</strong>

A view is a logical table based on a table or another view. A view contains no data of its own but is like a window through which data from tables can be viewed or changed. The tables on which a view is based are called <strong><em>base tables</em></strong>. The view is stored as a SELECT statement in the data dictionary.




<strong> </strong>

<strong>Syntax for creating a view </strong><strong><em> </em></strong>

<strong><em> </em></strong>

<h2>CREATE[OR REPLACE]</h2>

<strong>    </strong><strong>VIEW</strong><strong> view_name </strong><strong>[(</strong><strong>column_list</strong><strong>)]</strong>

<strong>    </strong><strong>AS</strong><strong> select_statement </strong><strong>;</strong>




<strong>Updatable Views:</strong>

<ul>

 <li>A simple view is one that:</li>

 <li>Derives data from only one table</li>

 <li>Contains no functions or groups of data</li>

 <li>Can perform DML operations through the view</li>

</ul>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>Non-updatable Views: </strong>

<ul>

 <li>A complex view is one that:</li>

 <li>Derives data from many tables</li>

 <li>Contains functions or groups of data</li>

 <li>Does not always allow DML operations through the view</li>

</ul>




<strong>The Syntax of CREATE VIEW statement</strong>:

Documentation: <a href="https://dev.mysql.com/doc/refman/8.0/en/create-view.html">https://dev.mysql.com/doc/refman/8.0/en/create</a><a href="https://dev.mysql.com/doc/refman/8.0/en/create-view.html">–</a><a href="https://dev.mysql.com/doc/refman/8.0/en/create-view.html">view.html</a>




<u>Note:</u> The MySQL error code 1064 is a syntax error. This means the reason there’s a problem is because MySQL doesn’t understand what you’re asking it to do.




<h3>Switch to SQL Editor</h3>

<ul>

 <li>You should specify the classicmodels database before writing SQL statements using the following command:</li>

</ul>

USE db_name;




The <a href="https://dev.mysql.com/doc/refman/8.0/en/use.html">USE</a> statement tells MySQL to use the named database as the default (current) database for subsequent statements. This statement requires some privilege for the database or some object within it. <strong> </strong>

<u>Note:</u> The MSRP is “Manufacturer’s suggested retail price” (ราคาขายปลกี แนะน าของผผู้ ลติ).

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>MySQL Workbench: </strong>

<ul>

 <li>You can see details of a table by clicking i button below:</li>

 <li>You can see the existing view by clicking “Views” menu below:</li>

</ul>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>













<strong> </strong>

<strong>Task 1: Using the “classicmodels” database and write SQL statements to answer the following questions. </strong>

<strong> </strong>

use classicmodels;




<ol>

 <li>Create a view named “mini_customer_view” to display the customer name of all customers whose names start with the word “Mini”. Please verify by querying data from this view.</li>

</ol>




<ol start="2">

 <li>Create a view named “prod_stock_view” to display the product name and quantity in stock of the product that has the minimum quantities in stock. Please verify by querying data from this view.</li>

</ol>




<ol start="3">

 <li>Create a view named “totalamount_orders_view” to display the order number, order date and the total amount of sales of all orders and sort the results in descending order by the total amount of sales. Name three columns of the view to orderno, orderdate and total_amount, respectively. Please verify by querying data from this view.</li>

</ol>




<ol start="4">

 <li>Create a view named “customer_samecity_view” to display the customer name and city of all customers who live in the same city of their sales rep employee’s office city. Name two view columns to cust_name and cust_city, respectively. Please verify by querying data from this view.</li>

</ol>




<ol start="5">

 <li>Create a view named “maxcredit_city_view” to display the city and the maximum credit limit of all customers in each city. Please verify by querying data from this view.</li>

</ol>




<ol start="6">

 <li>Create a view named “maxcredit_london_view” to display the city and the maximum credit limit of all customers who live in London city. You should create this view from the “maxcredit_city_view” view in <u>Question 5</u>. Please verify by querying data from this view.</li>

</ol>




<ol start="7">

 <li>Create a table named “offices_copy” with copying the structure and data from the “offices” table using the following commands:</li>

</ol>




create table offices_copy          as select * from offices;




Create a view named “usa_office_view” to display office code, city and state of the country “USA”  from the “offices_copy” table. Please verify by querying data from this view.




<ol start="8">

 <li>Try to insert a new row into the “offices_copy” table through the “usa_office_view” view created in <u>Question 7</u>. What happens about the data insertion? Please explain.</li>

</ol>




<ol start="9">

 <li>To resolve the problem found in <u>Question 8</u>, Please modify the “usa_office_view” view to ensure that you can insert a new row through this view (an updatable view). Please show the data insertion of the “offices_copy” table.</li>

</ol>

<u>Hint: </u>You can create a new row by yourself.




<ol start="10">

 <li>Please delete both the structure and data of the “offices_copy” table. What happens to an existing view that references the “offices_copy” table? Please explain.</li>

</ol>


