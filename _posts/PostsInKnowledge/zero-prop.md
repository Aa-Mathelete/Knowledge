---
title: Solving Quadratic Binomials With Zero Product Property
categories: Algebra 1
comment: 1
---
<p markdown="1" class="thi-tip">
<i class="material-icons mat-icon">info</i>
This trick only works when the sum is 0! 
</p>

You know that if you multiply two binomials you get a answer that is in ax^2+bx+c form, but there is a simpler way to solve for x *if your answer equals to 0*.  
## How  To Use It

{% include img-inline.html content="https://cdn.virtualnerd.com/thumbnails/Alg1_7_1_12-diagram_thumb-lg.png" %}

$$
Q: (2x−1)(4x−3)=0
First split the equations into two.
(2x-1)=0
(4x-3)=0
Then solve normally.
2x−1=0⇒x= 1/2 or 0.50

4x-3=0⇒x = 3/4 or 0.75
​
$$
So, step by step, here is what to do. 
<div class="thi-columns" markdown="1">
- Split Equation into two
- Solve Normally
- Check!
</div>

## Why 0?
The Zero **Product** Property states that if two numbers product is 0 then one of the factors is 0. Another way of writing this is:

*If a⋅b=0, then either a=0 or b=0*
Note that this property doesn't work for sums! When the product equals zero, you can conclude that one or more of the factors must be zero, but when the sum equals zero, you just need to solve the equation directly (i.e., isolate the variable).
$$
SUM EQUALS ZERO: 4x-3=0

FACTORS EQUALS ZERO: X*0
$$




## Test Your Knowledge!

---
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quadratic Binomial Quiz</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        .question {
            font-size: 18px;
            margin-bottom: 10px;
        }
        .answers {
            margin-bottom: 20px;
        }
        .answer {
            margin: 5px 0;
        }
        .correct {
            color: green;
            font-weight: bold;
        }
        .incorrect {
            color: red;
            font-weight: bold;
        }
        .explanation {
            font-size: 16px;
            margin-top: 10px;
            color: #555;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            font-size: 16px;
            border-radius: 5px;
            margin-top: 10px;
        }
        button:hover {
            background-color: #45a049;
        }
        .reset-btn {
            background-color: #f44336;
        }
        .reset-btn:hover {
            background-color: #e53935;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Quadratic Binomial Quiz</h1>
        <div id="quiz">
            <!-- Question 1 -->
            <div class="question">
                <strong>1. Solve the equation: </strong>(2x - 1)(4x - 3) = 0
            </div>
            <div class="answers">
                <div class="answer">a) x = 1/2, x = 3/4</div>
                <div class="answer">b) x = 1, x = 3</div>
                <div class="answer">c) x = -1/2, x = -3/4</div>
                <div class="answer">d) x = -1, x = -3</div>
            </div>
            <div class="explanation" id="explanation1">
                <!-- Explanation for Question 1 will be shown here -->
            </div>

            <!-- Question 2 -->
            <div class="question">
                <strong>2. Solve the equation: </strong>(x + 5)(x - 7) = 0
            </div>
            <div class="answers">
                <div class="answer">a) x = -5, x = 7</div>
                <div class="answer">b) x = 5, x = -7</div>
                <div class="answer">c) x = 0, x = -12</div>
                <div class="answer">d) x = 2, x = -3</div>
            </div>
            <div class="explanation" id="explanation2">
                <!-- Explanation for Question 2 will be shown here -->
            </div>

            <!-- Question 3 -->
            <div class="question">
                <strong>3. Solve the equation: </strong>(3x - 2)(x + 1) = 0
            </div>
            <div class="answers">
                <div class="answer">a) x = 2/3, x = -1</div>
                <div class="answer">b) x = 2, x = 1</div>
                <div class="answer">c) x = -2/3, x = -1</div>
                <div class="answer">d) x = 0, x = 1</div>
            </div>
            <div class="explanation" id="explanation3">
                <!-- Explanation for Question 3 will be shown here -->
            </div>

            <!-- Question 4 -->
            <div class="question">
                <strong>4. Solve the equation: </strong>(4x + 3)(2x - 5) = 0
            </div>
            <div class="answers">
                <div class="answer">a) x = -3/4, x = 5/2</div>
                <div class="answer">b) x = 3/4, x = -5/2</div>
                <div class="answer">c) x = -5/2, x = 3/4</div>
                <div class="answer">d) x = 0, x = -3/2</div>
            </div>
            <div class="explanation" id="explanation4">
                <!-- Explanation for Question 4 will be shown here -->
            </div>

            <!-- Question 5 -->
            <div class="question">
                <strong>5. Solve the equation: </strong>(5x - 4)(x + 3) = 0
            </div>
            <div class="answers">
                <div class="answer">a) x = 4/5, x = -3</div>
                <div class="answer">b) x = -4/5, x = 3</div>
                <div class="answer">c) x = 4, x = -3/5</div>
                <div class="answer">d) x = -4, x = 3/5</div>
            </div>
            <div class="explanation" id="explanation5">
                <!-- Explanation for Question 5 will be shown here -->
            </div>
            
            <button onclick="checkAnswers()">Check Answers</button>
            <button class="reset-btn" onclick="resetQuiz()">Reset Quiz</button>
        </div>
    </div>

    <script>
        function checkAnswers() {
            // Question 1: (2x - 1)(4x - 3) = 0
            const q1Answer = "a";
            const q1Explanation = "For the equation (2x - 1)(4x - 3) = 0, we set each factor equal to 0: 2x - 1 = 0 → x = 1/2 and 4x - 3 = 0 → x = 3/4.";

            // Question 2: (x + 5)(x - 7) = 0
            const q2Answer = "a";
            const q2Explanation = "For the equation (x + 5)(x - 7) = 0, we set each factor equal to 0: x + 5 = 0 → x = -5 and x - 7 = 0 → x = 7.";

            // Question 3: (3x - 2)(x + 1) = 0
            const q3Answer = "a";
            const q3Explanation = "For the equation (3x - 2)(x + 1) = 0, we set each factor equal to 0: 3x - 2 = 0 → x = 2/3 and x + 1 = 0 → x = -1.";

            // Question 4: (4x + 3)(2x - 5) = 0
            const q4Answer = "c";
            const q4Explanation = "For the equation (4x + 3)(2x - 5) = 0, we set each factor equal to 0: 4x + 3 = 0 → x = -3/4 and 2x - 5 = 0 → x = 5/2.";

            // Question 5: (5x - 4)(x + 3) = 0
            const q5Answer = "a";
            const q5Explanation = "For the equation (5x - 4)(x + 3) = 0, we set each factor equal to 0: 5x - 4 = 0 → x = 4/5 and x + 3 = 0 → x = -3.";

            // Displaying answers and explanations
            document.getElementById("explanation1").innerHTML = `Answer: ${q1Answer}. ${q1Explanation}`;
            document.getElementById("explanation2").innerHTML = `Answer: ${q2Answer}. ${q2Explanation}`;
            document.getElementById("explanation3").innerHTML = `Answer: ${q3Answer}. ${q3Explanation}`;
            document.getElementById("explanation4").innerHTML = `Answer: ${q4Answer}. ${q4Explanation}`;
            document.getElementById("explanation5").inner
---