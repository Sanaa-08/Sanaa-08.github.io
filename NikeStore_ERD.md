---
title: Nike Shoe Store ERD
---
erDiagram 
PRODUCT { int product_id PK
        string name
        string size
        string color
        decimal price
} 
CUSTOMER { int customer_id PK
        string name
        string email
        string phone_number

} 
SALE { int sale_id PK
        int customer_id FK
        int product_id FK
        date sale_date
        int quantity
        decimal total_price

} 
INVENTORY { int inventory_id PK
        int product_id FK
        int quantity_in_stock
        date restock_date

}
PRODUCT ||--o{ SALE : makes
CUSTOMER ||--o{ SALE : makes
PRODUCT ||--o{ INVENTORY : tracks
