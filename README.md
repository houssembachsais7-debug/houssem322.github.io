<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Order Product</title>

<style>
/* خلفية الصفحة */
body {
  font-family: Arial, sans-serif;
  background: linear-gradient(to bottom, #fdfbfb, #ebedee);
  margin: 0;
  padding: 0;
}

/* صندوق الطلب */
.container {
  width: 90%;
  max-width: 500px;
  margin: 40px auto;
  background: white;
  padding: 30px;
  border-radius: 15px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.2);
}

/* العنوان */
h1 {
  text-align: center;
  color: #333;
  margin-bottom: 20px;
}

/* الصورة */
.product-image {
  width: 100%;
  border-radius: 10px;
  margin-bottom: 15px;
}

/* النصوص */
p {
  text-align: center;
  font-size: 16px;
  color: #555;
  margin-bottom: 20px;
}

/* الحقول */
input, select {
  width: 100%;
  padding: 12px;
  margin-top: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  font-size: 15px;
}

/* الزر */
button {
  width: 100%;
  padding: 15px;
  margin-top: 20px;
  font-size: 18px;
  color: white;
  border: none;
  border-radius: 10px;
  background: linear-gradient(90deg, #ff7e5f, #feb47b);
  cursor: pointer;
  transition: 0.3s;
}
button:hover {
  opacity: 0.9;
}
</style>

</head>
<body>

<div class="container">

<h1>Order Your Product</h1>

<img src="product1.jpg" alt="Product" class="product-image">

<p>Check out this amazing product! Fill the form below to order.</p>

<label>Name</label>
<input type="text" placeholder="Your Name">

<label>Phone</label>
<input type="text" placeholder="Phone Number">

<label>State</label>
<select>
  <option>Algiers</option>
  <option>Blida</option>
  <option>Oran</option>
  <option>Constantine</option>
</select>

<label>Address</label>
<input type="text" placeholder="Your Address">

<label>Quantity</label>
<select>
  <option>1</option>
  <option>2</option>
  <option>3</option>
</select>

<button>Confirm Order</button>

</div>

</body>
</html>
