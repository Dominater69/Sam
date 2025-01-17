<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Samar's Form Submission</title>
<style>
  body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
  }

  .container {
    text-align: center;
    background-color: #fff;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
    max-width: 600px;
    width: 100%;
    box-sizing: border-box;
  }

  h1 {
    margin-bottom: 20px;
    color: #333;
  }

  .form-group {
    margin-bottom: 20px;
    text-align: left;
  }

  .form-group label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #555;
  }

  .form-group input[type="text"],
  .form-group input[type="tel"],
  .form-group input[type="email"],
  .form-group textarea {
    width: calc(100% - 20px);
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 16px;
    box-sizing: border-box;
  }

  .form-group textarea {
    height: 80px;
  }

  .form-group button {
    background-color: #4CAF50;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
  }

  .form-group button:hover {
    background-color: #45a049;
  }

  .thank-you-message {
    display: none;
    margin-top: 20px;
    font-size: 24px;
    color: #4CAF50;
  }
</style>
</head>
<body>

<div class="container">
  <h1>Welcome to Samar's Form Submission</h1>
  
  <!-- Submission Form -->
  <form id="submissionForm">
    <div class="form-group">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" placeholder="Enter your name" required>
    </div>
    <div class="form-group">
      <label for="phone">Phone Number:</label>
      <input type="tel" id="phone" name="phone" placeholder="Enter your phone number" required>
    </div>
    <div class="form-group">
      <label for="address">Address:</label>
      <textarea id="address" name="address" placeholder="Enter your address" required></textarea>
    </div>
    <div class="form-group">
      <label for="city">City:</label>
      <input type="text" id="city" name="city" placeholder="Enter your city" required>
    </div>
    <div class="form-group">
      <button type="submit">Submit</button>
    </div>
  </form>
  
  <!-- Thank You Message -->
  <div id="thankYouMessage" class="thank-you-message">
    Thank you for using Samar's JS Program!
  </div>
</div>

<script>
  // Form submission event listener
  document.getElementById('submissionForm').addEventListener('submit', function(event) {
    event.preventDefault(); // Prevent default form submission
    
    // Get form values
    var name = document.getElementById('name').value;
    var phone = document.getElementById('phone').value;
    var address = document.getElementById('address').value;
    var city = document.getElementById('city').value;
    
    // Display thank you message
    document.getElementById('submissionForm').style.display = 'none';
    document.getElementById('thankYouMessage').style.display = 'block';
  });
</script>

</body>
</html>
