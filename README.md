<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>System Hack</title>
<style>
body {
    background-color: black;
    color: #00ff00;
    font-family: monospace;
    margin: 0;
    padding: 20px;
    overflow: hidden;
}

#terminal {
    white-space: pre-line;
    font-size: 18px;
}

.blink {
    animation: blink 1s infinite;
}

@keyframes blink {
    50% { opacity: 0; }
}

.progress {
    width: 100%;
    border: 1px solid #00ff00;
    margin-top: 20px;
}

.bar {
    width: 0%;
    height: 20px;
    background: #00ff00;
    animation: load 10s linear forwards;
}

@keyframes load {
    from { width: 0%; }
    to { width: 100%; }
}

.warning {
    color: red;
    font-size: 24px;
    text-align: center;
    margin-top: 20px;
    display: none;
}
</style>
</head>
<body>

<div id="terminal"></div>

<div class="progress">
  <div class="bar"></div>
</div>

<div class="warning" id="warning">
⚠️ تم تحميل بياناتك ⚠️<br>
جاري الإرسال...
</div>

<script>
const lines = [
"Connecting to device...",
"IP Found: 192.168.1.1",
"Bypassing security...",
"Access Granted",
"Downloading Photos...",
"Downloading Contacts...",
"Downloading Messages...",
"Uploading Data...",
];

let i = 0;
function typeLine() {
  if (i < lines.length) {
    document.getElementById("terminal").innerHTML += lines[i] + "\\n";
    i++;
    setTimeout(typeLine, 1000);
  }
}
typeLine();

setTimeout(() => {
  document.getElementById("warning").style.display = "block";
}, 10000);

setTimeout(() => {
  alert("😂 أمزح بس! ما صار شي");
}, 12000);
</script>

</body>
</html>
