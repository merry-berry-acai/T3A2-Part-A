# Smoothie & Açaí Shop Online Ordering App

## Table of Contents

- [Smoothie \& Açaí Shop Online Ordering App](#smoothie--açaí-shop-online-ordering-app)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
    - [Tech Stack](#tech-stack)
  - [Dataflow Diagram](#dataflow-diagram)
  - [Application Architecture](#application-architecture)
    - [Layers](#layers)
  - [User Stories](#user-stories)
    - [Customer Perspective](#customer-perspective)
    - [Shop Owner Perspective](#shop-owner-perspective)
  - [Wireframes](#wireframes)
    - [Screenshots](#screenshots)
  - [Trello Board](#trello-board)
    - [Board Structure](#board-structure)

## Project Overview

The Smoothie & Açaí Shop Online Ordering App aims to enhance customer experience and streamline operations for a health-focused retail business. The app provides a user-friendly platform for customers to browse menus, customise orders, and track their orders, while offering efficient management tools for shop owners.

### Tech Stack

- **Front-end**: React.js
- **Back-end**: Node.js & Express
- **Database**: MongoDB
- **Design Tools**: Figma

## Dataflow Diagram

The Data Flow Diagram (DFD) visually represents how data moves through the application. It illustrates the interaction between users and the different layers of the system. Here's a detailed breakdown:

- **User Interaction Layer:** This is where users interact with the application via the front-end. When a user browses the menu, customizes an order, or makes a payment, these actions initiate data flow.
- **Data Input:** User actions are input to the system. For instance, when browsing the menu, the user is requesting data from the server.
- **Back-End Processing Layer:** The back-end, built with Node.js and Express, receives user requests. It processes these requests, interacts with the database, and sends responses back to the front-end. This layer handles business logic, such as calculating order totals and validating user inputs.
- **Data Storage:** The database, using MongoDB, stores all data related to the application. This includes menu items, user information, and order details. Data is read from and written to the database by the back-end.
- **Data Output:** The back-end sends processed data to the front-end. This might include displaying a menu, updating order status, or confirming a payment.
- **Data Flow:** The DFD also shows how the data flows between these layers. For example, when a customer places an order, the flow is: user input on the front-end, request to back-end, data processing and storage in the database, and confirmation back to the front-end. The specific details of this flow will be illustrated in the diagram itself.

[Insert DFD Here]

## Application Architecture

This section details the system's layered architecture, ensuring separation of concerns and scalability.

### Layers

1. **Presentation Layer**: React.js handles user interface.
2. **Business Logic Layer**: Node.js manages application logic.
3. **Data Access Layer**: MongoDB stores data with Mongoose as ORM.

[Insert Diagram Here]

## User Stories

Categorised by user roles, these stories highlight key functionalities.

### Customer Perspective

- As a customer, I want to browse the menu to explore available smoothies and açaí bowls.
- As a customer, I want to customise my order to include specific add-ons.
- As a customer, I want to track my order status to know when it's ready.

### Shop Owner Perspective

- As a shop owner, I want to manage menu items to update prices and descriptions.
- As a shop owner, I want to view sales reports to analyse revenue trends.

## Wireframes

Visual designs for key app screens ensure an intuitive user experience.

### Screenshots

1. **Menu Browsing**
2. **Order Customisation**
3. **Checkout Process**
4. **Order Tracking**

## Trello Board

Organised task management using Trello demonstrates efficient project tracking.

### Board Structure

- Lists: To Do, In Progress, Testing, Done
- Cards: Feature tasks (e.g., "Implement menu browsing")

[Insert Screenshots Here]

