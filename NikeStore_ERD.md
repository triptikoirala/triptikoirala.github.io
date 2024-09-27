
'''mermaid
erDiagram
    PRODUCT {
        string ProductID PK
        string ModelName
        float Price
        int StockQuantity
    }
    
    CUSTOMER {
        string CustomerID PK
        string Name
        string Email
    }
    
    SALE {
        string SaleID PK
        string CustomerID FK
        string ProductID FK
        int Quantity
    }
    
    INVENTORY {
        string InventoryID PK
        string ProductID FK
        int StockLevel
    }

    PRODUCT ||--o{ SALE : "sold"
    CUSTOMER ||--o{ SALE : "makes"
    PRODUCT ||--|| INVENTORY : "tracked"
    '''



















# Descriptions
## Products
- Represents the various types of Nike shoes.
- Attributes: ProductID, ModelName, Price, StockQuantity.
## Customers
- Contains information about customers who buy shoes.
- Attributes: CustomerID, Name, Email.
## Sales
- Records the transactions when shoes are purchased.
- Attributes: SaleID, CustomerID, ProductID, Quantity.
## Inventorys
- Manages the stock levels for each product.
- Attributes: InventoryID, ProductID, StockLevel.
## Relationships
- Product to Sale: A product can be sold many times.
- Customer to Sale: A customer can makes many purchases.
- Product to Inventory: Each product has one record in the inventory.
