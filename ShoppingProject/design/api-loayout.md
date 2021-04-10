# API Design

## Auth
---
## Registration

Inputs (POST Params):

- Full Name **(Anything but null or empty string)**
- email **(requires: valid email address)**
- password **(requires: min 8 characters, 1 symbol, 1 number, 1 uppercase letter and 1 lowercase letter)**

Outputs (json):
- success: true | false
- error_messsage: "" | "Email already in use" 

## Login

Inputs (POST params):

- email
- password

Outputs (json):
- success: true | false
- error_message: "" | "Incorrect Login Details"

## Logout

No Inputs

Outputs (json):

- success: true | false
- error_message: "" | "User not logged in to perform this action"

---
## Products
---

## List Products

No Inputs

Outputs (json): (array of product items)

    [
        {
            id: Integer,
            name: string,
            price: Integer as (price * 100),
            image: URL string
        }
    ]

## Get Product

Inputs (GET param):

- ID (Product ID)

Output (json):

- id: Integer
- name: String
- image: URL String
- price: Integer as (price * 100)
- description: Long String | Text

---
## Cart
---

## getProductsFromIDsAndQuantityArray (Store)

Inputs (POST):

- data as an array of id and quantity pairs
- format of each element = {'id': value, 'quantity': value}


Outputs (json):

success: true | false
products: [
    {
        id: product_id,
        name: product_name,
        quantity: product_quantity,
        price: product_price (stored as value * 100)
    }
]

---
## Order
---

## createOrder

Inputs: product id and quantity array

Outputs (json):

- success: true | false
- error_message: "" | "User not logged in to perform this action"


## Get Products from ProductIDandQuantityArray (List)

No Inputs

Outputs (json):

    [
        {
            id: Integer,
            name: string (Product Name),
            price: Integer as (price * 100),
            image: URL string,
            quantity: Integer (1 -> N)
        }
    ]

## Get Order History

No Inputs

Outputs (json): (array of orders with each having an array of items)

    [
        {
            id: Order id (UUID),
            items: [
                {
                    id: Integer (Product ID),
                    name: string (Product Name),
                    price: Integer as (price * 100),
                    image: URL string,
                    quantity: Integer (1 -> N)
                }
            ],
            total: Integer as (price * 100)
        }
    ]