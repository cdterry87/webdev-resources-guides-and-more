# Web Developer Interview Questions

## JavaScript

1. How to create an object

- var object = {}
- var object = new Object()
- var object = Object.create(null)
  or

```
class Person {
    constructor(name) {
      this.name = name;
    }
}
var object = new Person('');
```

2. What is hoisting in javascript?

- The default behavior of moving all the declarations at the top of the scope before code execution

## PHP

1. Difference between include and require

- Both include a file, but require results in fatal error if file can’t be included`

2. Get the IP address of client

- $\_SERVER['REMOTE_ADDR']

3. Difference between unset and unlink

- Unset sets a variable to undefined; unlink deletes a file

4. Error types

- Notice – non-critical errors that occurred during execution (ex. Access an undefined variable)
- Warning – more important errors but script execution continues (ex. Include a non-existent file)
- Fatal – causes termination of script execution (ex. Require a non-existent file)

5. Difference between GET and POST

- GET variables are in URL; POST are encoded in the request body
- GET has 2048 max chars and POST has no limit
- GET is to retrieve data and POST is to insert/update

6. How to handle error reporting

- Display_errors is on in php.ini
- Ini_set(‘display_errors’, 1)
- Error_reporting(E_ALL)

7. What are traits

- Allow you to create reusable code where inheritance is not supported. Trait cannot be instantiated on its own. Similar to a class but intended to group functionality.

8. Can a constant change during script execution?

- No; constants cannot be changed once declared

9. Can you extend a final class?

- No

10. What are construct and destruct

- Construct is a built in method that’s called when an object is instantiated and is used to initialize properties; destruct is called when object is destroyed and takes no params

11. How to get number of elements in array

- count()

12. Get the sum of string of integers: $input = ‘1, 2, 3, 4, 5, 6, 7’;

- echo array_sum(explode(‘,’ $input);

13. Three scope levels in php

- Private – visible in own class
- Public – visible to any code accessing class
- Protected – visible only to classes parents and classes that extend the current class

14. What are getters and setters

- Methods used to declare or obtain the values of variables (usually private ones). A central location to handle data before declaring or returning it

15. What is MVC

- Model – handle specific tasks related to a specific area of app or functionality; database interact
- View – passed data from controller and displayed to user
- Controller – handles data passed by view and passes data to view; sends/receives data from model

16. How to prevent “cannot modify header information – headers already sent” warning

- Don’t output anything before headers are set

17. What are SQL injections and how to prevent them

- Method for altering a SQL query which can compromise data in the database
- Escape user input and use prepared statements
- Don’t use mysql functions; use mysqli or PDO

18. Why use === instead of ==

- If you want to check for a specific type. It performs better since it doesn’t have to do type conversion and should especially be used for true/false

19. What are PSR’s?

- PHP standards recommendations to standardize common aspects of PHP development like coding style (PSR-2)

20. Why should you follow PSR's?

- Coding standards vary between developers and companies so it sets a standard for how code should look which reduces confusion and possibly errors

21. What is composer?

- Tool for dependency management; add libraries your app depends on. Example:

```
composer require nesbot/carbon
```

22. What is PEAR?

- PHP extension and application repository – extension of PHP with database classes, etc.

23. How to execute PHP from command line

- php script.php

24. Start/finish php script

```
<?php ?> and <? ?>
```

25. Display output to the browser

```
echo, print, and <?= ?>
```

26. PHP5 introduced OOP
27. Final classes and methods

- Final class cannot be extended, and final method can’t be overridden

28. Compare objects in PHP

- == to test if two objects are instanced from the same class and have same attributes and values
- === to test if two objects refer to same instance of same class

29. How to use image functions

- GD library

30. Require vs require_once

- Same except require_once checks if script is already included before execution

31. Display information in human readable format

- print_r()

32. Set infinite execution time for script

- Set_time_limit(0);
- Also set in php.ini

33. Export data into excel

- Write to .csv file with comma delimited values

34. What is file_get_contents for

- To read the contents of a file and store it in a variable

35. Connect to database

- $database = mysqli_connect("HOST", "USER_NAME", "PASSWORD"); mysqli_select_db($database,"DATABASE_NAME");

36. What is mysql_pconnect() for

- Create a persistent database connection that doesn’t close when script ends

37. Handle results in mysql

- mysqli_fetch_array, mysqli_feetch_assoc, mysqli_fetch_object, mysqli_fetch_row

38. Get number of results returned in a results set

- mysqli_num_rows()

39. Number of affected entries in a query

- mysqli_affected_rows()

40. Check if value is numeric

- is_numeric()

41. Check if value is alphanumeric

- ctype_alnum()

42. Check if variable is empty

- empty()

43. Escape data before storing in database

- addslashes()

44. Remove escape chars from a string

- stripslashes()

45. Remove html tags from data

- strip_tags()

46. Define a global variable with the global keyword
47. Best method to hash passwords

- password_hash()

48. Define a constant in PHP

- define(‘CONSTANT’, 123);

49. Pass a variable by reference

- With ampersand in front of variable; $var = &$var2;

50. How to cast types in php

- (int), (bool), (float), (string), (array), (object)

51. Ternary condition in php

- Condition ? expression1 : expression2

52. How to get number of params passed to function

- func_num_args()

53. What does :: mean?

- Static and does not require object initialization

54. In PHP objects are passed by value or reference?

- By value

55. Are parent constructors called implicitly inside a class constructor?

- No, must be called like `parent::constructor($value)`

56. What is a session

- A logical object enabling us to preserve temporary data across multiple PHP pages

57. How to initiate a session?

- session_start()

58. How to propagate a session id?

- Cookies or URL params

59. When do sessions end?

- When php script finishes executing or after session_write_close() is called

60. What is $GLOBALS

- Associative array of all variables in the global scope

61. What is $\_SERVER

- Array of information created by web server such as paths, headers, and script locations

62. What is $\_FILES

- Associative array of items uploaded to current script via the HTTP POST method

63. Difference between session_unregister() and session_unset()

- Unregister removes a global variable from current session
- Unset removes all session variables

64. $\_FILES['userfile']['name'] – original file name on the computer
65. $\_FILES['userfile']['tmp_name'] – file name stored on the server
66. Upload_max_filesize in php is max file upload size on server
67. What is $\_ENV

- Associative array of variables sent to PHP script via the environment method

68. What is $\_COOKIE

- Associative array of variables sent to php script using HTTP cookies which are temporary files the server stores on the user's computer that can be accessed whenever that same browser visits that page again.

69. What is scope?

- Context within which a variable is defined

70. Concatenation operators

- . concatenates left and right arguments
- .= appends argument on the right to argument on left

71. === is identity operator; both vars must be identical for it to return true
72. Determine if variable is set

- isset()

73. Difference between strstr() and stristr()

- Find first occurrence of a string; stristr is case insensitive search

74. Foreach is used to iterate over arrays
75. What is ereg_replace vs eregi_replace()

- Replace a regular expression; case insensitive

76. How to protect data in a query string

- urlencode()

77. How to destroy a cookie

- Set expiration time of cookie to a date in the past

78. What is composer?

- A dependency manager

79. What is ereg_replace vs eregi_replace()

- Replace a regular expression; case insensitive

80. How to sort using spaceship operator in php7?

```
usort(['Bbbbb', 'Ccccc', 'Aaaaa'], function($a, $b) {
  return $a <=> $b; // -1, 0, 1
})
```

81. What is the null coalesce operator?

- ?? – instead of typing $name = isset($\_GET[‘name’]) ? $\_GET[‘name’] : ‘’ you can type $name = $\_GET[‘name’] ?? ‘’

82. New in PHP7

- 7.1 - Array destructuring, null coalescing operator ??, type hints, nullable and void types
- 7.4 – null coalescing assignment operator ??=, arrow functions with fn (), spread operator

83. What is XSS and how do you prevent it?

- Where an attacker gains access to a website and executes a potentially malicious script at the client’s side. This is one of the code injections attacks which can be caused by incorrectly validating user data, which usually gets inserted into the page through a web form or using a hyperlink that has been tampered with.

- Prevent it with functions like `htmlspecialchars()`, `htmlentities()`, `strip_tags()`, `addslashes()`

84. Explain the output buffering.

- Starts with ob_start(). Storing output in a buffer/memory and outputting it all at once to improve performance. Otherwise the output gets sent in pieces as it's processed. You can call ob_flush() or ob_end_flush() to clear out the buffer and the buffer is also cleared out when the script ends. With output buffering you can capture output and even manipulate it before it gets output to the browser.

85. What are SOLID principles?

- Single Responsibility - Classes/modules should solve only one problem
- Open/Closed - Should not modify existing/well-tested classes when a new feature is built to avoid introducing bugs; Should instead extend the class/interface to add new features
- Liskov Substitution - If you have a Class that extends another Class, such as `Class B extends A`, you should be able to use `Class A` anywhere you would use `Class B` and vice versa.
- Interface Segregation - Interfaces should not enforce unnecessary methods to promote smaller interfaces
- Dependency Inversion - High level classes should not depend on low level classes and should not need to know the details of those lower level classes; See dependency injection and IOC

86. Explain namespaces

- Namespaces provide a way in which to group related classes, interfaces, functions and constants and also help to prevent name conflicts between classes/functions and 3rd party classes/functions

87. What is Opcache and why is it useful?

- A caching engine built into php that increases performance by storing precompiled scripts so php doesn't have to load/parse those scripts on each request.

88. What is an interface?

- Defines the structure of a class and how it should be implemented. A class should have the same behavior as the interface it implements. `ClassName implements InterfaceName`

89. How do you get the request URI in PHP?

- $\_SERVER['REQUEST_URI']

90. Describe dependency injection / inversion of control.

- Say you have a class, and a method of that class needs another class, and the method of that class needs another class. With IOC, you first define the lowest level dependency, and you inject it into the class that needs it like this:

```
# From https://php-di.org/doc/understanding-di.html
class StoreService {
    private $geolocationService;

    public function __construct(GeolocationService $geolocationService) {
        $this->geolocationService = $geolocationService;
    }

    public function getStoreCoordinates($store) {
        return $this->geolocationService->getCoordinatesFromAddress($store->getAddress());
    }
}
```

and define your services using an interface like this:

```
interface GeolocationService {
    public function getCoordinatesFromAddress($address);
}

class GoogleMaps implements GeolocationService { ...

class OpenStreetMap implements GeolocationService { ...

class MapQuest implements Geolocation Service { ...
```

Dependency injection prevents your classes from being tightly coupled to their dependencies. Instead of hard-coding class dependencies, you inject them at runtime. For example, you can define a generic service like the `$geolocationService` above, then in your script, initialize your service and pass it to your class like this:

```
$geolocationService = new GoogleMaps();
$storeService = new StoreService($geolocationService);
```

91. ELI5 OOP programming

- I think of it kind of like a puzzle. Your program is the full puzzle when it's put together, and the code you write is like the individual pieces. Each piece of the puzzle, called an Object/Class, will be a specific "thing" in your app, like a "User", or a "File", or a "Task". Each object has a set of instructions called "methods/functions" that define what that "thing" can do or have done to it. The advantage is that code is broken up into smaller manageable pieces and more people can work on different parts instead of one big application.

92. How to encrypt a password:

```
$encrypted = password_hash($password, PASSWORD_DEFAULT);
```

93. How to validate an email address with filters?

```
filter_input(INPUT_POST, 'email', FILTER_VALIDATE_EMAIL);
```

94. What is a variadic function?

```
// Accept a variable number of arguments which get converted into an array in the function using the splat operator (...)
function process(...$vals) {}
```

95. Describe encapsulation

- Wrapping variables and methods into a class. Encapsulation is used to protect variables and methods by restricting access to them using accessors (protected, private) and having getter/setter methods to access data in the class.

```
class Person
{
  private $name;

  public function getName()
  {
    return $this->name;
  }

  public function setName($name)
  {
    $this->name = $name;
  }
}
```

96. What is the singleton pattern?

- When only one instance of a class is needed. Instead of creating a new instance you reference the existing instance of the class.

97. How does the internet work?

- Websites have a domain name like `www.google.com`. You enter this domain name in the browser.
- The browser uses DNS to look up the IP address of that domain and sends a request to that domain's server.
- Your browser connects to that domain's web server on port 80 (HTTP) or 443 (HTTPS) and the web server responds with a web page which gets downloaded by the browser.

### Laravel

1. What is Laravel?

- An open source PHP framework written by Taylor Otwell in PHP7 (currently). Uses MVC architecture.

2. What is an Event in Laravel?

- An observer implementation that lets you subscribe and listen to certain actions that occur in the app.

3. What is artisan?

- CLI interface tool that is included with laravel that lets you run commands that help with building your app like saffolding models and controllers. Ex. `php artisan make:model ModelName`

4. What are some Laravel packages?

- Breeze - authentication scaffolding with Tailwind
- Cashier - implement payments with Stripe
- Jetstream - a starter kit that implements login, registration, email verification, 2fa and uses Tailwind with Livewire or Inertia scaffolding
- Passport - OAuth2 server implementation
- Sail - a docker container for laravel
- Horizon - dashboard for Redis queues
- Socialite - OAuth with 3rd parties like Facebook, Twitter, LinkedIn, Google, Github, BitBucket
- Telescope - look at requessts, exceptions, logs, database queries, queues, mail, etc. for development purposes
- Valet - dev environment for MacOs that's quick and easy to setup

5. What are named routes?

- You can specify a route and give it a name that's different than the actual path. Then in your code when you want to refernce the route, you can just specify it by name instead of the path.

6. What are database migrations?

- Like version control for databases. You build your database structure in PHP scripts using something like `php artisan make:migration create_users_table`, then open the script and modify it. When you have your structure, you run `php artisan migrate` and it will create your database structure for you.

7. What are service providers?

- A central location where the core laravel application features and your app are bootstrapped. They use the ServiceProvider class

8. What is the Laravel service container?

- Used to resolve class dependencies and perform dependency injection. Class dependencies are injected into classes via the class constructors or setters rather than being instantiated in the classes themselves.

9. What are Laravel Contracts?

- Interfaces that define the core services in the framework

10. What are facades?

- Basically like static methods for core laravel features to give easy access to those methods in an expressive syntax like `Route::get()` or `DB::table('table_name')->get()`

11. What is eloquent?

- Laravel's ORM and query builder which is an ActiveRecord implementation for working with databases.

12. What are traits?

- Lets you define a method that caan be shared across different classes.

```
trait Sharable {
  public function share($item)
  {
    return 'share this item';
  }
}

class Post {
  use Sharable;
}

class Comment {
  use Sharable;
}
```

13. What about caching?

- Laravel uses Memcached and Redis for caching

14. What is Lumen?

- A PHP micro-framework based on Laravel's main components used to build APIs and microservices

15. What is dd()?

- dump and die for debugging

16. What are laravel guards?

- Define how users are authenticated for each request; The session guard maintains state using session and storage cookies.

17. How to put in maintenance mode?

```
php artisan down
php artisan up
```

18. What are factories and seeders?

- Factories are a way to put values in fields of a particular model automatically. Used with seeders to populate fake data in a database.
- Seeders are used to seed the database with mock data using something like Faker to simulate data.

19. How do you implement soft deletes?

- `use SoftDeletes;` in your Model

20. How do you do form/request validation?

```
public function store(Request $request)
{
    $validated = $request->validate([
        'title' => 'required|unique:posts|max:255',
        'body' => 'required',
    ]);
}
```

21. What are collections?

- A wrapper for an array of data; Eloquent returns collections from database queries. There are methods that make it easier to work with collections by iterating over them or performing operations on them.

22. What are queues?

- When a task would otherwise take a long time to process, you can run it in the background with queues.

## HTML

## CSS

1. What does `article + article` do?

- Will apply styles to all article tags except the first one.

## MySQL

1. What is MySQL?

- A multi-threated, multi-user open-source relational database currently owned by Oracle.

2. What is the difference between a table and a database?

- A table is a collection of rows and columns; a database is a collection of tables.

3. What types of tables are present in MySQL?

- MyISAM, Heap, Merge, INNODB, ISAM
- MyISAM has table level locking while a query is running; Also has Fulltext searches and is smaller than innodb
- INNODB has row level locking so it only locks the row being modified. INNODB also has transactions, primary/foreign key constraints, and better crash recovery than MyISAM

4. Check MySQL version

- linux prompt: mysql -v
- mysql prompt: SHOW VARIABLES LIKE "%version%";

5. How to add columns

- ALTER TABLE table_name ADD COLUMN column_name VARCHAR(30) NOT NULL;

6. How to delete a table?

- DROP TABLE tablename;

7. How to add a foreign key?

- [CONSTRAINT constraint_name] FOREIGN KEY [foreign_key_name] (col_name, ...) REFERENCES parent_tbl_name (col_name,...)

8. How to change mysql password?

- ALTER USER 'root'@'localhost' IDENTIFIED BY 'NewPassword';

9. How to rename a table?

- RENAME old_table TO new_table;

10. How to change database name?

- Create a new database, mysqldump your existing database, and import into the new database
- mysqldump -u username -p "password" -R oldDbName > oldDbName.sql
- mysql -u username -p"password" newDbName < oldDbName.sql

11. How to change column name?

- ALTER TABLE table_name CHANGE COLUMN old_column new_column [column definition]

12. How to delete columns?

- ALTER TABLE table_name DROP COLUMN column1, column2, etc.

13. How to insert into a table?

- INSERT INTO table_name (field1, field2, field3) VALUES (value1, value2, valu3)

14. How to delete from table?

- DELETE FROM table_name WHERE condition

15. How to join tables

- INNER - returns only those results from the tables that match the specified condition and hides other rows and columns. MySQL assumes this as the default Join.
- LEFT - return all the records from the first (left-side) table, even no matching records found from the second (right side) table. If it will not find any matches record from the right side table, then returns null.
- RIGHT - returns all rows from the right-hand table, and only those results from the other table that fulfilled the join condition. If it finds unmatched records from the left side table, it returns Null value; Also known as an OUTER join.
- CROSS - used to combine all possibilities of the two or more tables and returns the result that contains every row from all contributing tables

16. Join two tables

- SELECT name, scores, address, email FROM Student s INNER JOIN Marks m on s.stud_id = m.stud_id
- SELECT name, scores, address, email FROM Student s, Marks m WHERE s.stud_id = m.stud_id

17. How to update table

- UPDATE table_name SET field1=new-value1, field2=new-value2, ... [WHERE Clause]

18. How to drop primary key

- ALTER TABLE table_name DROP PRIMARY KEY;

19. What is a stored procedure and how to create one?

- A group of SQL statements that we save in the database. The SQL queries, including INSERT, UPDATE, DELETE, etc. can be a part of the stored procedure

```
DELIMITER &&
CREATE PROCEDURE procedure_name [[IN | OUT | INOUT] parameter_name datatype [, parameter datatype]) ]
BEGIN
    Declaration_section
    Executable_section
END &&
DELIMITER ;
```

```
CALL stored_procedure_name (argument_list);
```

21. What is a view and how to create one?

- a database object whose values are based on the base table. It is a virtual table created by a query by joining one or more tables. It is operated similarly to the base table but does not contain any data of its own. If any changes occur in the underlying table, the same changes reflected in the View also.

```
CREATE [OR REPLACE] VIEW view_name AS
SELECT columns
FROM tables
[WHERE conditions];
```

22. What is a trigger and how to create one?

- a procedural code in a database that automatically invokes whenever certain events on a particular table or view in the database occur. It can be executed when records are inserted into a table, or any columns are being updated

```
CREATE TRIGGER trigger_name
[before | after]
{insert | update | delete}
ON table_name [FOR EACH ROW]
BEGIN
    --variable declarations
    --trigger code
END;
```

23. Create a mysql user

```
CREATE USER [IF NOT EXISTS] account_name IDENTIFIED BY 'password';
```

24. Load data from csv into a table

```
LOAD DATA INFILE '/path/to/file/filename.csv'
INTO TABLE tablename
FIELDS TERMINATED BY ','
OPTIONALLY ENCLOSED BY '"'
LINES TERMINATED BY '\r\n'
IGNORE 1 ROWS;
```

25. The difference between CHAR and VARCHAR

```
CHAR and VARCHAR have differed in storage and retrieval.
CHAR column length is fixed, while VARCHAR length is variable.
The maximum no. of character CHAR data types can hold is 255 characters, while VARCHAR can hold up to 4000 characters.
CHAR is 50% faster than VARCHAR.
CHAR uses static memory allocation, while VARCHAR uses dynamic memory allocation.
```

26. What is default mysql port number

- 3306

27. How to use limit to display first 20 rows

- SELECT \* FROM table_name LIMIT 0,20;

28. Write a query to select all teams that won either 1, 3, 5, or 7 games.

- SELECT team_name FROM team WHERE team_won IN (1, 3, 5, 7);

29. What are the advantages of MyISAM over InnoDB?

- MyISAM follows a conservative approach to disk space management and stores each MyISAM table in a separate file, which can be further compressed if required. On the other hand, InnoDB stores the tables in the tablespace. Its further optimization is difficult.

30. How to display the nth largest salary from a table

- select distinct(salary)from employee order by salary desc limit n-1,1

31. How to count the number of rows

- SELECT COUNT user_id FROM users;

32. What are DDL, DML, and DCL

- DDL - Data Definition Language (DDL) deals with all the database schemas, and it defines how the data should reside in the database. Commands like CREATE TABLE and ALTER TABLE
- DML - Data Manipulative Language (DML) deals with operations and manipulations on the data. The commands in DML are Insert, Select, etc.
- DCL - Data Control Languages (DCL) are related to the Grant and permissions. In short, the authorization to access any part of the database is defined by these.

33. Select entries for a single month from a table

- select \* from tasks where month(date_time_column) = 2;

34. How to use the WHERE, IN clause

```
SELECT * FROM table_name WHERE column IN (value1, value2, value3, ...)
```

35. How to use the BETWEEN clause

```
SELECT * FROM contacts WHERE contact_id BETWEEN 100 AND 200;
```

36. How to export an entire database?

- mysqldump

37. Describe the GROUP BY clause.

- The GROUP BY clause returns one row for each group. In other words, it reduces the number of rows in the result set. Can be combined with another method like COUNT to get a count of each of a specific value. Example:

```
SELECT
    status, COUNT(*) as count
FROM
    orders
GROUP BY status;
```

- This yields a result that looks like this:

```
status | count
------------------
Active      15
On Hold     3
Cancelled   6
```

- Or you can join tables and use SUM to get the sum of all items of a group like this:

```
SELECT
    status,
    SUM(quantity * price) AS amount
FROM
    orders
INNER JOIN orderdetails
    USING (orderNumber)
GROUP BY
    status;
```

## Linux

1. Difference between Unix and Linux

- Unix is proprietary (bell labs); Linux is open source by Linus Torvalds

2. What is bash

- Default shell for most linux operating systems

3. What is the kernel?

- Core part of the OS that manages interactions with hardware

4. Difference between bash and dos

- Bash is case sensitive, uses forward slashes; dos is not case sensitive and uses backslashes

5. What is swap?

- Partition; Temporary space the OS uses when there isn’t enough RAM to perform an action

6. How to check memory usage

- Top
- Free -m

7. What are Symbolic links?
8. How to change permissions

- Chmod 777 filename.ext
- Chmod -R 777 foldername
- Chown is the same and changes group/owner

9. What does pwd do?

- Prints the current working directory

10. What is a daemon?

- A service that’s running waiting for a request so it can perform an action

11. What are the types of permissions

- Read, write, execute

12. What is the grep command?

- Pattern based searching

13. How do you terminate a process?

- Kill -9 process_id

14. How to find all js files with the word ‘project’ in it

- Find / -name ‘\*.js’ | xargs grep “project”

15. Find the status of a process

- Ps ux
- Ps -ef|grep httpd or ps -ef|grep apache2 or ps -ef|grep php

16. How to tar/untar files

- Tar -zcvf tarfilename.tar.gz file1 file2 file3 # compress and zip files
- Tar -zxvf tarfilename.tar.gz # unzip tar file

17. How to delete files

- Rm filename
- Rm -rf directory

18. What is sudo?

- Temporary root access

19. How to restart apache?

- Sudo service apache2 restart

## Data Structures and Algorithms

1. What is Big O Notation?

- Big O notation is used to describe the performance or complexity of an algorithm. Can be used to describe the execution time or space/memory used. Only cares about the worst case.

- O(1) – constant time; describes an algorithm that will always execute in the same amount of time or space regardless of the input

- O(n) –linear time; scales linearly with the size of the input

- O(n^2) – quadratic time; describes an algorithm whose performance is proportional to the square of the size of the input

- O(2^n) – exponential time; doubles with each addition to input

- O(n!) – factorial time; adding a loop for every element

2. Big O Notation Rules:

- Different steps get added together; always the worst case
- Remove constants (2n = n)
- Different inputs have different variables
- Drop non-dominant terms

3. Space complexity – memory; total size available relative to size of input

- Heap – where we store variables
- Stack – where we keep track of function calls

4. What causes space complexity?

- Variables
- Data Structures
- Function calls
- Allocations

5. Arrays

- Static arrays - fixed in size; you must specify the length beforehand
- Dynamic arrays - expands automatically as you add more elements; copy and rebuild an array in a new memory location with more memory if needed
