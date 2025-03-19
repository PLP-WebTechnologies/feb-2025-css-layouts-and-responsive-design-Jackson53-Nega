<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: Arial, sans-serif;
        }
        
        /* Navigation Bar */
        nav {
            background-color: #333;
            color: white;
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        nav ul {
            list-style: none;
            display: flex;
        }
        nav ul li {
            margin: 0 15px;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
        }

        /* Main Layout */
        .container {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 20px;
            padding: 20px;
        }
        .sidebar {
            background-color: #f4f4f4;
            padding: 20px;
        }
        .content {
            background-color: #e0e0e0;
            padding: 20px;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }
            nav {
                flex-direction: column;
                align-items: center;
            }
            nav ul {
                flex-direction: column;
                padding: 10px 0;
            }
            nav ul li {
                margin: 10px 0;
            }
        }
    </style>
</head>
<body>
    <nav>
        <h1>My Website</h1>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>
    <div class="container">
        <aside class="sidebar">Sidebar Content</aside>
        <section class="content">Main Content Area</section>
    </div>
</body>
</html>
