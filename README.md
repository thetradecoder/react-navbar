# react-navbar
We used bootstrap4 for this navbar (version 4.5.2)

Create a file in the components folder and name it

`navbar.component.js`

Then import the component in the relevant file
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
