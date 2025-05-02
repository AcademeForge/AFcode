<html lang="en">
<meta name="google-site-verification" content="F1L0xfSoJ09Jp0SjvlmTnzkWK_fuYyhBw36QvRdDGwM" />
<!-- Moving Banner -->
<div style="width: 100%; background-color: #0a0a0a; color: white; padding: 10px 0; overflow: hidden; position: fixed; top: 0; left: 0; z-index: 10000;">
  <div class="scroll-text">
    After registering, please send your Name, School Name, School Address, and Payment Screenshot to our official Telegram account:
    <a href="https://t.me/AcademeforgeScholarsTest_AST" target="_blank" style="color: #00BFFF; font-weight: bold; text-decoration: underline;">t.me/AcademeforgeScholarsTest_AST</a>
  </div>

<style>
.scroll-text {
  display: inline-block;
  white-space: nowrap;
  animation: scroll-left 18s linear infinite;
  padding-left: 100%; /* Start closer to visible area */
}

@keyframes scroll-left {
  0% { transform: translateX(0%); }
  100% { transform: translateX(-100%); }
}
</style>

</div>
<!-- Logo -->
<div class="logo-container">
    <a href="https://ibb.co/23qH49sJ" target="_blank">
        <img src="https://i.ibb.co/k2KvC79Z/IMG-20250320-164334-559.jpg" alt="AcademeForge Logo">
    </a>
</div>

<style>
    /* Logo Styling */
    .logo-container {
        position: fixed;
        top: 120px; /* Adjust this to position it under the banner */
        Right: 10px; /* Positions the logo on the Right side */
        z-index: 9997;
    }

    .logo-container img {
        height: 40px; /* Reduced size */
        width: auto; 
        border-radius: 5px;
    }
</style>


  
  <meta charset="UTF-8">
  <title>AcademeForge Scholars Test Registration</title>
  <style>
    body { font-family: Arial, sans-serif; background: #00B4D8; padding: 20px; }
    form { max-width: 600px; margin: auto; background: #FF6B6B; padding: 20px; border-radius: 10px; }
    label { display: block; margin: 10px 0 5px; }
    input, select, textarea { width: 100%; padding: 8px; }
    .conditional { display: none; }
    button { margin-top: 20px; padding: 10px 20px; background: #00e5ff; color: white; border: none; border-radius: 5px; cursor: pointer; }
  </style>

<body>

  <h2>AcademeForge Scholars Test Registration</h2>

  <form id="registrationForm">
    
    <!-- Form Fields -->
    <label for="name">Full Name*</label>
    <input type="text" id="name" name="name" required>

    <label for="class">Class*</label>
    <select id="class" name="class" required>
      <option value="">Select Class</option>
      <option value="1">1</option>
      <option value="2">2</option>
      <option value="3">3</option>
      <option value="4">4</option>
      <option value="5">5</option>
      <option value="6">6</option>
      <option value="7">7</option>
      <option value="8">8</option>
      <option value="9">9</option>
      <option value="10">10</option>
    </select>

    <label for="Pincode">pincode*</label>
<input type="text" id="pincode" name="pincode" required>

    <label for="mode">Mode (Offline/Online)*</label>
    <select id="mode" name="mode" onchange="toggleOfflineFields()" required>
      <option value="">Select Mode</option>
      <option value="Offline">Offline</option>
      <option value="Online">Online</option>
    </select>

    
    <label for="mobile">Mobile Number*</label>
    <input type="tel" id="mobile" name="mobile" required pattern="[0-9]{10}">

    <label for="email">Email Address*</label>
    <input type="email" id="email" name="email" required>

    <label for="gender">Gender*</label>
    <select id="gender" name="gender" required>
      <option value="">Select Gender</option>
      <option value="Male">Male</option> <option value="Female">Female</option> <option value="Other">Other</option>
    </select>

    <label for="dob">Date of Birth*</label>
    <input type="date" id="dob" name="dob" required>
<!-- Payment Info before screenshot -->
    <label>
    <p><strong>Final Step : Pay ₹10 to UPI ID:</strong> <code>devrajkumar01@ybl</code> using any UPI app.</p>

   <!-- UPI Pay Button -->
    <a href="upi://pay?pa=devrajkumar01@ybl&pn=Devraj+Kumar&mc=0000&tid=1234567890&tr=1234567890&tn=Test+Payment&am=10&cu=INR" 
       target="_blank">
       <button type="button">Pay ₹10 Now</button>
    </a>
<button type="submit">Register Now</button>
  
   <script>
    document.getElementById("registrationForm").addEventListener("submit", function(e) {
      e.preventDefault();
      const form = e.target;
      const formData = new FormData(form);

      fetch("https://script.google.com/macros/s/AKfycbxKUHRKkUA8Mt42QGrYR07fDye-tcs9R6_qkCJsv8osOpyG_gus6_9Xa7AyhzNjx84SpQ/exec", {
        method: "POST",
        body: formData
      })
      .then(response => response.text())
      .then(result => {
        alert("Registration successful!");
        form.reset();
      })
      .catch(error => {
        alert("Error submitting form.");
        console.error(error);
      });
    });
  </script>
    
<!-- Telegram Button and Instructions -->
<div style="margin-top: 30px; background: #f9f9f9; padding: 20px; border-radius: 10px;">
  <h3>After Form Submission</h3>
  <p><strong>Important:</strong> Please send your <strong>payment screenshot</strong>, <strong>School Name</strong>, and <strong>School Address</strong> to our official Telegram handle:</p>
  <a href="https://t.me/AcademeforgeScholarsTest_AST" target="_blank">
    <button style="background-color: #0088cc;">Send Details via Telegram</button>
  </a>

 <p>Or you can email us at: <strong><a href="mailto:academeforge@gmail.com?subject=AST%20Registration%20Query&body=Hello%20Team%20AcademeForge,%0A%0AI%20have%20a%20query%20regarding%20the%20AcademeForge%20Scholars%20Test.%0A%0AThankYou,%0A%0Aacademeforge@gmail.com ♥️!">academeforge@gmail.com</a></strong></p>

</div>
 
<style>
  footer {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    background: #5E60CE; /* Violet blue */
    color: white;
    text-align: center;
    padding: 15px 10px;
    font-size: 14px;
    box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.3);
    z-index: 999;
  }

  footer .social-links a {
    color: white;
    text-decoration: none;
    margin: 0 8px;
    font-weight: bold;
  }

  footer .social-links a:hover {
    color: #F1FAFF;
    text-decoration: underline;
  }
</style>

<footer>
  <div class="social-links">
    <a href="https://www.youtube.com/@AcademeForgePro" target="_blank">YouTube</a> |
    <a href="https://www.instagram.com/academeforgee" target="_blank">Instagram</a> |
    <a href="https://t.me/addlist/CVX57k_dpG4wNGJl" target="_blank">Join Telegram</a>
  </div>
  <p>&copy; 2025 AcademeForge. All rights reserved.</p>
</footer>
