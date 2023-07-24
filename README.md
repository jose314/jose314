<!DOCTYPE html>
<html>
<head>
  <title>Real-time Typing Effect</title>
  <style>
    #text-container {
      border: 1px solid #000;
      padding: 10px;
      font-family: Arial, sans-serif;
      font-size: 24px;
      white-space: nowrap;
      overflow: hidden;
    }
  </style>
</head>
<body>
  <div id="text-container">
    <h1>Hello My name is <span id="name"> </span></h1>
  </div>

  <script>
    // Replace your name with "Jose Rodriguez"
    const name = "Jose Rodriguez";
    const nameSpan = document.getElementById("name");
    let index = 0;

    function typeWriter() {
      if (index < name.length) {
        nameSpan.textContent += name.charAt(index);
        index++;
        setTimeout(typeWriter, Math.random() * 200 + 100); // Adjust the delay as needed
      }
    }

    typeWriter();
  </script>
</body>
</html>
