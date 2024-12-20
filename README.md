<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>3D Animated Landing Page</title>
    <style>
        /* Global Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background-color: #f5f5f5;
            overflow: hidden;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            position: relative;
            width: 100%;
            height: 100%;
            background: #333;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            text-align: center;
            color: white;
        }

        /* 3D Background Animation */
        @keyframes rotateBackground {
            0% {
                transform: rotateY(0deg);
            }
            50% {
                transform: rotateY(180deg);
            }
            100% {
                transform: rotateY(360deg);
            }
        }

        .background {
            position: absolute;
            width: 120%;
            height: 120%;
            background: linear-gradient(45deg, #ff7e5f, #feb47b);
            top: -10%;
            left: -10%;
            animation: rotateBackground 10s infinite linear;
            transform-origin: center;
        }

        /* Main Content */
        .content {
            z-index: 2;
            color: white;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.4);
            transform: translateY(0);
            animation: fadeInUp 2s ease-out;
        }

        .content h1 {
            font-size: 4rem;
            margin-bottom: 20px;
            letter-spacing: 3px;
            font-weight: bold;
        }

        .content p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0;
            animation: fadeInUp 2s ease-out 1s forwards;
        }

        .cta-button {
            font-size: 1.2rem;
            padding: 15px 30px;
            background-color: #feb47b;
            color: #333;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .cta-button:hover {
            background-color: #ff7e5f;
            transform: scale(1.1);
        }

        .cta-button:active {
            transform: scale(0.98);
        }

        /* Animation for Content */
        @keyframes fadeInUp {
            0% {
                opacity: 0;
                transform: translateY(30px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .content h1 {
                font-size: 2.5rem;
            }

            .content p {
                font-size: 1rem;
            }

            .cta-button {
                font-size: 1rem;
                padding: 12px 25px;
            }
        }

        @media (max-width: 480px) {
            .content h1 {
                font-size: 2rem;
            }

            .content p {
                font-size: 0.9rem;
            }

            .cta-button {
                font-size: 0.9rem;
                padding: 10px 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="background"></div>
        <div class="content">
            <h1>Welcome to Our Amazing Service</h1>
            <p>Empowering you with innovative solutions that take your business to the next level.</p>
            <button class="cta-button" onclick="window.location.href='home.html'">Get Started</button>
        </div>
    </div>

    <script>
        // Optional JS for additional functionality
    </script>
</body>
</html>
