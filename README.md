About.jsx
import React from 'react'
import { NavLink } from 'react-router-dom';
import b from "./1st_pic_pjm.jpg";
import smile from "./pic2_pjm.jpg";
const About =() => {
   return (
     <> <div style={{ backgroundImage: `url(${b})` }}>
     <h1 className='text-center'>About us</h1>
   <center>  <h5>Project management is very important for the organization to govern the project. A team leader needs to understand project lifecycle, risk and risk management in order to create the strategy for the project to be successful. Moreover, applying the proper tool during the process duration estimation by considering the iron triangle can lead to reach the goal of the project. </h5> </center>

<center><img src={smile} alt="..." className="col-2 mx-auto"/></center>
     </div>

 </>  
  )
}

export default About;


login.jsx
import { NavLink } from 'react-router-dom';
import React, { useState } from 'react';
import { makeStyles } from '@material-ui/core';
import TextField from '@material-ui/core/TextField';
import Button from '@material-ui/core/Button';
import b from "./1st_pic_pjm.jpg";
import pic from "./pic3_pjm (2).jpg";

const useStyles = makeStyles(theme => ({
  root: {
   
    display: 'flex',
    flexDirection: 'column',
    justifyContent: 'center',
    alignItems: 'center',
    padding: theme.spacing(2),

    '& .MuiTextField-root': {
      margin: theme.spacing(1),
      width: '300px',
    },
    '& .MuiButtonBase-root': {
      margin: theme.spacing(2),
    },
  },
}));

const Login= ({ handleClose }) => {
  const classes = useStyles();
  // create state variables for each input
  const [firstName, setFirstName] = useState('');
  const [lastName, setLastName] = useState('');
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');

  const handleSubmit = e => {
    e.preventDefault();
    console.log(firstName, lastName, email, password);
    handleClose();
  };

  return (
   
    <div style={{ backgroundImage: `url(${b})` }}>
    
    <form className={classes.root} onSubmit={handleSubmit}>
     
      <TextField
        label="FirstName"
        variant="filled"
        type="firstName"
        required
        value={firstName}
        onChange={e => setFirstName(e.target.value)}
      />
      <TextField
        label="LastName"
        variant="filled"
        type="lastName"
        required
        value={lastName}
        onChange={e => setLastName(e.target.value)}
      />
      <TextField
        label="Email"
        variant="filled"
        type="email"
        required
        value={email}
        onChange={e => setEmail(e.target.value)}
      />
      <TextField
        label="Password"
        variant="filled"
        type="password"
        required
        value={password}
        onChange={e => setPassword(e.target.value)}
      />
      <div>
        <Button variant="contained" onClick={handleClose}>
          Cancel
        </Button>
        <Button type="submit" variant="contained" color="primary">
          Login
        </Button>
      </div>
      
      
    </form>
    <center><img src={pic} alt="..." className="col-2 mx-auto"/></center>
   </div>
    
     
  );
};

export default Login;

signup.jsx
import { NavLink } from 'react-router-dom';
import React, { useState } from 'react';
import { makeStyles } from '@material-ui/core';
import TextField from '@material-ui/core/TextField';
import Button from '@material-ui/core/Button';
import b from "./1st_pic_pjm.jpg";
import s from "./pic4_pjm.png";
const useStyles = makeStyles(theme => ({
  root: {
   
    display: 'flex',
    flexDirection: 'column',
    justifyContent: 'center',
    alignItems: 'center',
    padding: theme.spacing(2),

    '& .MuiTextField-root': {
      margin: theme.spacing(1),
      width: '300px',
    },
    '& .MuiButtonBase-root': {
      margin: theme.spacing(2),
    },
  },
}));

const Signup= ({ handleClose }) => {
  const classes = useStyles();
  // create state variables for each input
  const [firstName, setFirstName] = useState('');
  const [lastName, setLastName] = useState('');
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');

  const handleSubmit = e => {
    e.preventDefault();
    console.log(firstName, lastName, email, password);
    handleClose();
  };

  return (
   
    <div style={{ backgroundImage: `url(${b})` }}>
    
    <form className={classes.root} onSubmit={handleSubmit}>
      
      <TextField
        label="First Name"
        variant="filled"
        required
        value={firstName}
        onChange={e => setFirstName(e.target.value)}
      />
      <TextField
        label="Last Name"
        variant="filled"
        required
        value={lastName}
        onChange={e => setLastName(e.target.value)}
      />
      <TextField
        label="Email"
        variant="filled"
        type="email"
        required
        value={email}
        onChange={e => setEmail(e.target.value)}
      />
      <TextField
        label="Password"
        variant="filled"
        type="password"
        required
        value={password}
        onChange={e => setPassword(e.target.value)}
      />
      <div>
        <Button variant="contained" onClick={handleClose}>
          Cancel
        </Button>
        <Button type="submit" variant="contained" color="black">
          Signup
        </Button>
      </div>
 
      
    </form>
    <center><img src={s} alt="..." className="col-2 mx-auto"/></center>
   </div>
   

    
     
  );
};

export default Signup;

services.jsx
import React from 'react'
import Common from './Common';
import b from "./1st_pic_pjm.jpg";
import s from "./pic5_pjm.jpg";

const Service =() => {
   return (
     <>  <div style={{ backgroundImage: `url(${b})` }}>
    <center> <div className="my-10">
       <h1 className='text-left'>Our Services</h1>
       </div>
       <div className="container-fulid nav-bg">
       <div className="row">
        <div className="col-30 mux-auto">
          <div className='row'>
            <div className='col-md-5 mx-auto'>
            <div class="card">

  <div class="card-body">
    <h5 class="card-title">PROJECT MANAGEMENT</h5>
    <p class="card-text">Project management services specialize in planning, coordinating, and executing projects according to specific requirements and constraints. They perform some or all of the activities related to project work, from conceptualization to completion. The end goal is to complete the project on time and within budget. </p>
    <a href="#" class="btn btn-primary">View Services</a>
  </div>
 
</div>

<div class="card">

  
</div> 
            </div>
          </div>
        </div>
        </div>
        </div></center>
       <br/> <center><img src={s} alt="..." className="col-2 mx-auto"/></center>  
        </div>
     </>
   )
}

export default Service;

contact.jsx
import React, { useState } from 'react'
import b from "./1st_pic_pjm.jpg";


const Contact =() => {
  
  
   return (
     <>
      <div style={{ backgroundImage: `url(${b})` }}>
     <div className="my-10"> 
     <h1 className="text-center">Contact Us</h1>
     <div className="container contac_div">
       <div className="row">
       <div className="col-mod-6 col-10 mx-auto">
         <form>
         <div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Full Name</label>
  <input type="text" class="form-control" id="exampleFormControlInput1"  placeholder=""/>
</div>
<div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">User Name</label>
  <input type="text" class="form-control" id="exampleFormControlInput1"  placeholder=""/>
</div>
<div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Mobile number</label>
  <input type="Numnber" class="form-control" id="exampleFormControlInput1"   onChange={InputEvent} placeholder=""/>
</div>
      
         <div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Email address</label>
  <input type="email" class="form-control" id="exampleFormControlInput1"  onChange={InputEvent} placeholder="name@example.com"/>
</div>
<div class="mb-3">
  <label for="exampleFormControlTextarea1" class="form-label">Queries</label>
  <textarea class="form-control" id="exampleFormControlTextarea1" rows="5"></textarea>
</div>
<div class="col-12">
    <button class="btn btn-primary" type="submit">Submit</button>
  </div>
         </form>
          </div>
         
       
       </div>

     </div>
     
     </div>
     </div>
     </>
   )
}

export default Contact;

footer.jsx

import b from "./1st_pic_pjm.jpg";
const Footer=()=>{
    return(
        <>
        <footer className= "bg-light text-center">
        <div className="">
            <p><div style={{ backgroundImage: `url(${b})` }}>
                PROJECT MANAGEMENT SYSTEM: PJM-385
              <br /> 
              This website is made according to the project given by KL university.
           </div> </p>
</div>
        </footer>
       
        </>
    )
}
export default Footer;

common.jsx

import React from 'react'
import { NavLink } from 'react-router-dom';
import b from "./1st_pic_pjm.jpg";
import web from "./pjs_pic.png";
import web2 from "./pic6_pjm.jpg";
import web4 from "./pic7_pjm.png";
import web5 from "./pic8_pjm.png";
const Common =(props) => {
   return (
     <>
        <div style={{ backgroundImage: `url(${b})` }}>
       
      <section id="header" className="" >
      <div className="container-fluid ">
      <div className='row'>
          <div className="col-100 mx-auto">
           
        <div className="col-md-8 pt-5 pt-lg-0 order-2 order-lg-1">
         <center> <p> 
            {props.name}
             <strong className="bramd-name">
             
             <h5><br/>Project Management is used as a tool to discipline all resource involved in the project to achieve the goals of the project. The objective of this paper is to indicate how project management plays an importance role to make the project succeed. It also points out the risk and risk management, which is important for the project manager to identify the risk and plan the strategy for it.
</h5>


 
 </strong>
          </p> </center>
          <center><img src={web} alt="..." className="col-6 mx-auto"/></center>
         
          <h5 className="my-10">
          <h3><b>Background of Project Management</b></h3>


   <br/>Project management is like a series of actions added to a process of getting things
done on a project by working with project team members to reach project
schedule, cost and technical performance objectives. Definitely we could say that
project management is a carefully planned and organized effort to accomplish a
specific one-time objective. It doesn‟t matter if it is for constructing a building or
implementing a major new computer system. <br/>
   <br/>RISK CATEGORIZING<br/>
   <img src={web2} alt="..." className="col-2 mx-auto"/>
   <br/>Risk occurs when the organization operates in the face of uncertainty, constrained by capability and cost. The project manager or team project needs to find the dimension that causes the risk. Risk management is usually defined as a set of principles and practices aimed at identifying, analyzing and handling risk factors to improve the chances of achieving a successful project outcome and/or avoid project failure.

Risk and risk management are also important because IT projects (including software projects) can be vehicles of delivering IT-enabled organizational change, so achieving business objectives can be critically dependent upon their success.<br/>
   <br/><b> PROJECT SPECIFICATION</b>
   <img src={web4} alt="..." className="col-2 mx-auto"/>
   <br/>Think of the project spec as a blueprint for your project. It should give a full outline of the project scope, deliverables and deadlines. The project specification explains what each part of the website is going to do, and why.<br/>
   <br/><b>ANALYSIS/DESIGN</b>
   <img src={web5} alt="..." className="col-2 mx-auto"/>
   <br/>The purpose of the Analysis Phase is to formulate and formalize the system's requirements. This is accomplished by establishing what the system is to do, according to the requirements and expectations of the system's end users.<br/>
</h5>
          <div classNamemt="my-10">
           <button><NavLink  to={props.visit} className="btn-get-started" to="/sinup"> 
             <h6> FOR MORE DETAILS</h6> 
            </NavLink></button> 
          </div>
        </div>
       </div>
       </div>
       <div className="col-lg-6 order-1 or order-lg-2 header-img">
        </div>
       </div>
      </section>
     </div>
     
     </>
   )
}

export default Common;

Navbar.js

import React from 'react'
import { NavLink } from 'react-router-dom';
import b from "./1st_pic_pjm.jpg";
import web from "./pic2_pjm.jpg";



const Navbar =() => {
   return (
     <> 
     <div style={{ backgroundImage: 'url({b})' }}></div>
    <div class="collapse" id="navbarToggleExternalContent">
  <div class="bg-secondary p-3">
    <h1 class="text-black h4">PROJECT MANAGEMENT SYSTEM (PJM)</h1>
    <span class="text-muted"></span>
  </div>
  <ul className="navbar navbar-light" >
        <li className="nav-item">
          <NavLink activeClassName='menu_active ' className="nav-link active" aria-current="page" to="/Home">Home</NavLink>
        </li>
        <li className="nav-item">
          <NavLink ActiveClassname='menu_active' className="nav-link" to="/Login">Login</NavLink>
        </li>
        <li className="nav-item">
        <NavLink ActiveClassname='menu_active' className="nav-link" to="/Sinup">Signup </NavLink>
        </li>
        
        <li className="nav-item">
          <NavLink ActiveClassname='menu_active' className="nav-link" to="/Service">Services </NavLink>
        </li>
        <li className="nav-item">
        <NavLink ActiveClassname='menu_active' className="nav-link" to="/Contact">Contact</NavLink>
        </li>
        <li className="nav-item">
      
        <NavLink ActiveClassname='menu_active' className="nav-link" to="/about">About </NavLink>
        </li>
        
      </ul>
</div>
<nav class="navbar navbar-light bg-light">
  <div class="container-fluid">
  <div>
    <a class="pic2_pjm.jpg" href="#">
      <img src="/docs/5.0/assets/brand/bootstrap-logo.svg" alt="" width="70" height="50" class="d-inline-block align-text-top"/>
      PROJECT MANAGEMENT SYSTEM(PJM)
    </a>
    </div>
  </div>
</nav>
<nav class="navbar navbar-dark bg-dark">
  <div class="container-fluid">
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarToggleExternalContent" aria-controls="navbarToggleExternalContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
  </div>
</nav>
     </>
   )
}

export default Navbar;
