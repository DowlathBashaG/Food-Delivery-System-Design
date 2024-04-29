# Food-Delivery-System-Design

Restaurant Personal :

<img width="1275" alt="Restaurant_Personal" src="https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/f571851d-1213-4042-9905-ee458ab70bcd">

Customer Personal :

<img width="1265" alt="Customer_Personal" src="https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/99d63070-83ac-4b93-b0db-a3a2b5b87a80">

Payment Eco-System :

<img width="774" alt="Payment_Ecosystem" src="https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/1e795f5f-296c-4bc6-97f6-139a8300746b">

Delivery Partner Personal :

<img width="1253" alt="Delivery_Partner" src="https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/5871bd72-bf31-4ba1-a216-5e98f24e4ccb">

Cloud Architecture :

![food_del_aws](https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/bfb51a2f-8e58-4971-b2a3-236cb82ccd90)


Functional Requirements
=======================


User can search different restaurant based on his/her location

User can select a restaurant

User can see the menu of selected restaurant

Restraunt can change the menu any time

User selects restraunt and add different food items from the menu

User orders the food by selecting different online payment modes

Cash on delivery can be also option (Optional)

User can track the order in real time

User can cancel the order

The restaurant process the orders by preparing the meal and packaging the orders.

The restaurant contacts the delivery service or their personnel delivery staff to deliver.

Daily allows users to schedule their meals in advance or opt for a daily, weekly or monthly subscription. (Not in scope but it will be good to have in future.)

Customers will have different offers in the form of coupon, discounts, etc.

Non-functional Requirements
===========================

No. of orders = 10,000 orders per minute

No. of cities and towns operational = 500

Total number of restraunts listed on the application = 140,000

Total active delivery partners = 2,00000

Total number of order cancellations = 1,500 daily

System should be highly scalable and available.

User should be able to get all features with minimal latency.

Scalability Estimation
======================

Traffic Estimates

System is expecting 10,000 orders per minute. So, order requests per second will be:

10, 000 orders per minute/60 = ~ 167 Orders /Second

Storage Estimates

Since we are expecting 10,000 orders per minute so, per day will be:

Orders per day = 10, 000 orders/minute * 60 * 24 = 14,400,000 orders/day

Total expected orders in 5 years = 14,400,000 orders/day * 12 Months * 5 Years = 864,000,000

Lets assume the size of object = 500 bytes

Total storage in 5 years = 432 GB

Bandwidth Estimates

For order, since we are expecting 167 Orders /Second so, the total incoming data for the service will be:

167 Orders/Second * 500 bytes = ~ 1 MB/Second

High Level Design (HLD)

Food delivery system can be devided into three major components:

Customer's Application

Driver's Application or Delivery guy's application
Admin Panel
Customer's Application

Selection of city and listing of restraunts

Searching menu: Allow users to search for different restaurants, cafes, pubs, and bars by location and cuisines. Users can go through the menus and choose an item from using the search filter; users can easily 

find their favorite eating places.

Order placement/Cancellation: The user can place an order of selected dishes and food with just a few simple taps on the screen. User can cancel order with a given allowed time.

Tracking Drivers: Users can check how much time a driver will take to reach their food parcel.

Payment gateway integration: It will be required for the payment by users. It will have multiple options of payment.

Driver's Application or Delivery guy's application

Driver's profile - Driver can update his profile details like his name, email, address, phone number, photos, or any other details.

Notification for orders: Through push notifications, drivers can get constant updates & alerts for new food orders online. It will help in the accurate delivery service of your restaurant.

Map for the delivery route: Integrate Google Map or Waze and allow drivers to choose the shortest and fastest routes to reach the location.

Admin Panel

Restaurant management: Being on the admin panel, one can directly manage all the restaurants by adding, updating, and removing any eating joint from the list. He can also check active restaurant status and also 

menu pricing.

Analytics & report generation: Using the analysis and report feature, you can get real-time insights of reports and other accounting information, which helps you to identify the growth and opportunities to expand 

reach.

Monitoring every action: Monitor all the drivers, changes in the menu, deliveries, ratings & reviews of drivers, canceled orders, and other important data related to the driver’s performance.

Payment and commission management: Allow owners to set payment and commission rates and manage it directly from the panel with every single partner and make payments.

Other components can also be included (Not in current scope. This can be the part of future scope):

Customer Relationship Management (CRM): This will be required to help and understand about customers. It will include the solution or query related to ordering or any problem related to order and delivery, likes-

deslikes, transancation details, sales details, order patterns, etc.

Estock Management: It can maintain raw material management, stock availability, consumption report (monthly/yearly), and stock expiration date, etc.

High level design for each component or area can be very wide. Each component will have separate high level design. You should discuss about the area before the development and drawing of high-level design. 

Interviewer will ask you to pickup one from three of them. Lets say its customer's application.

High-level design in general is as below:

<img width="1662" alt="Food_Delivery_Functions" src="https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/119d6c95-c6b6-47ae-943b-cb7b9c3986c9">

Entities :

<img width="1662" alt="Entities_1" src="https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/c8641e45-c2fe-49ff-8f9f-eca5b3365af4">

<img width="1662" alt="Entities_2" src="https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/fa4582be-8743-4707-af49-c889fec43b7b">

<img width="1662" alt="Entities_3" src="https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/98c1d1bd-6156-4f7b-91ad-e0d4f1478542">

API's :

<img width="1662" alt="APIs_1" src="https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/1d28c050-761f-4474-8b5c-25ca24a91699">

<img width="1662" alt="APIs-2" src="https://github.com/DowlathBashaG/PaymentSystem-System-Design/assets/9671419/cf26f5d3-5a9f-40f4-91d1-a82d069b9584">
