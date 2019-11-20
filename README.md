bamazon
This is bamazon. Bamazon, as it's name suggests, is a simple e-commerce app, or at least the backend for it. Check out this screencast on youtube to see how it works: bamazon on youtube.

Bamazon uses some third-party node modules, has it's own modules, and connects to a mysql database to store and retrieve product and department information.

Third-party Node Modules
Bamazon uses these node modules: console.table, inquirer, mysql.

They are all dependencies in the package.json, so just run:

npm install

Customer Module
The customer module lets users select a product to purchase, enter the number of items they wish to purchase, and then complete the purchase.

The complete purchase process shows how much the total cost is (based on number of items).

The customer module also updates to the total sales for a department, based on the purchased product's department.

To run this module in the terminal:

node bamazonCustomer.js

![Screen Shot 2019-11-20 at 5 06 22 PM](https://user-images.githubusercontent.com/49074642/69282416-48b60d80-0bb8-11ea-85cc-3f39b8b17795.png)

Manager Module
The manager module lets managers view the list of products, view low inventory, add inventory, and add products.

As part of adding a product, if the department doesn't exist, it will get added automatically, so the manager doesn't have to worry about it.

New products and new departments appear in the products and departments tables.

To run this module in the terminal:

node bamazonManager.js

Supervisor Module
The supervisor module lets supervisors view product sales by departments and add new departments.

The product sales are displayed in the terminal using the console.table node module, so it looks pretty.

The table also uses mysql aliases to also include an on-the-fly calculated total sales for a department, which is the product sales minus the overhead.

To run this module in the terminal:

node bamazonSupervisor.js
