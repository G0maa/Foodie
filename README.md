# Foodie

A feature breakdown for a **food delivery application** — actors, example user journeys, and an epic → feature decomposition. Produced as a product-scoping / mentorship exercise.

## Table of Contents

- [Actors](#actors)
- [User Journeys (Examples)](#user-journeys-examples)
  - [Customer](#customer)
  - [Delivery Man (Courier)](#delivery-man-courier)
  - [Restaurant Cashier](#restaurant-cashier)
  - [Restaurant Owner](#restaurant-owner)
- [Features](#features)
  - [Auth](#auth)
  - [Account](#account)
  - [Search](#search)
  - [Restaurant](#restaurant)
  - [Menu](#menu)
  - [Order](#order)
  - [Delivery](#delivery)
  - [Payment](#payment)
  - [Payout](#payout)
  - [Rating](#rating)
  - [Admin Dashboard (inc. Customer Support)](#admin-dashboard-inc-customer-support)
  - [Notification](#notification)
  - [Fraud](#fraud)
- [Non-functional Features](#non-functional-features)

## Actors

| Actor Name         | Actor Type     | Description                                                                                                               |
| ------------------ | -------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Customer           | Primary        | End user on the demand side — browses restaurants, builds and pays for orders, tracks delivery, rates the experience.     |
| Delivery Man       | Primary        | Last-mile courier — accepts delivery jobs, picks up from the restaurant, delivers to the customer, earns per trip.        |
| Customer Support   | Administrative | Internal agent who resolves issues after the fact — refunds, disputes, "where's my order," account help.                  |
| System             | Administrative | Automated, time-triggered behavior — auto-assign nearest driver, auto-cancel unaccepted orders, scheduled notifications.  |
| System Admin       | Administrative | Platform operator — manages users/restaurants, configures the platform, monitors health, handles escalations.            |
| Payment Gateway    | External       | Third-party service (Stripe, PayPal, etc.) that processes charges, payouts, and refunds via API.                          |
| Restaurant Cashier | Secondary      | Restaurant-floor staff who accepts/rejects incoming orders and updates prep status (preparing → ready).                   |
| Restaurant Owner   | Secondary      | Restaurant manager who sets up menu, pricing, and hours, and reviews sales, analytics, and payouts.                       |

## User Journeys (Examples)

### Customer

1. Register/login => Browse restaurants => search for food => add to basket => checkout => add address => apply coupon => add payment method => place order => track order => receive order => rate order

### Delivery Man (Courier)

1. Register/login => Go online => Receive nearby orders => Choose order to deliver => go to restaurant => receive order => deliver order => go to customer => contact customer => proof order got received => receive payment => rate customer

### Restaurant Cashier

1. Login => go online => receive orders => accept/reject orders => mark preparing => mark ready for pickup => give orders to delivery men

### Restaurant Owner

1. Register/login => add restaurant name => add location => add menu => add items => add item options => add images => add prices => add opening hours => add bank details => accept terms and commission => submit for approval => go online

## Features

### Auth

1. Register using Phonenumber
2. Login using Phone number
3. Login using Google
4. Login using Apple
5. Logout

### Account

1. Update account details
2. Delete Account (Close Account)
3. Manage addresses (add/edit/delete)

### Search

1. Search Restaurants
2. Location Based search
3. Search Items
4. Location based search

### Restaurant

1. On-boarding of restaurant owner
2. Create Restaurant
3. Add Restaurant details (e.g. location, opening hours)
4. Delete Restaurant
5. Create coupon codes
   1. Create Global coupon codes (Admin)
   2. Create Restaurant specific codes (Restaurant Owner)
6. Delete coupon codes
7. pause/ready orders
8. accept terms
9. Add bank details
10. Manage staff

### Menu

1. Add menu item
2. Add menu item images
3. Add menu item options
4. Add menu item prices

### Order

1. Add item to basket
2. Edit item in basket
3. Remove item from basket
4. Apply coupon
5. Place Order
6. Restaurant accept order (?)
7. Live tracking of order
8. Cancel Order

### Delivery

1. Delivery men go online
2. Delivery pickup order
3. Delivery contact customer
4. Delivery earnings
5. Send order to delivery men
6. Delivery men Accept order
7. Proof of delivery

### Payment

1. Add payment card
2. Remove payment card
3. Pay using COD
4. Pay using Payment card
5. Refund payment

### Payout

1. Request payout
2. Send payout (delivery man/restaurant)

### Rating

1. Rate order
2. Rate restaurant
3. Rate item
4. Rate delivery man
5. Rate customer

### Admin Dashboard (inc. Customer Support)

1. Accepting restaurants

### Notification

1. Push notification for nearby orders (delivery man)
2. Push notification for order status (customer)

### Fraud

1. ...

## Non-functional Features

1. Assume Mobile app for customer.
