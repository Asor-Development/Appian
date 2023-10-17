# Burgers And More: Customer Site

## Record Types

### ATF_Category  
|    Name          |   DataType    |
| ---------------- | ------------- |
|  **id**          | `Integer: PK` |
| **categoryName** | `String`      |


### ATF_Size

|    Name          |   DataType    |
| ---------------- | ------------- |
| **id**           | `Integer: PK` |
| **size**         | `String`      |


### ATF_Item

|    Name          |   DataType    |
| ---------------- | ------------- |
| **id**           |  `Integer: PK`|
| **name**         |  `String`     |
| **price**        |  `Decimal`    |
| **description**  |  `String`     |
| **image**        |  `Integer`    |
| **sizeId**       |  `Integer: FK`|
| **categoryId**   |  `Integer: FK`|

### ATF_Order

|    Name           |   DataType     |
| ----------------- | -------------- |
| **id:**           |  `Integer: PK` |
| **customerName:** |  `String`      |
| **orderTotal:**   |  `Integer`     |
| **orderStatus:**  |  `String`      |
| **numberofItems:**| `Integer`      |


**Many to many Relationship**

### ATF_OrderItem

|    Name           |   DataType     |
| ----------------- | -------------- |
| **id:**           | `Integer: PK`  |
| **orderId:**      | `Integer: FK`  |
| **itemId:**       | `Integer: FK`  |

- from the Order record type add a one to many relationship with OrderItem
- from the Item record type add a one to many relationship with OrderItem
- allows you to index into the related record types

_________________________________
## Site Interfaces 
- `BAM_LandingPage`
    - when the button is clicked the process start by navigating you to the `BAM_OrderMilestone`
- `BAM_OrderMilestone`
    - `BAM_PlaceOrderHeader`
    - **Step 1**
        - `BAM_Menu`
            - `BAM_MenuNavigationList`
                - Contains no Interfaces
            - `BAM_MenuItemsList`
                - `ATF_CategoryItemsList`
                    - Contains no Interfaces
        - `BAM_Cart`
            - Contains no Interfaces




## `BAM_LandingPage`
- columsLayout with two columns that each contain a billboardLayout
- the first column billboardLayout contains a `Place Order` button created with a card layout
- cardLayout contains a linkField component, display as a button, that uses the startProcessLink function to start the process of placing an order by opening the `BAM_OrderMilestone`

## `BAM_OrderMilestone`
- uses a milestone component to display each step in the ordering process
- **Step 1: Create Order** uses a column layout with two columns
    - **Column One**
        - `BAM_Menu` interface that takes the cart rule input
        - the cart rule input contains a list of items placed into the cart
    - **Column Two**
           
    - **Step 2: Review Cart** uses
    - **Step 3: Provide Payment** uses


## `BAM_Menu`
- `local!activeCategory` is used to hold the active category
- `local!categoryListNav` is used to hold 
    - **Expression Rule:** `BAM_NavigationList`
        - return a list of navigation items containing all category name
- **Interface:** `BAM_MenuNavigationList`, navigation containing all categories
- **Interface:** `BAM_MenuItemsList`, a list of items for the specified category

    
        

## `BAM_MenuNavigationList`
- uses a the forEach function to display navigation containing all categories
- has two rule inputs `categoryListNav` and `activeCategory`, the values are passed in via local variables `categoryListNav` and `activeCategory`

## `BAM_MenuItemsList`
- uses the match function to return a list of items for the specified category
    - value is **Rule Input:** `activeCategory`
    - whenTrue: `activeCategory` is null or empty
    - then: a text field("Please enter a integer for active category section")
    - default: uses the choose function to display the appropiate items list using the `ATF_CategoryItemsList`


        - has three rule inputs `categoryListNav` and `activeCategory`, the values are passed in via local variables `categoryListNav` and `activeCategory`
        - the third rule input `cart` gets its value from a rule input
        - the rule input value is passed down from the `BAM_OrderMilestone` interface cart rule input
        - the cart rule input contains a list of items placed into the cart


## `ATF_CategoryItemsList`
- **Expression Rule:** `ATF_ItemsList`
    - takes a categoryID and returns all the items within that category
    - value is stored in local variable `items`
- the match function is used to handle what happens when `local!items` is null/empty and when it has avalue
    - value is **Rule Input:** `local!items`
    - whenTrue: `local!items` is null or empty
    - then: a text field("There are not items for this Category")
    - whenTrue: `local!items` has a value
    - then: a forEach function is used to display each item in `local!items`




BAM_GetItemQuantity
        takes an item and counts how many their are in the shopping carrt