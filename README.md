# Full-Stack Forum Website with Laravel & MySQL backend
## With complete login and accounts system (users CRUD), complete posting, commenting, admininstration system (content CRUD)

Completely made from scratch by me (Eduardo Correia) using Laravel, PHP and Javascript.
The database uses MySQL. No configuration needed, database automatic migrations and creations are included in the code.
It covers all the principal Laravel Full-Stack functionality, and all the MySQL basic knowledge.
All databases have relationships between them (1:m, 1:n, m:n)

Users can create posts on each category. Each post can have multiple categories. Users can comment on posts from other users. Each user can delete or edit its own comment or post, other users cannot. Admin can edit or delete every post or comment. Every post edited by admin gets an *EDITED BY ADMIN* flag at the end. Everything is ordered chronologically. The front page shows the most active categories and shows who made the latest post, how many comments, who made the latest comment.
Admins can also add or remove whole forum categories.
Each user has its own profile where it can edit its details, like name, email, password or even delete the account. Every change asks the user for the current password.
Security is taken very seriously, passwords are never sent to the server or even stored as plain text. They are hashed and encrypted right away on the client/user's own device before being sent to the server. The database only stores encripted passwords, and cannot decrypt them, not even admins.
The passwords are confirmed to be correct at user login or whatever by comparing hashes, not plain text.
Laravel Auth system was used. If a user forgets the email or password, he can ask for a recovery email that is automatically sent using SMTP to the users email with a private token that expires after some hours. With that, he can create a new password.
As a good practice, nothing is ever deleted from the database, only "deactivated". I've made a system where every user, post, comment or even category has an active status of 1 or 0. 1 is the default state. Deleting something only switches it to 0, does not delete it.

The programs used where VSCode for coding, Laravel as the framework with some extensions, and MAMP (like XAMPP for Mac) as the local MySQL server.
MySQL Workbench as used to make some EER Diagrams to help build up the database relationships.
Every database detail is coded into the migrations in Laravel, so it creates databases automatically and even creates some random posts and users for testing.



## Laravel License
The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
