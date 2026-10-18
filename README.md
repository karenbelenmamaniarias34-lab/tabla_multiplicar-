# tabla_multiplicar-
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Tabla de multiplicar</title>
  <style>
    body {
      background-color: blue;
      font-family: "Times New Roman", serif;
      margin: 0;
      padding: 10px;
    }
    h1 {
      color: white;
      text-align: center;
      font-size: 22px;
      margin: 5px 0 15px;
    }
    #contenedor {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 8px;
      max-width: 1000px;
      margin: 0 auto;
    }
    table {
      background-color: black;
      color: white;
      border: 3px solid #b0b0d0;
      border-collapse: collapse;
      font-size: 14px;
    }
    td {
      padding: 2px 6px;
      text-align: center;
      white-space: nowrap;
    }
  </style>
</head>
<body>
  <h1>Tabla de multiplicar</h1>
  <div id="contenedor"></div>

  <script>
    var contenedor = document.getElementById("contenedor");

    // tablas del 1 al 9
    for (var i = 1; i <= 9; i++) {
      var tabla = document.createElement("table");

      // multiplicamos del 1 al 10
      for (var j = 1; j <= 10; j++) {
        var fila = document.createElement("tr");
        var celda = document.createElement("td");
        celda.textContent = i + " x " + j + " = " + (i * j);
        fila.appendChild(celda);
        tabla.appendChild(fila);
      }

      contenedor.appendChild(tabla);
    }
  </script>
</body>
</html>
