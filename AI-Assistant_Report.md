![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | The AI Assistant Trials, who’s the Best Co-Pilot?

> :test_tube: Focus: Critical AI comparison, Prompt Engineering, Output Review

## :brain: Scenario

Your dev team is considering integrating an AI assistant into your daily workflow, but which one fits best?

You’ve been tasked with leading **“The AI Assistant Trials”**, a side-by-side comparison between:

-  **ChatGPT (Free)**  
-  **Claude (Free)**  
-  **Your pick** (if you use another AI tool like Gemini or so)

You’ll evaluate each AI by giving them the same set of coding challenges and analysing their responses.

<br />

## :dart: Learning Goals

By completing this lab, you will:

:white_check_mark: Compare AI assistants on real-world tasks   <br>
:white_check_mark: Practice prompt clarity and iteration   <br>
:white_check_mark: Learn how to critically evaluate AI suggestions   <br>
:white_check_mark: Choose the best assistant for your own dev flow

<br />

<br>

## Requirements

- Fork this repo.
- Clone this repo.

<br>

## Submission

- Upon completion, run the following commands:

```bash
git add .
git commit -m "Solved lab"
git push origin master
```

- Create a Pull Request so that your work can be checked.

<br>

## :test_tube: Tasks

Perform **3 challenges** with each AI. You must use the **same prompt** for all three.

### :white_check_mark: Task 1: Explain a Function

**Prompt:**  
> “Explain this JavaScript function in detail. Add comments as needed.”

```js
function mysteryOp(arr) {//
  return arr.reduce((acc, val) => acc ^ val, 0); //this function finds a non duplicated number in an array using XOR, this is because when duplicates meet each other in xor they cancel each other out. leaving the none duplicate to cancel out against 0, leaving it's self.
}
```

<br />

### :white_check_mark: Task 2: DOM Manipulation

**Prompt:**  
> “Write a function that changes the text of an HTML element with id `status` when a button is clicked. Use vanilla JavaScript and follow accessibility best practices.”
```js
function initStatusToggle() {
  const statusEl = document.getElementById('status');
  const button   = document.getElementById('toggle-btn');

  if (!statusEl || !button) {
    console.warn('initStatusToggle: required elements not found.');
    return;
  }

  let isActive = false;

  button.addEventListener('click', () => {
    isActive = !isActive;

    // Update visible status text
    statusEl.textContent = isActive ? 'Active' : 'Inactive';

    // Keep button label in sync with current state
    button.textContent = isActive ? 'Deactivate' : 'Activate';

    // Reflect toggle state for assistive technologies
    button.setAttribute('aria-pressed', String(isActive));
  });
}

// Run after the DOM is ready
document.addEventListener('DOMContentLoaded', initStatusToggle);
```
<br />

### :white_check_mark: Task 3: Refactor Obfuscated Code

**Prompt:**  
> “Refactor this function to make it readable and efficient. Add meaningful variable names and comments.”

```js
// Before — imperative, noisy
function sumEvenNumbers(numbers) {
  return numbers.reduce((sum, current) => {
    const isEven = current % 2 === 0;
    return isEven ? sum + current : sum;
  }, 0);
}
```

<br />

## :bar_chart: AI Evaluation Table

| AI Tool     | Task | Clarity (1–5) | Accuracy (1–5) | Speed (1–5) | Tone (1–5) | Notes |
|-------------|------|----------------|----------------|--------------|-------------|-------|
| ChatGPT     | 1    |        3       |        5       |      5       |      2      |       |
| ChatGPT     | 2    |        3       |        5       |      5       |      4      |       |
| ChatGPT     | 3    |        5       |        5       |      5       |      4      |       |
| Claude      | 1    |        5       |        5       |      3       |      5      |       |
| Claude      | 2    |        3       |        5       |      3       |      2      |       |
| Claude      | 3    |        4       |        5       |      3       |      5      |       |
| Your Pick   | 1    |     Claude     |                |              |             |       |
| Your Pick   | 2    |     ChatGPT    |                |              |             |       |
| Your Pick   | 3    |     ChatGPT    |                |              |             |       |


### AI_Assistant_Report.md

# AI Assistant Trials – Final Report

## :trophy: My Pick:
Claude

## :white_check_mark: Pros & Cons

### ChatGPT
- :white_check_mark: ChatGPT is much faster, and it's results relatively easier to understand.
- :x: Sometimes it's answers are spread out very far and it makes it harder to interpret

### Claude
- :white_check_mark: Claude has a much nicer user interface, and the style of it generating an answer
is nicer.
- :x: Claude is relatively slower than ChatGPT

### [Your Pick]
- :white_check_mark: ChatGPT

## :pushpin: Task-by-Task Highlights
- Task 1: Claude was easier to understand and gave better examples
- Task 2: ChatGPT included the possible html file while Claude didn't
- Task 3: ChatGPT recommened a less factored way to solve it which could be easier to understand, both renamed the variables. ChatGPT stuck to the for loop where Claude changed it to forEach.
## :mag: Surprises & Bugs
- No halluciantions.

## Final Thoughts
Which AI would you trust in a real project? Why?
Though both are good, I'd choose Claude. Though ChatGpt is faster, it isn't like Claude is slow, and it is much nicer to use. And both of them give good clarity over answers. So over an extended project I'd prefer Claude.
<br />

