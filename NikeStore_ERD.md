
































# Descriptions
## Product
- Represents the various types of Nike shoes.
- Attributes: ProductID, ModelName, Price, StockQuantity.
## Customer
- Contains information about customers who buy shoes.
- Attributes: CustomerID, Name, Email.
## Sale
- Records the transactions when shoes are purchased.
- Attributes: SaleID, CustomerID, ProductID, Quantity.
## Inventory
- Manages the stock levels for each product.
- Attributes: InventoryID, ProductID, StockLevel.
## Relationships
- Product to Sale: A product can be sold many times.
- Customer to Sale: A customer can make many purchases.
- Product to Inventory: Each product has one record in the inventory.
