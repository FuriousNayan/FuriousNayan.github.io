# Nike Store ERD

```mermaid
erDiagram
    
    Products {
      int ProductID PK
      string ProductName
      string Brand
      float Price
      string Size
      string Color
    }

    Customers {
      int CustomerID PK
      string FirstName
      string LastName
      string Email
      string PhoneNumber
      string Address
    }

   
    Sales {
      int SaleID PK
      date SaleDate
      int CustomerID FK
      int ProductID FK
      int Quantity
      float TotalPrice
    }

    Inventory {
      int InventoryID PK
      int ProductID FK
      int StockLevel
      string Location
    }

    Products ||--|{ Sales : "sold in"
    Customers ||--|{ Sales : "make"
    Products ||--|{ Inventory : "tracked in"
```

### Documentation
This ERD outlines the relationships between key entities in a shoe store: Products, Customers, Sales, and Inventory. It models how transactions and stock levels are tracked.

Entities Overview
Products

ProductID (PK): Unique identifier.
Includes name, brand, price, size, and color.
Customers

CustomerID (PK): Unique identifier.
Includes name, email, phone, and address.
Sales

SaleID (PK): Unique transaction ID.
Links CustomerID (FK) and ProductID (FK) with sale date and quantity.
Inventory

InventoryID (PK): Unique identifier.
Tracks stock by ProductID (FK) and location.
Relationships
Products are linked to sales and inventory.
Customers are linked to sales.