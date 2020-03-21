# Paypal-Product-Managment

LINK TO SHOPPINGKART API - https://app.swaggerhub.com/apis/SthitPragya/ShoppingKart/1.0.0#/Customer/get_Customer__id_

STRUCTURE OF THE SYSTEM:

CUSTOMER

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Customer |
| name | Name of the Customer |
| username | Username for authentication |
| password | Password for authentication |
| address | Address of the Customer |
| order | Order history of the Customer |
| phone | Phone number of the Customer |


Item

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Item |
| name | Name of the Item |
| rating | Average rating by Customers |
| brand | Brand that make this product |
| seller | Seller that sells this product |


Seller

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Seller |
| name | Name of the Seller |
| homePage | Website of the Seller |
| phone | Phone number of the Seller |
| rating | Average rating by Customers |
| stuff | Items sold by the Seller |


Brand

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Brand |
| name | Name of the Brand |
| homePage | Website of the Brand |
| phone | Phone number of the Brand |
| stuff | Items sold by the Brand |


Order

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Order |
| stuff | Items in the Order |
| shipDate | Date when the order was shipped |
| status | current status of order |
| complete | Order complete or not |


Cart

| PARAMETERS | DESCRIPTION |
| ------------- | ------------- |
| id | ID of the Cart |
| stuff | Items in the Cart |


METHODS:

| METHOD  | PATH | DESCRIPTION |
| ------------- | ------------- | --------- |
| GET  | /Item  | Fetch all Item Details |
| POST  | /Item  | Add a new Item |
| GET  | /Item/id  | Fetch items based on a query |
| GET  | /Item/name  | Fetch items based on name |
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
| GET  | /Seller  | Fetch all Sellers |
| POST  | /Seller  | Add a Seller |
| GET  | /Seller/{id}  | Get Seller details by ID |
| PUT  | /Seller/{id}  | Update Seller detail by ID |
| DELETE  | /Seller/{id}  | Remove Seller by ID |
| GET  | /Brand  | Fetch all Brands |
| POST  | /Brand  | Add a new Brand |
| GET  | /Brand/{id}  | Fetch Brand details by ID |
| PUT  | /Brand/{id}  | Update Brand details by ID |
| DELETE  | /Brand/{id}  | Remove Brand by ID |
| GET  | /Order  | Fetch all Orders |
| POST  | /Order  | Add a new Order |
| GET  | /Order/id  | Fetch Orders based on a query |
| GET  | /Order/{id}  | Fetch Order details by ID |
| PUT  | /Order/{id}  | Update Order details by ID |
| DELETE  | /Order/{id}  | Delete Order by ID |
