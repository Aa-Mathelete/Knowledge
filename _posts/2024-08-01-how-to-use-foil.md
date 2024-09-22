---
title: How to Multiply Binomials
categories: Algebra 1
tags: [Algebra, Math, Foil, Double Distribution, Basics To Solving Quadratics ]
maths: 1
comment: 1
---

Hi! In this post I'm going to cover: what FOIL is in math, how to apply it, some exampes, and tips! Along with teaching you how to multiply binomials, I'll teach you another way, which I like to call Double Distribution. 🤓 Have fun!

{% include tip.html content="If you have any questions or comments please write them down below!" %}

{% include toc.html %}
Lets first start with FOIL!
 
## What does FOIL stand for?

Foil stands for:

 **F**irst

 **O**uter

 **I**nner

 **L**ast


Ok, so this sequence is **essential** to **multiplying binomials** correctly. Now that you know what FOIL stands for let's figure out how to use it!

<p class="post-more-info" markdown="1">
 Reminder: FOIL is used for multiplying binomials, not dividing, adding, or subtracting!
</p>

 

## Applying FOIL 
<img src="https://study.com/cimages/multimages/16/foil.png" alt="Foil Image">

Based on the image above, you should get an idea of what applying foil looks like. 
    **First** we multiply the first two terms.  Next, we multiply the terms near the **outside** of the parathesis.Next, we multiply the two terms in the middle, or the **inside**. Finally, we multiply the **last** two terms. A trick to remember this is by thinking of multiplying binomials as a jelly filled donut. For example, the jelly is the inside of the equation; then the crunchy outside would be where the paranthesis are.
    Think about it!
<img src="https://www.tastingtable.com/img/gallery/strawberry-jam-doughnut-recipe-donut/image-import.jpg" alt="Jelly Filled Donut">

<p class="post-more-info" markdown="1">
Reminder: When applying FOIL, everything must be done in relation to the paranthesis!
</p>

## Examples of Foil
Below, I'm going to solve some FOIL problems. I suggest you solving them first, and then check your work with mine!

Here is the first question:
<img src="images/posts/maths/foil.png" alt="FOIL Question 1">

Here is the solution:<img src="images/posts/maths/math.png" alt="FOIL Answer 1">

Here is another question:<img src="images/posts/maths/FoilQ2.png" alt="FOIL Question 2">

Here is the solution:<img src="images/posts/maths/Foila2.png" alt="FOIL Answer 2">

---
<ul class="collapsible" data-collapsible="accordion">
<li>
<div class="collapsible-header" markdown="1"><i class="material-icons">face</i>
Watch this video for more practice:

</div>
<div class="collapsible-body" markdown="1">

{% include youtube.html content="nyk3UGwCAms" size="10" %}

</div>
</li>
</ul>
--
For this quiz, please type exponents like ^, multiplying like *, subraction like - , addition like + , and parenthesis normaly like ().
--
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Binomials Quiz</title>
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
    <h1>Binomials Quiz</h1>
    <form>
        <div class="question">
            <label>1. (x + 2)(x + 3) = </label>
            <input type="text" id="answer1">
            <span class="answer" id="correct1">x^2 + 5x + 6</span>
            <span id="result1"></span>
        </div>
        <div class="question">
            <label>2. (x - 4)(x + 5) = </label>
            <input type="text" id="answer2">
            <span class="answer" id="correct2">x^2 + x - 20</span>
            <span id="result2"></span>
        </div>
        <div class="question">
            <label>3. (2x + 3)(x - 1) = </label>
            <input type="text" id="answer3">
            <span class="answer" id="correct3">2x^2 + x - 3</span>
            <span id="result3"></span>
        </div>
        <div class="question">
            <label>4. (x - 2)(x - 3) = </label>
            <input type="text" id="answer4">
            <span class="answer" id="correct4">x^2 - 5x + 6</span>
            <span id="result4"></span>
        </div>
        <div class="question">
            <label>5. (3x + 2)(x + 4) = </label>
            <input type="text" id="answer5">
            <span class="answer" id="correct5">3x^2 + 14x + 8</span>
            <span id="result5"></span>
        </div>
        <div class="question">
            <label>6. (x + 1)(x - 1) = </label>
            <input type="text" id="answer6">
            <span class="answer" id="correct6">x^2 - 1</span>
            <span id="result6"></span>
        </div>
        <div class="question">
            <label>7. (2x - 3)(x + 2) = </label>
            <input type="text" id="answer7">
            <span class="answer" id="correct7">2x^2 + x - 6</span>
            <span id="result7"></span>
        </div>
        <div class="question">
            <label>8. (x + 5)(x + 6) = </label>
            <input type="text" id="answer8">
            <span class="answer" id="correct8">x^2 + 11x + 30</span>
            <span id="result8"></span>
        </div>
        <div class="question">
            <label>9. (x - 7)(x + 3) = </label>
            <input type="text" id="answer9">
            <span class="answer" id="correct9">x^2 - 4x - 21</span>
            <span id="result9"></span>
        </div>
        <div class="question">
            <label>10. (2x + 1)(x - 4) = </label>
            <input type="text" id="answer10">
            <span class="answer" id="correct10">2x^2 - 7x - 4</span>
            <span id="result10"></span>
        </div>
        <button type="button" onclick="checkAnswers()">Check Answers</button>
    </form>
</body>
</html>

## Double Distribution
Let's say, you don't like how FOIL is: it feels to "robotic" to you. There is another way to multiply binomials that ties in the distributive property-not a acronyms. I named this method Double Distribution, and it's very simple. 

Here it is: <img src="images/posts/maths/Dd1E.png" alt="Double Distribution Example 1">

{% include tip.html content="If you would like more examples to be included here, comment below!" %}

{% include toc.html %}

---
## Tips/Extra Help
For practicing FOIL/Double Distribution I suggest going to 
<a href="https://www.khanacademy.org/math/algebra/x2f8bb11595b61c86:quadratics-multiplying-factoring/x2f8bb11595b61c86:multiply-binomial/e/multiply-binomials-coefficient" target="_blank">Khanacademy</a>
there you will find extra practice and videos. Additionaly, I suggest studying with <a href="https://www.youtube.com/@TheOrganicChemistryTutor/search?query=Multiplying%20Binomials" target="_blank">The Organic Chemistry Teacher!</a> 

Thanks, and keep on learning!
    ~Aarushi D.

