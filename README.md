# Todolist

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/afbe491f48d3422fbf15cf9d352912fe)](https://app.codacy.com/gh/binblink/Todolist?utm_source=github.com&utm_medium=referral&utm_content=binblink/Todolist&utm_campaign=Badge_Grade_Settings)

### Requirements  
  - PHP 7.4.9+
  - Composer (https://getcomposer.org/)
  - MariaDB or MySQL 5.7+ database 
  - Symfony CLI https://symfony.com/download

### How to install
- Clone the git repo locally on your computer
- Open the folder in your IDE
- You need a local server such as Mamp or Wamp (https://www.wampserver.com/)
- Create a .env.local file at the root of the project. This file will override the variables contained in the .env file.
    - Modify the following variables to match your database connection parameters (replace username, password, host, port & database values)
      - ```APP_SECRET=<ChangeThisToYourSecret>```
      - ```DATABASE_URL="mysql://username:password@host:3306/database"```

- Open a terminal and run the following commands to connect the app to your database 
    - ```symfony check:requirements```
      - here follow the instructions in the terminal in case you are missing some PHP extensions such as pdo_mysql
    - ```composer install```
    - ```php bin/console doctrine:schema:update --force```
- You can now access the application from http://localhost:8080 (or different port according to your local web server settings)
- Alternatively, if you do not wish to use Wamp, Mamp or Laragon, you can also type ```symfony serve``` from a terminal and then access the project from http://localhost:8000
