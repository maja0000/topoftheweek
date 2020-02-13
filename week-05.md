#  week5 recap 🧠

Wednesday (12.02.2020)



## Pure React (create react app without Babel)

### 1. Create src folder
### 2. Create html skeleton 
### 3. Create root div
        
    (<div id="root"> Not rendered yet </div>)
          
### 4. Add React and ReactDOM
             
    <script src="https://cdnjs.cloudflare.com/ajax/libs/react/16.12.0/umd/react.production.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/16.11.0/umd/react-dom.production.min.js"></script>

  
### 5. Check if React is present :)
- console.log(React) 
- console.log(ReactDOM)


### 6. create (functional) component 
(param - element, tag with id and value)
                            
    function App() {
    return React.createElement('div', { className: 'hello' },
    )};
                       
                       
### 7. element inside another element - h1 inside of <div> tag 

    function App() {
    return React.createElement('div', { className: 'hello' },
    React.createElement('h1', {}, "Hello World")
     );
     }


### 8. Render App component inside of root element    
              
    ReactDOM.render(
    react.createElement(App), document.getElementById('root'));

### 9. create components in seperate files (multiple elements in an array)

    function Title(props) {
    return React.createElement('div', { className: "hello" }, [
     React.createElement('h1', {}, "Article Title"),
    React.createElement('h2', {}, "Subtitle"),
    React.createElement('p', {}, "Lorem ipsuma, minus similique sint mollitia a cumque consequatur illo minima?                    Similique animi iste labore."),
     ])
     };

### 10. import seperate sheets.js into index.html 
                
    <script src="Title.js"></script>
    <script src="App.js"></script>
                  
                              
## React Router 
(https://reacttraining.com/react-router/web/guides/quick-start)

- render components dynamically in a Single Page Application

How to create :
1) install 

        npm/yarn install react-router-dom
        
2) import 

        import { BrowserRouter as router, Switch} from "react-router-dom";

3) wrap all components in App.js in <Router/> component
 add <Switch>, looks through its children <Route>s and renders the first one that matches the current URL.

(name of the path is whatever u want)


        <Router>
      <Navbar />
      <Switch>
        <Route exact path="/">
          <Homepage />
        </Route>
        <Route path="/about-us">
          <AboutUs />
        </Route>
        <Route path="/contact">
          <Contact />
        </Route>
      </Switch>
    </Router>

4)  OR 

        <Route exact path="/" component={Homepage} />
        <Route path="/aboutUs" component={AboutUs} />
        <Route exact path="/contact" component={contact} />


5) import links 

        import { Link } from 'react-router-dom';

6) add link inside <li>

         <h3><Link to="/">My super Company</Link></h3>

         <li className="nav-items"><Link to="/About">Infos</Link></li>



#### Navlink 

        import { Navlink } from 'react-router-dom';

Change css when link active 

       <li className="nav-items"><NavLink activeClassName="active" to="About">About</NavLink></li>


# HTTP
- Hypertext Transfer Protocol is an application-layer protocol for transmitting hypermedia documents, such as HTML.

<img width="563" alt="Screenshot 2020-02-13 at 08 43 15" src="https://user-images.githubusercontent.com/52657665/74412167-1de8f780-4e3d-11ea-94c4-8d6012439163.png">

Request methods :

1) GET - The GET method requests a representation of the specified resource. Requests using GET should only retrieve data.

2) POST - The POST method is used to submit an entity to the specified resource, often causing a change in state or side effects on the server

3) DELETE - The DELETE method deletes the specified resource.

4) CONNECT - The CONNECT method establishes a tunnel to the server identified by the target resource.


# PROMISE 
- The Promise object represents the eventual completion (or failure) of an asynchronous operation, and its resulting value.


![promises](https://user-images.githubusercontent.com/52657665/74412658-34dc1980-4e3e-11ea-8750-33d89f5a55c4.png)

Working with promises : 
1) create a promise instance using Promise() Constructor
2) Define what should happen when promise is fulfilled or rejected
3) Consume the value of the fulfilled promise or provide ar provide a rejection reason for a rejected promise, 

        const myNewPromise = new Promise ((resolve, reject)=> {
        setTimeOut (()=>{
        resolve ("Your order is ready!")
        },3000);
        });


        myNewPromise.then(val => console.log(val))
        
(returns fullfiled value (whatever passed into resolve is avalible here ))


Promise.all() -bmethod returns a single Promise that fulfills when all of the promises passed as an iterable have been fulfilled ( usefull when program needs to wait more than one promise to resolve ). It rejects with the reason of the first promise 


## Functional programming -  form of programming in which you can pass functions as parameters to other functions and also return them as values.

First-Class Functions (first-class citizens)


Thursday (13.02.2020)

Higher order function - functions that operate on other functions, either by taking them as arguments or by returning them. (function that receives a function as an argument or returns the function as output)

For example :
Array.prototype.map, 
Array.prototype.filter 
Array.prototype.reduce 












Friday(14.02.2020)
