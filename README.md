# unit-2-notes
| CRUD Action | RESTful Action | HTTP Method | Definition |
| ----------- | -------------- | ----------- | ------------------------ |
| | `new` | `GET` | Show a form to create a new item |
| Create | `create` | `POST` | Add a new item to the database |
| Read | `index` | `GET` | Show all items |
| Read | `show` | `GET` | Show one specific item |
|  | `edit` | `GET` | Show a form to edit an existing item |
| Update | `update` | `PUT` | Save changes to an existing item |
| Delete | `delete` | `DELETE` | Remove an item from the database |



## SETUP

-create a directory
-create server file `touch server.js`
-initialize a node project with `npm init -y`
-install express and morgan`npm i express morgan, `

### Write Server Boilerplate 
server.js
```js
//bring express into our serves
const express=require('express')
 const age =req.query.age
//actually use express
const app = express()


app.use(morgan('dev'))

app.listen(3000,function(){
console.log('Listening on port 3000');
    
})
```
Run the serves with `nodemon serves.js`
<img width="371" height="151" alt="image" src="https://github.com/user-attachments/assets/a2689433-175d-4972-909c-72f95e6e6193" />


 Navigate to `http://localhost:3000`to view our server.
 Use `Ctrl + c`to stope the serves in the terminal.


 ```js
app.get('/test',function(ress,reqq){
    ress.send('<h1>this is test</h1>')

})
 ```

### Using request parameters
```js
app.get('/greet/:name', function(req, res){
    res.send(`hello ${req.params.name}`)
    console.log(req.params.name)

})
```
Navigate to
`http:localhost:3000/2490`

<img width="355" height="106" alt="image" src="https://github.com/user-attachments/assets/0e852f8a-7edf-4269-bb63-80b6990b5ac9" />
