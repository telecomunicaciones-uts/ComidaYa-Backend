# COMIDAYA
![ComidaYa](https://github.com/user-attachments/assets/a19ca071-b217-444c-b1ac-5a78f7ba91c5)

Este repositorio universitario, es de la carrera de Ingeniería en Telecomunicaciones de las Unidades Tecnológicas de Santander; Para la recreación de una APIREST, con un enfoque de un resturante.

# DATABASE SUMMARY. 
This database is designed to manage information for an online ordering system for restaurants. Below is an overview of its main components and how they are related:

## 1. Users
The database begins with the Users table, which stores basic information about each user in the system. Each user has a unique identifier (user_id), name, email, password, phone number, address, and a user type (such as customer, administrator, or delivery person).

## 2. Clients
The Customers table is linked directly to the Users table through user_id. Contains additional details specific to customers, such as name, email, phone, and address. This allows us to distinguish between different types of users and manage information more efficiently.

## 3. Restaurants
The Restaurants table stores information about the restaurants available in the system. Each restaurant has a unique identifier (restaurant_id), along with its name, address, telephone number, email, and opening and closing times. This table allows you to manage the data of the restaurants that offer the menus and dishes.

## 4. Menus
Each restaurant can have one or more Menus. The Menus table includes a unique identifier (menu_id), a reference to the restaurant offering the menu (restaurant_id), and details such as the name, description, and price of the menu.

## 5. Dishes
Within each menu, there are the Dishes. The Dishes table contains information about each available dish, such as the unique identifier (dish_id), a reference to the menu it belongs to (menu_id), the name, description, price, and an image of the dish. This makes it easier for customers to choose what they want to order.

## 6. Orders
When a customer places an order, a record is created in the Orders table. This table records the unique identifier of the order (order_id), the user who placed it (user_id), the restaurant where the order was placed (restaurant_id), the date and time of the order, and the status of the order (such as in preparation, in road or delivered).

## 7. Order Details
For each order, the Order_Details table details the dishes included. It includes a unique identifier (detail_id), the order it belongs to (order_id), the specific dish (dish_id), the quantity of the dish, and the subtotal associated with that dish.

## 8. Reviews
Customers can leave Reviews about restaurants. The Reviews table includes a unique identifier (review_id), the user who left the review (user_id), the restaurant reviewed (restaurant_id), a rating from 1 to 5 stars, a comment, and the date of the review.

## 9. Invoices
Each order can be associated with an Invoice, which includes a unique identifier (invoice_id), a reference to the order (order_id), the date the invoice was issued, the invoice total and the payment method used.

## 10. Invoice Detail
The Invoice_Detail table provides a detailed breakdown of each invoice. It contains a unique identifier (invoice_detail_id), the invoice to which it belongs (invoice_id), the invoiced plate (plate_id), the quantity, the unit price and the subtotal.

## 11. Delivery drivers
Finally, the Delivery Drivers table manages the information of the delivery drivers who deliver the orders. It includes a unique identifier (deliverer_id), a reference to the user in the Users table (user_id), name, telephone number, type of vehicle they use, license number (optional) and their availability (such as available or busy).

# Key Relationships
Users and Clients: Clients are related to users through the user_id, allowing their additional details to be managed.
Restaurants and Menus: Menus are associated with a specific restaurant using restaurant_id.

Menus and Dishes: Dishes belong to a specific menu, linked through the id_menu.

Orders and Order Details: Each order can have multiple details, indicating the dishes and quantities requested.

Invoices and Orders: Each order can have an associated invoice, with a detailed breakdown of the dishes billed.

Delivery Drivers and Orders: Delivery drivers can be assigned to several orders, managing deliveries.

![ComidaYa](https://github.com/user-attachments/assets/c8402106-a34e-4e47-b39b-dc8db8d4721a)


## Members:
* Edwin Duarte 
* Edwar Caro
