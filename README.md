# WhatsNext Vision Motors

## Salesforce CRM Implementation for Automotive Sales and Service

### Project Overview

**WhatsNext Vision Motors** is a Salesforce-based CRM solution developed for an automotive company to improve customer experience and streamline vehicle sales and service operations.

The project provides a centralized platform to manage **customers, vehicles, dealers, orders, test drives, and service requests**. It also uses Salesforce automation and Apex programming to reduce manual work and enforce important business rules.

The primary focus of the project is to automate the vehicle ordering process, validate vehicle stock availability, automatically assign the nearest dealer, and maintain accurate order statuses.

---

## Objectives

- Centralize vehicle, customer, dealer, and order information in Salesforce.
- Manage vehicle stock and availability efficiently.
- Prevent customers from placing orders for out-of-stock vehicles.
- Automatically assign orders to the nearest dealer based on customer location.
- Track customer orders and their fulfillment status.
- Manage test drive schedules and reminders.
- Manage customer service requests.
- Automate periodic stock monitoring and availability updates.
- Reduce manual effort and improve operational efficiency.

---

## Key Features

### Vehicle Management

The system stores and manages vehicle information such as vehicle name, model, price, vehicle type, stock quantity, and availability status.

Vehicle stock information is used during the order creation process to determine whether a vehicle is currently available for purchase.

### Customer Management

Customer records store important information such as name, email, phone number, address, and location.

Customer location is used to support automatic dealer assignment during the ordering process.

### Dealer Management

Dealer records contain dealership information and location details.

The system uses customer and dealer location information to identify and assign the nearest dealer to a customer's order.

### Order Management

Customers can place orders for available vehicles.

Before an order is processed, the system validates the vehicle's stock availability. Orders are maintained with information such as customer, vehicle, dealer, order date, quantity, and order status.

### Stock Validation

The system prevents customers from placing orders for vehicles that are out of stock.

This business rule is implemented using **Apex Triggers**, ensuring that stock validation is performed at the backend level.

If the vehicle is available, the order can proceed. If the vehicle is unavailable, the system prevents the invalid transaction or maintains the order as pending based on the implemented business process.

### Automatic Dealer Assignment

The system automatically assigns the nearest dealer to an order using the customer's location and dealer location information.

This eliminates the need for employees to manually select a dealer and makes the ordering process more efficient.

### Order Status Management

Order status is maintained based on vehicle stock availability.

- **Confirmed** – when the required vehicle is available.
- **Pending** – when the vehicle is currently unavailable.

This provides clear visibility into the current status of customer orders.

### Test Drive Management

Customers can schedule test drives for selected vehicles.

Test drive records maintain information such as the customer, vehicle, date, time, and status. Automated reminders can also be used to notify customers about upcoming test drives.

### Service Request Management

Customers can raise service requests related to their vehicles.

Service request records can contain details such as request type, description, priority, and status, allowing the company to track customer service requirements efficiently.

---

## Salesforce Automation

The project combines Salesforce declarative automation with programmatic development.

### Record-Triggered Flow

Record-Triggered Flows are used to automate business processes when Salesforce records are created or updated.

Flows provide a low-code approach for implementing automation where Apex is not required.

### Apex

Apex is used to implement custom business logic that requires programmatic processing.

The project uses Apex for important requirements such as stock validation and dealer assignment.

### Apex Triggers

Apex Triggers are used to enforce business rules when records are inserted or updated.

The main trigger functionality includes:

- Validating vehicle stock before processing an order.
- Preventing invalid orders.
- Initiating automatic dealer assignment.
- Supporting order status management.

### Trigger Handler

The project follows a **Trigger Handler pattern** to separate trigger logic from business logic.

The trigger acts as the entry point, while the handler class contains the actual processing logic.

This improves:

- Code organization
- Maintainability
- Reusability
- Testability
- Scalability

### Batch Apex

Batch Apex is used to process large numbers of vehicle records efficiently.

The batch process can periodically check vehicle stock levels and update vehicle availability information.

This is useful when the organization has a large volume of vehicle records.

### Scheduled Apex

Scheduled Apex is used to execute stock-related processes automatically at predefined times.

It can be used to schedule the Batch Apex process for periodic stock monitoring and availability updates.

---

## Data Model

The project uses Salesforce objects and relationships to represent the automotive business requirements.

The major entities include:

- Customer
- Vehicle
- Dealer
- Order
- Test Drive
- Service Request

Relationships between these records allow customer, vehicle, dealer, sales, and service information to be managed in a centralized Salesforce environment.

---

## Business Rules

The following key business rules are implemented:

1. A customer should not be allowed to place an order for an out-of-stock vehicle.
2. Available vehicle orders should be assigned to the appropriate nearest dealer.
3. Order status should reflect the current vehicle availability.
4. Vehicle stock should be periodically monitored and updated.
5. Scheduled test drives should be managed and customers can be notified through automated reminders.

---

## Salesforce Concepts Used

- Salesforce CRM
- Data Modelling
- Custom Objects
- Custom Fields
- Object Relationships
- Lightning App Builder
- Record-Triggered Flow
- Apex Classes
- Apex Triggers
- Trigger Handler Pattern
- SOQL
- Batch Apex
- Scheduled Apex
- Process Automation
- Business Rule Validation

---

## Benefits

### Customer Benefits

- Simplified vehicle ordering process.
- Automatic identification of the nearest dealer.
- Prevention of unavailable vehicle orders.
- Clear order status information.
- Convenient test drive scheduling.
- Better service request tracking.

### Business Benefits

- Reduced manual effort.
- Centralized customer and vehicle information.
- Improved order accuracy.
- Automated stock monitoring.
- Efficient dealer assignment.
- Better order management.
- Scalable processing of large amounts of data.

---

## Future Enhancements

The project can be extended with additional features such as:

- Online payment integration.
- Customer self-service portal.
- Real-time inventory synchronization.
- Dealer performance dashboards.
- Advanced sales and service reports.
- Mobile application integration.
- Automated customer notifications.
- Vehicle recommendation based on customer preferences.

---

## Learning Outcomes

This project provided practical experience in developing a Salesforce CRM solution for a real-world automotive use case.

The major learning outcomes include designing a Salesforce data model, creating objects and relationships, building applications using Lightning App Builder, implementing Record-Triggered Flows, developing Apex classes and triggers, following the Trigger Handler pattern, implementing business validations, and processing large datasets using Batch Apex and Scheduled Apex.

---

## Project Summary

**Project Name:** WhatsNext Vision Motors  
**Domain:** Automotive  
**Platform:** Salesforce CRM  
**Focus:** Vehicle Sales, Dealer Management, Stock Management, Customer Service, and Process Automation

WhatsNext Vision Motors demonstrates how Salesforce can be used to automate automotive sales and service operations while improving customer experience, reducing manual effort, and maintaining accurate vehicle and order information.

I will now share my demo video for my project below in the form of drive link

https://drive.google.com/file/d/1-CNz3v-BFOLOgWKvSTeSzeOn4Qo1cokC/view?usp=drive_link
