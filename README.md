todo-list
تطبيق مذكرة مهام يومية باستخدام HTML و CSS و JavaScript.
<!DOCTYPE html>
<html>
<head>
  <title>قائمة المهام</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>📋 قائمة المهام</h1>
  <input type="text" id="taskInput" placeholder="أدخل مهمة جديدة">
  <button onclick="addTask()">➕ أضف</button>
  <ul id="taskList"></ul>
  <script src="script.js"></script>
</body>
</html>
body {
  font-family: Arial;
  background: #f2f2f2;
  text-align: center;
  padding: 20px;
}

input, button {
  padding: 10px;
  margin: 5px;
}

li {
  list-style: none;
  background: #fff;
  margin: 5px;
  padding: 10px;
  border-radius: 5px;
}
function addTask() {
  const taskText = document.getElementById("taskInput").value;
  if (taskText === "") return;

  const li = document.createElement("li");
  li.textContent = taskText;

  li.onclick = function () {
    this.remove(); // احذف المهمة عند الضغط عليها
  };

  document.getElementById("taskList").appendChild(li);
  document.getElementById("taskInput").value = "";
}
