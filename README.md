<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Administration Portal</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            height: 100vh;
            margin: 0;
        }
        table {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 600px; /* Adjust width as needed */
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        caption {
            caption-side: top;
            font-size: 1.5em;
            margin-bottom: 10px;
        }
        td, th {
            padding: 10px;
            vertical-align: middle;
            border: 1px solid #ddd;
        }
        input[type="text"],
        input[type="password"],
        input[type="email"],
        input[type="date"],
        select {
            width: 100%;
            padding: 8px;
            margin: 4px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
        input[type="submit"] {
            width: 100%;
            background-color: #4CAF50;
            color: white;
            padding: 10px;
            margin: 8px 0;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>

<!-- Form for data submission -->
<table>
    <caption>Administration Portal - Register User</caption>
    <form action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]); ?>" method="post">
        <tr>
            <td><label for="name">Name:</label></td>
            <td><input type="text" id="name" name="name" required></td>
        </tr>
        <tr>
            <td><label for="id">ID:</label></td>
            <td><input type="text" id="id" name="id" required></td>
        </tr>
        <tr>
            <td><label for="email_id">Email:</label></td>
            <td><input type="email" id="email_id" name="email_id" required></td>
        </tr>
        <tr>
            <td><label for="gender">Gender:</label></td>
            <td>
                <input type="radio" id="male" name="gender" value="Male" required>
                <label for="male">Male</label>
                <input type="radio" id="female" name="gender" value="Female" required>
                <label for="female">Female</label>
            </td>
        </tr>
        <tr>
            <td><label for="country">Country:</label></td>
            <td>
                <select id="country" name="country">
                    <option value="Pakistan">Pakistan</option>
                    <option value="India">India</option>
                    <option value="England">England</option>
                    <option value="New Zealand">New Zealand</option>
                </select>
            </td>
        </tr>
        <tr>
            <td><label for="pass">Password:</label></td>
            <td><input type="password" id="pass" name="pass" required></td>
        </tr>
        <tr>
            <td><label for="date">Date:</label></td>
            <td><input type="date" id="date" name="date" required></td>
        </tr>
        <tr>
            <td colspan="2"><input type="submit" name="sbt" value="Register"></td>
        </tr>
    </form>
</table>

<!-- Form for selecting date range -->
<table>
    <caption>Filter by Date Range</caption>
    <form action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]); ?>" method="get">
        <tr>
            <td><label for="start_date">Start Date:</label></td>
            <td><input type="date" id="start_date" name="start_date" required></td>
        </tr>
        <tr>
            <td><label for="end_date">End Date:</label></td>
            <td><input type="date" id="end_date" name="end_date" required></td>
        </tr>
        <tr>
            <td colspan="2"><input type="submit" value="Filter"></td>
        </tr>
    </form>
</table>

<!-- Table for displaying user data -->
<table>
    <caption>User Data</caption>
    <tr>
        <th>ID</th>
        <th>Name</th>
        <th>Gender</th>
        <th>Email</th>
        <th>Country</th>
        <th>Date</th>
    </tr>
