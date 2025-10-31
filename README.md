# Ex03 To-Do List using JavaScript

# Register Number:212223040226
## Name: Tarun S

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
todo.html
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>To-Do List</title>
<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: "Poppins", sans-serif;
    }

    body {
        background: linear-gradient(135deg, #4facfe, #00f2fe);
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .container {
        background: #fff;
        width: 350px;
        border-radius: 12px;
        padding: 20px;
        box-shadow: 0 6px 20px rgba(0,0,0,0.2);
    }

    h2 {
        text-align: center;
        margin-bottom: 15px;
        color: #333;
    }

    .inputArea {
        display: flex;
        gap: 8px;
        margin-bottom: 15px;
    }

    input {
        flex: 1;
        padding: 10px;
        font-size: 16px;
        border: 2px solid #4facfe;
        border-radius: 8px;
        outline: none;
    }

    button {
        padding: 10px 16px;
        border: none;
        background: #4facfe;
        color: white;
        font-weight: bold;
        border-radius: 8px;
        cursor: pointer;
        transition: 0.2s;
    }

    button:hover {
        background: #007bff;
    }

    ul {
        list-style: none;
        margin-top: 10px;
    }

    li {
        background: #f7f7f7;
        padding: 10px;
        border-radius: 6px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 8px;
        cursor: pointer;
        transition: 0.2s;
    }

    li.completed {
        text-decoration: line-through;
        opacity: 0.6;
    }

    span {
        color: red;
        font-weight: bold;
        cursor: pointer;
    }

    li:hover {
        background: #e9e9e9;
    }
</style>
</head>
<body>

<div class="container">
    <h2>✅ To-Do List</h2>

    <div class="inputArea">
        <input type="text" id="taskInput" placeholder="Enter task">
        <button onclick="addTask()">Add</button>
    </div>

    <ul id="taskList"></ul>
</div>

<script>
function addTask() {
    let input = document.getElementById("taskInput");
    let task = input.value.trim();

    if (task === "") {
        alert("Enter a task!");
        return;
    }

    let li = document.createElement("li");
    li.innerHTML = `${task} <span onclick="removeTask(this)">✖</span>`;
    li.onclick = function(event) {
        if (event.target.tagName !== "SPAN") {
            this.classList.toggle("completed");
        }
    };

    document.getElementById("taskList").appendChild(li);
    input.value = "";
}

function removeTask(element) {
    element.parentElement.remove();
}
</script>

</body>
</html>

```
## OUTPUT

<img width="1857" height="907" alt="Screenshot 2025-10-31 153307" src="https://github.com/user-attachments/assets/95bec7d9-2b55-44b1-8063-3f8853c800b2" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
