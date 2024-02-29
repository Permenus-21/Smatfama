# Smatfama
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Agriconnect - Your Agricultural Companion</title>
    <style>
        body {
            margin: 0;
            font-family: prime 'Courier New', Courier, monospace;
        }

        header {
            background-color: #4CAF50;
            padding: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        #logo {
            color: #fff;
            font-size: 28px;
            font-weight: bold;
            text-decoration: none;
        }

        nav {
            display: flex;
        }

        nav a {
            color: #fff;
            letter-spacing: 1px;
            text-decoration: none;
            padding: 10px;
            margin-left: 20px;
            font-size: 18px;
            font-weight: bold;
            transition: color 0.3s ease-in-out;
            border-radius: 5px;
            border: 1px solid #fff;
            cursor: pointer;
            text-transform: uppercase;
            background-color: #4CAF50;
            color: #fff;

        }

        nav a:hover {
            color: #d9ff00; /* Change the color on hover */
        }

        .mission-vision-container {
            background-color: #f0f0f0;
            padding: 30px;
            margin: 20px;
            border-radius: 10px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease-in-out;
            width: 400px;
            height: 400px;
            margin: 20px;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
        }

        h2 {
            color: #4CAF50;
            font-size: 28px;
            font-weight: bold;
            text-decoration: none;
            text-transform: uppercase;
            margin-bottom: 20px;
            margin-top: 20px;
            letter-spacing: 1px;
            transition: color 0.3s ease-in-out;
            border-radius: 5px;
            border: 1px solid #fff;
        }

        p {
            color: #333;
            font-size: 18px;
            font-weight: bold;
            text-decoration: none;
            text-transform: uppercase;
            margin-bottom: 20px;
            margin-top: 20px;
            letter-spacing: 1px;

        }

          /* Button Styles */
          .get-started-button {
            display: inline-block;
            padding: 10px 20px;
            font-size: 16px;
            align-items: center;
            text-align: center;
            text-decoration: none;
            background-color: #4CAF50;
            color: #fff;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease-in-out;
        }

        .get-started-button:hover {
            background-color: #45a049; /* Darker color on hover */
            color: #fff;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease-in-out;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease-in-out;

        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
        }

        .modal-content {
            background-color: #fff;
            padding: 20px;
            margin: 10% auto;
            width: 80%;
            border-radius: 5px;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        
        form {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        input {
            margin: 10px;
            padding: 10px;
            width: 100%;
            box-sizing: border-box;
            border: 1px solid #ccc;
            border-radius: 5px;
            outline: none;
            font-size: 16px;
            transition: border-color 0.3s ease-in-out;
            background-color: #fff;
        }

        .create-account {
            margin-top: 20px;
            margin-bottom: 20px;
            padding: 10px;

        }

        .create-account {
            margin-top: 20px;
        }

        /* Create Account Form Styles */
        .create-account-form {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;        
        }

        .error-message {
            color: red;
            margin: 5px 0;
            font-size: 12px;
            text-align: center;
            display: none;
        }
    </style>
</head>
<body>
    <header>
        <div id="logo">Agriconnect</div>
        <nav>
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Vet Services</a>
            <a href="#">Lab Services</a>
            <a href="#">Contacts</a>
        </nav>
    </header>

    <!-<div class="mission-vision-container">
        <h2>Mission</h2>
        <p>To empower farmers with cutting-edge technology and information, fostering sustainable agriculture and ensuring food security.</p>
        
        <h2>Vision</h2>
        <p>To be the leading agricultural platform, connecting farmers with innovative solutions, promoting environmental stewardship, and transforming the future of farming globally.</p>
    </div>


    <a href="#" class="get-started-button" onclick="openModal()">GET STARTED</a>

    <!-- Modal -->
    <div id="myModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <!-- Your login form goes here -->
            <h2>Login</h2>
            <form>
                <input type="email" placeholder="Email" required>
                <input type="password" placeholder="Password" required>
                <button type="submit">Login</button>
            </form>
            <p class="create-account">Don't have an account? <a href="#">Create one</a></p>
        </div>

        <div id="createAccountForm" style="display: none;">
            <h2>Create Account</h2>
            <form class="create-account-form" onsubmit="return validateCreateAccount()">
                <input type="email" id="createEmail" placeholder="Email" required>
                <input type="password" id="createPassword" placeholder="Password" required>
                <input type="password" id="confirmPassword" placeholder="Confirm Password" required>
                <button type="submit">Create Account</button>
            </form>
        </div>
    </div>

    <script>
         // Modal functionality
         function openModal() {
            document.getElementById("myModal").style.display = "block";
        }

        function closeModal() {
            document.getElementById("myModal").style.display = "none";
            // Reset create account form on modal close
            document.getElementById("createAccountForm").style.display = "none";
            document.getElementById("createEmail").value = "";
            document.getElementById("createPassword").value = "";
            document.getElementById("confirmPassword").value = "";
        }

        // Show create account form
        function showCreateAccountForm() {
            document.getElementById("createAccountForm").style.display = "block";
        }

        // Validate create account form
        function validateCreateAccount() {
            var createEmail = document.getElementById("createEmail").value;
            var createPassword = document.getElementById("createPassword").value;
            var confirmPassword = document.getElementById("confirmPassword").value;

            // Basic email validation
            var emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(createEmail)) {
                alert("Invalid email address");
                return false;
            }

            // Password and Confirm Password validation
            if (createPassword.length < 8) {
                alert("Password must be at least 8 characters");
                return false;
            }

            if (createPassword !== confirmPassword) {
                alert("Passwords do not match");
                return false;
            }

            // Success - You can proceed with form submission
            alert("Account created successfully!");
            closeModal();
        }
    </script>
</body>
</html>
