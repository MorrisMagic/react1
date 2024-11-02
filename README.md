// product.js
const product = {
  name: "Sample Product",
  price: "$29.99",
  description: "This is a great product!",
  image: "https://via.placeholder.com/150" 
};
export default product;


import React from "react";
import product from "./product";

function Name() {
  return <h2>{product.name}</h2>;
}

export default Name;

import React from "react";
import product from "./product";

function Price() {
  return <p>{product.price}</p>;
}

export default Price;

import React from "react";
import product from "./product";

function Description() {
  return <p>{product.description}</p>;
}

export default Description;

import React from "react";
import product from "./product";

function Image() {
  return <img src={product.image} alt={product.name} />;
}

export default Image;

import React from "react";
import Name from "./Name";
import Price from "./Price";
import Description from "./Description";
import Image from "./Image";
import { Card } from "react-bootstrap";
import "bootstrap/dist/css/bootstrap.min.css";

const firstName = "Youssef"; // Your name here, or leave as an empty string to test

function App() {
  return (
    <div className="App">
      <Card style={{ width: "18rem" }}>
        <Card.Body>
          <Image />
          <Name />
          <Price />
          <Description />
        </Card.Body>
      </Card>
      <div>
        {firstName ? <p>Hello, {firstName}!</p> : <p>Hello, there!</p>}
        {firstName && <img src="https://via.placeholder.com/50" alt="greeting" />}
      </div>
    </div>
  );
}

export default App;
