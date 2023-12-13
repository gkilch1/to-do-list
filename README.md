# to-do-list
This to-do list was created to demonstrate my ability to develop a fully functional backend application connected to a PostgreSQL database, which can successfully execute the CRUD process.


PostgreSQL / pgAdmin download - https://www.postgresql.org/download/ 

Node / NPM download - https://docs.npmjs.com/downloading-and-installing-node-js-and-npm

Steps to running locally:

1. Make sure PostgresSQL and PgAmin are downloaded to your computer.
   - If they are not, use the below links to begin the download:
     - Mac - https://sbp.enterprisedb.com/getfile.jsp?fileid=1258653
         - Mac Users: If a pop-up asks permission to run the installer, select Open. You might need to enter your Mac password to allow the installer to run.
     - Windows - https://sbp.enterprisedb.com/getfile.jsp?fileid=1258649
         - Windows Users: If prompted to run the installer, select YES.
    - Click 'Next' until you see the screen that asks you to check all the packages you want installed.
      - For Mac and Windows users, you want to make sure all boxes are checked
        - PostgreSQL Server
        - pgAdmin
        - Stack Builder
        - Command Line Tools
    - Keep clicking on the 'Next' button until you come across a prompt asking you to enter a username and password.
    - The username will be 'postgres' and you will need to create a password. It is EXTREMELY important to write this password down for later use.
    - Continue until you click 'Finish'
    - A prompt for Stack Builder may appear after installation, but you can close it.
2. Once PostgreSQL is successfully installed, you will need to build out your database.
   - To begin, launch pgAdmin. Once pgAdmin is open, navigate to the PostgreSQL server.
   - Here, you will be prompted to enter the password you created earlier.
   - After logging in, go to the 'Databases' section and create a new database. To do this, right-click on 'Databases' and select 'Create', followed by 'Database...'. A pop-up menu will appear where you should enter the name 'permalist' as the database name. Leave all the default settings unchanged and click 'Save'. Next, click on the newly created database and look for the 'Start Query' button on the top left corner. Click on it to run a new query.

       ![Screenshot (363)](https://github.com/gkilch1/to-do-list/assets/113639024/71c3de4f-f56a-49f6-a2c9-47e4fefc6fa7)


    - In the query editor, you will want to run the below command to create the table we will use:

            CREATE TABLE items ( id SERIAL PRIMARY KEY, title VARCHAR(500) );
      
    - If you have created the items table correctly, you can find it under the 'permalist' database. To locate it, navigate to 'Schemas' and then to 'Tables'. After refreshing the 'Tables', the items table should appear. You can easily view and edit data by right-clicking on the 'items' table. As of now, there are no records available.

3. Now move to the code editor you will be using.
   - You will want to download or clone this repo. Once you have successfully opened this project in the code editor of your choice, you will need to start up your terminal. In your terminal cd over to where you are storing the project and run 'npm i' or 'npm install' to download all of the packages required for this application.
       - if you need assistance with installing npm and node, please refer to the link at the top.
   - Toggle back over to your code editor and open up the 'index.js' file. Here you will want to insert the password you created for PostgreSQL.
     
        ![Screenshot (362)](https://github.com/gkilch1/to-do-list/assets/113639024/ecc7e8b6-4a95-445c-9d5e-9b903a8c7ec9)

    - Once you have made the changes to the 'index.js' file, save them and return to your terminal. Run the command 'nodemon index.js' to launch the app on 'localhost:3000'. Open your browser and go to 'localhost'. You can then start the to-do list.

     - Here should be what you get as the result:

       ![Screenshot (361)](https://github.com/gkilch1/to-do-list/assets/113639024/8f466f7c-8833-4099-bc9e-d4af9029be3f)




