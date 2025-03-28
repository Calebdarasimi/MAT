<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>5-Minute Math Test</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            line-height: 1.6;
        }
        #timer {
            position: fixed;
            top: 10px;
            right: 10px;
            font-size: 24px;
            font-weight: bold;
            color: #d9534f;
            background-color: #f9f9f9;
            padding: 10px 15px;
            border: 2px solid #d9534f;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        .student-info {
            background-color: #f5f5f5;
            padding: 20px;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        .question {
            margin-bottom: 20px;
            padding: 15px;
            background-color: #fff;
            border-left: 4px solid #5bc0de;
            border-radius: 3px;
        }
        .options {
            margin-left: 20px;
        }
        .option {
            margin: 8px 0;
        }
        #results {
            display: none;
            background-color: #e8f8f5;
            padding: 20px;
            border-radius: 5px;
            margin-top: 20px;
        }
        input[type="text"], input[type="tel"] {
            padding: 8px;
            margin: 5px 0 15px 0;
            width: 100%;
            box-sizing: border-box;
        }
        button {
            background-color: #5cb85c;
            color: white;
            border: none;
            padding: 12px 20px;
            font-size: 16px;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 20px;
        }
        button:hover {
            background-color: #4cae4c;
        }
        .warning {
            color: #d9534f;
            font-weight: bold;
        }
        .blink {
            animation: blink 1s linear infinite;
        }
        @keyframes blink {
            50% { opacity: 0.5; }
        }
    </style>
</head>
<body>
    <div id="timer">05:00</div>
    
    <h1>Mathematics Test</h1>
    <p class="warning">Time Allowed: 5 minutes (Auto-submits when time expires)</p>
    
    <form id="testForm">
        <div class="student-info">
            <h2>Student Information</h2>
            <label for="name">Full Name:</label>
            <input type="text" id="name" name="name" required>
            
            <label for="phone">Phone Number:</label>
            <input type="tel" id="phone" name="phone" pattern="[0-9]{10,11}" required>
        </div>

        <h2>Test Questions (10 Questions)</h2>
        
        <!-- Question 1 -->
        <div class="question">
            <p>1. What is the value of 15 + 27 - 8?</p>
            <div class="options">
                <div class="option"><input type="radio" name="q1" value="A" required> A) 30</div>
                <div class="option"><input type="radio" name="q1" value="B"> B) 34</div>
                <div class="option"><input type="radio" name="q1" value="C"> C) 40</div>
                <div class="option"><input type="radio" name="q1" value="D"> D) 44</div>
            </div>
        </div>

        <!-- Question 2 -->
        <div class="question">
            <p>2. Solve for x in the equation 3x + 5 = 20.</p>
            <div class="options">
                <div class="option"><input type="radio" name="q2" value="A" required> A) 3</div>
                <div class="option"><input type="radio" name="q2" value="B"> B) 5</div>
                <div class="option"><input type="radio" name="q2" value="C"> C) 7</div>
                <div class="option"><input type="radio" name="q2" value="D"> D) 10</div>
            </div>
        </div>

        <!-- Question 3 -->
        <div class="question">
            <p>3. What is the area of a rectangle with length 8 cm and width 5 cm?</p>
            <div class="options">
                <div class="option"><input type="radio" name="q3" value="A" required> A) 13 cm²</div>
                <div class="option"><input type="radio" name="q3" value="B"> B) 30 cm²</div>
                <div class="option"><input type="radio" name="q3" value="C"> C) 40 cm²</div>
                <div class="option"><input type="radio" name="q3" value="D"> D) 45 cm²</div>
            </div>
        </div>

        <!-- Question 4 -->
        <div class="question">
            <p>4. Simplify 12/18 to its lowest terms.</p>
            <div class="options">
                <div class="option"><input type="radio" name="q4" value="A" required> A) 1/2</div>
                <div class="option"><input type="radio" name="q4" value="B"> B) 2/3</div>
                <div class="option"><input type="radio" name="q4" value="C"> C) 3/4</div>
                <div class="option"><input type="radio" name="q4" value="D"> D) 6/9</div>
            </div>
        </div>

        <!-- Question 5 -->
        <div class="question">
            <p>5. What is 25% of 200?</p>
            <div class="options">
                <div class="option"><input type="radio" name="q5" value="A" required> A) 25</div>
                <div class="option"><input type="radio" name="q5" value="B"> B) 50</div>
                <div class="option"><input type="radio" name="q5" value="C"> C) 75</div>
                <div class="option"><input type="radio" name="q5" value="D"> D) 100</div>
            </div>
        </div>

        <!-- Question 6 -->
        <div class="question">
            <p>6. Evaluate 2⁴.</p>
            <div class="options">
                <div class="option"><input type="radio" name="q6" value="A" required> A) 8</div>
                <div class="option"><input type="radio" name="q6" value="B"> B) 16</div>
                <div class="option"><input type="radio" name="q6" value="C"> C) 32</div>
                <div class="option"><input type="radio" name="q6" value="D"> D) 64</div>
            </div>
        </div>

        <!-- Question 7 -->
        <div class="question">
            <p>7. If a book costs \$12 and a pen costs \$3, how much do 2 books and 4 pens cost together?</p>
            <div class="options">
                <div class="option"><input type="radio" name="q7" value="A" required> A) \$24</div>
                <div class="option"><input type="radio" name="q7" value="B"> B) \$30</div>
                <div class="option"><input type="radio" name="q7" value="C"> C) \$36</div>
                <div class="option"><input type="radio" name="q7" value="D"> D) \$42</div>
            </div>
        </div>

        <!-- Question 8 -->
        <div class="question">
            <p>8. What is the greatest common divisor (GCD) of 24 and 36?</p>
            <div class="options">
                <div class="option"><input type="radio" name="q8" value="A" required> A) 6</div>
                <div class="option"><input type="radio" name="q8" value="B"> B) 12</div>
                <div class="option"><input type="radio" name="q8" value="C"> C) 18</div>
                <div class="option"><input type="radio" name="q8" value="D"> D) 24</div>
            </div>
        </div>

        <!-- Question 9 -->
        <div class="question">
            <p>9. A fair six-sided die is rolled. What is the probability of getting an even number?</p>
            <div class="options">
                <div class="option"><input type="radio" name="q9" value="A" required> A) 1/6</div>
                <div class="option"><input type="radio" name="q9" value="B"> B) 1/3</div>
                <div class="option"><input type="radio" name="q9" value="C"> C) 1/2</div>
                <div class="option"><input type="radio" name="q9" value="D"> D) 2/3</div>
            </div>
        </div>

        <!-- Question 10 -->
        <div class="question">
            <p>10. What is the derivative of f(x) = 5x³ + 2x - 7 with respect to x?</p>
            <div class="options">
                <div class="option"><input type="radio" name="q10" value="A" required> A) 5x² + 2</div>
                <div class="option"><input type="radio" name="q10" value="B"> B) 15x² + 2</div>
                <div class="option"><input type="radio" name="q10" value="C"> C) 15x³ + 2x</div>
                <div class="option"><input type="radio" name="q10" value="D"> D) 10x + 2</div>
            </div>
        </div>

        <button type="submit">Submit Test</button>
    </form>

    <div id="results">
        <h2>Test Results</h2>
        <p id="studentDetails"></p>
        <p id="scoreResult"></p>
        <p id="percentageResult"></p>
    </div>

    <script>
        // Test configuration
        const TEST_DURATION = 300; // 5 minutes in seconds
        let timeLeft = TEST_DURATION;
        let timerActive = true;
        const timerElement = document.getElementById('timer');
        const testForm = document.getElementById('testForm');
        const resultsDiv = document.getElementById('results');

        // Correct answers
        const solutions = {
            q1: "B",
            q2: "B",
            q3: "C",
            q4: "B",
            q5: "B",
            q6: "B",
            q7: "C",
            q8: "B",
            q9: "C",
            q10: "B"
        };

        // Timer functionality
        const timerId = setInterval(updateTimer, 1000);

        function updateTimer() {
            if (!timerActive) return;
            
            const minutes = Math.floor(timeLeft / 60);
            let seconds = timeLeft % 60;
            seconds = seconds < 10 ? '0' + seconds : seconds;
            
            timerElement.textContent = `${minutes}:${seconds}`;
            
            // Blink when 1 minute left
            if (timeLeft <= 60) {
                timerElement.classList.add('blink');
            }
            
            if (timeLeft <= 0) {
                timerActive = false;
                clearInterval(timerId);
                submitTest();
            }
            timeLeft--;
        }

        // Submission handler
        function submitTest() {
            timerActive = false;
            clearInterval(timerId);
            
            // Calculate score
            let score = 0;
            const totalQuestions = Object.keys(solutions).length;
            
            for (let i = 1; i <= totalQuestions; i++) {
                const question = `q${i}`;
                const selectedOption = document.querySelector(`input[name="${question}"]:checked`);
                if (selectedOption && selectedOption.value === solutions[question]) {
                    score++;
                }
            }

            // Display results
            document.getElementById('studentDetails').textContent = 
                `Student: ${document.getElementById('name').value} | Phone: ${document.getElementById('phone').value}`;
            
            document.getElementById('scoreResult').textContent = 
                `Score: ${score}/${totalQuestions}`;
            
            const percentage = (score / totalQuestions * 100).toFixed(1);
            document.getElementById('percentageResult').textContent = 
                `Percentage: ${percentage}%`;
            
            resultsDiv.style.display = 'block';
            window.scrollTo(0, document.body.scrollHeight);
        }

        // Form submission
        testForm.addEventListener('submit', function(e) {
            e.preventDefault();
            submitTest();
        });

        // Prevent cheating
        document.addEventListener('contextmenu', function(e) {
            e.preventDefault();
        });

        // Auto-submit warning
        window.addEventListener('beforeunload', function(e) {
            if (timerActive) {
                e.preventDefault();
                e.returnValue = 'Your test is still in progress. Are you sure you want to leave?';
            }
        });
    </script>
</body>
</html>
