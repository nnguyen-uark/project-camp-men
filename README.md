# yelpCamp
 
version 3
branch: v3seeds
new technology: mongoose exports,  mongoose seeds
technology: mongoose (connect mongodb), RESTful, bootstrap, nodejs, expressjs
4 terminals: mongod, nodemon, mongo for debug database, and 1 free terminal

--------------------------------------------------
Note: 
- (git) if we make a change in branch2, but not stage/commit, you will lose all the changes if you switch to other branches
- (mongoose) Cat.find returns array, whereas Cat.findById return 1 object

--------------------------------------------------
YelpCamp: Refactoring App.js	
- create a models directory {:mainProject/models/campgrounds.js}
- use module.exports
- require everything correctly!

YelpCamp: Seeding the Database. Add Seeds File
- add a seeds.js files {seeds.js}
- run the seeds file every time the server starts {remove all camps- remove all comments- hardcode add camps- add comments, Referencing data }

YelpCamp: Comment Model.	Add the Comment model
- make our errors go away! {make Comment model comment.js with text-author, add comment property to campground db, Referencing data }
- display comments on campground show page {update app.get(/campgrounds/:id) to populate the comments, Referencing data }
