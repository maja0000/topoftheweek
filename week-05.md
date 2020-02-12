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
                  
                              




Thursday (13.02.2020)
Friday(14.02.2020)
