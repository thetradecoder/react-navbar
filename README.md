# react-navbar
We used bootstrap4 for this navbar (version 4.5.2)

Create a file in the `components` folder and name it

`navbar.component.js`

Then use the following code in the `navbar.component.js` file and make necessary modification like brand-name, link-names, path 

```
import React from 'react';
import {Link} from "react-router-dom";
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap/dist/js/bootstrap.bundle';
import 'jquery/dist/jquery';

export default function Navbar(){
    return (
        <nav className="navbar navbar-expand-lg navbar-dark bg-dark">
            <div className="container-fluid">
                <div className="navbar-header">
                    <a href="/" className="navbar-brand">tradecoder</a>
                </div>
                    <button data-target="#main-menu" data-toggle="collapse" className="navbar-toggler">
                        <span className="navbar-toggler-icon"></span>
                    </button>
                    <div id="main-menu" className="collapse navbar-collapse">
                        <ul className="navbar-nav ml-auto">
                            <li className="nav-item"><Link to="/link-one/" className="nav-link">Link One</Link></li>
                            <li className="nav-item"><Link to="/link-two/" className="nav-link">Link Two</Link></li>
                            <li className="nav-item"><Link to="/link-three/" className="nav-link">Link Three</Link></li>
                        </ul>
                    </div>       
            </div>
        </nav>
    );
}
```

Then import the Navbar component in the relevant file.

Sample import of Navbar component to `App.js` file

```
import React from 'react';
import {BrowserRouter as Router, Route} from "react-router-dom";
import Counter from './components/counter.component';
import Navbar from './components/navbar.component.js';
// import AotherComonent from './components/another-component.component.js';
// import ThreeComponent from './components/three-component.comonent.js';

function App() { 
  return (    
    <Router>
      <Navbar />
   //   <Route path="/" exact component = {AnotherComponent} />
   //   <Route path="/link-three" component = {ThreeComponent} />
    </Router>
  );
}

export default App;

```
