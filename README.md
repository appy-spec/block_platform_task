SimpleBlog
A simple blogging platform built on Node.js and Express.js that uses Markdown syntax for posting.

To speed things up, Simple doesn't make use of user sessions. Since there are no sessions, there is no admin user. Simple makes all admin pages (new post, edit, etc) accessible to the public but requires a master password to do anything serious.

Demo: My blog

Installation
npm install simple-blog
Enviroment Setup
Your app will need access to a MongoDb database to save posts. You can do one of the following:

Have MongoDb installed locally on port 27017
Set environment variable MONGO_URL to a remote location (ex. MongoHQ)
You can also set the password you will use to create/edit posts by setting the environment variable BLOG_SECRET. The password is only required if NODE_ENV is set to production and will default to "password" if not specified.

Sample Server
require('simple-blog').start();
Server With Custom Views And Stuff
Simple Uses Express.js for a backend so setup is very simple.

Copy template and public directories
Simple comes with a default template but I'm sure you'll want to make your own. To make sure you have everything you need to get started you can copy the sample files from the module by doing the following:

$ cd myApp/
$ cp -r node_modules/simple-blog/public ./
$ cp -r node_modules/simple-blog/views ./
