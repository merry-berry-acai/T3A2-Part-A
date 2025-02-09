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

## 🌟 Vision
To become the leading online platform empowering healthy lifestyles by providing a seamless and delightful experience for ordering nutritious smoothies and açaí bowls, fostering a community of health-conscious individuals.

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


## Features

### 🍓 Browse Menu

**Feature:**
Enables customers to easily explore our offerings, directly supporting Objective 1 (Empower Healthy Eating) by showcasing the variety of healthy options. This is especially important for Health-Conscious Consumers and Busy Professionals who want to quickly see what's available.

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


## Tech Stack

- **Front-end**: `React.js`
- **Back-end**: `Node.js & Express`
- **Database**: `MongoDB`
- **Design Tools**: `Figma`

### Tech Stack Justification
We have chosen `React.js` for the front-end to build a dynamic and responsive user interface, crucial for reaching our diverse target audience across devices. 
`Node.js with Express` provides a scalable and efficient back-end, ideal for handling real-time order updates and secure transactions. 
`MongoDB`'s NoSQL nature allows for flexible data schemas, accommodating the evolving needs of our menu and user data. 
`Figma` was selected for collaborative and iterative wireframing and UI design.


## 🗺️ Dataflow Diagram: Visualizing Data Flow within the Merry Berry System

To comprehensively illustrate the flow of data within the Merry Berry Smoothie & Açaí Shop Online Ordering App, we have developed a Dataflow Diagram (DFD). This diagram adheres strictly to standard DFD conventions and provides a clear, visual representation of how data moves through our application, from user interactions to database storage and backend processing.  The DFD is essential for understanding the system's data handling processes and ensuring data integrity throughout the application lifecycle.

### 🔑 Key Components of the Dataflow Diagram

Our Dataflow Diagram explicitly identifies and depicts the following key components, adhering to standard DFD notation:

*   **External Entities:**  These represent actors or systems outside of our application that interact with it.  In our DFD, the primary External Entity is the **"Customer"**, who initiates requests and receives data from the system.  We also implicitly consider the **"Payment Gateway (Stripe)"** as an external entity for payment processing.
*   **Processes:**  Processes represent actions or transformations performed by the system on the data. Our DFD clearly identifies all critical processes within the Merry Berry application. Examples include:
    *   `Browse Menu Items`:  The process of retrieving and displaying menu information to the customer.
    *   `Customize Order`:  The process of handling user selections for order modifications (size, toppings, etc.).
    *   `Add to Cart`: The process of storing selected items in the user's shopping cart.
    *   `Process Order`: The core process encompassing order placement, validation, and storage.
    *   `Process Payment`:  The interaction with the external Payment Gateway (Stripe) to handle transactions.
    *   `Track Order Status`:  The process of updating and displaying the real-time status of an order.
    *   `Manage Menu Items (Admin)`:  (Potentially depicted if admin functionalities are within scope of the DFD) The process for shop owners to update menu information.
*   **Data Stores:** Data Stores represent where data is held or persisted within the system. Our DFD clearly indicates the primary Data Store:
    *   `MongoDB Database`:  Representing our MongoDB database, which stores menu items, user data, order information, and reviews.
*   **Data Flows:** Data Flows represent the movement of data between entities, processes, and data stores.  Our DFD meticulously labels each data flow with a descriptive name indicating the data being transferred. Examples include:
    *   `Menu Item Request`: Data flow from Customer to `Browse Menu Items` process.
    *   `Menu Item Details`: Data flow from `MongoDB Database` to `Browse Menu Items` process.
    *   `Customization Selections`: Data flow from Customer to `Customize Order` process.
    *   `Order Details`: Data flow between various processes and to the `MongoDB Database`.
    *   `Payment Information`: Data flow to and from the `Process Payment` process and `Payment Gateway (Stripe)`.
    *   `Order Status Update`: Data flow from backend processes to the Customer.

The complete Dataflow Diagram, visually representing these components and their interactions, is available as a separate image file in the [`docs/diagrams/`](./docs/diagrams/) directory, named `dataflow_diagram.png`.  This diagram provides a detailed and standards-compliant view of data movement within the Merry Berry application.

[Insert DFD here]

---

## 🏗️ Application Architecture Diagram: Layered Structure for Scalability and Maintainability

To illustrate the high-level structure and architectural design of the Merry Berry Smoothie & Açaí Shop application, we have created an Application Architecture Diagram (AAD). This diagram visually represents the layered architecture of our system, demonstrating a clear separation of concerns and our strategic approach to building a scalable, maintainable, and robust application.  The AAD provides an "almost flawless" understanding of the application's structural organization and component interactions.

### 📂 Layers of the Application Architecture

Our Application Architecture Diagram clearly depicts the following distinct layers, reflecting a standard layered architectural pattern:

*   **Presentation Layer:**  This layer is responsible for handling user interactions and presenting the user interface.  As shown in the AAD, the **React.js Frontend** constitutes our Presentation Layer. It encompasses all React components, UI elements, and client-side logic responsible for rendering the user interface and handling user input.
*   **Business Logic Layer (Application Layer):** This layer encapsulates the core application logic, business rules, and processing.  In our architecture, the **Node.js & Express Backend** forms the Business Logic Layer.  This layer houses our API endpoints, server-side logic for order processing, authentication, data validation, and interaction with the Data Access Layer. Key components within this layer include:
    *   API Controllers (handling routes and requests)
    *   Services (encapsulating business logic for specific features like order management, menu management, user authentication)
    *   potentially Middleware (for authentication, request logging, etc.)
*   **Data Access Layer:** This layer is responsible for managing data persistence and interaction with the database.  The **MongoDB Database** and **Mongoose ORM** together constitute our Data Access Layer.  Mongoose acts as an Object-Document Mapper, facilitating interaction with the MongoDB database. This layer handles database queries, data retrieval, and data storage operations.

The Application Architecture Diagram visually connects these layers and indicates the flow of requests and data between them.  It demonstrates how the Presentation Layer (Frontend) interacts with the Business Logic Layer (Backend API), which in turn interacts with the Data Access Layer (MongoDB).

The complete Application Architecture Diagram, visually representing these layers and their interconnections, is available as a separate image file in the [`docs/diagrams/`](./docs/diagrams/) directory, named `architecture_diagram.png`. This diagram provides a clear and comprehensive overview of the Merry Berry application's high-level architecture.

[Insert AAD here]

## User Stories

## Persona 1: Emily - The Fitness-Focused Health Seeker

**Persona Description:** Emily, 28, is a dedicated fitness enthusiast living a busy, health-conscious lifestyle in the city.  She works as a marketing professional and prioritizes regular exercise and nutritious eating to maintain her energy levels and well-being. Emily is training for a half-marathon and is very conscious of her macronutrient intake, particularly post-workout protein and natural sugars. After intense gym sessions, she seeks quick, healthy, and customizable meal options that align with her fitness goals.  She values efficiency and appreciates technology that simplifies her healthy lifestyle choices.

### User Story 1: Browse Menu with Dietary Filters and Visual Appeal

- **What:** As Emily, a **Fitness-Focused Health Seeker**, I want to easily browse the menu with distinct categories (smoothies, açaí bowls, toppings), dietary filters (vegan, gluten-free, high-protein, low-sugar), and high-quality images for each item.

- **Why:** So that **I can quickly discover healthy and appealing options that perfectly fit my dietary needs and training regime, allowing me to make informed and efficient choices after my workouts without spending unnecessary time searching.**  I need to ensure the food I order supports my fitness goals and dietary preferences, and a visually rich, well-organized menu will help me do this quickly.

- **Revision:** Following initial user feedback and usability testing, the menu was significantly improved to include comprehensive dietary filters (vegan, gluten-free, added keto, low-sugar options) and high-resolution, mouth-watering photos for every menu item. Originally, the menu was a simple, text-based list with limited categorization, which users found overwhelming and difficult to navigate quickly when trying to make healthy choices on the go.

### User Story 2: Customize Orders for Personalized Nutrition

- **What:** As Emily, a **Fitness-Focused Health Seeker**, I want to precisely customize my açaí bowl or smoothie to suit my specific nutritional requirements by easily adding or removing ingredients (like almond milk, various protein powders, specific fruits, seed types, etc.) and specifying portion sizes.

- **Why:** To ensure that **my purchase not only tastes fantastic but also perfectly aligns with my post-workout nutritional goals, allowing me to fine-tune the macronutrient profile (protein, carbohydrate, healthy fat content) to optimally support my training and recovery.**  Precise customization empowers me to take control of my nutrition and maximize the health benefits of my meal.

- **Revision:** Based on user input and Emily's persona needs, the customization feature was significantly expanded to enable a wider range of dietary preferences and nutritional adjustments.  Beyond the original three basic selections, we incorporated options for keto-friendly, low-sugar, and high-protein customizations, reflecting the diverse dietary needs of health-conscious users like Emily.  We also improved the UI for customization to be more intuitive and visually clear, making it easier for users to see the impact of their choices on the nutritional content of their order.

### User Story 3: Track Order Status in Real-Time for Time Management

- **What:** As Emily, a **Fitness-Focused Health Seeker**, I want to be able to track my order status in real-time, with clear updates on each stage (e.g., "Preparing," "Blending," "Ready for Pickup"), displayed with a progress bar and timely notifications.

- **Why:** To effectively plan my time after my workout and gym sessions, **allowing me to precisely time my arrival for pickup or anticipate delivery, avoid unnecessary waiting at the shop, and seamlessly integrate my healthy meal into my busy schedule without disrupting my workout routine or other commitments.**  Knowing the exact order status gives me control and reduces stress in my time-constrained day.

- **Revision:**  The order tracking feature was substantially enhanced for a superior user experience by adding a visually informative progress bar that dynamically updates through each stage of order fulfillment.  We also implemented push notifications (initially planned for future iteration, but prioritized based on user feedback emphasizing the importance of real-time updates) to proactively inform users of status changes without requiring constant page refreshing.  This revision directly addresses the need for efficient time management expressed by busy, fitness-focused users like Emily.

## Persona 2: John - The Busy Professional Seeking Quick & Healthy Lunch

**Persona Description:** John, 35, is a busy marketing manager working long hours in a demanding corporate environment.  He values convenience and efficiency, especially during his limited lunch breaks. John is increasingly health-conscious and wants to make better food choices but often struggles to find healthy options that are also quick and easy to access near his office. He appreciates streamlined digital experiences and relies heavily on mobile ordering for lunch.

### User Story 4: Quick Reorder of Favorite Items for Lunchtime Efficiency

- **What:** As John, a **Busy Professional Seeking Quick & Healthy Lunch**, I would like to be able to quickly reorder my favorite smoothie or açaí bowl combinations from my past order history with just a single click or tap, directly from the homepage or order history section.

- **Why:** To drastically save time during my short lunch breaks and ensure that **I can consistently get my preferred healthy and satisfying meal as quickly and effortlessly as possible, maximizing my limited break time for relaxation and recharging before returning to work.**  Reordering saves me from having to browse and customize my order each time, which is crucial when time is of the essence.

- **Revision:** To maximize accessibility and user convenience for busy professionals like John, the reorder option was strategically moved from the initially less prominent account settings area to a more easily discoverable location directly on the homepage and within the order history section.  This placement ensures that frequent reordering is a primary and effortless action, aligning with the user need for speed and efficiency during lunch breaks.  We also added visual cues (like a "heart" icon on past orders) to further highlight and encourage the reorder functionality.

## Persona 3: Maria - The Shop Owner Optimizing Operations

**Persona Description:** Maria, 40, is the owner and manager of the Merry Berry Smoothie & Açaí Shop. She is passionate about providing healthy and delicious options to her community and is focused on efficiently managing her shop's operations to ensure customer satisfaction and profitability. Maria needs tools to streamline order management, understand customer preferences, and optimize her menu offerings.

### User Story 5: Real-Time Order Management Dashboard for Operational Efficiency

- **What:** As Maria, the **Shop Owner Optimizing Operations**, I need a comprehensive and real-time dashboard that allows me to efficiently view and manage all incoming online orders, track their status, and prioritize them effectively.  The dashboard should display key order details, customer notes, and order history.

- **Why:** To effectively prioritize and fulfill incoming orders in a timely manner, **enabling me to optimize my shop's operations, minimize customer wait times, reduce order errors, and ultimately increase customer satisfaction and repeat business.  Real-time order visibility is crucial for efficient workflow management within my shop and ensuring smooth service during peak hours.**

- **Revision:**  The order management dashboard, initially displaying only basic order details, was significantly enhanced based on Maria's operational needs and feedback.  We added key features such as customer-provided special notes (e.g., allergy information, specific requests), a readily accessible customer order history view (to anticipate regular customer preferences), and priority flags to highlight large or urgent orders.  These additions empower Maria to manage orders more proactively, personalize service, and optimize her shop's workflow for peak efficiency.

## Persona 4: Sarah - The First-Time App User Seeking Easy Onboarding

**Persona Description:** Sarah, 22, is a tech-savvy college student who is new to the Merry Berry app and is exploring healthy food options in her area.  She is comfortable with mobile apps and online ordering but appreciates a smooth and intuitive onboarding experience when trying a new platform. Sarah is also budget-conscious and interested in any promotions or discounts for first-time users.

### User Story 6: Interactive Onboarding Tutorial for Seamless First Experience

- **What:** As Sarah, a **First-Time App User Seeking Easy Onboarding**, I would need a brief, interactive tutorial that guides me through the key features of the app as soon as I launch it for the first time, showing me how to browse the menu, customize orders, and place my first order smoothly.

- **Why:** To quickly feel comfortable and confident using the app without needing to search for help or figure things out on my own, **ensuring a positive first impression and encouraging me to explore the app's features and place my first order without frustration.  A good onboarding experience is essential for me to adopt a new app and become a regular user.**

- **Revision:**  To significantly improve user engagement and reduce initial user friction, the onboarding tutorial was completely redesigned from a primarily text-based walkthrough to a more engaging and interactive experience.  We incorporated interactive elements, subtle animations to highlight key UI elements, and progress indicators to guide Sarah through the app's core functionalities in a user-friendly and visually appealing manner.  This revision directly addresses the need for intuitive onboarding for new users like Sarah, maximizing app adoption and first-time user conversion.

### User Story 7:  Visible Discounts and Promotions to Incentivize First Order

- **What:** As Sarah, a **First-Time App User Seeking Easy Onboarding**, I would want to easily see any available promotions and discounts specifically for first-time users, displayed prominently when I first open the app or browse the menu.

- **Why:** To save money on my first order and feel like I'm getting good value as a new user, **incentivizing me to place my first order and explore the app's offerings.  As a budget-conscious student, discounts and promotions are a significant factor in my purchasing decisions, and clear visibility of these offers will encourage me to try Merry Berry.**

- **Revision:**  To enhance the visibility of promotions and attract new users like Sarah, discounts and promotional banners were strategically moved from a less prominent location within the menu section to a highly visible position at the top of the homepage. This placement ensures that first-time users are immediately aware of any available offers, maximizing the impact of promotions on app downloads and initial order conversions.  We also made the promotional banners visually appealing and clearly indicated the terms and conditions of each offer.

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

