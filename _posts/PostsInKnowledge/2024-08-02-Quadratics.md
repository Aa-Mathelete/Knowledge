---
title: Quadratic Equations
categories: Maths
tags: [Math, Algebra]
maths: 1
comment: 1
---
///In Progress

## Formulas
--
<ul class="collapsible" data-collapsible="accordion">
<li>
<div class="collapsible-header" markdown="1"><i class="material-icons">face</i>
Quadratic Formula
</div>
<div class="collapsible-body" markdown="1">

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQa4B5z7owG3M4qGsBZ98o5A7pUsaMO1i5QbA&s" alt="Quadratic Formula">

</div>
</li>
</ul>
--

## Solving them
## Quiz
--
 For this quiz, please type exponents like ^, multiplying like *, subraction like - , addition like + , and parenthesis normally like so (). 

--

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quadratic Equations Quiz</title>
    <style>
        body {
            font-family: Georgia, serif;
            margin: 20px;
        }
        .question {
            margin-bottom: 15px;
        }
        .answer {
            display: none;
            color: green;
        }
    </style>
    <script>
        function checkAnswers() {
            for (let i = 1; i <= 10; i++) {
                let userAnswer = document.getElementById('answer' + i).value;
                let correctAnswer = document.getElementById('correct' + i).textContent;
                if (userAnswer === correctAnswer) {
                    document.getElementById('result' + i).textContent = 'Correct!';
                    document.getElementById('result' + i).style.color = 'green';
                } else {
                    document.getElementById('result' + i).textContent = 'Incorrect. The correct answer is ' + correctAnswer;
                    document.getElementById('result' + i).style.color = 'red';
                }
                document.getElementById('correct' + i).style.display = 'inline';
            }
        }
    </script>
</head>
<body>
    <h1>Quadratic Equations Quiz</h1>
    <form>
        <div class="question">
            <label>1. Solve for x: $$x^2 + 5x + 6 = 0$$</label>
            <input type="text" id="answer1">
            <span class="answer" id="correct1">x = -2, x = -3</span>
            <span id="result1"></span>
        </div>
        <div class="question">
            <label>2. Solve for x: $$x^2 - 4x - 5 = 0$$</label>
            <input type="text" id="answer2">
            <span class="answer" id="correct2">x = 5, x = -1</span>
            <span id="result2"></span>
        </div>
        <div class="question">
            <label>3. Solve for x: $$2x^2 + 3x - 2 = 0$$</label>
            <input type="text" id="answer3">
            <span class="answer" id="correct3">x = 1/2, x = -2</span>
            <span id="result3"></span>
        </div>
        <div class="question">
            <label>4. Solve for x: $$x^2 - 6x + 9 = 0$$</label>
            <input type="text" id="answer4">
            <span class="answer" id="correct4">x = 3</span>
            <span id="result4"></span>
        </div>
        <div class="question">
            <label>5. Solve for x: $$3x^2 + x - 2 = 0$$</label>
            <input type="text" id="answer5">
            <span class="answer" id="correct5">x = 1, x = -2/3</span>
            <span id="result5"></span>
        </div>
        <div class="question">
            <label>6. Solve for x: $$x^2 + 2x - 8 = 0$$</label>
            <input type="text" id="answer6">
            <span class="answer" id="correct6">x = 2, x = -4</span>
            <span id="result6"></span>
        </div>
        <div class="question">
            <label>7. Solve for x: $$2x^2 - 4x - 6 = 0$$</label>
            <input type="text" id="answer7">
            <span class="answer" id="correct7">x = 3, x = -1</span>
            <span id="result7"></span>
        </div>
        <div class="question">
            <label>8. Solve for x: $$x^2 + 7x + 10 = 0$$</label>
            <input type="text" id="answer8">
            <span class="answer" id="correct8">x = -2, x = -5</span>
            <span id="result8"></span>
        </div>
        <div class="question">
            <label>9. Solve for x: $$x^2 - 3x - 4 = 0$$</label>
            <input type="text" id="answer9">
            <span class="answer" id="correct9">x = 4, x = -1</span>
            <span id="result9"></span>
        </div>
        <div class="question">
            <label>10. Solve for x: $$x^2 + 4x + 4 = 0$$</label>
            <input type="text" id="answer10">
            <span class="answer" id="correct10">x = -2</span>
            <span id="result10"></span>
        </div>
        <button type="button" onclick="checkAnswers()">Check Answers</button>
    </form>
</body>
</html>



