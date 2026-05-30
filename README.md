index.html// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
import { getAnalytics } from "firebase/analytics";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
// For Firebase JS SDK v7.20.0 and later, measurementId is optional
const firebaseConfig = {
  apiKey: "AIzaSyDuUi90WzChIqWbKkOlAEUvipOdmGskq0s",
  authDomain: "traderwin-31a54.firebaseapp.com",
  projectId: "traderwin-31a54",
  storageBucket: "traderwin-31a54.firebasestorage.app",
  messagingSenderId: "1023266862923",
  appId: "1:1023266862923:web:ab44e35cdb2f599a061ace",
  measurementId: "G-RLM0MY8THJ"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);<!DOCTYPE html>
<html>
<head>
  <title>TraderWin</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

dashboard.html<!DOCTYPE html>
<html>

<head>
  <title>TraderWin Pro</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>

<!-- SIDEBAR -->

<div class="sidebar">

  <h1>TW</h1>

  <button>Dashboard</button>
  <button>Bots</button>
  <button>Signals</button>
  <button>Markets</button>
  <button>Settings</button>

</div>

<!-- MAIN CONTENT -->

<div class="main">

<header>

<div>

<h2>TraderWin Pro</h2>

<p id="clock"></p>

</div>

<div class="top-buttons">

<button class="deposit-btn"
onclick="window.location.href='deposit.html'">
Deposit
</button>
Deposit
</button>

<button class="withdraw-btn"
onclick="window.location.href='withdraw.html'">
Withdraw
</button>

</div>

</header>

<!-- BALANCE -->

<section class="balance-card">
<section class="market-grid">

<div class="market-card">
<h3>EUR/USD</h3>
<p class="up">+1.25%</p>
</div>

<div class="market-card">
<h3>BTC/USD</h3>
<p class="down">-0.42%</p>
</div>

<div class="market-card">
<h3>Volatility 75</h3>
<p class="up">+3.12%</p>
</div>

</section>
<div>
<h3>Account Balance</h3>
<h1 id="balance">$0.00</h1>
</div>

<div class="profit-box">
+12.6%
</div>

</section>

<!-- DERIV -->

<section class="signal-card">

<h2>Deriv Connection</h2>

<p id="connectionStatus">
Not Connected
</p>

<button onclick="connectDeriv()">
Connect Deriv
</button>

</section>

<!-- LIVE MARKET -->

<section class="chart-card">

<h2>Live Market</h2>

<iframe
src="https://s.tradingview.com/widgetembed/?symbol=FX:EURUSD&interval=1"
height="450">
</iframe>

</section>

<!-- AI SIGNALS<section class="history-card">

<h2>Recent Trades</h2>

<div class="trade-item">
<span>BUY V75</span>
<span class="profit">+$42</span>
</div>

<div class="trade-item">
<span>SELL EUR/USD</span>
<span class="loss">-$12</span>
</div>

<div class="trade-item">
<span>BUY BTC/USD</span>
<span class="profit">+$105</span>
</div>

</section> -->

<section class="signal-card">

<h2>AI Trading Signal</h2>

<h1 id="signalText">
WAIT
</h1>

<button onclick="generateSignal()">
Generate Signal
</button>

</section>

<!-- BUY SELL -->

<section class="trading-panel">
<section class="history-card">

<h2>Live Trader Activity</h2>
<section class="history-card">

<h2>Bot Builder</h2>
<section class="history-card">

<h2>Running Bots</h2>
<section class="history-card">

<h2>Trading Statistics</h2>

<div class="market-grid">

<div class="market-card">
<h3>Total Trades</h3>
<p class="up" id="totalTrades">
0
</p>
</div>

<div class="market-card">
<h3>Total Profit</h3>
<p class="up" id="totalProfit">
$0
</p>
</div>

<div class="market-card">
<h3>Win Rate</h3>
<p class="up" id="winRate">
0%
</


<div class="trade-item">
<span>AI Sniper Bot</span>
<span class="profit">RUNNING</span>
</div>

</div>

</section>
<input
type="text"
id="botName"
placeholder="Bot Name"
>

<select id="botStrategy">

<option>Trend Following</option>
<option>Scalping</option>
<option>Breakout</option>
<option>AI Momentum</option>

</select>

<select id="botRisk">

<option>Low Risk</option>
<option>Medium Risk</option>
<option>High Risk</option>

</select>

<button onclick="createBot()">
Create Bot
</button>

</section>
<div id="liveFeed">
<div id="botList">

<div class="trade-item">

<div>

<span>AI Sniper Bot</span>

<br>

<small>
Scalping | Medium Risk
</small>

</div>

<div>

<button onclick="stopBot(this)"
class="stop-btn">
STOP
</button>

</div>

</div>

</div>
<div class="trade-item">
<span>Mike bought V75</span>
<span class="profit">+$25</span>
</div>

</div>

</section>
<h2>Quick Trade</h2>

<select id="assetSelect">

<option>Volatility 75</option>
<option>Volatility 50</option>
<option>EUR/USD</option>
<option>BTC/USD</option>

</select>

<input
type="number"
id="tradeAmount"
placeholder="Enter Amount"
value="10"
>

<select id="tradeTime">

<option>1 Minute</option>
<option>5 Minutes</option>
<option>15 Minutes</option>

</select>

<div class="trade-buttons">

<button class="buy-btn" onclick="placeTrade('BUY')">
BUY
</button>

<button class="sell-btn" onclick="placeTrade('SELL')">
SELL
</button>

</div>

</section>

<button class="buy-btn">
BUY
</button>

<button class="sell-btn">
SELL
</button>

</section>

<!-- FLOATING AI -->

<div class="ai-float">
AI
</div>

</div>

<script src="script.js"></script>

</body>
</html>
style.css/* STOP BUTTON */

.stop-btn{
  background:#d50000;
  color:white;
  border:none;
  padding:10px 15px;
  border-radius:10px;
}

/* BOT STATUS */

.running{
  color:#00ff95;
  font-weight:bold;
}

.stopped{
  color:#ff5252;
  font-weight:bold;
}/* BOT BUILDER */

.history-card input,
.history-card select{
  width:100%;
  margin-top:15px;
  padding:15px;
  border:none;
  border-radius:15px;
  background:#1f2937;
  color:white;
  font-size:16px;
}

.history-card button{
  width:100%;
  margin-top:15px;
  padding:15px;
  border:none;
  border-radius:15px;
  background:#6c5ce7;
  color:white;
  font-size:16px;
  font-weight:bold;
}/* TRADING PANEL */

.trading-panel{
  margin-top:20px;
  background:#111827;
  padding:20px;
  border-radius:25px;
}

.trading-panel select,
.trading-panel input{
  width:100%;
  margin-top:15px;
  padding:15px;
  border:none;
  border-radius:15px;
  background:#1f2937;
  color:white;
  font-size:16px;
}

/* FEED */

#liveFeed{
  margin-top:15px;
}/* MARKET GRID */

.market-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
  gap:15px;
  margin-top:20px;
}

.market-card{
  background:#111827;
  padding:20px;
  border-radius:20px;
  text-align:center;
  box-shadow:0 0 20px rgba(0,255,174,0.05);
}

.market-card h3{
  margin:0;
}

.up{
  color:#00ff95;
  font-size:22px;
  font-weight:bold;
}

.down{
  color:#ff5252;
  font-size:22px;
  font-weight:bold;
}

/* HISTORY */

.history-card{
  margin-top:20px;
  background:#111827;
  padding:20px;
  border-radius:25px;
}

.trade-item{
  display:flex;
  justify-content:space-between;
  margin-top:15px;
  padding:15px;
  background:#1f2937;
  border-radius:15px;
}

.profit{
  color:#00ff95;
  font-weight:bold;
}

.loss{
  color:#ff5252;
  font-weight:bold;
}

/* GLOW EFFECT */

.signal-card,
.balance-card,
.chart-card,
.history-card,
.market-card{
  transition:0.3s;
}

.signal-card:hover,
.balance-card:hover,
.chart-card:hover,
.history-card:hover,
.market-card:hover{
  transform:translateY(-3px);
  box-shadow:0 0 25px rgba(0,255,174,0.15);
}

/* MOBILE */

@media(max-width:768px){

  .sidebar{
    width:80px;
    padding:10px;
  }

  .sidebar h1{
    font-size:20px;
  }

  .sidebar button{
    font-size:11px;
    padding:10px;
  }

  .main{
    margin-left:90px;
    padding:10px;
  }

  .balance-card{
    flex-direction:column;
    align-items:flex-start;
  }

  .trade-buttons{
    flex-direction:column;
  }

}body{
  margin:0;
  font-family:Arial;
  background:#070b14;
  color:white;
  display:flex;
}

/* SIDEBAR */

.sidebar{
  width:220px;
  background:#0f172a;
  height:100vh;
  padding:20px;
  position:fixed;
  left:0;
  top:0;
}

.sidebar h1{
  color:#00ffae;
  text-align:center;
  margin-bottom:40px;
}

.sidebar button{
  width:100%;
  margin-top:15px;
  padding:15px;
  background:#111827;
  border:none;
  border-radius:12px;
  color:white;
  font-size:15px;
}

/* MAIN */

.main{
  margin-left:240px;
  width:100%;
  padding:20px;
}

/* HEADER */

header{
  display:flex;
  justify-content:space-between;
  align-items:center;
}

header h2{
  color:#00ffae;
}

.top-buttons button{
  padding:12px 18px;
  border:none;
  border-radius:12px;
  color:white;
  margin-left:10px;
}

.deposit-btn{
  background:#00b894;
}

.withdraw-btn{
  background:#6c5ce7;
}

/* BALANCE */

.balance-card{
  margin-top:20px;
  background:linear-gradient(135deg,#111827,#1f2937);
  border-radius:25px;
  padding:25px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  box-shadow:0 0 20px rgba(0,255,174,0.1);
}

.balance-card h1{
  color:#00ffae;
  font-size:42px;
}

.profit-box{
  background:#00b894;
  padding:12px 18px;
  border-radius:15px;
  font-weight:bold;
}

/* CARDS */

.signal-card,
.chart-card{
  margin-top:20px;
  background:#111827;
  padding:20px;
  border-radius:25px;
  box-shadow:0 0 20px rgba(0,0,0,0.3);
}

.signal-card h1{
  color:#00ffae;
  font-size:50px;
  text-align:center;
}

.signal-card button{
  width:100%;
  padding:15px;
  border:none;
  border-radius:15px;
  background:#00b894;
  color:white;
  font-size:16px;
}

iframe{
  width:100%;
  border:none;
  border-radius:20px;
}

/* BUY SELL */

.trade-buttons{
  display:flex;
  gap:15px;
  margin-top:20px;
}

.buy-btn,
.sell-btn{
  flex:1;
  padding:18px;
  border:none;
  border-radius:18px;
  color:white;
  font-size:20px;
  font-weight:bold;
}

.buy-btn{
  background:linear-gradient(45deg,#00c853,#00ff95);
}

.sell-btn{
  background:linear-gradient(45deg,#d50000,#ff5252);
}

/* FLOAT AI */

.ai-float{
  position:fixed;
  right:30px;
  bottom:30px;
  width:70px;
  height:70px;
  background:#6c5ce7;
  border-radius:50%;
  display:flex;
  justify-content:center;
  align-items:center;
  font-size:24px;
  font-weight:bold;
  box-shadow:0 0 20px rgba(108,92,231,0.5);
}
script.js/* DEPOSIT */

function submitDeposit(){

  let name =
    document.getElementById(
      "depositName"
    ).value;

  let amount =
    document.getElementById(
      "depositAmount"
    ).value;

  let code =
    document.getElementById(
      "depositCode"
    ).value;

  if(
    name === "" ||
    amount === "" ||
    code === ""
  ){

    showNotification(
      "Fill all fields"
    );

    return;

  }

  showNotification(
    "Deposit Submitted"
  );

}

/* WITHDRAW */

function requestWithdraw(){

  let number =
    document.getElementById(
      "withdrawNumber"
    ).value;

  let amount =
    document.getElementById(
      "withdrawAmount"
    ).value;

  if(
    number === "" ||
    amount === ""
  ){

    showNotification(
      "Fill all fields"
    );

    return;

  }

  showNotification(
    "Withdrawal Requested"
  );

}/* ADMIN SIGNAL */

function sendAdminSignal(){

  let signal =
    document.getElementById(
      "adminSignal"
    ).value;

  showNotification(

    "Admin Signal Sent: " +
    signal

  );

}/* BOT STOP */

function stopBot(button){

  let item =
    button.parentElement.parentElement;

  item.style.opacity = "0.5";

  button.innerHTML = "STOPPED";

  button.disabled = true;

  showNotification(
    "Bot Stopped"
  );

}

/* TRADING STATS */

let totalTrades = 0;
let totalProfit = 0;
let wins = 0;

/* AUTO BOT TRADING */

function autoBotTrading(){

  totalTrades++;

  let win =
    Math.random() > 0.4;

  if(win){

    let profit =
      Math.floor(Math.random()*100);

    totalProfit += profit;

    wins++;

  }else{

    let loss =
      Math.floor(Math.random()*50);

    totalProfit -= loss;

  }

  let winRate =
    Math.floor(
      (wins / totalTrades) * 100
    );

  document.getElementById(
    "totalTrades"
  ).innerHTML =
    totalTrades;

  document.getElementById(
    "totalProfit"
  ).innerHTML =
    "$" + totalProfit;

  document.getElementById(
    "winRate"
  ).innerHTML =
    winRate + "%";

}

/* AUTO UPDATE */

setInterval(autoBotTrading,6000);/* LOGIN */

function login(){

  window.location.href =
    "dashboard.html";

}

/* NOTIFICATIONS */

function showNotification(message){

  let notify =
    document.createElement("div");

  notify.innerHTML = message;

  notify.style.position = "fixed";
  notify.style.top = "20px";
  notify.style.right = "20px";
  notify.style.background = "#00b894";
  notify.style.color = "white";
  notify.style.padding = "15px";
  notify.style.borderRadius = "12px";
  notify.style.zIndex = "9999";
  notify.style.boxShadow =
    "0 0 15px rgba(0,0,0,0.3)";

  document.body.appendChild(notify);

  setTimeout(() => {

    notify.remove();

  },3000);

}

/* AI SIGNALS */

function generateSignal(){

  let signals = [

    "BUY",
    "SELL",
    "WAIT",
    "STRONG BUY",
    "STRONG SELL"

  ];

  let random =
    signals[Math.floor(
      Math.random()*signals.length
    )];

  document.getElementById(
    "signalText"
  ).innerHTML = random;

  showNotification(
    "New AI Signal: " + random
  );

}

/* AUTO SIGNALS */

setInterval(() => {

  let signal =
    document.getElementById(
      "signalText"
    );

  if(signal){

    generateSignal();

  }

},10000);

/* DERIV CONNECTION */

function connectDeriv(){

  let status =
    document.getElementById(
      "connectionStatus"
    );

  let balance =
    document.getElementById(
      "balance"
    );

  if(status){

    status.innerHTML =
      "Connected Successfully";

  }

  if(balance){

    balance.innerHTML =
      "$" +
      (Math.floor(
        Math.random()*5000
      ) + 1000);

  }

  showNotification(
    "Connected to Deriv"
  );

}

/* BUY / SELL TRADING */

function placeTrade(type){

  let asset =
    document.getElementById(
      "assetSelect"
    );

  let amount =
    document.getElementById(
      "tradeAmount"
    );

  if(!asset || !amount){

    showNotification(
      type + " Order Placed"
    );

    return;

  }

  showNotification(

    type +
    " " +
    asset.value +
    " $" +
    amount.value

  );

  setTimeout(() => {

    let win =
      Math.random() > 0.5;

    if(win){

      showNotification(
        "Trade Won"
      );

    }else{

      showNotification(
        "Trade Lost"
      );

    }

  },4000);

}

/* LIVE FEED */

function updateFeed(){

  let feed =
    document.getElementById(
      "liveFeed"
    );

  if(!feed) return;

  let traders = [

    "Mike",
    "Sarah",
    "Alex",
    "John",
    "Daniel"

  ];

  let assets = [

    "BTC/USD",
    "EUR/USD",
    "V75",
    "V50"

  ];

  let trader =
    traders[Math.floor(
      Math.random()*traders.length
    )];

  let asset =
    assets[Math.floor(
      Math.random()*assets.length
    )];

  let amount =
    Math.floor(
      Math.random()*100
    );

  let div =
    document.createElement("div");

  div.className = "trade-item";

  div.innerHTML =

    "<span>" +
    trader +
    " traded " +
    asset +
    "</span>" +

    "<span class='profit'>+$" +
    amount +
    "</span>";

  feed.prepend(div);

}

/* AUTO FEED */

setInterval(updateFeed,5000);

/* BOT BUILDER */

function createBot(){

  let botName =
    document.getElementById(
      "botName"
    );

  let strategy =
    document.getElementById(
      "botStrategy"
    );

  let risk =
    document.getElementById(
      "botRisk"
    );

  if(!botName){

    return;

  }

  if(botName.value === ""){

    showNotification(
      "Enter Bot Name"
    );

    return;

  }

  let botList =
    document.getElementById(
      "botList"
    );

  if(botList){

    let div =
      document.createElement("div");

    div.className =
      "trade-item";

    div.innerHTML =

      "<span>" +

      botName.value +

      "<br><small>" +

      strategy.value +

      " | " +

      risk.value +

      "</small></span>" +

      "<span class='profit'>RUNNING</span>";

    botList.prepend(div);

  }

  showNotification(
    botName.value +
    " Bot Started"
  );

  botName.value = "";

}

/* FLOATING AI BUTTON */

window.onload = function(){

  let ai =
    document.querySelector(
      ".ai-float"
    );

  if(ai){

    ai.onclick = function(){

      showNotification(
        "AI Assistant Activated"
      );

    };

  }

};
admin.html<!DOCTYPE html>
<html>

<head>
  <title>TraderWin Admin</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>

<div class="sidebar">

<h1>ADMIN</h1>

<button>Dashboard</button>
<button>Users</button>
<button>Bots</button>
<button>Signals</button>
<button>Deposits</button>
<button onclick="window.location.href='admin.html'">
Admin
</button>

</div>

<div class="main">

<header>

<h2>TraderWin Admin Panel</h2>

<button class="deposit-btn">
Logout
</button>

</header>

<!-- STATS -->

<section class="market-grid">

<div class="market-card">
<h3>Total Users</h3>
<p class="up">1,245</p>
</div>

<div class="market-card">
<h3>Total Deposits</h3>
<p class="up">$52,340</p>
</div>

<div class="market-card">
<h3>Running Bots</h3>
<p class="up">328</p>
</div>

<div class="market-card">
<h3>Signals Sent</h3>
<p class="up">1,892</p>
</div>

</section>

<!-- SIGNAL CONTROL -->

<section class="history-card">

<h2>Send Trading Signal</h2>

<select id="adminSignal">

<option>BUY</option>
<option>SELL</option>
<option>WAIT</option>
<option>STRONG BUY</option>
<option>STRONG SELL</option>

</select>

<button onclick="sendAdminSignal()">
Send Signal
</button>

</section>

<!-- USER TABLE -->

<section class="history-card">

<h2>Recent Users</h2>

<div class="trade-item">
<span>Michael</span>
<span class="profit">$500 Deposit</span>
</div>

<div class="trade-item">
<span>Sarah</span>
<span class="profit">$1200 Deposit</span>
</div>

<div class="trade-item">
<span>Alex</span>
<span class="loss">Pending Withdrawal</span>
</div>

</section>

<!-- BOT CONTROL -->

<section class="history-card">

<h2>Bot Management</h2>

<div class="trade-item">

<span>AI Sniper Bot</span>

<button class="stop-btn">
Disable
</button>

</div>

<div class="trade-item">

<span>Trend Master Bot</span>

<button class="stop-btn">
Disable
</button>

</div>

</section>

</div>

<script src="script.js"></script>

</body>
</html>
deposit.html<!DOCTYPE html>
<html>

<head>
  <title>Deposit</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>

<div class="main">

<header>

<h2>Deposit Funds</h2>

<button class="deposit-btn"
onclick="window.location.href='dashboard.html'">
Back
</button>

</header>

<section class="history-card">

<h2>M-Pesa Deposit</h2>

<p>
Send money to:
</p>

<h1 style="color:#00ffae;">
0712345678
</h1>

<input
type="text"
id="depositName"
placeholder="Your Name"
>

<input
type="number"
id="depositAmount"
placeholder="Amount"
>

<input
type="text"
id="depositCode"
placeholder="M-Pesa Code"
>

<button onclick="submitDeposit()">
Submit Deposit
</button>

</section>

</div>

<script src="script.js"></script>

</body>
</html>
withdraw.html<!DOCTYPE html>
<html>

<head>
  <title>Withdraw</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>

<div class="main">

<header>

<h2>Withdraw Funds</h2>

<button class="deposit-btn"
onclick="window.location.href='dashboard.html'">
Back
</button>

</header>

<section class="history-card">

<h2>Request Withdrawal</h2>

<input
type="text"
id="withdrawNumber"
placeholder="M-Pesa Number"
>

<input
type="number"
id="withdrawAmount"
placeholder="Amount"
>

<button onclick="requestWithdraw()">
Request Withdrawal
</button>

</section>

</div>

<script src="script.js"></script>

</body>
</html>
