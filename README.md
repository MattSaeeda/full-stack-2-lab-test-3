# LAB TEST 

# MongoDB
1. Write a MongoDB query to display all the documents in the collection restaurants.
db.restaurants.find();


2. Write a MongoDB query to display the fields restaurant_id, name, borough and cuisine for all the documents in the collection restaurant.
db.restaurants.find( {restaurant_id}, {name}, {borough}, {cuisine});


3. Write a MongoDB query to display the fields restaurant_id, name, borough and cuisine, but exclude the field _id for all the documents in the collection restaurant.
db.restaurants.find({"restaurant_id" : 1,"name":1,"borough":1,"cuisine" :1,"_id":0});

4. Write a MongoDB query to display the fields restaurant_id, name, borough and zip code, but exclude the field _id for all the documents in the collection restaurant.
db.restaurants.find({},{"restaurant_id" : 1,"name":1,"borough":1,"zipcode" :1,"_id":0});

5. Write a MongoDB query to display all the restaurant which is in the borough Bronx.
db.restaurants.find({"borough": "Bronx"});


6. Write a MongoDB query to display the first 5 restaurant which is in the borough Bronx.
db.restaurants.find({"borough": "Bronx"}).limit(5);
   

7. Write a MongoDB query to find the restaurants who achieved a score more than 90.
db.restaurants.find({grades : { $elemMatch:{"score":{$gt : 90}}}});

8. Write a MongoDB query to find the restaurants that do not prepare any cuisine of 'American' and their grade score more than 70 and latitude less than -65.754168.
db.restaurants.find( @and [{"cuisine" : {$ne : "American "} , "grades.score" :{$gt : 70} ,
                             "coord": {$lt : -65.754168}]});

9. Write a MongoDB query to find the restaurants which do not prepare any cuisine of 'American' and achieved a score more than 70 and located in the longitude less than -65.754168.
Note : Do this query without using $and operator.

10. Write a MongoDB query to find the restaurants which do not prepare any cuisine of 'American ' and achieved a grade point 'A' not belongs to the borough Brooklyn. The document must be displayed according to the cuisine in descending order.
db.restaurants.find( @and [{"cuisine" : {$ne : "American "} , "grades.grade" :{$eq : A} ,
                             "borough: {$not : Brooklyn}]}).sort(cuisine : -1);

11. Write a MongoDB query to find the restaurants which belong to the borough Bronx and prepared either American or Chinese dish.
db.restaurant.find( {
    $and : [ borough : Bronx
        { $or : [ { cuisine : American }, { cuisine : chinese } ] },]
} )

12. Write a MongoDB query to find the restaurant Id, name, borough and cuisine for those restaurants which belong to the borough Staten Island or Queens or Bronxor Brooklyn.
db.restaurants.find( {{restaurant_id}, {name}, {borough}, {cuisine}} , $and : [ $or {borough : Staten Island)} , {borough : Queens} , {borough : bronx}, {borough : Brooklyn};


------  
# NodeJS
Q 1 - What is Callback?
answer = A

A - Callback is an asynchronous equivalent for a function.
B - Callback is a technique in which a method call back the caller method.
C - Both of the above.
D - None of the above.


Q 2 - Which of the following is true about EventEmitter.emit property?
Answer : C

A - emit property is used to locate an event handler.
B - emit property is used to bind a function with the event.
C - emit property is used to fire an event.
D - None of the above.


Q 4 - Which of the following is true about File I/O in Node applications?
answer = C

A - Node implements File I/O using simple wrappers around standard POSIX functions.
B - Node File System (fs) module should be imported for File I/O opearations.
C - Both of the above.
D - None of the above.


Q 4 - Which of the following is true about clearTimeout(t) global function?
answer C

A - The clearTimeout( t ) global function is used to stop a timer that was previously created with setTimeout().
B - The clearTimeout( t ) function returns an opaque value that represents the timer which can be used to clear the timer.
C - Both of the above.
D - None of the above.


Q 5 - Which of the following is the correct way to get an extension of a file?
Answer D

A - fs.extname('main.js')
B - path.extname('main.js')
C - os.extname('main.js')
D - None of the above.


Q 6 - net.isIP(input) returns 0 for invalid input.
answer true

A - true
B - false


Q 7 - Which of the following module is required to create a child process?
answer is B

A - process module
B - child_process module
C - child module
D - web module


Q 8 - A stream fires end event when there is no more data to read.
answer is A

A - true
B - false



# Submission
- Create 2 Answer files, one more Mongodb and other for NodeJS
- Send me your Github URL of your project in private direct message in slack