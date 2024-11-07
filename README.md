# retorno.github.io
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple HTML Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
        }
        .container {
            text-align: center;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #333;
        }
        p {
            color: #666;
        }
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            background-color: #007BFF;
            color: white;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Página de retorno</h1>
        <p>Página que deve ser direcionado ao final do fluxo do OPF.</p>
        <button onclick="getParamsInUrl()">Resultado</button>
        <div id="result"></div>
    </div>
    <script>
        function getParamsInUrl() {
            var url_string = window.location.href
            var url = new URL(url_string);
            var getErrorCode = url.searchParams.get("error_code");
            var myDiv = $("#result");
            var paragraph = document.createElement("p");
            paragraph.textContent = getErrorCode.toString();
            myDiv.append(paragraph);
            //alert(c);}
    </script>
</body>
</html>
