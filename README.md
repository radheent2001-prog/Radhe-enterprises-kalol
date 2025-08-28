<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Radhe Enterprises - Order Management</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 20px; background: #f4f4f4; }
    h1 { text-align: center; color: #2c3e50; }
    .container { max-width: 1100px; margin: auto; background: #fff; padding: 20px; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    form { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 20px; }
    input, select, button { padding: 10px; border: 1px solid #ccc; border-radius: 5px; }
    button { background: #2ecc71; color: #fff; cursor: pointer; }
    button:hover { background: #27ae60; }
    table { width: 100%; border-collapse: collapse; margin-top: 20px; }
    th, td { border: 1px solid #ddd; padding: 10px; text-align: center; }
    th { background: #3498db; color: white; cursor: pointer; }
    .delete-btn { background: red; color: white; border: none; padding: 5px 10px; cursor: pointer; border-radius: 5px; }
    .delete-btn:hover { background: darkred; }
    #search { width: 100%; margin-top: 10px; }
    .section { margin-top: 40px; }
  </style>
</head>
<body>
  <div class="container">
    <h1>📦 Radhe Enterprises - Order Management</h1>
    
    <!-- Add Party -->
    <h2>➕ Add New Party</h2>
    <form id="partyForm">
      <input type="text" id="partyName" placeholder="Party Name" required>
      <button type="submit">Save Party</button>
    </form>

    <!-- Add Product -->
    <h2>➕ Add New Product</h2>
    <form id="productForm">
      <input type="text" id="productName" placeholder="Product Name" required>
      <button type="submit">Save Product</button>
    </form>

    <!-- Add Order -->
    <h2>➕ Add New Order</h2>
    <form id="orderForm">
      <select id="partySelect" required>
        <option value="">-- Select Party --</option>
      </select>
      <select id="productSelect" required>
        <option value="">-- Select Product --</option>
      </select>
      <input type="text" id="orderId" placeholder="Order ID" required>
      <input type="number" id="quantity" placeholder="Quantity" required>
      <input type="number" id="price" placeholder="Price per unit" required>
      <input type="date" id="orderDate" required>
      <select id="paymentStatus" required>
        <option value="Pending">Pending</option>
        <option value="Paid">Paid</option>
      </select>
      <input type="text" id="notes" placeholder="Notes / Remarks">
      <button type="submit">Save Order</button>
    </form>

    <input type="text" id="search" placeholder="🔍 Search Orders...">

    <!-- Orders Table -->
    <table id="orderTable">
      <thead>
        <tr>
          <th onclick="sortTable(0)">Party</th>
          <th onclick="sortTable(1)">Order ID</th>
          <th onclick="sortTable(2)">Product</th>
          <th onclick="sortTable(3)">Quantity</th>
          <th onclick="sortTable(4)">Price</th>
          <th onclick="sortTable(5)">Total</th>
          <th onclick="sortTable(6)">Date</th>
          <th onclick="sortTable(7)">Payment</th>
          <th>Notes</th>
          <th>Delete</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>

    <!-- Reports -->
    <div class
