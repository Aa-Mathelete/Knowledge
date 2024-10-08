---
title: How to solve simple Absolute Value equations
categories: [Academics, Mathematics]
tags: [Math, Algebra]
toc: 1
snippet: 1
date: 2024-09-28
comment: 1
---


<ul class="collapsible" data-collapsible="accordion">
<li>
<div class="collapsible-header" markdown="1"><i class="material-icons">face</i>
Refresh On Absolute Value
</div>
<div class="collapsible-body" markdown="1">
Absolute Value is the distance from zero a number has; Absoulute Value bars look like this ||.  If you have a number inside them, then that numeber, no matter if it is negative, turns positive. Here is an example:  |6| = 6,  |-6| = 6. If there is a *negative sign outside* then the result is negative. Here is what I mean:  -|300| = -300. Once you solve inside the bars, then the negative is attached.
<img src="https://mathbitsnotebook.com/Algebra2/AbsoluteValue/AbsGraphRB.jpg" alt="Number Line Example">
</div>
</li>
</ul>

## How to solve Absolute Value equations

To solve an absolute value equation you have to break it into 2 parts, one side equaling a negative, and other positive. Doing this gets rid of the absolute value bars.

<div class="thi-box" markdown="1">
<div class="box-title" markdown="1">
Example 1
</div>
<div class="box-content" markdown="1">
|2x-4|=20
</div>
</div>

    $
    First we will solve positive twenty, then negative twenty.
    2x-4=20
     +4 on both sides
    2x=20
    Divide by 2 on both sides
    x=10
    $

<p class="post-more-info" markdown="1">
If you have any questions remember to comment them below!
</p>

Now let's solve for -20

    $

    2x-4=-20

    +4     +4 
    Add 4 on both sides

    2x=-16
    2/2x=-16/2
    Divide by 2 on both sides

    x=-8
    $

Finally, we solved **both** for negative and positive our answers are: x=-8 and x=10. 

Try practicing more questions below!

## Practice Problems

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Absolute Value Quiz</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f0f8ff;
        }
        .quiz-container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            border: 1px solid #ddd;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        .question {
            margin-bottom: 20px;
        }
        .question p {
            font-size: 1.2em;
        }
        .question input {
            width: 100%;
            padding: 10px;
            font-size: 1em;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .submit-btn {
            display: block;
            width: 100%;
            padding: 10px;
            font-size: 1.2em;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .submit-btn:hover {
            background-color: #0056b3;
        }
        .results {
            margin-top: 20px;
        }
        .results p {
            font-size: 1.2em;
        }
    </style>
</head>
<body>
    <div class="quiz-container">
        <h1>Absolute Value Quiz</h1>
        <form id="quizForm">
            <div class="question">
                <p>1. Solve for x: |x - 3| = 7</p>
                <input type="text" id="q1">
            </div>
            <div class="question">
                <p>2. Solve for x: |2x + 5| = 9</p>
                <input type="text" id="q2">
            </div>
            <div class="question">
                <p>3. Solve for x: |x + 1| = 4</p>
                <input type="text" id="q3">
            </div>
            <button type="button" class="submit-btn" onclick="checkAnswers()">Submit</button>
        </form>
        <div class="results" id="results"></div>
    </div>
    <script>
        function checkAnswers() {
            const answers = [
                { q: "|x - 3| = 7", correct: ["10", "-4"], explanation: "The absolute value equation |x - 3| = 7 has two solutions: x - 3 = 7 or x - 3 = -7, which gives x = 10 or x = -4." },
                { q: "|2x + 5| = 9", correct: ["2", "-7"], explanation: "The absolute value equation |2x + 5| = 9 has two solutions: 2x + 5 = 9 or 2x + 5 = -9, which gives x = 2 or x = -7." },
                { q: "|x + 1| = 4", correct: ["3", "-5"], explanation: "The absolute value equation |x + 1| = 4 has two solutions: x + 1 = 4 or x + 1 = -4, which gives x = 3 or x = -5." }
            ];
            let score = 0;
            let feedback = '';

            for (let i = 0; i < answers.length; i++) {
                const userAnswer = document.getElementById(`q${i+1}`).value.trim();
                if (answers[i].correct.includes(userAnswer)) {
                    score++;
                } else {
                    feedback += `<p>Question ${i+1}: ${answers[i].q}<br>Correct answers: ${answers[i].correct.join(' or ')}<br>Explanation: ${answers[i].explanation}</p>`;
                }
            }

            document.getElementById('results').innerHTML = `<p>Your score is ${score}/${answers.length}</p>${feedback}`;
        }
    </script>
</body>
</html>
