<!DOCTYPE html>
<html>
<head>
    <title>Comfort and Encouragement</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Comfort and Encouragement</h1>
        <p>What problem are you facing right now?</p>
        <textarea id="problemInput" rows="4" cols="50"></textarea>
        <br>
        <button onclick="provideComfort()">Provide Comfort</button>

        <div id="comfortMessages" style="display: none;">
            <h2>Comforting Messages</h2>
            <p id="message"></p>
            <button onclick="showNextMessage()">Next Message</button>
        </div>
    </div>

    <script>
        var problemInput = document.getElementById("problemInput");
        var comfortMessages = document.getElementById("comfortMessages");
        var message = document.getElementById("message");
        var messages = [
            "Remember that every problem has a solution. Stay positive and keep seeking ways to overcome it. You are stronger than you think. Trust in your abilities to navigate through this challenging time. Difficulties are temporary. Keep moving forward, and you'll come out even stronger on the other side. Don't be too hard on yourself. Remember that everyone faces struggles and setbacks in life. Take a step back andd reassess the situation. Sometimes a fresh perspective can reveal new solutions. Lean on your support system. Reach out to loved ones who can provide comfort and guidance. Believe in your resilience. You've overcome obstacles before, and you can do it again. Believe in your resillence. You've overcome obstacles before, and you can do it again. Focus on what you can control and take small steps towards improvement. Progress is progress, no matter how small. Embrace self-care. Take time for activities that bring you joy and help alleviate stress. Remember that it's okay to ask for help. Seeking support from others is a sign of strenght, not weakness."
        ];
        var currentIndex = 0;

        function provideComfort() {
            var problem = problemInput.value.trim();
            if (problem !== "") {
                problemInput.style.display = "none";
                comfortMessages.style.display = "block";
                showNextMessage();
            }
        }

        function showNextMessage() {
            message.textContent = messages[currentIndex];
            currentIndex = (currentIndex + 1) % messages.length;
        }
    </script>
</body>
</html>
