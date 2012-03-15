Lydia, a PHP-based, MVC-inspired CMF
====================================

This project is used while teaching advanced PHP-programming with Model View Controller (MVC)
frameworks with a taste of Content Management Framework (CMF). 

Material below is mainly in swedish.

* http://dbwebb.se/lydia/current (try out the code)
* http://dbwebb.se/f/123 (forum with some tutorials on how the code was built, only in swedish)


History
-------

Todo.

* Yes, a lot of things to do.


v0.2.02 (2012-03-15) 

* Uppgraded `CMUser` with groups and group-membership for each user.


v0.2.01 (2012-03-15) 

* Added `CMUser` and `CCUser` to handle users. Created code for testing login and logout of user.
* Added inteface convenience methods `RedirectToController` and `RedirectToControllerMethod` in `CObject`.


v0.1.9 (2012-03-13) 

* Added `CMGuestbook` as a model for the sample guestbook application.
* Rewrote code and separated between guestbook controller and model.


v0.1.8 (2012-03-05) 

* Added `CSession` as a wrapper to `$_SESSION`.
* Enabled flashmemory in `CSession` for as a memory to live through pagerequests, useful to send 
feedback to users and showing debuginfo to the developer.
* Updated `Guestbook` to make use of the new features.


v0.1.7 (2012-02-24) 

* Added a container for the views `CViewContainer`.
* Integrated `CViewContainer` in `CCGuestbook`, `CLydia`, `CObject`, and the theme handling.
* This makes `$ly->data` obsolete and to be removed in coming releases.


v0.1.6 (2012-02-24) 

* Added interface to those classes that uses SQL, `IUseSQL`.
* Updated `CCGuestbook` to use `IUseSQL`.


v0.1.5 (2012-02-24) 

* Introduced the database layer as `CMDatabase`.
* Showed how to use it in the `CCGuestbook` controller example.
* Enabled debug output from the database operations using settings in config-file and theme-helper 
`get_debug()`.
* Created a default exception handler in `bootstrap.php`.
* `CLydia` creates and owns the databaseobject as `$ly->db`.
* `CObject` makes the database object available for subclasses through `$this->db`.


v0.1.4 (2012-02-23) 

* Improved guestbook example to store messages in database using PHP PDO and SQLite.
* Added konfigurationsitem fpr database in site/config.php.
* Added site/data directory which should be writable bu the webserver.


v0.1.3 (2012-02-15) 

* Added some style and an icon the the core theme.
* Added a guestbook application as an example of a controller using database and forms.
* The guestbook is fully working and stores entries in the session.
* Cope with querystring sent to controller and methods.
* Added theme helper theme_url($url) which prepends $url with the url to the theme directory.
* Added session_start() in CLydia.
* Use default timezone as defined in site/config.php, set in CLydia::__construct()


v0.1.2 (2012-02-15) 

* One common baseclass for controllers and modules, CObject, holds access to CLydia through $this->
* Output from theme helper get_debug() is configurable in site/config.php.
* Wrapper htmlent() for htmlentities() to support character encoding from site/config.php.
* Remove all - and _ from the url before checking if method exists. Enables developer/display-object 
and developer/display_object to point to developer/displayobject.


v0.1.1 (2012-02-14) 
v0.1.0 (2012-02-14) 

* All requests handled by `index.php` and using mod_rewrite in `.htaccess`. 
* A base structure with `bootstrap.php`, frontcontroller and theme engine.
* Frontcontroller `CLydia::FronControllerRoute()` supporting varius url-constructs.
* A basic theme controller, `CLydia::ThemeEngineRender()`, with `functions.php`, `style.css` and template files.
* Managing base_url and introducing theme helper functions.
* 'CRequest' manages creation of internal links.

v0.01 - v0.03 (2011 december)
* This was the first release used in a course called dbwebb2.


 .   
..:  Copyright 2011 by Mikael Roos (me@mikaelroos.se)
