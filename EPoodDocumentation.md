1. Category

The Category class represents a product category in the online store
Attributes:
Id – unique identifier of the category
Name – name of the category
A category can contain multiple products. Each product belongs to one category

2. Product
The Product class represents an item available for purchase
Attributes:
Id – unique identifier of the product
Name – product name
Description – information about the product
Photo – product image
Price – current product price
Each product belongs to one category and can be included in multiple orders

3. Order
The Order class represents a customer's purchase
Attributes:
Id – unique identifier of the order
Status – current status of the order
Methods:
MarkAsPaid() – marks the order as paid
MarkAsShipped() – marks the order as shipped
An order contains one or more order lines. After payment, the order can be shipped

4. OrderLine
The OrderLine class represents one product included in an order
Attribtes:
Id – unique identifier of the order line
ProductPrice – price of the product at the time of purchase
Quantity – number of ordered items
Method:
CalculateTotal() – calculates the total price of the order line

The original product price is stored in the order line so that later price changes do not affect previous orders

Business Rules:
Each product belongs to one category
Categories have only one level
Each order contains at least one product
The price at the time of purchase is saved in the order line
An order is marked as paid after the customer completes payment
The warehouse can ship the order after payment
Separate invoice and payment records are not included in the first version of the system
