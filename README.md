# paskeeggjakt

<!DOCTYPE html>
<html>
<head>
  <title>Påskeegg tilgang</title>
  <style>
    body {
      background-color: #ffe4ec; /* lyserosa */
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 100px;
    }

    h1, h2 {
      color: #d63384; /* mørkerosa */
    }

    input, button {
      padding: 10px;
      font-size: 16px;
      margin-top: 10px;
    }

    .egg {
      margin-top: 40px;
    }

    /* Egg 1 farger */
    .egg1 span:nth-child(1) { color: #0077be; } /* havblå */
    .egg1 span:nth-child(2) { color: #ff8c00; } /* oransje */

    /* Egg 2 farger */
    .egg2 span:nth-child(1) { color: #8a2be2; } /* lilla */
    .egg2 span:nth-child(2) { color: #28a745; } /* grønn */
  </style>
</head>
<body>
  <h2>Skriv inn kode:</h2>
  <input type="password" id="passord">
  <button onclick="sjekk()">OK</button>

  <script>
    function sjekk() {
	  var r = atob("RU5LQUxERU5JU09MQQ==");
	  var riktig = r.split("").reverse().join("").split("").reverse().join("");
      var input = document.getElementById("passord").value;
	  
// DIN SNIK!!! IKKE NOE JUKSING!!!

      if(input === riktig) {
        document.body.innerHTML = `
          <h1>🎉 Koordinater:</h1>

          <div class="egg egg1">
            <h2>Egg 1:</h2>
            <p>
              <span>61.1479818</span>, 
              <span>10.3803779</span>
			   <span>🐣</span>
            </p>
          </div>

          <div class="egg egg2" style="margin-top: 80px;">
            <h2>Egg 2:</h2>
            <p>
              <span>61.1487495</span>, 
              <span>10.3838054</span>
			  <span>🐣</span>
            </p>
          </div>
        `;
      } else {
        alert("Feil kode!");
      }
    }
  </script>
</body>
</html>
