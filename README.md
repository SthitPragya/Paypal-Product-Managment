# Paypal-Product-Managment

LINK TO SHOPPINGKART API - https://app.swaggerhub.com/apis/SthitPragya/ShoppingKart/1.0.0
\n LINK TO API DOCUMENTATION - https://app.swaggerhub.com/apis-docs/SthitPragya/ShoppingKart/1.0.0

### STRUCTURE OF THE SYSTEM:

#### customers

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Customer |
| name | Name of the Customer |
| username | Username for authentication |
| password | Password for authentication |
| address | Address of the Customer |
| order | Order history of the Customer |
| cart | Items currently in cart of the Customer |
| phone | Phone number of the Customer |


Customer has to login through username and password
His account has a record of his name, id, address and phone number
He has a list of Orders done by him.
There is cart that stores the Item selected but not yet ordered


#### items

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Item |
| name | Name of the Item |
| rating | Average rating by Customers |
| brand | Brand that make this product |
| seller | Seller that sells this product |


Each Item has a unique ID and is linked to the Brand which manufactures it.
It also has a seller associated which sells it


#### sellers

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Seller |
| name | Name of the Seller |
| homePage | Website of the Seller |
| phone | Phone number of the Seller |
| rating | Average rating by Customers |
| stuff | List of Items sold by the Seller of a Brand |


Seller has an ID. He has a list of stuff he sells. He has an attribute rating which is done by the Customers.


#### brands

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Brand |
| name | Name of the Brand |
| homePage | Website of the Brand |
| phone | Phone number of the Brand |
| stuff | Items sold by the Brand |


Each brand has it's unique ID and they have a list of stuff they manufacture.


#### orders

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Order |
| stuff | Items in the Order |
| shipDate | Date when the order was shipped |
| status | current status of order |
| complete | Order complete or not |


Each order can be identified with it's unique ID. It has stuff which is the list of all items in that order. It has the details of when the order was shipped and whether the order is deliverd or not.


#### carts

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Cart |
| stuff | Items in the Cart |


Cart has an ID. It is linked to Order and Customer. Each Order has one cart and each customer has a cart. A cart is


**ADMIN** can view, edit and delete items, customers, orders, carts, sellers, brands. 

### RESPONSE CODES USED:

- 200 for successful operation
- 400 for Invalid request
- 401 for Unauthorized access
- 404 for Not found
- 503 for no response from Server


### METHODS:

| METHOD  | PATH | DESCRIPTION |
| ------------- | ------------- | --------- |
| GET  | /items  | Fetch all Item Details |
| POST  | /items  | Add a new Item |
| GET  | /items/search  | Fetch items based on a query |
| GET  | /items/{id}  | Fetch Item detail by ID |
| PUT  | /items/{id}  | Update details of an item by ID |
| DELETE  | /items/{id}  | Remove an item by ID |
| GET  | /customers  | Fetch all Customer Details |
| POST  | /customers  | Add a new Customer |
| GET  | /customers/login  | Existing Customer login |
| GET  | /customers/logout  | Customer account logout |
| GET  | /customers/{id}  | Fetch Customer details by ID |
| PUT  | /customers/{id}  | Update Customcr details by ID |
| DELETE  | /customers/{id}  | Remove Custcmer account by ID |
| GET | /customers/{id}/order | Fetch allcOrders of a Customer by ID |
| GET  | /sellers  | Fetch all Sellers c
| POST  | /sellers  | Add a Seller c
| GET  | /sellers/{id}  | Get Sellec details by ID |
| PUT  | /sellers/{id}  | Update Sellec detail by ID |
| DELETE  | /sellers/{id}  | Removc Seller by ID |
| GET | /sellers/{id}/stuff | Fetch all items sold by a Seller by ID |
| GET  | /brands  | Fetch all Brands |
| POST  | /brands  | Add a new Brand |
| GET  | /brands/{id}  | Fetch Brand details by ID |
| PUT  | /brands/{id}  | Update Brand details by ID |
| DELETE  | /brands/{id}  | Remove Brand by ID |
| GET | /brands/{id}/stuff | Fetch all items manufactured by a Brand by ID |
| GET  | /orders  | Fetch all Orders |
| POST  | /orders  | Add a new Order |
| GET  | /orders/search  | Fetch Orders based on a query |
| GET  | /orders/{id}  | Fetch Order details by ID |
| PUT  | /orders/{id}  | Update Order details by ID |
| DELETE  | /orders/{id}  | Delete Order by ID |
| GET | /orders/{id}/stuff | Fetch all items from a Order by ID |
| GET | /carts | Fetch details of all Carts |
| POST | /carts | Add a new Cart |
| GET | /carts/search | Fetch carts based on a query |
| GET | /carts/{id} | Fetch Cart details by ID |
| PUT | /carts/{id} | Update Cart items by ID |
| DELETE | /carts/{id} | Delete Cart by ID |
| GET | /carts/{id}/stuff | Fetch items in Cart by ID |
| PUT | /carts/{id}/stuff | Update Cart items by ID |
| DELETE | /carts/{id}/stuff | Delete items from Cart by ID |
| GET | /* | Handle all Invalid URL's of GET|
| PUT | /* | Handle all Invalid URL's of PUT |
| POST | /* | Handle all Invalid URL's of POST |
| DELETE | /* | Handle all Invalid URL's of DELETE |
