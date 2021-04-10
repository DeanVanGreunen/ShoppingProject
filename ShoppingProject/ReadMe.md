# **Shopping Cart**
This is part of the Shopping Cart (Frontend and Backend) Assignment. Which has been assigned to [Dean Van Greunen](deanvg9000@gmail.com)

---

## **Backend Instructions (shopping-app)**
In order to run the backend, We first need to set up the database.

**Requirements:**

- PHP 7.2.5
- PHP Extensions as per the [Laravel Framework Docs](https://laravel.com/docs/7.x/installation#server-requirements)

### **Database**

Create a database on the [Postgresql](https://www.postgresql.org/) System.
Using these details: (These can be changed in the .env file found in the shopping-app folder relative from this files directory)
```
Database Name: shopping
Database User Username: shopping
Database User Password: shopping
```

**Note:**
If you want to use another database system besides postgresql then follow [this](https://laravel.com/docs/8.x/database) guide.

### **Laravel**
After you have finished with creating and setting up the database, run the following commands, to cd into the correct directory from this current folder path, create the database and then seed the database.

Seeding will populate the database with 20 products, each with an unqiue ID, Name, Price and an Image (Images are stored on 3rd Party websites, message me if they do not load or if there is any other issue)

```bash
cd shopping-app
php artisan migrate
php artisan db:seed
```

Now that the database is setup, we may now run the server with this command

This command will open the laravel app and server its contents on http://127.0.0.1:8000/

```bash
php artisan serve
```

## Frontend Instructions (shopping-cart)
In order to run the frontend, we will need to install the following tools and frameworks.

**Tools / Frameworks:**

- NodeJS a.k.s [Node CLI](https://nodejs.org/en/)
- NPM a.k.a [Nodes Package Manager](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)

after `cd`'ing into the `shopping-cart` directory run these commands to setup the project.

```bash
cd shopping-cart
npm install
```

To Run the frontend, run the following command, it will open the frontend project at http://127.0.0.1:3000/

```bash
npm start
```

---
## **Other Info**
---

### **Tools Used:**
- VS Code
- PgAdmin
- Command Promt
- Git SVN Software

### **Note**
This was developed and design on a Windows 10 Installation.