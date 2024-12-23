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
function addToDo(event) {
  DOMSelectors.toDoList.innerHTML = "";
  const inputtedToDo = DOMSelectors.userInput.value;
  event.preventDefault();
  ToDoItems.push(inputtedToDo);
  displayToDoList(ToDoItems);
  DOMSelectors.userInput.value = "";
}
```

Selection

```JS
function displayToDoList(array) {
  array.forEach((inputs) => {
    DOMSelectors.toDoList.insertAdjacentHTML(
      "beforeend",
      `<div class="card"><div class = "to-do-card">${inputs}</div>
    <button type ="submit" class="remove-button" id="remove-reminder"> Remove </button>
    </div>`
    );
  });
  const removeButton = document.querySelectorAll(".remove-button");
  removeButton.forEach((button) => {
    button.addEventListener("click", removeToDo);
  });

  function removeToDo() {
    const specificCard = this.parentElement;
    const specificCardText =
      specificCard.querySelector(".to-do-card").textContent;

    for (let i = 0; i < ToDoItems.length; i++) {
      if (ToDoItems[i] === specificCardText) {
        ToDoItems.splice(i, 1);
        break;
      }
    }
    specificCard.remove();
  }
}

```

Iteration

```Javascript
function displayToDoList(array) {
  array.forEach((inputs) => {
    DOMSelectors.toDoList.insertAdjacentHTML(
      "beforeend",
      `<div class="card"><div class = "to-do-card">${inputs}</div>
    <button type ="submit" class="remove-button" id="remove-reminder"> Remove </button>
    </div>`
    );
  });
  const removeButton = document.querySelectorAll(".remove-button");
  removeButton.forEach((button) => {
    button.addEventListener("click", removeToDo);
  });
```

### Question 1

Programs accept input to achieve their intended functionality. **Describe at least one valid input to your program and what your program does with that input.**

- Write your responses to this question only on the designated pages in the separate Written Response booklet.
- If there are multiple parts to this question, write the part letter with your response.

```
This is an example of a iteration, an valid input for this iteration would be "Do bio homework at 7pm" the array would take the inputs provided and create cards with the value from the input.
```

---

### Question 2

Refer to your Personalized Project Reference when answering this question.

#### Part (a):

Consider the first iteration statement included in the Procedure section of your Personalized Project Reference. **Describe what is being accomplished by the code in the body of the iteration statement.**

```
The code is taking in the input from the user and putting the input in a card which is being inserted into the HTML
```

#### Part (b):

Consider the procedure identified in part (i) of the Procedure section of your Personalized Project Reference.

- Write two calls to your procedure that each cause a different code segment in the procedure to execute.
- Describe the expected behavior of each call. If it is not possible for two calls to your procedure to cause different code segments to execute, explain why this is the case for your procedure.

```
In the function RemoveToDo, it deletes the to do card if the card text length is not above 0. So if you put in a todo request and the todo is not longer than one character then it will not print a todo card.
```

#### Part (c):

Suppose another programmer provides you with a procedure called `checkValidity(value)` that:

- Returns `true` if a value passed as an argument is considered valid by the other programmer.
- Returns `false` otherwise.

Using the list identified in the List section of your Personalized Project Reference, **explain in detailed steps an algorithm that uses `checkValidity` to check whether all elements in your list are considered valid by the other programmer.** Your explanation must be detailed enough for someone else to write the program code for the algorithm that uses `checkValidity`.

- Write your responses to this question only on the designated pages in the separate Written Response booklet.
- If there are multiple parts to this question, write the part letter with your response.

```
The amount of cards made will start at 0 then for each card made the lentgth will be increased by one and when the length is greater to every addition of i then it will break the for loop.
```

---

### End of Exam
