# 2024 AP Computer Science Principles Free-Response Questions: Set 1

## AP® Computer Science Principles Written Response Prompts

### Instructions:

- **Time:** 1 hour
- **Questions:** 2
- Read each question carefully and completely.
- Write your response in the space provided for each question in the Written Response booklet.
- You may plan your answers in this orange booklet, but no credit will be given for anything written in this booklet. You will only earn credit for what you write in the separate Written Response booklet.

---

### Pre-FRQ Practice

## Identify the Algorithm present in the JavaScript Files.

### Aspects of Algorithm

Sequencing

```JS
 async function main() {
 const api = 'https://opentdb.com/api.php?amount=50&type=boolean'
 const response = await fetch(api)
 const data = await response.json()


 const qa = data.results.map(question =>
     ({
     question: question.question,
     correct: question.correct_answer,
     incorrect: question.incorrect_answers
     })
     )
     game(qa)
 }
```

Selection

```JS
 function game(qa) {
     let i = 0
     const used = []

     DOMSelectors.form.addEventListener('submit', function(event) {
         event.preventDefault()
         const input = DOMSelectors.input.value;
         displayQuestion(input)
     });

     function displayQuestion(input) {
         if (i < input) {
             let q = qa[i]
             console.log(q)
             clear()
             DOMSelectors.question.insertAdjacentHTML("beforeend", `<h1>${q.question}</h1>`)
         }

     }
 DOMSelectors.true.addEventListener('click', function(event) {
         event.preventDefault()
             let answer = "True"
             checkAnswer(answer)
             displayQuestion(DOMSelectors.input.value)
             console.log(DOMSelectors.input.value)
     });

     DOMSelectors.false.addEventListener('click', function(event) {
         event.preventDefault()
             let answer = "False"
             checkAnswer(answer)
             displayQuestion(DOMSelectors.input.value)
             console.log(DOMSelectors.input.value)
         }
     );


```

Iteration

```Javascript
     function checkAnswer(answer) {
         let q = qa[i]
         if (q.correct.includes(answer)) {
            used.push("Correct")
         }
         else {
            used.push("Incorrect")
         }
         i++
         if (i === Number(DOMSelectors.input.value)){final(used)}
     }
     function final(array){
        let a = 0
        let b = 0
        for (let i = 0; i < array.length; i++){
         if (array[i].includes("Correct")) {a++}
         if (array[i].includes("Incorrect")) {b++}}
         clear()
         const correct = a * 100/DOMSelectors.input.value
         const incorrect = b * 100/DOMSelectors.input.value
         DOMSelectors.question.insertAdjacentHTML("beforeend", `<h1>You got ${correct}% of them right and ${incorrect}% of them wrong!</h1>`)
        }
 }

```

### Question 1

Programs accept input to achieve their intended functionality. **Describe at least one valid input to your program and what your program does with that input.**

- Write your responses to this question only on the designated pages in the separate Written Response booklet.
- If there are multiple parts to this question, write the part letter with your response.

```
This is an example of a iteration, an valid input for this iteration would be by inputting the correct answer and then at the very end it will iterate through all the correct and incorrect questions to find the score the player got.
```

---

### Question 2

Refer to your Personalized Project Reference when answering this question.

#### Part (a):

Consider the first iteration statement included in the Procedure section of your Personalized Project Reference. **Describe what is being accomplished by the code in the body of the iteration statement.**

```
The code is taking in the input from the user and putting the input in a array which then is used to calculate the users score
```

#### Part (b):

Consider the procedure identified in part (i) of the Procedure section of your Personalized Project Reference.

- Write two calls to your procedure that each cause a different code segment in the procedure to execute.
- Describe the expected behavior of each call. If it is not possible for two calls to your procedure to cause different code segments to execute, explain why this is the case for your procedure.

```
In the function check answer and if it is correct then the question will be deemed as correct ad else it will be incorrect.
```

#### Part (c):

Suppose another programmer provides you with a procedure called `checkValidity(value)` that:

- Returns `true` if a value passed as an argument is considered valid by the other programmer.
- Returns `false` otherwise.

Using the list identified in the List section of your Personalized Project Reference, **explain in detailed steps an algorithm that uses `checkValidity` to check whether all elements in your list are considered valid by the other programmer.** Your explanation must be detailed enough for someone else to write the program code for the algorithm that uses `checkValidity`.

- Write your responses to this question only on the designated pages in the separate Written Response booklet.
- If there are multiple parts to this question, write the part letter with your response.

```
If the input for a question is correct then the answer will be marked true and if the question is chosen to be false then the answer will be marked false.
```

---

### End of Exam
