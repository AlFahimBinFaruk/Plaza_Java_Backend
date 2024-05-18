## Plaza Backend API
* Live Link: todo
* Frontend : todo
* Admin panel : todo

### Client Requirements

As a guest user, I can

* View Homepage,Products
* Signup to be an customer
* Search for products

As an Admin user, I can

* Login
* View & edit profile(first,last name,email,password)
* CRUD Users
* CRUD roles(only 2 roles: admin,customer)
* CRUD Products
* Logout

As a Customer, I can

* Login
* View & edit profile(first,last name,email,password)
* Purchase new products if available quantity.
* Cancel purchase.
* See my purchase history
* Checkout - currently we only have COD feature.

### Technology

* Language: Java 17
* Build Tool: Maven
* Spring boot 3.0
* Database: MongoDB


### Database Models
![Database model image](https://drive.google.com/uc?export=view&id=1fUP_Zbt3zhHXvIPe400ccX7XACpZ8Ish)


### API Routes
* To register - POST
```text
/api/user/register
```

* To login : will get and jwt token. - POST
```text
/api/user/login
```

* To Logout - will logout user/admin - GET
```text
/api/user/logout
```

* Get all user list : secured, authorized to admin only - GET
```text
/api/user/all
```

* Get individual user details : secured, only authorized admin and user himself and access it - GET
```text
/api/user/{id}
```

* Update user information : secured, only authorized admin and user himself and access it - PUT
```text
/api/user/update/{id}
```

* Update user role : only authorized admin can access it - PUT
```text
/api/user/update/role/{id}
```

* Delete a user : secured, only authorized admin and user himself and access it - DELETE
```text
/api/user/delete/{id}
```

* Get all category - all visitors can access it - GET
```text
/api/category/all
```

* Add new category : only admin can access it - POST
```text
/api/category/add-new
```

* Update category : only admin can access it - PUT
```text
/api/category/update/{id}
```

* Delete category : only admin can access it - DELETE
```text
/api/category/delete/{id}
```

* Get all product List - all visitors can access it, it will have pagination - GET
```text
/api/product/all
```

* Get all product of a single category - all visitors can access it, it will have pagination - GET
```text
/api/category/{category_id}/product/all
```

* Search for products - all visitors can access it , it will have pagination - GET
```text
/api/product/search/q=?
```

* Get product Details - all visitors can access it - GET
```text
/api/product/details/{id}
```

* Add new product : only authorized admin can access it - POST
```text
/api/product/add-new
```

* Update product : only authorized admin can access it - PUT
```text
/api/product/update/{id}
```

* Delete product : only authorized admin can access it - DELETE
```text
/api/product/delete/{id}
```

* Purchase product : only authorized users can buy product - POST
```text
/api/product/purchase
```

* Show order History : only admin or user himself can access it,it will have pagination - GET
```text
/api/order/history/{user_id}
```

* Cancel order : only admin or user himself can access it - PUT
```text
/api/order/history/{order_id}
```

* Update order status : only authorized admin can do it - PUT
```text
/api/order/update-status
```



### How to Build & Run
