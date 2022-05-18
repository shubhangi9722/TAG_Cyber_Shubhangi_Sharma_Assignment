# TAG_Cyber_Shubhangi_Sharma_Assignment
Blogpost website where users can post, edit or delete their posts. 

A simple website application is developed using MySQL and PHP along with Laravel framework. This webiste provide users the authority to create and update their blog. Also, one more CRUD, application is delete, with the Admin's authorization users are able to delete their blog post. Adding to these, users can comment on posts as well. Let us walk through the entire application and the resources utilized in creating this website. 

**Resources:**
1. PHP (version 8.1.6)
2. MySQL (version 8.0)
3. Laravel (version 9)
4. OS - Windows 11, WSL2 (Windows Subsystem Linux 2), Docker Desktop
5. XAMPP Control Panel v3.3.0
6. IDE - VS Code


**Motivation**
The reason behind creating this application is to practically understand the concepts of PHP and Laravel framework, and how useful they are in real world web applications. Let us begin with initial steps in the development: 


**PHP:**
Primarily PHP, MySQL, Laravel, XAMPP, WSL2, Docker Desktop were installed and configured on the computer. Now, you can visit (https://windows.php.net/download#php-8.1) for installing latest PHP version. After visiting, click on VS16 x64 Thread Safe. Thread safe is preferrable as it will allow multiple threads to execute simultaneously. 

**MySQL:**
To install MySQL, follow the documentation process from (https://dev.mysql.com/downloads/windows/installer/8.0.html). After successful download, you will have to configure settings before installing the MySQL services. In the configuration process, you can select for MySQL Workbench, MySQL Servers and many more. Moreover, you will be asked to create password for databse and your username will be set as "root". Later, you will be able to install MySQL.


**Laravel:**
Laravel is a Scalabale, Community Framework that helps in building the web application progressively. Following the Laravel Documentation (https://laravel.com/docs/8.x/installation), you can easily understand the installation process and start with the very first Laravel project. The framework includes many dependencies and in-built functions that are necessary prominently for any website application. It includes in-built connections and middleware functions which are used to render respective routes when requested for. Starting form /GET, we can retrieve the users information from Log in and Registeration routes. The Laravel documentation, also guides through various packages that come along with the framework. 

I am using TailwindCSS for the frontend of this website application. TailwindCSS helps in creating widgets and cards. We can use Bootstrap as well, but TailwindCSS has more benefits compared to Bootstrap. The documentation can be found here (https://laravel.com/docs/9.x/mix#tailwindcss). With this we will also have to install the,


      1. composer require laravel/breeze --save-dev 
      2. php artisan breeze:install
      3. npm install
      4. npm run dev


Moving ahead, you can install the Docker Desktop (https://www.docker.com/products/docker-desktop) and create containers for your project. Before doing so, lets enable the connections for WSL2 by installing it (https://docs.microsoft.com/en-us/windows/wsl/install). 

( I faced some issues while running the Docker engine and WSL2 terminal initially. Thus, by changing the settings in Docker Desktop and making sure you have enabled the WSL2 connection by visiting (https://docs.docker.com/desktop/windows/wsl/) ) 


**XAMPP Control Panel:**
After these connections, we can start downloading XAMPP which is a complete package of Apache HTTP server, Maria DB, PHP and Perl langauges. Next step would be to configure the XAMPP control panel by setting the MySQL database port. We can now start Apache and MySQL together, and by clicking on "Admin" you will be redirecetd to "phpMyAdmin" webpage. On this webiste, you can create your database on PhpMyAdmin using SQL queries or directly on the website. 


Coming back to the backend of the website, as discussed earlier about the Signing In and Registeration, we might first need to populate the database and for that we have to connect the MySQL database with Laravel. For doing so, we can first start by giving permissions to users by installing the Spatie Permissions package through (https://github.com/spatie/laravel-permission and https://spatie.be/docs/laravel-permission/v5/introduction). After reading the documentation, you can install by entering the following commands through CLI:
                
                
                1. composer require spatie/laravel-permission
                2. To check if providers is updated, visit config/ app.php in your laravel projects folder. 
                       'providers' => [
                                          Spatie\Permission\PermissionServiceProvider::class,
                                      ];
                                      
                3. For migrating the permissions,
                         php artisan vendor:publish --provider="Spatie\Permission\PermissionServiceProvider"
                   The permissions will be migrated and copied
                   
                4. For clearing the cache in config,
                       php artisan config:clear
                       
                5. In the last, we can use the following the command:
                       php artisan migrate
 
 Now, the connection can be established between Laravel and MySQL database. The basic tables are created in the database. 
 
 
Currently, the website is created for Sign In and Register pages. The users are able to navigate through either website. I am yet to connect Laravel and MySQL database successfully. Even after numerous tries throughtout the day, I am still unable to establish the connection. I have pushed the code on GitHub, could you please guide me where I am going wrong in the code. 

This is the Progress of the Assignment till date. The soon I am able to connect database with Laravel, it will be little convenient for me to implement CRUD operations.  





