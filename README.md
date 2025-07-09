# todo-list
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
