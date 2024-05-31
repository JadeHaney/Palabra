Palabra 🚀

User Story
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies

Mock-Up
Getting Started
Database Models
Associations
Hints
Author
Description
This project is a back end for an e-commerce website built using Express.js API and Sequelize to interact with a MySQL database. It aims to provide a foundation for an internet retail company to compete effectively in the e-commerce industry.

User Story
css
Copy code
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
Acceptance Criteria
Functional Express.js API
Ability to connect to a database using Sequelize
Creation of development database seeded with test data
Server started and Sequelize models synced to the MySQL database
API GET routes in Insomnia Core for categories, products, or tags display data in a formatted JSON
Ability to successfully create, update, and delete data in the database using API POST, PUT, and DELETE routes in Insomnia Core
Mock-Up
Mock-up animations demonstrating API routes tested in Insomnia Core are available in the assignment description.

Getting Started
Clone the starter code repository.
Use MySQL2 and Sequelize packages to connect the Express.js API to a MySQL database.
Utilize the dotenv package to store sensitive data in environment variables.
Create the database using the schema.sql file in the db folder.
Define database models and execute association methods between them.
Fill out API routes in product-routes.js, tag-routes.js, and category-routes.js to perform RESTful CRUD operations.
Seed the database by running npm run seed.
Sync Sequelize to the database on server start in server.js.
Database Models
Category

id (Integer, Primary Key, Auto Increment)
category_name (String, Not Null)
Product

id (Integer, Primary Key, Auto Increment)
product_name (String, Not Null)
price (Decimal, Not Null)
stock (Integer, Not Null, Default: 10)
category_id (Integer, References Category Model's id)
Tag

id (Integer, Primary Key, Auto Increment)
tag_name (String, Not Null)
ProductTag

id (Integer, Primary Key, Auto Increment)
product_id (Integer, References Product Model's id)
tag_id (Integer, References Tag Model's id)

Associations
Product belongs to Category
Category has many Product models
Product belongs to many Tag models (through ProductTag)
Tag belongs to many Product models (through ProductTag)

Hints
Fill out API routes to perform CRUD operations
Seed the database to test routes
Sync Sequelize to the database on server start

Author
Jade Haney 📝





