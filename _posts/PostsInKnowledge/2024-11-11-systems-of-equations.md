---
title: Systems of equations
categories: [Algebra 1]
tags: [Algebra 1, Math]
toc: 1
comment: 1
maths: 1
date: 2024-11-11
---

## Into
Most highschoolers struggle with systems of equations, so it's important to get this concept right! There are two ways to solve systems and with practice you will know which to use and when!

## Substitution
In Substitution you rewrite the equation in terms of 'y', then plug it in to the other equation.
<div class="thi-columns" markdown="1">
- Rewrite Equation in terms of 'y'
- Plug in and Solve
- Find Value and plug into a equation
- Solve for other value
- Check by pluging in the other equation
- Write as an ordered pair (x,y)
</div> 

## Elimination
## Practice Quiz
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Systems of Equations Quiz</title>
    <style>
        .correct { color: green; }
        .wrong { color: red; }
    </style>
</head>
<body>
    <h1>Systems of Equations Quiz</h1>
    <form id="quizForm">
        <h2>Mandatory Substitution</h2>
        <ol>
            <li>Solve by substitution: 
                <br>x + y = 7 
                <br>2x - y = 1
                <br><input type="text" name="q1" id="q1">
            </li>
            <li>Solve by substitution: 
                <br>3x + 4y = 24 
                <br>y = 2x + 1
                <br><input type="text" name="q2" id="q2">
            </li>
            <li>Solve by substitution: 
                <br>5x - 2y = -1 
                <br>x + 3y = 9
                <br><input type="text" name="q3" id="q3">
            </li>
        </ol>

        <h2>Mandatory Elimination</h2>
        <ol>
            <li>Solve by elimination: 
                <br>2x + 3y = 6 
                <br>4x - 3y = 9
                <br><input type="text" name="q4" id="q4">
            </li>
            <li>Solve by elimination: 
                <br>5x + 2y = 20 
                <br>3x - 2y = -4
                <br><input type="text" name="q5" id="q5">
            </li>
            <li>Solve by elimination: 
                <br>3x + 4y = 18 
                <br>6x + 8y = 36 (Infinite solutions)
                <br><input type="text" name="q6" id="q6">
            </li>
        </ol>

        <h2>Optional Method</h2>
        <ol>
            <li>Solve using your preferred method: 
                <br>x - 2y = 3 
                <br>2x + 3y = 1
                <br><input type="text" name="q7" id="q7">
            </li>
            <li>Solve using your preferred method: 
                <br>x/2 + y/3 = 2 
                <br>3x - 4y = -1.5
                <br><input type="text" name="q8" id="q8">
            </li>
            <li>Solve using your preferred method: 
                <br>2x + 3y = 7 
                <br>4x + 6y = 9 (No solution)
                <br><input type="text" name="q9" id="q9">
            </li>
        </ol>
        <input type="button" value="Submit" onclick="checkAnswers()">
    </form>

    <h2>Results</h2>
    <div id="results"></div>

    <script>
        const correctAnswers = {
            q1: 'x=2,y=5',
            q2: 'x=5,y=11',
            q3: 'x=1,y=2',
            q4: 'x=3,y=0',
            q5: 'x=2,y=5',
            q6: 'Infinite solutions',
            q7: 'x=1,y=-1',
            q8: 'x=3.5,y=-0.5',
            q9: 'No solution'
        };

        function checkAnswers() {
            const form = document.getElementById('quizForm');
            let score = 0;
            let total = 9;
            let results = '';

            for (let key in correctAnswers) {
                const userAnswer = form[key].value.trim();
                if (userAnswer.toLowerCase() === correctAnswers[key].toLowerCase()) {
                    results += `<p class="correct">Question ${key[1]}: Correct!</p>`;
                    score++;
                } else {
                    results += `<p class="wrong">Question ${key[1]}: Wrong. The correct answer is ${correctAnswers[key]}</p>`;
                }
            }

            let grade = (score / total) * 100;
            results += `<h3>Your Grade: ${grade}%</h3>`;

            document.getElementById('results').innerHTML = results;
        }
    </script>
</body>
</html>
