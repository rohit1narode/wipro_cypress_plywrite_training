<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Registration Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 50px;
        }
        form {
            max-width: 400px;
            margin: 0 auto;
        }
        label {
            display: block;
            margin-bottom: 8px;
        }
        input, button {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <h1>Student Registration Form</h1>
    <form id="studentForm">
        <label for="firstName">First Name</label>
        <input type="text" id="firstName" name="firstName" required>
        <label for="lastName">Last Name</label>
        <input type="text" id="lastName" name="lastName" required>
        <label for="age">Age</label>
        <input type="number" id="age" name="age" required>
        <label for="email">Email</label>
        <input type="email" id="email" name="email" required>
        <button type="button" onclick="registerStudent()">Register</button>
    </form>
    <script>
        function registerStudent() {
            const form = document.getElementById('studentForm');
            const formData = new FormData(form);
            const studentInfo = {};
            formData.forEach((value, key) => {
                studentInfo[key] = value;
            });
            console.log(JSON.stringify(studentInfo, null, 2));
        }
    </script>

</body>
</html>


