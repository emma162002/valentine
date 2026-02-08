<!doctype html>
<html lang="it">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Valentine?</title>
  <style>
    body { font-family: system-ui, -apple-system, Segoe UI, Roboto, sans-serif; display: grid; place-items: center; min-height: 100vh; margin: 0; background: #fff; }
    .card { width: min(520px, 92vw); padding: 28px; border: 1px solid #eee; border-radius: 18px; box-shadow: 0 10px 30px rgba(0,0,0,.06); text-align: center; }
    h1 { margin: 0 0 10px; font-size: 28px; }
    p { margin: 0 0 18px; opacity: .85; }
    .btns { display: flex; gap: 12px; justify-content: center; flex-wrap: wrap; }
    button { padding: 12px 18px; border-radius: 12px; border: 1px solid #ddd; background: #fafafa; cursor: pointer; font-size: 16px; }
    button.primary { background: #111; color: #fff; border-color: #111; }
    .small { margin-top: 16px; font-size: 13px; opacity: .7; }
  </style>
</head>
<body>
  <div class="card">
    <h1 id="title">Vuoi essere il mio Valentine? 💘</h1>
    <p id="msg"></p>

    <div class="btns" id="btns">
      <button class="primary" id="yes">Sì 😍</button>
      <button id="no">No 🙈</button>
    </div>

    <div class="small" id="footer"></div>
  </div>

  <script>
    // Personalizzazione via query string, es:
    // valentine.html?from=Giulia&to=Marco&msg=Se%20dici%20s%C3%AC%20ti%20porto%20a%20cena%20😉
    const qs = new URLSearchParams(location.search);
    const from = qs.get("from") || "Io";
    const to = qs.get("to") || "";
    const customMsg = qs.get("msg") || "";

    const title = document.getElementById("title");
    const msg = document.getElementById("msg");
    const footer = document.getElementById("footer");
    const btns = document.getElementById("btns");

    title.textContent = to ? `${to}, vuoi essere il mio Valentine? 💘` : "Vuoi essere il mio Valentine? 💘";
    msg.textContent = customMsg ? customMsg : `Da: ${from} ✨`;

    function showResult(text) {
      btns.innerHTML = "";
      const p = document.createElement("p");
      p.style.fontSize = "20px";
      p.style.marginTop = "10px";
      p.textContent = text;
      btns.appendChild(p);
    }

    document.getElementById("yes").onclick = () => {
      showResult("YESSS! 🥰💞 Ci vediamo presto!");
      footer.textContent = "Screenshot e mandalo come prova 😄";
    };

    document.getElementById("no").onclick = () => {
      showResult("Ok 🙈 Però ci riprovo tra 3…2…1… 💘");
      footer.textContent = "Daiii 😄";
    };
  </script>
</body>
</html>
