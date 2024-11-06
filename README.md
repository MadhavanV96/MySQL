# MySQL Task

## -- To create the ecommerce database:
```sql
>CREATE DATABASE ecommerce;
```

```sql
>USE ecommerce;
```

## -- To create the customers table with id, name, email, and address:


```sql
> CREATE TABLE customers (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    address VARCHAR(255)
);
```


## -- Create orders table


> CREATE TABLE orders (
    id INT AUTO_INCREMENT PRIMARY KEY,
    customer_id INT,
    order_date DATE,
    total_amount DECIMAL(10, 2),
    FOREIGN KEY (customer_id) REFERENCES customers(id)
);

## -- Create products table
> CREATE TABLE products (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    price DECIMAL(10, 2),
    description TEXT
);


## -- Insert sample data into customers table 

> INSERT INTO customers (name, email, address) VALUES
('Edward Torphy', 'Idella_Koss@gmail.com', 'Gary'),
('Dana Lakin', 'Callie_Mante92@gmail.com', 'San Ramon'),
('Henry Smitham', 'Antwon.Gusikowski3@yahoo.com', 'Tillmanbury'),
('Jeffery Farrell', 'Brandt.Douglas61@yahoo.com', 'North Kurtis'),
('Glenn Lebsack', 'Ernesto.Robel@yahoo.com', 'Bayerstead'),
('Claire Gibson', 'Laurianne_Mosciski@yahoo.com', 'Koreyport'),
('Allen Hackett', 'Jacklyn70@yahoo.com', 'West Tadhaven'),
('Forrest Wisoky', 'Merlin41@hotmail.com', 'Lake Alexanderstad'),
('Beth Walter', 'Korey_Windler80@gmail.com', 'Ornboro'),
('Vicky Kreiger', 'Elliott_Bahringer31@gmail.com', 'Starkworth'),
('Leslie Considine', 'Skylar_Miller@hotmail.com', 'Kuhlmanfort'),
('Mildred Daniel', 'Grant47@gmail.com', 'Kesslerfurt'),
('Mr. William Vandervort', 'Verda_Becker@yahoo.com', 'East Mariofurt'),
('Clyde Koelpin', 'Marquis.Kshlerin@gmail.com', 'Hackensack'),
('Samantha Price II', 'Mavis_McGlynn51@gmail.com', 'New Frankfort'),
('Joan Heaney', 'Brandon84@gmail.com', 'Nampa'),
('Dr. Brendan Corwin', 'Asia.Erdman@gmail.com', 'Coon Rapids'),
('Freda Goldner', 'Dudley98@hotmail.com', 'North Leafort'),
('Alexander Spinka', 'Antonietta.Jast@gmail.com', 'Sonnyshire'),
('Bryant Veum', 'Keshawn_Hirthe90@yahoo.com', 'Uptonstead'),
('Louise Spencer', 'Terrence.Bode50@hotmail.com', 'Fort Rubenboro'),
('Mr. Mindy Thompson', 'Kyle.Greenfelder@yahoo.com', 'Orenberg'),
('Louise Okuneva', 'Mark_Koepp78@yahoo.com', 'Fort Velma'),
('Hubert Bogan', 'Queen4@yahoo.com', 'North Nicklaus'),
('Allan Romaguera', 'Marisa6@yahoo.com', 'Bodestead'),
('Reginald Lueilwitz', 'Dominique13@yahoo.com', 'Cincinnati'),
('Mark Rolfson', 'Uriah.Terry83@gmail.com', 'Moriahfield'),
('Dustin Runolfsdottir IV', 'Amelie.Cummerata@gmail.com', 'Clarksville'),
('Dr. Tracy Schaden', 'Claud_Anderson@gmail.com', 'Tarynchester'),
('Miss Juana Sanford', 'Carmela14@gmail.com', 'Rebecaville');


## -- Insert sample data into products table (30 products)
> INSERT INTO products (name, price, description) VALUES
INSERT INTO products (name, price, description) VALUES
('Product A', 25.00, 'Durable home appliance'),
('Product B', 30.00, 'Latest tech gadget'),
('Product C', 45.50, 'Eco-friendly kitchen tool'),
('Product D', 55.00, 'High-quality furniture item'),
('Product E', 15.00, 'Affordable stationery'),
('Product F', 10.00, 'Portable charger for mobile devices'),
('Product G', 20.00, 'Wireless earbuds with great sound quality'),
('Product H', 80.00, 'Smart home assistant device');
('Product I', 60.00, 'Stylish and ergonomic office chair'),
('Product J', 35.00, 'Compact Bluetooth speaker'),
('Product K', 25.50, 'Stainless steel water bottle'),
('Product L', 40.00, 'Noise-canceling headphones'),
('Product M', 50.00, 'High-performance laptop stand'),
('Product N', 45.00, 'Wireless keyboard and mouse combo'),
('Product O', 75.00, 'Smart thermostat for energy savings'),
('Product P', 90.00, 'Electric kettle with temperature control'),
('Product Q', 12.00, 'Eco-friendly reusable shopping bags'),
('Product R', 20.00, 'Digital alarm clock with LED display'),
('Product S', 85.00, 'Adjustable standing desk converter'),
('Product T', 30.00, 'Portable mini fan for desk'),
('Product U', 55.00, 'High-definition web camera'),
('Product V', 22.50, 'USB-C hub for multi-device connectivity'),
('Product W', 15.00, 'Cable management kit'),
('Product X', 100.00, 'Smart light bulbs, pack of 4'),
('Product Y', 65.00, 'Advanced fitness tracker watch'),
('Product Z', 120.00, 'Robot vacuum cleaner with app control');


> INSERT INTO orders (customer_id, order_date, total_amount) VALUES
 (12, CURDATE() - INTERVAL 25 DAY, 980.00),
(27, CURDATE() - INTERVAL 30 DAY, 637.00),
(17, CURDATE() - INTERVAL 34 DAY, 237.00),
(2,CURDATE() - INTERVAL 15 DAY, 640.00),
(18, CURDATE() - INTERVAL 12 DAY, 793.00),
(15, CURDATE() - INTERVAL 38 DAY, 184.00),
(28, CURDATE() - INTERVAL 51 DAY, 471.00),
(14, CURDATE() - INTERVAL 65 DAY, 460.00),
(26, CURDATE() - INTERVAL 48 DAY, 706.00),
(16, CURDATE() - INTERVAL 46 DAY, 797.00),
(17, CURDATE() - INTERVAL 24 DAY, 850.00),
(10, CURDATE() - INTERVAL 13 DAY, 718.00),
(8,CURDATE() - INTERVAL 26 DAY, 474.00),
(26, CURDATE() - INTERVAL 5 DAY, 438.00),
(21, CURDATE() - INTERVAL 2 DAY, 241.00),
(2,CURDATE() - INTERVAL 20 DAY, 697.00),
(7, CURDATE() - INTERVAL 1 DAY, 331.00),
(12, CURDATE() - INTERVAL 1 DAY, 182.00),
(17, CURDATE() - INTERVAL 17 DAY, 91.00),
(19,CURDATE() - INTERVAL 12 DAY, 856.00),
(13, CURDATE() - INTERVAL 14 DAY, 140.00),
(29, CURDATE() - INTERVAL 11 DAY, 617.00),
(14, CURDATE() - INTERVAL 13 DAY, 340.00),
(19,CURDATE() - INTERVAL 8 DAY, 511.00),
(14, CURDATE() - INTERVAL 48 DAY, 477.00),
(10, CURDATE() - INTERVAL 62 DAY, 591.00),
(18, CURDATE() - INTERVAL 41 DAY, 488.00),
(13, CURDATE() - INTERVAL 40 DAY, 129.00),
(6, CURDATE() - INTERVAL 16 DAY, 84.00),
(10, CURDATE() - INTERVAL 4 DAY, 135.00);


## -- Insert sample data into order_items table (normalized item-level details per order)
> CREATE TABLE order_items (
    id INT AUTO_INCREMENT PRIMARY KEY,
    order_id INT,
    product_id INT,
    quantity INT,
    FOREIGN KEY (order_id) REFERENCES orders(id),
    FOREIGN KEY (product_id) REFERENCES products(id)
);


## -- Insert data into order_items to reference items in each order
> INSERT INTO order_items (order_id, product_id, quantity) VALUES
(12,15,5),
(17,12,4),
(6,4,3),
(14,5,2),
(10,6,2),
(2,24,4),
(8,8,1),
(13,6,4),
(7,16,2),
(26,5,1),
(8,6,2),
(2,2,2),
(6,4,3);


## -- Queries for the e-commerce system:

### -- 1. Retrieve all customers who have placed an order in the last 30 days.
> SELECT DISTINCT customers.name
FROM customers
JOIN orders ON customers.id = orders.customer_id
WHERE orders.order_date >= CURDATE() - INTERVAL 30 DAY;


### -- 2. Get the total amount of all orders placed by each customer.
> SELECT customers.name, SUM(orders.total_amount) AS total_spent
FROM customers
JOIN orders ON customers.id = orders.customer_id
GROUP BY customers.name;



### -- 3. Update the price of Product C to 45.00.
> UPDATE products
SET price = 45.00
WHERE name = 'Product C';


### -- 4. Add a new column `discount` to the products table.
> ALTER TABLE products
ADD COLUMN discount DECIMAL(5, 2) DEFAULT 0.00;


### -- 5. Retrieve the top 3 products with the highest price.
> SELECT name, price
FROM products
ORDER BY price DESC
LIMIT 3;


### -- 6. Get the names of customers who have ordered Product A.
> SELECT DISTINCT customers.name
FROM customers
JOIN orders ON customers.id = orders.customer_id
JOIN order_items ON orders.id = order_items.order_id
JOIN products ON order_items.product_id = products.id
WHERE products.name = 'Product A';



### -- 7. Join the orders and customers tables to retrieve the customer's name and order date for each order.
> SELECT customers.name, orders.order_date
FROM customers
JOIN orders ON customers.id = orders.customer_id;


### -- 8. Retrieve the orders with a total amount greater than 150.00.
> SELECT *
FROM orders
WHERE total_amount > 150.00;


### -- 9. The `order_items` table was created earlier to normalize the data by storing items for each order, allowing a many-to-many relationship between `orders` and `products`.


### -- 10. Retrieve the average total of all orders.
> SELECT AVG(total_amount) AS average_order_total
FROM orders;



