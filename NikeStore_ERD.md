
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


















