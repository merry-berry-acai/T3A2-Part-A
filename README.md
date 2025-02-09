# Smoothie & Açaí Shop Online Ordering App

## Table of Contents

- [🥤 Smoothie & Açaí Shop Online Ordering App](#smoothie--açaí-shop-online-ordering-app)
  - [📌 Project Overview](#project-overview)
    - [🏆 Core Objectives](#core-objectives)
    - [🛠️ Tech Stack](#tech-stack)
  - [🗺️ Dataflow Diagram](#dataflow-diagram)
    - [🔑 Key Components](#key-components)
  - [🏗️ Application Architecture](#application-architecture)
    - [📂 Layers](#layers)
  - [🚀 Features](#features)
    - [🍓 Browse Menu](#-browse-menu)
    - [🥤 Customize Orders](#-customize-orders)
    - [🛒 Persistent Shopping Cart](#-persistent-shopping-cart-frontend-state)
    - [🛍️ Order Management & History](#-order-management--history)
    - [📊 Real-Time Order Tracking](#-real-time-order-tracking)
    - [🔒 Secure Payment Processing](#-secure-payment-processing)
    - [💰 Promo Codes & Discounts](#-promo-codes--discounts)
    - [⭐ User Reviews & Ratings](#-user-reviews--ratings)
    - [🔐 Authentication (JWT & OAuth2)](#-authentication-jwt--oauth2)
    - [📱 Responsive Design](#-responsive-design)
  - [🎯 Target Audience](#target-audience)
  - [📐 Wireframes](#wireframes)
    - [🖼️ Screenshots](#screenshots)
  - [📌 Trello Board](#trello-board)
    - [📋 Board Structure](#board-structure)


# Project Overview

# 🎯 Purpose of the **Merry Berry Smoothie & Açaí Shop** Project

**Merry Berry Smoothie & Açaí Shop** is a full-stack solution designed to enhance the online ordering experience for health-conscious customers. The project’s main objective is to offer a platform where customers can easily browse, customize, order, and enjoy a variety of smoothies, açaí bowls, and other health-focused snacks—all with a few clicks. With this platform, we aim to provide not only delicious and nutritious options but also a smooth and user-friendly digital experience that simplifies the ordering process.

---

## 🏆 **Core Objectives:**

### 1. **Empower Healthy Eating:**
The primary goal of the project is to promote healthier food choices. By providing easy access to smoothies, açaí bowls, and other nutritious snacks, we are enabling customers to make better eating decisions and integrate healthy habits into their everyday lives.

### 2. **Provide a Seamless Digital Ordering Experience:**
The project is focused on creating a user-friendly digital platform where customers can explore menu items, customize orders, and track deliveries with minimal effort. Whether they are ordering on their phone, tablet, or desktop, the shopping experience is designed to be intuitive and responsive.

### 3. **Efficient Order Management:**
The project ensures a smooth and efficient order placement process. With a persistent shopping cart, real-time order tracking, and a robust order history feature, users can quickly review their past purchases and reorder with ease, fostering customer loyalty and satisfaction.

### 4. **Integration of Secure Payment Solutions:**
Ensuring the security of customer payments is a key focus. The project integrates **Stripe** for payment processing, ensuring safe and efficient transactions while providing various payment options like credit cards and digital wallets (Apple Pay, Google Pay).

### 5. **Offer Personalization and Flexibility:**
Customers can personalize their orders by selecting their preferred sizes, toppings, and special instructions. This level of customization allows for a tailored experience that meets individual tastes and dietary preferences.

### 6. **Promote Customer Engagement:**
By enabling user reviews and ratings, the project fosters a sense of community, where customers can share their experiences and provide valuable feedback on products. This helps to continuously improve the offerings and ensures customer satisfaction.


# Features

## 🍓 Browse Menu
**Feature:**
Customers can explore the menu, which includes a variety of smoothies, açaí bowls, and other products, each displayed with essential details for an engaging shopping experience.

**Details:**
- **Categories for Easy Navigation:** Products are grouped into categories like "Smoothies," "Açaí Bowls," and "Snacks" so customers can quickly find what they need.
- **High-Quality Images:** Each product includes a visually appealing image to help customers decide.
- **Detailed Descriptions:** Customers can view a list of ingredients and key benefits (e.g., "Rich in antioxidants").
- **Pricing Information:** Base price is clearly displayed, and additional costs (e.g., extra toppings) are shown before checkout.
- **Availability Status:** Only items that are currently in stock will be shown to customers.

## 🥤 Customize Orders
**Feature:**
Customers can personalize their orders based on preferences such as size, toppings, and special instructions before adding items to their cart.

**Details:**
- **Size Selection:** Some drinks may offer different sizes (Small, Medium, Large), with prices adjusting accordingly.
- **Topping Choices:** Customers can choose from a predefined list of toppings, such as chia seeds, honey, or protein powder, with pricing shown for each.
- **Special Instructions:** Customers can add free-text notes (e.g., "Less ice, please").

## 🛒 Persistent Shopping Cart (Frontend State)
**Feature:**
Customers can build their cart dynamically, and the cart remains available even if they leave the page.

**Details:**
- **Cart Stored on Frontend:** The cart is managed using React state (or a similar approach) instead of storing it in a database.
- **Persistence:** Even after a page refresh, the cart remains available by saving items in local storage.
- **Real-Time Updates:** Users can:
  - Add items with customized options.
  - Remove individual items or clear the entire cart.
  - Modify existing items (e.g., changing the quantity or toppings).
- **Cart Summary:** Displays itemized costs, subtotal, and estimated total before checkout.

## 🛍️ Order Management & History
**Feature:**
Users can place orders and track their past purchases in their account dashboard.

**Details:**
- **Order Placement:** Once checkout is complete, the order is stored in the Orders Collection.
- **Order Details Stored:** Each order record contains:
  - Item names and quantities
  - Selected toppings or customizations
  - Total price paid
  - Order date and time
- **Order History:** Users can view all past orders and quickly reorder a previous purchase with one click.

## 📊 Real-Time Order Tracking
**Feature:**
After placing an order, users can track its status in real time.

**Details:**
- **Order Status Updates:** The system tracks an order through four key stages:
  - **Processing:** Order received and being prepared.
  - **In Progress:** Smoothie is being blended and packed.
  - **Ready for Pickup:** Order is completed and available at the store.
  - **Out for Delivery:** If delivery is enabled, customers receive real-time delivery updates.
- **Live Updates:** Users can refresh their order page or receive push notifications for updates.

## 🔒 Secure Payment Processing
**Feature:**
Customers can securely complete their purchases using a reliable third-party payment processor.

**Details:**
- **Stripe Integration:** Payments are handled via Stripe, ensuring safe and fast transactions.
- **Secure Checkout Flow:** Uses HTTPS encryption and tokenized payments to protect sensitive financial data.
- **Multiple Payment Methods:** Customers can pay using:
  - Credit or debit cards
  - Digital wallets (Apple Pay, Google Pay)
- **Order Confirmation:** After a successful transaction, users receive an email confirmation and receipt.

## 💰 Promo Codes & Discounts
**Feature:**
Customers can apply promo codes to receive discounts during checkout.

**Details:**
- **Discount Validation:** The system checks if a promo code is:
  - Valid (active within its start and end date).
  - Eligible for the cart total (e.g., a $10-off code might require a $50+ purchase).
  - Applicable to specific items (e.g., "Get 20% off all smoothies, but not snacks").
- **Automatic Discount Application:** If the promo code is valid, the system deducts the discount from the total price.
- **Error Handling:** If a code is invalid or expired, users get a clear message explaining why it cannot be applied.

## ⭐ User Reviews & Ratings
**Feature:**
Customers can leave feedback on menu items by submitting a star rating and written review.

**Details:**
- **Rating System:** Users can assign a 1 to 5-star rating to each menu item.
- **Review Submission:** Customers can provide comments on their experience (e.g., "Great smoothie, but a bit too sweet!").
- **Review Storage:** All reviews are stored in the Reviews Collection, linked to both:
  - The user who submitted the review
  - The menu item being reviewed
- **Public Visibility:** Reviews appear on the menu item’s page for other customers to see.

## 🔐 Authentication (JWT & OAuth2)

**Feature:**
Secure user authentication using JWT for stateless sessions and OAuth2 for third-party login integration.

**Details:**

### **JWT Authentication**
- **User Registration:** New users can create an account by providing necessary information such as email, username, and password.
- **Login:** Existing users can log in using their username/email and password. Upon successful login, a **JWT token** is generated and sent back to the user.
  - The JWT token contains:
    - User information (e.g., user ID)
    - Expiration time
    - A secret key to verify the authenticity of the token.
- **Token Storage:** The token is stored in local storage or an HTTP-only cookie, depending on security requirements.
- **Token Validation:** For each subsequent request, the user sends the token in the HTTP Authorization header as `Bearer <token>`. The backend validates the token, ensuring it's not expired or tampered with.
- **Secure Routes:** Routes requiring authentication (such as placing an order or viewing order history) check if the request includes a valid JWT token.

### **OAuth2 Authentication**
- **Third-Party Login Integration:** Users can log in using their **Google**, **Facebook**, or other OAuth2-supported platforms.
- **OAuth2 Flow:** The application follows the standard OAuth2 authorization flow:
  1. **Authorization Request:** The user is redirected to the third-party platform’s login page.
  2. **Access Token Retrieval:** After the user logs in, the third-party platform redirects back to the application with an authorization code, which is exchanged for an access token.
  3. **User Information:** The access token is used to request user information from the third-party platform’s API (such as name, email, etc.).
- **Token Handling:** The application stores the OAuth2 access token, either in local storage or session storage, to manage the user session.
- **Account Linking:** If the user already has an account, they can link their third-party OAuth2 login to their existing account for future logins.

### **Secure Routes and Role-Based Access**
- **JWT Middleware:** The backend checks for a valid JWT token for any protected routes. If the token is invalid or expired, the user is denied access and asked to log in again.
- **Role-Based Access:** Users with different roles (e.g., admin, regular user) have access to different routes:
  - Admins can view and manage all orders and users.
  - Regular users can only view and manage their own orders.

### **Logout:**
- **JWT Logout:** When the user logs out, the token is deleted from the local storage or invalidated by the backend if using a token blacklist.
- **OAuth2 Logout:** The user is logged out from the OAuth2 provider (e.g., Google) and their session is ended in the application.

### **Token Expiry & Refresh Tokens**
- **Access Token Expiry:** JWT tokens typically have a short lifespan (e.g., 15 minutes). After expiration, the user must either log in again or use a **refresh token**.
- **Refresh Tokens:** A refresh token is issued alongside the access token and is used to obtain a new access token when the original expires.
  - Refresh tokens are stored securely and can be exchanged for a new access token by sending the refresh token to a secure endpoint.

---

### Summary of Authentication Features:
✔ **JWT Authentication** ensures stateless, secure sessions for users.  
✔ **OAuth2 Integration** allows third-party logins for easier user access.  
✔ **Token Expiry & Refresh** ensures a smooth user experience with minimal disruptions.  
✔ **Role-Based Access** secures the app by restricting routes based on user roles. 

## 📱 Responsive Design
**Feature:**
The website is optimized for a seamless shopping experience across mobile, tablet, and desktop.

**Details:**
- **Flexible UI Components:** Uses Tailwind CSS to ensure a modern and responsive layout.
- **Mobile-First Approach:** Pages adapt to different screen sizes, with smooth navigation for smaller devices.
- **Touch-Friendly Elements:** Buttons and inputs are designed for easy tapping on touchscreens.

---

## 🎯 **Target Audience**  

The **Merry Berry Smoothie & Açaí Shop** platform is tailored to meet the needs of a diverse customer base that values health, convenience, and digital accessibility. Below is a detailed breakdown of the target audience:  

---

### **👥  Health-Conscious Consumers 🥑**  
 
- Individuals committed to maintaining a healthy diet.  
- People focused on balanced nutrition and natural ingredients.  
- Those following dietary plans such as **vegan, keto, high-protein, or gluten-free**.  

🎯 **Why They Need Merry Berry:**  
- Access to **fresh, organic, and nutrient-rich** smoothies and bowls.  
- Ability to customize orders based on dietary needs.  
- Transparency in ingredients and nutritional benefits.  

---

### **👥  Fitness Enthusiasts & Athletes 🏋️‍♂️**  

- Gym-goers, runners, and sports professionals.  
- Those seeking **high-protein, low-sugar, or energy-boosting** meal options.  

🎯 **Why They Need Merry Berry:**  
- **Post-workout recovery** smoothies with protein add-ons.  
- Easily accessible **nutrient-dense snacks** to fuel workouts.  
- Ability to track past orders and reorder their favorite blends.  

---

### **👥 Busy Professionals & Students 📚**  
 
- Office workers, entrepreneurs, and students with **hectic schedules**.  
- People who prefer fast, **on-the-go** meals.  

🎯 **Why They Need Merry Berry:**  
- Quick ordering and **pickup-ready** meals.  
- Mobile-friendly platform for **ordering during work/study breaks**.  
- Secure payment processing for fast transactions.  

---

### **👥 Tech-Savvy Digital Shoppers 📱**  
- Consumers who prefer **online ordering over in-store purchases**.  
- Millennials and Gen Z users who engage with brands digitally.  

🎯 **Why They Need Merry Berry:**  
- **User-friendly interface** with smooth browsing and checkout.  
- **Real-time order tracking** and notifications.  
- Multiple payment options, including **Apple Pay & Google Pay**.  

---

### **👥 Local Community & Regular Customers 🏡**  

- Customers who frequently visit smoothie and açaí bowl shops.  
- Those who want a **personalized loyalty experience**.  

🎯 **Why They Need Merry Berry:**  
- **Order history & quick reorder** for favorite items.  
- Access to **promo codes and discounts**.  
- **In-store pickup & delivery tracking** for added convenience.  


### Tech Stack

- **Front-end**: React.js
- **Back-end**: Node.js & Express
- **Database**: MongoDB
- **Design Tools**: Figma

## Dataflow Diagram

The DFD outlines the flow of data within the system, showing interactions between users and the application layers.

### Key Components

1. **User Interaction Layer**: Front-end requests initiated by users.
2. **Back-end Processing**: Node.js processes requests and interacts with MongoDB.
3. **Database Layer**: Storage of menu items, orders, and user information.

[Insert Diagram Here]

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

