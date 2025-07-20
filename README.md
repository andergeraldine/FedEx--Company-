# FedEx--Company
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>FedEx Delivery Company Tracker</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <div class="header" style="text-align:center; margin-bottom:20px;">
      <img src="YOUR_UPLOADED_LOGO_URL" alt="FedEx Logo">
      <h2>FedEx Delivery Company</h2>
    </div>

    <p style="text-align:center;">Enter your tracking number to view shipment status:</p>
    <input type="text" id="trackingNumber" placeholder="e.g. 1234567890">
    <button onclick="go()">Track Now</button>

    <div style="text-align:center; margin-top:30px;">
      <h4>Scan QR Code to Access Tracker</h4>
      <img src="https://api.qrserver.com/v1/create-qr-code/?data=https://fedex-delivery-company.glitch.me&size=200x200" alt="QR Code to Tracker" style="margin-top:10px;">
    </div>
  </div>

  <script>
    function go() {
      const num = document.getElementById('trackingNumber').value.trim();
      if (!num) return alert('Please enter a tracking number.');
      window.location.href = `tracking.html?num=${encodeURIComponent(num)}`;
    }
  </script>
</body>
</html>
