---
title: "React Router V6"
date: 2022-03-20T16:55:33+01:00
draft: true
categories: [development]
ShowToc: true
---

## React Router (v6)
https://reactrouter.com/  

React routing is needed to have different pages but still be able to navigate between different components/pages.


### Install react router v.6 (in your project folder)
```
npm install react-router-dom@6 
```

### Activate Routes in index.js
To activate routes in your project, you need to wrap App component with the BrowserRouter in index.js, like this:
```java
import ReactDOM from 'react-dom';
import { BrowserRouter } from 'react-router-dom';
 
import './index.css';
import App from './App';
 
ReactDOM.render(<BrowserRouter><App /></BrowserRouter>, document.getElementById('root'));
```

### Import react route in your module (App.js for example)
```java
import { Route } from 'react-router-dom';
```

### Add your first route
For example in App.js, you could now add a route. 
- Add a new component called Home.js (for example)
- Add a route to Home.js (see code below)
Let's say there is a page called Home.js. Then we could set up a route to Home like this:  

```java
import { Route } from 'react-router-dom';
import Welcome from './components/Home';
 
 
function App() {
 return (
   <div>
     <Route path="/home">
       <Home />
     </Route>
   </div>
 );
}
 
export default App;
```


