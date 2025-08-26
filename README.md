<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>To-Do List App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f3f4f6;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
    }
    .todo-container {
      background: white;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      width: 350px;
    }
    h1 {
      text-align: center;
      margin-bottom: 20px;
    }
    .input-row {
      display: flex;
      gap: 8px;
      margin-bottom: 15px;
    }
    input {
      flex: 1;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    button {
      padding: 8px 12px;
      border: none;
      border-radius: 6px;
      background: #2563eb;
      color: white;
      cursor: pointer;
    }
    button:hover {
      background: #1d4ed8;
    }
    ul {
      list-style: none;
      padding: 0;
      margin: 0;
    }
    li {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 8px;
      margin-bottom: 8px;
      background: #f9fafb;
      border-radius: 6px;
    }
    li.completed span {
      text-decoration: line-through;
      color: gray;
    }
    .delete-btn {
      color: red;
      cursor: pointer;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="todo-container">
    <h1>✅ To-Do List</h1>
    <div class="input-row">
      <input id="taskInput" type="text" placeholder="Add a new task..." />
      <button onclick="addTask()">Add</button>
    </div>
    <ul id="taskList"></ul>
  </div>  <script>
    const taskInput = document.getElementById("taskInput");
    const taskList = document.getElementById("taskList");

    function addTask() {
      const text = taskInput.value.trim();
      if (text === "") return;

      const li = document.createElement("li");
      const span = document.createElement("span");
      span.textContent = text;

      // toggle complete
      span.onclick = () => {
        li.classList.toggle("completed");
      };

      // delete button
      const del = document.createElement("span");
      del.textContent = "✖";
      del.className = "delete-btn";
      del.onclick = () => li.remove();

      li.appendChild(span);
      li.appendChild(del);
      taskList.appendChild(li);

      taskInput.value = "";
    }

    // allow Enter key
    taskInput.addEventListener("keydown", (e) => {
      if (e.key === "Enter") addTask();
    });
  </script></body>
</html><!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>To-Do List App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f3f4f6;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
    }
    .todo-container {
      background: white;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      width: 350px;
    }
    h1 {
      text-align: center;
      margin-bottom: 20px;
    }
    .input-row {
      display: flex;
      gap: 8px;
      margin-bottom: 15px;
    }
    input {
      flex: 1;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    button {
      padding: 8px 12px;
      border: none;
      border-radius: 6px;
      background: #2563eb;
      color: white;
      cursor: pointer;
    }
    button:hover {
      background: #1d4ed8;
    }
    ul {
      list-style: none;
      padding: 0;
      margin: 0;
    }
    li {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 8px;
      margin-bottom: 8px;
      background: #f9fafb;
      border-radius: 6px;
    }
    li.completed span {
      text-decoration: line-through;
      color: gray;
    }
    .delete-btn {
      color: red;
      cursor: pointer;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="todo-container">
    <h1>✅ To-Do List</h1>
    <div class="input-row">
      <input id="taskInput" type="text" placeholder="Add a new task..." />
      <button onclick="addTask()">Add</button>
    </div>
    <ul id="taskList"></ul>
  </div>  <script>
    const taskInput = document.getElementById("taskInput");
    const taskList = document.getElementById("taskList");

    function addTask() {
      const text = taskInput.value.trim();
      if (text === "") return;

      const li = document.createElement("li");
      const span = document.createElement("span");
      span.textContent = text;

      // toggle complete
      span.onclick = () => {
        li.classList.toggle("completed");
      };

      // delete button
      const del = document.createElement("span");
      del.textContent = "✖";
      del.className = "delete-btn";
      del.onclick = () => li.remove();

      li.appendChild(span);
      li.appendChild(del);
      taskList.appendChild(li);

      taskInput.value = "";
    }

    // allow Enter key
    taskInput.addEventListener("keydown", (e) => {
      if (e.key === "Enter") addTask();
    });
  </script></body>
</html>
