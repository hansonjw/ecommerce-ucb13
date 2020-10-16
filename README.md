# Ecommerce Backend with Sequelize  
  No license is applicable for this application

  ## Description:  
  TBD

  ## Table of Contents:
  * [Installation Instructions](#Installation:)
  * [How to use This Application:](#How-To:)
  * [How to Contibute:](#Contibute:)
  * [License Information:](#License:)
  * [Questions:](#Questions:)
  
  <a name="Installation:"></a>
  ## Installation:  
  TBD
  
  <a name="How-To:"></a>
  ## Walk Through Video:  
  TBD

  <a name="Contribute:"></a>
  ## Contribute:  
  If you would like to contribute please contact me...see below

  <a name="License:"></a>
  ## License:  
  This application is covered under the following license...
  No License  
  For more information on the license click on the badge below:
  No license is applicable for this application
  
  <a name="Questions:"></a>
  ## Questions:  
  For questions, comments, suggestions, I can be reached at the following  
  https://github.com/hansonjw/fantastic-unbrella  
  hansonjw@gmail.com

  ## Creating the Database:
  - Use the schema.sql file in the db folder to create the database using MySQL shell commands.
  - Use environment variables to store sensitive data, like your MySQL username, password, and database name.
  
  ## Database Model:
  ### Category

    - id - Integer Doesn't allow null values; Set as primary key; Uses auto increment
    - category_name - String; Doesn't allow null values

  ### Product

    - id - Integer; Doesn't allow null values; Set as primary key; Uses auto increment
    - product_name - String; Doesn't allow null values;
    - price - Decimal; Doesn't allow null values; Validates that the value is a decimal
    - stock - Integer; Doesn't allow null values; Set a default value of 10; Validates that the value is numeric
    - category_id - Integer; References the category model's id

  ### Tag

    - id - Integer; Doesn't allow null values; Set as primary key; Uses auto increment
    - tag_name - String

  ### ProductTag

    - id - Integer; Doesn't allow null values; Set as primary key; Uses auto increment; 
    - product_id - Integer; References the product model's id
    - tag_id - Integer; References the tag model's id


  ### Associations

    - Product belongs to Category, as a category can have multiple products but a product can only belong to one category.
    - Category has many Product models.
    - Product belongs to many Tag models. Using the ProductTag through model, allow products to have multiple tags and tags to have many products.
    - Tag belongs to many Product models.

  ### Seed the Database
  After creating the models and routes, run npm run seed to seed data to your database so that you can test your routes.

  Sync Sequelize to the Database on Server Start
  Create the code needed in server.js to sync the Sequelize models to the MySQL database on server start.