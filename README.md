# My Clock Widget

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      background-color: rgb(25, 25, 25);
      color: #ffffff;
      font-family: Arial, sans-serif;
    }

    #widget {
      padding: 2vw;
      border-radius: 1vw;
      font-size: 5vw;
    }
  </style>
</head>
<body>
  <div id="widget"></div>
  <script>
    function updateDateTime() {
      const now = new Date();
      const year = now.getFullYear();
      const month = String(now.getMonth() + 1).padStart(2, '0');
      const day = String(now.getDate()).padStart(2, '0');
      const hours = String(now.getHours()).padStart(2, '0');
      const minutes = String(now.getMinutes()).padStart(2, '0');

      const dateTimeString = `${year}/${month}/${day} ${hours}:${minutes}`;
      document.getElementById('widget').innerText = dateTimeString;
    }

    setInterval(updateDateTime, 1000);
    updateDateTime();
  </script>
</body>
</html>
```html
