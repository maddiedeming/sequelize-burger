# [sequelize-burger]()
## Overview
In this assignment, you're going to Sequelize the `Burger` app you made last week. We've split this exercise into three different tiers, all with different tasks and expectations. Finish whichever tier will provide you with the most reasonable challenge.
## Dependencies
* body-parser
* dotenv
* express
* express-handlebars
* method-override
* mysql2
* sequelize
## Installation
### Install Locally
```
git clone https://github.com/maddiedeming/sequelize-burger.git
npm install
```
### Setup Database
```
mysql -u <Your MySQL Username> -p
<Your MySQL Password>
\. \db\schema.sql
\. \db\seeds.sql
\q
```
### .env File
1. Create a new file and save as ".env" in the root directory.
2. Copy and paste the following into the .env file:

    DB_HOST=[localhost]

    DB_USER=[root]

    DB_PASS=[password]
3. Edit any of the values in the brackets above to coordinate with your MySQL Database.
### Command
`node server.js`
## Requirements
### Tier 1: Sequelized (Basic to Moderate)
- [ ] Remove all references to your vanilla MySQL queries and replace them with Sequelize queries.
  - [ ] Replace your MySQL `Burger` model with a Sequelized equivalent.
    - [ ] Edit the model and initial migration file to make the burger's devoured field carry a default value of false.
    - [ ] Sync the models.
- [ ] Edit your new `config.json` file to include your database configurations. 
  - [ ] Place your JawsDB details in the `production` property of your json file; the details of your local database go in the `developer` property.
- [ ] Remove your old ORM file, as well as any references to it in `burgers_controller.js`. 
  - [ ] Replace those references with Sequelize's ORM methods.
### Tier 2: Customer Associations (Challenge)
- [ ] Add in a Customer association to the project. 
  - [ ] Create at least one new `Customer` model and connect it with your `Burger` model.
- [ ] Edit the handlebars files and CSS stylesheets to implement some sort of additional feature to the site. 
### Bonus! (Challenge)
- [ ] Add validations to your models where:
  - [ ] A burger's name cannot be null
  - [ ] A burger's devoured status is false by default
  - [ ] A Customer's name cannot be null
- [ ] Order the Burgers you send back to the user in alphabetical order using the Sequelize "order" option.