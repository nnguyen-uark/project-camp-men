# yelpCamp

version 10
- branch: v10updateDestroy
- new technology: 
- 4 terminals: mongod, nodemon, mongo for debug database, and 1 free terminal
---------------
Notice: 
- the ejs files (like /view/partials/header.ejs or views/campgrounds/show.ejs) can access currentUser but not req.user
 + Vice versa, the js routes/files (like /routes/campgroundRoutes.js)can access req.user but not currentUser
- useful redirect: res.redirect('back');
---------------
Campground Edit and Update	Editing Campgrounds
- add method-override {install package}
- add edit route for campgrounds {app.get(‘/campgrounds/:id/edit’)…/views/campgrounds/route_edit.ejs…build route_edit.ejs }
- add update route {app.put(‘/campgrounds/:id’) }
- add link to edit page {/views/campgrounds/route_show.ejs }
- fix $set problem

Campground Destroy	Deleting Campgrounds
- add destroy route {app.delete(‘/campgrounds/:id’) }
- add delete button {/views/campgrounds/route_show.ejs }
- notice that we need to delete comments associated with the deleted campground link

Campground Authorization Part 1	Authorization Pt 1
- user can only edit his/her campgrounds {
 + idea is to use both grounds 1.middleware for the route 2.hide buttons
 + modify /routes/campgroundRoutes.js routes app.get(/edit) first}
- user can only delete his/her campgrounds {build middleware function for both edit and delete}

Campground Authorization Part 2	Authorization Pt 2
- hide/show edit and delete buttons {modify show views/campgrounds/route_show.ejs }
