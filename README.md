# trading-app
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<title>RTR — Risk To Reward</title>

<style>
:root{
  --bg:#070b10;
  --panel:#0f151d;
  --panel2:#151d27;
  --line:#25303d;
  --text:#f5f7fa;
  --muted:#8793a3;
  --green:#39d98a;
  --red:#ff6471;
}

*{box-sizing:border-box}

body{
  margin:0;
  background:radial-gradient(circle at 20% 0,#13221c 0,#070b10 35%);
  color:var(--text);
  font:15px Inter,system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;
}

button,input,select,textarea{font:inherit}

button{cursor:pointer}

.wrap{
  max-width:1180px;
  margin:auto;
  padding:18px;
}

.brand{
  display:flex;
  align-items:center;
  gap:10px;
  font-weight:900;
  letter-spacing:.5px;
}

.mark{
  width:42px;
  height:42px;
  border-radius:12px;
  background:linear-gradient(135deg,#39d98a,#187c53);
  display:grid;
  place-items:center;
  color:#06120c;
  font-weight:1000;
  font-size:18px;
}

.sub{
  font-size:10px;
  color:#9ba6b5;
  letter-spacing:1.8px;
  margin-top:2px;
}

header{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:20px;
}

.top-actions{
  display:flex;
  gap:8px;
}

.btn{
  background:var(--green);
  color:#06120c;
  border:0;
  border-radius:11px;
  padding:11px 15px;
  font-weight:850;
}

.btn.dark{
  background:var(--panel2);
  color:#fff;
  border:1px solid var(--line);
}

.tabs{
  display:flex;
  gap:7px;
  overflow:auto;
  margin-bottom:18px;
}

.tab{
  border:1px solid var(--line);
  background:var(--panel);
  color:#aeb8c5;
  border-radius:10px;
  padding:10px 14px;
  white-space:nowrap;
}

.tab.active{
  background:var(--green);
  border-color:var(--green);
  color:#06120c;
  font-weight:800;
}

.hero{
  background:linear-gradient(135deg,#101a19,#10151d 55%,#0d1219);
  border:1px solid var(--line);
  border-radius:20px;
  padding:22px;
  margin-bottom:14px;
}

.eyebrow{
  font-size:11px;
  color:var(--green);
  font-weight:800;
  letter-spacing:1.5px;
}

.hero h1{
  font-size:30px;
  margin:7px 0;
}

.hero p{
  color:var(--muted);
  margin:0;
  max-width:700px;
}

.grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:12px;
}

.card{
  background:rgba(15,21,29,.92);
  border:1px solid var(--line);
  border-radius:16px;
  padding:16px;
}

.label{
  font-size:11px;
  color:var(--muted);
  text-transform:uppercase;
  letter-spacing:.8px;
}

.value{
  font-size:26px;
  font-weight:900;
  margin-top:7px;
}

.green{color:var(--green)}
.red{color:var(--red)}
.muted{color:var(--muted)}

.section{
  margin-top:14px;
}

.section-title{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:10px;
}

.section-title h2{
  font-size:17px;
  margin:0;
}

.table-wrap{
  overflow:auto;
}

.table{
  width:100%;
  border-collapse:collapse;
}

.table th,
.table td{
  text-align:left;
  padding:12px;
  border-bottom:1px solid var(--line);
  white-space:nowrap;
}

.table th{
  font-size:11px;
  color:var(--muted);
  text-transform:uppercase;
}

.pill{
  padding:5px 8px;
  border-radius:999px;
  background:#19232e;
  font-size:11px;
}

.good{
  background:#103523;
  color:#72e6aa;
}

.bad{
  background:#35151b;
  color:#ff8790;
}

.profile{
  display:grid;
  grid-template-columns:1fr;
  gap:12px;
}

.bars{
  display:grid;
  gap:12px;
}

.barrow{
  display:grid;
  grid-template-columns:85px 1fr 38px;
  gap:9px;
  align-items:center;
  font-size:12px;
}

.bar{
  height:9px;
  background:#1a232d;
  border-radius:99px;
  overflow:hidden;
}

.fill{
  height:100%;
  background:var(--green);
  border-radius:99px;
}

.form{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:12px;
}

.field label{
  display:block;
  color:var(--muted);
  font-size:12px;
  margin-bottom:6px;
}

.field input,
.field select,
.field textarea{
  width:100%;
  background:#090e14;
  border:1px solid var(--line);
  border-radius:10px;
  color:#fff;
  padding:12px;
}

.field textarea{
  min-height:90px;
  resize:vertical;
}

.full{
  grid-column:1/-1;
}

.hidden{
  display:none !important;
}

.login{
  min-height:100vh;
  display:grid;
  place-items:center;
  padding:20px;
}

.loginbox{
  width:min(430px,100%);
  background:rgba(15,21,29,.96);
  border:1px solid var(--line);
  border-radius:22px;
  padding:25px;
}

.loginbox h1{
  margin:18px 0 4px;
}

.loginbox p{
  color:var(--muted);
}

.loginbox .field{
  margin:12px 0;
}

.wide{
  width:100%;
  margin-top:6px;
}

.small{
  font-size:12px;
}

.click{
  cursor:pointer;
}

.click:hover{
  background:#121c26;
}

.message{
  margin-top:12px;
  padding:10px;
  border-radius:10px;
  background:#35151b;
  color:#ff8790;
  display:none;
}

@media(max-width:800px){
  .grid{
    grid-template-columns:repeat(2,1fr);
  }

  .form{
    grid-template-columns:1fr;
  }

  .hero h1{
    font-size:25px;
  }
}

@media(max-width:500px){
  .wrap{
    padding:12px;
  }

  .grid{
    grid-template-columns:1fr 1fr;
  }

  .value{
    font-size:22px;
  }

  .top-actions .dark{
    display:none;
  }
}
</style>
</head>

<body>

<!-- LOGIN -->
<div id="login" class="login">

  <div class="loginbox">

    <div class="brand">
      <div class="mark">R</div>
      <div>
        <div>RTR</div>
        <div class="sub">RISK TO REWARD</div>
      </div>
    </div>

    <h1>Welcome to RTR</h1>

    <p>
      Trading performance, risk management and psychology —
      all in one place.
    </p>

    <div class="field">
      <label for="email">Email</label>
      <input
        id="email"
        type="email"
        value="coach@rtr.demo"
        autocomplete="username"
      >
    </div>

    <div class="field">
      <label for="password">Password</label>
      <input
        id="password"
        type="password"
        value="demo"
        autocomplete="current-password"
      >
    </div>

    <button
      id="loginButton"
      class="btn wide"
      type="button"
    >
      Sign in
    </button>

    <div id="loginMessage" class="message">
      Demo login: coach@rtr.demo / demo
    </div>

    <p class="small">
      Demo access: coach@rtr.demo / demo
    </p>

  </div>

</div>


<!-- APP -->
<div id="app" class="hidden">

  <div class="wrap">

    <header>

      <div class="brand">
        <div class="mark">R</div>
        <div>
          <div>RTR</div>
          <div class="sub">RISK TO REWARD</div>
        </div>
      </div>

      <div class="top-actions">
        <button id="logoutButton" class="btn dark" type="button">
          Log out
        </button>

        <button id="logTradeButton" class="btn" type="button">
          + Log Trade
        </button>
      </div>

    </header>


    <!-- NAVIGATION -->
    <nav class="tabs">

      <button
        class="tab active"
        id="t-dashboard"
        type="button"
        data-view="dashboard"
      >
        Overview
      </button>

      <button
        class="tab"
        id="t-students"
        type="button"
        data-view="students"
      >
        Students
      </button>

      <button
        class="tab"
        id="t-trade"
        type="button"
        data-view="trade"
      >
        Log Trade
      </button>

      <button
        class="tab"
        id="t-psych"
        type="button"
        data-view="psych"
      >
        Psychology
      </button>

    </nav>


    <!-- DASHBOARD -->
    <section id="dashboard">

      <div class="hero">
        <div class="eyebrow">COACH COMMAND CENTRE</div>
        <h1>Risk To Reward</h1>
        <p>
          Track student performance, risk discipline and
          trading psychology from one dashboard.
        </p>
      </div>


      <div class="grid">

        <div class="card">
          <div class="label">Students</div>
          <div class="value" id="sCount">0</div>
        </div>

        <div class="card">
          <div class="label">Group P/L</div>
          <div class="value green" id="gPL">£0</div>
        </div>

        <div class="card">
          <div class="label">Avg win rate</div>
          <div class="value" id="gWin">0%</div>
        </div>

        <div class="card">
          <div class="label">Avg confidence</div>
          <div class="value" id="gConf">0/10</div>
        </div>

      </div>


      <div class="section card">

        <div class="section-title">
          <h2>Student performance</h2>
          <span class="muted small">Tap a student</span>
        </div>

        <div class="table-wrap">

          <table class="table">

            <thead>
              <tr>
                <th>Student</th>
                <th>P/L</th>
                <th>Win rate</th>
                <th>Confidence</th>
                <th>Plan discipline</th>
              </tr>
            </thead>

            <tbody id="dash"></tbody>

          </table>

        </div>

      </div>

    </section>


    <!-- STUDENTS -->
    <section id="students" class="hidden">

      <div class="section card">

        <div class="section-title">

          <h2>Students</h2>

          <button
            id="addStudentButton"
            class="btn"
            type="button"
          >
            + Student
          </button>

        </div>

        <div class="table-wrap">

          <table class="table">

            <thead>
              <tr>
                <th>Name</th>
                <th>Email</th>
                <th>Trades</th>
                <th>P/L</th>
                <th></th>
              </tr>
            </thead>

            <tbody id="studentsTable"></tbody>

          </table>

        </div>

      </div>


      <div id="profile" class="section hidden"></div>

    </section>


    <!-- TRADE -->
    <section id="trade" class="hidden">

      <div class="card">

        <div class="section-title">
          <h2>Log a trade</h2>
          <span class="pill">Psychology included</span>
        </div>


        <form id="tradeForm" class="form">

          <div class="field">
            <label for="student">Student</label>
            <select id="student"></select>
          </div>


          <div class="field">
            <label for="asset">Asset / Pair</label>
            <input id="asset" placeholder="XAUUSD">
          </div>


          <div class="field">
            <label for="direction">Direction</label>

            <select id="direction">
              <option value="Buy">Buy</option>
              <option value="Sell">Sell</option>
            </select>

          </div>


          <div class="field">
            <label for="risk">Risk %</label>
            <input
              id="risk"
              type="number"
              step="0.1"
              placeholder="1"
            >
          </div>


          <div class="field">
            <label for="rr">Risk : Reward</label>
            <input
              id="rr"
              type="number"
              step="0.1"
              placeholder="2.5"
            >
          </div>


          <div class="field">
            <label for="pl">Profit / Loss (£)</label>
            <input
              id="pl"
              type="number"
              step="0.01"
              value="0"
            >
          </div>


          <div class="field">
            <label for="strategy">Strategy</label>
            <input
              id="strategy"
              placeholder="Break & Retest"
            >
          </div>


          <div class="field">
            <label for="followed">Followed the plan?</label>

            <select id="followed">
              <option value="yes">Yes</option>
              <option value="no">No</option>
            </select>

          </div>


          <div class="field full">
            <label for="reason">
              Why did you take the trade?
            </label>

            <textarea id="reason"></textarea>
          </div>


          <div class="field full">
            <label for="before">
              How did you feel before?
            </label>

            <textarea id="before"></textarea>
          </div>


          <div class="field full">
            <label for="during">
              How did you feel during?
            </label>

            <textarea id="during"></textarea>
          </div>


          <div class="field full">
            <label for="after">
              How did you feel after?
            </label>

            <textarea id="after"></textarea>
          </div>


          <div class="grid full">

            <div class="card">

              <div class="label">Confidence</div>

              <input
                id="confidence"
                type="range"
                min="1"
                max="10"
                value="5"
              >

              <b id="cv">5</b>/10

            </div>


            <div class="card">

              <div class="label">Stress</div>

              <input
                id="stress"
                type="range"
                min="1"
                max="10"
                value="5"
              >

              <b id="sv">5</b>/10

            </div>


            <div class="card">

              <div class="label">Fear</div>

              <input
                id="fear"
                type="range"
                min="1"
                max="10"
                value="5"
              >

              <b id="fv">5</b>/10

            </div>


            <div class="card">

              <div class="label">Greed</div>

              <input
                id="greed"
                type="range"
                min="1"
                max="10"
                value="5"
              >

              <b id="gv">5</b>/10

            </div>

          </div>


          <div class="field">

            <label for="rating">
              Trade rating
            </label>

            <input
              id="rating"
              type="range"
              min="1"
              max="10"
              value="5"
            >

          </div>


          <div class="full">

            <button
              class="btn"
              type="submit"
            >
              Save trade to RTR
            </button>

          </div>

        </form>

      </div>

    </section>


    <!-- PSYCHOLOGY -->
    <section id="psych" class="hidden">

      <div class="hero">

        <div class="eyebrow">
          TRADING PSYCHOLOGY
        </div>

        <h1>Mindset patterns</h1>

        <p>
          See where emotion and discipline are affecting performance.
        </p>

      </div>


      <div class="profile">

        <div class="card">

          <h2>Group averages</h2>

          <div class="bars" id="bars"></div>

        </div>


        <div class="card">

          <h2>Coach focus</h2>

          <p id="focus" class="muted"></p>

        </div>

      </div>

    </section>

  </div>

</div>


<script>
"use strict";

/* =========================
   RTR DEMO DATA
========================= */

const KEY = "rtr_pro_demo_v2";

let data;

try {
  data = JSON.parse(localStorage.getItem(KEY) || "null");
} catch(e) {
  data = null;
}

if (!data) {
  data = {
    students: [
      {
        id: 1,
        name: "Jake",
        email: "jake@example.com",
        notes: "Work on patience when trades move into profit.",
        trades: [
          {
            asset: "XAUUSD",
            direction: "Buy",
            pl: 420,
            confidence: 8,
            stress: 3,
            fear: 2,
            greed: 4,
            followed: "yes",
            rating: 9,
            rr: 2.5,
            before: "Calm and focused",
            during: "Comfortable",
            after: "Happy with execution"
          },
          {
            asset: "EURUSD",
            direction: "Sell",
            pl: -110,
            confidence: 5,
            stress: 7,
            fear: 7,
            greed: 5,
            followed: "no",
            rating: 4,
            rr: 1.2,
            before: "Felt rushed",
            during: "Nervous",
            after: "Frustrated"
          }
        ]
      },

      {
        id: 2,
        name: "Liam",
        email: "liam@example.com",
        notes: "",
        trades: [
          {
            asset: "GBPUSD",
            direction: "Buy",
            pl: 180,
            confidence: 7,
            stress: 4,
            fear: 3,
            greed: 3,
            followed: "yes",
            rating: 8,
            rr: 2,
            before: "Focused",
            during: "Calm",
            after: "Pleased"
          }
        ]
      },

      {
        id: 3,
        name: "Ryan",
        email: "ryan@example.com",
        notes: "",
        trades: []
      }
    ]
  };

  saveData();
}


/* =========================
   ELEMENT HELPER
========================= */

function $(id) {
  return document.getElementById(id);
}


/* =========================
   STORAGE
========================= */

function saveData() {
  try {
    localStorage.setItem(KEY, JSON.stringify(data));
  } catch(e) {
    console.log("Could not save demo data.");
  }
}


/* =========================
   LOGIN
========================= */

function login() {

  const email = $("email").value.trim().toLowerCase();
  const password = $("password").value;

  const message = $("loginMessage");

  if (
    email !== "coach@rtr.demo" ||
    password !== "demo"
  ) {
    message.style.display = "block";
    return;
  }

  message.style.display = "none";

  $("login").classList.add("hidden");
  $("app").classList.remove("hidden");

  refresh();
}


/* =========================
   LOGOUT
========================= */

function logout() {

  $("app").classList.add("hidden");
  $("login").classList.remove("hidden");

  $("password").value = "demo";
}


/* =========================
   VIEW SWITCHING
========================= */

function openView(id) {

  const views = [
    "dashboard",
    "students",
    "trade",
    "psych"
  ];

  views.forEach(function(view) {

    const section = $(view);

    if (section) {
      section.classList.toggle(
        "hidden",
        view !== id
      );
    }

  });


  views.forEach(function(view) {

    const tab = $("t-" + view);

    if (tab) {
      tab.classList.toggle(
        "active",
        view === id
      );
    }

  });


  refresh();
}


/* =========================
   METRICS
========================= */

function metrics(student) {

  const trades = student.trades || [];

  const pl = trades.reduce(
    function(total, trade) {
      return total + Number(trade.pl || 0);
    },
    0
  );

  const wins = trades.filter(
    function(trade) {
      return Number(trade.pl || 0) > 0;
    }
  ).length;

  const average = function(key) {

    if (!trades.length) {
      return 0;
    }

    return trades.reduce(
      function(total, trade) {
        return total + Number(trade[key] || 0);
      },
      0
    ) / trades.length;

  };

  const discipline = trades.length
    ? trades.filter(function(trade) {
        return trade.followed === "yes";
      }).length / trades.length * 100
    : 0;

  return {
    t: trades,
    pl: pl,
    win: trades.length ? wins / trades.length * 100 : 0,
    conf: average("confidence"),
    stress: average("stress"),
    fear: average("fear"),
    greed: average("greed"),
    disc: discipline
  };
}


/* =========================
   MONEY
========================= */

function money(number) {

  const n = Number(number || 0);

  return (
    n < 0 ? "-£" : "£"
  ) +
  Math.abs(n).toLocaleString(
    "en-GB",
    {
      maximumFractionDigits: 2
    }
  );
}


/* =========================
   REFRESH DASHBOARD
========================= */

function refresh() {

  const students = data.students || [];

  const metricsList = students.map(metrics);

  const totalPL = metricsList.reduce(
    function(total, metric) {
      return total + metric.pl;
    },
    0
  );

  const averageWin = metricsList.length
    ? metricsList.reduce(
        function(total, metric) {
          return total + metric.win;
        },
        0
      ) / metricsList.length
    : 0;

  const averageConfidence = metricsList.length
    ? metricsList.reduce(
        function(total, metric) {
          return total + metric.conf;
        },
        0
      ) / metricsList.length
    : 0;


  $("sCount").textContent = students.length;

  $("gPL").textContent = money(totalPL);

  $("gWin").textContent =
    averageWin.toFixed(0) + "%";

  $("gConf").textContent =
    averageConfidence.toFixed(1) + "/10";


  /* DASHBOARD TABLE */

  $("dash").innerHTML = students.map(
    function(student) {

      const m = metrics(student);

      return `
        <tr class="click" data-student-id="${student.id}">
          <td>
            <b>${escapeHTML(student.name)}</b>
            <br>
            <span class="muted small">
              ${escapeHTML(student.email)}
            </span>
          </td>

          <td class="${m.pl >= 0 ? "green" : "red"}">
            ${money(m.pl)}
          </td>

          <td>
            ${m.win.toFixed(0)}%
          </td>

          <td>
            ${m.conf.toFixed(1)}/10
          </td>

          <td>
            ${m.disc.toFixed(0)}%
          </td>
        </tr>
      `;

    }
  ).join("");


  /* STUDENT TABLE */

  $("studentsTable").innerHTML = students.map(
    function(student) {

      const m = metrics(student);

      return `
        <tr>
          <td>
            <b>${escapeHTML(student.name)}</b>
          </td>

          <td>
            ${escapeHTML(student.email)}
          </td>

          <td>
            ${m.t.length}
          </td>

          <td class="${m.pl >= 0 ? "green" : "red"}">
            ${money(m.pl)}
          </td>

          <td>
            <button
              class="btn dark view-student"
              type="button"
              data-student-id="${student.id}"
            >
              View
            </button>
          </td>
        </tr>
      `;

    }
  ).join("");


  /* STUDENT SELECT */

  $("student").innerHTML = students.map(
    function(student) {

      return `
        <option value="${student.id}">
          ${escapeHTML(student.name)}
        </option>
      `;

    }
  ).join("");


  /* PSYCHOLOGY */

  const allTrades = students.flatMap(
    function(student) {
      return student.trades || [];
    }
  );

  function averagePsychology(key) {

    if (!allTrades.length) {
      return 0;
    }

    return allTrades.reduce(
      function(total, trade) {
        return total + Number(trade[key] || 0);
      },
      0
    ) / allTrades.length;
  }


  const psychology = [
    ["Confidence", averagePsychology("confidence")],
    ["Stress", averagePsychology("stress")],
    ["Fear", averagePsychology("fear")],
    ["Greed", averagePsychology("greed")]
  ];


  $("bars").innerHTML = psychology.map(
    function(item) {

      return `
        <div class="barrow">

          <span>${item[0]}</span>

          <div class="bar">
            <div
              class="fill"
              style="width:${Math.min(item[1] * 10, 100)}%"
            ></div>
          </div>

          <b>${item[1].toFixed(1)}</b>

        </div>
      `;

    }
  ).join("");


  if (allTrades.length) {

    $("focus").textContent =
      "The group averages " +
      averagePsychology("confidence").toFixed(1) +
      "/10 confidence, " +
      averagePsychology("stress").toFixed(1) +
      "/10 stress, " +
      averagePsychology("fear").toFixed(1) +
      "/10 fear and " +
      averagePsychology("greed").toFixed(1) +
      "/10 greed.";

  } else {

    $("focus").textContent =
      "Log trades to generate psychology insights.";

  }

}


/* =========================
   STUDENT PROFILE
========================= */

function viewStudent(id) {

  const student = data.students.find(
    function(item) {
      return Number(item.id) === Number(id);
    }
  );

  if (!student) {
    return;
  }

  openView("students");

  const m = metrics(student);

  const profile = $("profile");

  profile.classList.remove("hidden");


  profile.innerHTML = `
    <div class="card">

      <div class="section-title">

        <div>
          <h2>${escapeHTML(student.name)}</h2>

          <span class="muted">
            ${escapeHTML(student.email)}
          </span>
        </div>

        <span class="pill">
          RTR STUDENT
        </span>

      </div>


      <div class="grid">

        <div>
          <div class="label">P/L</div>

          <div class="value ${m.pl >= 0 ? "green" : "red"}">
            ${money(m.pl)}
          </div>
        </div>


        <div>
          <div class="label">Win rate</div>

          <div class="value">
            ${m.win.toFixed(0)}%
          </div>
        </div>


        <div>
          <div class="label">Confidence</div>

          <div class="value">
            ${m.conf.toFixed(1)}/10
          </div>
        </div>


        <div>
          <div class="label">Discipline</div>

          <div class="value">
            ${m.disc.toFixed(0)}%
          </div>
        </div>

      </div>


      <div class="section">

        <div class="section-title">

          <h2>Coach notes</h2>

          <button
            class="btn save-notes"
            type="button"
            data-student-id="${student.id}"
          >
            Save
          </button>

        </div>

        <textarea
          id="notes"
          style="width:100%;min-height:80px;background:#090e14;border:1px solid var(--line);border-radius:10px;color:#fff;padding:12px"
        >${escapeHTML(student.notes || "")}</textarea>

      </div>


      <div class="section">

        <h2>Trade history</h2>

        <div class="table-wrap">

          <table class="table">

            <thead>

              <tr>
                <th>Asset</th>
                <th>Direction</th>
                <th>R:R</th>
                <th>P/L</th>
                <th>Confidence</th>
                <th>Stress</th>
                <th>Plan</th>
                <th>Before</th>
                <th>After</th>
              </tr>

            </thead>

            <tbody>

              ${
                m.t.length
                ?
                m.t.map(function(trade) {

                  return `
                    <tr>

                      <td>
                        ${escapeHTML(trade.asset || "-")}
                      </td>

                      <td>
                        ${escapeHTML(trade.direction || "-")}
                      </td>

                      <td>
                        1:${escapeHTML(String(trade.rr || "-"))}
                      </td>

                      <td class="${Number(trade.pl) >= 0 ? "green" : "red"}">
                        ${money(Number(trade.pl))}
                      </td>

                      <td>
                        ${trade.confidence || 0}/10
                      </td>

                      <td>
                        ${trade.stress || 0}/10
                      </td>

                      <td>
                        ${
                          trade.followed === "yes"
                          ?
                          '<span class="pill good">Followed</span>'
                          :
                          '<span class="pill bad">Broken</span>'
                        }
                      </td>

                      <td>
                        ${escapeHTML(trade.before || "")}
                      </td>

                      <td>
                        ${escapeHTML(trade.after || "")}
                      </td>

                    </tr>
                  `;

                }).join("")
                :
                `
                  <tr>
                    <td colspan="9" class="muted">
                      No trades logged yet.
                    </td>
                  </tr>
                `
              }

            </tbody>

          </table>

        </div>

      </div>

    </div>
  `;
}


/* =========================
   SAVE NOTES
========================= */

function saveNotes(id) {

  const student = data.students.find(
    function(item) {
      return Number(item.id) === Number(id);
    }
  );

  if (!student) {
    return;
  }

  student.notes = $("notes").value;

  saveData();

  refresh();

  viewStudent(id);

  alert("Coach notes saved.");
}


/* =========================
   ADD STUDENT
========================= */

function addDemoStudent() {

  const name = prompt("Student name?");

  if (!name || !name.trim()) {
    return;
  }

  const cleanName = name.trim();

  data.students.push({
    id: Date.now(),
    name: cleanName,
    email:
      cleanName
        .toLowerCase()
        .replace(/\s+/g, ".") +
      "@rtr.demo",
    notes: "",
    trades: []
  });

  saveData();

  refresh();

  openView("students");
}


/* =========================
   ESCAPE HTML
========================= */

function escapeHTML(value) {

  return String(value || "")
    .replace(/&/g, "&amp;")
    .replace(/</g, "&lt;")
    .replace(/>/g, "&gt;")
    .replace(/"/g, "&quot;")
    .replace(/'/g, "&#039;");
}


/* =========================
   ADD TRADE
========================= */

function addTrade(event) {

  event.preventDefault();

  const studentId = Number($("student").value);

  const student = data.students.find(
    function(item) {
      return Number(item.id) === studentId;
    }
  );

  if (!student) {
    alert("Please select a student.");
    return;
  }


  const trade = {

    asset: $("asset").value.trim(),

    direction: $("direction").value,

    risk: $("risk").value,

    rr: $("rr").value,

    pl: Number($("pl").value || 0),

    strategy: $("strategy").value.trim(),

    reason: $("reason").value.trim(),

    before: $("before").value.trim(),

    during: $("during").value.trim(),

    after: $("after").value.trim(),

    confidence: Number($("confidence").value),

    stress: Number($("stress").value),

    fear: Number($("fear").value),

    greed: Number($("greed").value),

    followed: $("followed").value,

    rating: Number($("rating").value),

    date: new Date().toISOString()

  };


  if (!trade.asset) {

    alert("Please enter an asset or pair.");

    $("asset").focus();

    return;
  }


  student.trades.push(trade);

  saveData();


  event.target.reset();


  $("confidence").value = 5;
  $("stress").value = 5;
  $("fear").value = 5;
  $("greed").value = 5;
  $("rating").value = 5;

  $("cv").textContent = "5";
  $("sv").textContent = "5";
  $("fv").textContent = "5";
  $("gv").textContent = "5";


  refresh();

  openView("students");

  viewStudent(student.id);

}


/* =========================
   EVENT LISTENERS
========================= */

document.addEventListener("DOMContentLoaded", function() {


  /* LOGIN BUTTON */

  $("loginButton").addEventListener(
    "click",
    login
  );


  /* ENTER KEY LOGIN */

  $("password").addEventListener(
    "keydown",
    function(event) {

      if (event.key === "Enter") {
        login();
      }

    }
  );


  $("email").addEventListener(
    "keydown",
    function(event) {

      if (event.key === "Enter") {
        login();
      }

    }
  );


  /* LOGOUT */

  $("logoutButton").addEventListener(
    "click",
    logout
  );


  /* LOG TRADE */

  $("logTradeButton").addEventListener(
    "click",
    function() {
      openView("trade");
    }
  );


  /* ADD STUDENT */

  $("addStudentButton").addEventListener(
    "click",
    addDemoStudent
  );


  /* NAVIGATION */

  document.querySelectorAll(".tab").forEach(
    function(button) {

      button.addEventListener(
        "click",
        function() {
          openView(button.dataset.view);
        }
      );

    }
  );


  /* TRADE FORM */

  $("tradeForm").addEventListener(
    "submit",
    addTrade
  );


  /* RANGE SLIDERS */

  $("confidence").addEventListener(
    "input",
    function() {
      $("cv").textContent = this.value;
    }
  );


  $("stress").addEventListener(
    "input",
    function() {
      $("sv").textContent = this.value;
    }
  );


  $("fear").addEventListener(
    "input",
    function() {
      $("fv").textContent = this.value;
    }
  );


  $("greed").addEventListener(
    "input",
    function() {
      $("gv").textContent = this.value;
    }
  );


  /* DASHBOARD STUDENT CLICK */

  $("dash").addEventListener(
    "click",
    function(event) {

      const row =
        event.target.closest("[data-student-id]");

      if (!row) {
        return;
      }

      viewStudent(row.dataset.studentId);
    }
  );


  /* STUDENT VIEW BUTTON */

  $("studentsTable").addEventListener(
    "click",
    function(event) {

      const button =
        event.target.closest(".view-student");

      if (!button) {
        return;
      }

      viewStudent(button.dataset.studentId);
    }
  );


  /* PROFILE BUTTONS */

  $("profile").addEventListener(
    "click",
    function(event) {

      const button =
        event.target.closest(".save-notes");

      if (!button) {
        return;
      }

      saveNotes(button.dataset.studentId);
    }
  );


  refresh();

});
</script>

</body>
</html>
