# Paypal-Product-Managment

LINK TO SHOPPINGKART API - https://app.swaggerhub.com/apis/SthitPragya/ShoppingKart/1.0.0

### STRUCTURE OF THE SYSTEM:

#### Customer

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


#### Item

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Item |
| name | Name of the Item |
| rating | Average rating by Customers |
| brand | Brand that make this product |
| seller | Seller that sells this product |


Each Item has a unique ID and is linked to the Brand which manufactures it.
It also has a seller associated which sells it


#### Seller

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Seller |
| name | Name of the Seller |
| homePage | Website of the Seller |
| phone | Phone number of the Seller |
| rating | Average rating by Customers |
| stuff | List of Items sold by the Seller of a Brand |


Seller has an ID. He has a list of stuff he sells. He has an attribute rating which is done by the Customers.


#### Brand

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Brand |
| name | Name of the Brand |
| homePage | Website of the Brand |
| phone | Phone number of the Brand |
| stuff | Items sold by the Brand |


Each brand has it's unique ID and they have a list of stuff they manufacture.


#### Order

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Order |
| stuff | Items in the Order |
| shipDate | Date when the order was shipped |
| status | current status of order |
| complete | Order complete or not |


Each order can be identified with it's unique ID. It has stuff which is the list of all items in that order. It has the details of when the order was shipped and whether the order is deliverd or not.


#### Cart

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Cart |
| stuff | Items in the Cart |


Cart has an ID. It is linked to Order and Customer. Each Order has one cart and each customer has a cart. A cart is


### RESPONSE CODES USED:

- 200 for successful operation
- 400 for Invalid request
- 401 for Unauthorized access
- 404 for Not found
- 503 for no response from Server


### METHODS:

| METHOD  | PATH | DESCRIPTION |
| ------------- | ------------- | --------- |
| GET  | /Item  | Fetch all Item Details |
| POST  | /Item  | Add a new Item |
| GET  | /Item/search  | Fetch items based on a query |
| GET  | /Item/{id}  | Fetch Item detail by ID |
| PUT  | /Item/{id}  | Update details of an item by ID |
| DELETE  | /Item/{id}  | Remove an item by ID |
| GET  | /Customer  | Fetch all Customer Details |
| POST  | /Customer  | Add a new Customer |
| GET  | /Customer/login  | Existing Customer login |
| GET  | /Customer/logout  | Customer account logout |
| GET  | /Customer/{id}  | Fetch Customer details by ID |
| PUT  | /Customer/{id}  | Update Customer details by ID |
| DELETE  | /Customer/{id}  | Remove Customer account by ID |
| GET | /Customer/{id}/order | Fetch all Orders of a Customer by ID |
| GET  | /Seller  | Fetch all Sellers |
| POST  | /Seller  | Add a Seller |
| GET  | /Seller/{id}  | Get Seller details by ID |
| PUT  | /Seller/{id}  | Update Seller detail by ID |
| DELETE  | /Seller/{id}  | Remove Seller by ID |
| GET | /Seller/{id}/stuff | Fetch all items sold by a Seller by ID |
| GET  | /Brand  | Fetch all Brands |
| POST  | /Brand  | Add a new Brand |
| GET  | /Brand/{id}  | Fetch Brand details by ID |
| PUT  | /Brand/{id}  | Update Brand details by ID |
| DELETE  | /Brand/{id}  | Remove Brand by ID |
| GET | /Brand/{id}/stuff | Fetch all items manufactured by a Brand by ID |
| GET  | /Order  | Fetch all Orders |
| POST  | /Order  | Add a new Order |
| GET  | /Order/search  | Fetch Orders based on a query |
| GET  | /Order/{id}  | Fetch Order details by ID |
| PUT  | /Order/{id}  | Update Order details by ID |
| DELETE  | /Order/{id}  | Delete Order by ID |
| GET | /Order/{id}/stuff | Fetch all items from a Order by ID |
| GET | /* | Handle all Invalid URL's of GET|
| PUT | /* | Handle all Invalid URL's of PUT |
| POST | /* | Handle all Invalid URL's of POST |
| DELETE | /* | Handle all Invalid URL's of DELETE |
| GET | /Cart | Fetch details of all Carts |
| POST | /Cart | Add a new Cart |
| GET | /Cart/search | Fetch carts based on a query |
| GET | /Cart/{id} | Fetch Cart details by ID |
| PUT | /Cart/{id} | Update Cart items by ID |
| DELETE | /Cart/{id} | Delete Cart by ID |
| GET | /Cart/{id}/stuff | Fetch items in Cart by ID |
| PUT | /Cart/{id}/stuff | Update Cart items by ID |
| DELETE | /Cart/{id}/stuff | Delete items from Cart by ID |
