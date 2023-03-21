Hi Welcome to the Cart

Life Cycle (in Brief):

**Authenticated User Logs In => Browse the Products => Add to Cart**

**Functional Description of Main Components: **

**Login:**
1. User Enters UserName and Password.
2. If unauthorized username is entered, error would be displayed as "Invalid Username"
3. If either of both mentioned at serial 1 is not valid, error would be displayed as "Invalid Username" or "Password did not match"
4. Once user logs in successfully,user gets redirected to Home Component,a JSON token is generated and a Cookie is set with the name "jwt_token". This is done with the help of js-Cookies
5. Till the time jwt_token is available in cookies, user would never get redirected to "login" page

**Header**
1. This Component is wrapped with withRouter
2. That would facilitate to use the history props
3. Header component consists of Links to components like "Home","Products","Cart".
4. It has Logout Button. Clicking the same removes the jwt_token and thereby redirects the user to "Login" Component

**Home**

1.This component displays info about "Cart Application" and a button "Shop Now". Clicking the same would take to products component


**Products**

1. This Component displays two sections:
2. Incase the user has prime membership, prime deals along with the All Products are displayed
3. If the user is not a prime member, only All Products are displayed.
4. There are filters to: Search/Category/Rating/Sort by Price
5. When a specific product is selected, it takes to the product details component

**Product Details**

1.Product Details component displays the details of product such as Image,name of the product, description, rating etc. Along with three kinds of similar products
2. By default, the quantity is 1 on Plus and Minus buttons on both sides
3. There is a button below the quantity named as "Add To Cart"
4. Clicking on Plus and Minus would increment the quantity accordingly
5. When Add to Cart button is clicked, item gets added to Cart.
6. Cart Icon on Header gets displayed with the number of products added.

**Cart**:

1.Incase no items are added to cart, default view appears.
2. If Items are added, list of items added to the cart gets displayed with the price details and total price
3. Against each item, there are Plus and Minus buttons that would increment the quantity accordingly


**Important Note**:

React Context is used to Store Cart Data, add/delete items, increment/decrement the quantity

