# HackTUES 2 Ruby on Rails workshop

## Part 1 - Getting comfortable

### Introduction
* What is Rails?
* Prerequisites
  * Basic programming knowledge
  * UNIX command line
  * Some HTML, CSS, JS
* The "Google the error message" algorithm

### Up and running
* Development environment
* Installing Rails
  * Linux: http://guides.railsgirls.com/install/#setup_for_linux
  * Windows: http://www.railsinstaller.com/
  * Mac: Why are you using one?
* When you are done installing your Rails environment, go [try out Ruby](http://tryruby.org)

### Quick note on scaffolding
* Auto-generated code is overwhelming
* Relying on scaffolding will turn you into a code monkey

### First application
* The command line is powerful, don't be afraid!
* Common UNIX commands

Description                         | Command
------------------------------------|---------------------
list contents                       | ls
make directory                      | mkdir <dirname>
change directory                    | cd <dirname>
move file (rename)                  | mv <source> <target>
copy file                           | cp <source> <target>
remove file                         | rm <file>
remove empty directory              | rmdir <directory>
remove nonempty directory           | rm -rf <directory>
concatenate & display file contents | cat <file>

* ```rails new```
* Standard directory and file structure

File/Dir      | Purpose
--------------|----------------------------------------------------------------------------------------
app/          | Core application (app) code, including models, views, controllers, and helpers
app/assets    | Applications assets such as cascading style sheets (CSS), JavaScript files, and images
bin/          | Binary executable files
config/       | Application configuration
db/           | Database files
doc/          | Documentation for the application
lib/          | Library modules
lib/assets 	  | Library assets such as cascading style sheets (CSS), JavaScript files, and images
log/ 	        | Application log files
public/ 	     | Data accessible to the public (e.g., via web browsers), such as error pages
bin/rails     | A program for generating code, opening console sessions, or starting a local server
test/         | Application tests
tmp/ 	        | Temporary files
vendor/       | Third-party code such as plugins and gems
vendor/assets | Third-party assets such as cascading style sheets (CSS), JavaScript files, and images
README.rdoc   | A brief description of the application
Rakefile 	    | Utility tasks available via the rake command
Gemfile     	 | Gem requirements for this app
Gemfile.lock 	| A list of gems used to ensure that all copies of the app use the same gem versions
config.ru 	   | A configuration file for Rack middleware
.gitignore   	| Patterns for files that should be ignored by Git

* Bundler
  * Gems are truly outrageous
  * ```bundle install```
  * Gemfile
* ```rails server```
* MVC
  * Architectural pattern
  * Separates internal representation of information from the way the user receives it
  * Interactions
  * Note: HTTP requests
* Hello World!
  * Add a hello action to the Application controller
  * Set the root route

### Exercises
* Change the **hello** action to display a sentence of your choice
* Add a **goodbye** action that renders "Goodbye, world!" and edit the routes file accordingly

## Part 2 - Twitter-style application

### Planning
* REST
* Remember note about scaffolding
* ```rails new```
* Models for user and micropost
  * Users - id, name, email
  * Microposts - id, content, user_id
 
### Users resource
* ```rails generate scaffold```
* Migrating our database
* Note: Rake
* MVC in action - let's take a tour
* RESTful routes

HTTP request |	URL           |	Action  |	Purpose
-------------|---------------|---------|-----------------------------
GET          |	/users        |	index   |	page to list all users
GET          |	/users/1      |	show    |	page to show user with id 1
GET          |	/users/new    |	new     |	page to make a new user
POST         |	/users        |	create  |	create a new user
GET          |	/users/1/edit |	edit    |	page to edit user with id 1
PATCH        |	/users/1      |	update  |	update user with id 1
DELETE       |	/users/1      |	destroy |	delete user with id 1

* Weaknesses
 * No data validation
 * No auth
 * No styling
 * **No real understanding**

### Microposts resource
* Repeat first steps just like the users resource
* Validations - constraining microposts to 140 characters
* Associations
  * **has_many**
  * **belongs_to**

### Exercises
* Find out how to validate the presence of micropost content
* When you do, validate the presence of name and email attributes in the User model as well

## Conclusion
* Very high-level overview of Rails
* Taste of MVC and REST
* Working simple web app

## What next?
* This workshop is based on Chapter 1 & 2 of [Michael Hartl's Rails Tutorial](https://www.railstutorial.org/)
* You can read the whole book to get a great understanding of Rails
