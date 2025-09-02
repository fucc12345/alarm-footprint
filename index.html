-<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Carbon Footprint Knower</title>
<style>
  :root{
    --bg:#f8fafc;
    --text:#0f172a;
    --muted:#64748b;
    --card:#ffffff;
    --primary:#2563eb;
    --secondary:#16a34a;
    --warning:#f59e0b;
    --danger:#dc2626;
    --accent:#0ea5e9;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  body{
    font-family:system-ui, sans-serif;
    background:var(--bg);
    color:var(--text);
    padding:20px;
    display:flex;
    justify-content:center;
  }
  .app{width:100%;max-width:1100px;display:grid;grid-template-columns:1fr 380px;gap:20px}
  .panel{background:var(--card);border-radius:12px;padding:20px;box-shadow:0 4px 16px rgba(0,0,0,0.08)}
  h1{font-size:22px;margin-bottom:4px}
  p{color:var(--muted)}
  .form-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:14px;margin-top:16px}
  .card{background:#f9fafb;border-radius:10px;padding:14px;border:1px solid #e2e8f0}
  label{font-size:14px;font-weight:500;color:var(--text);display:block;margin-bottom:6px}
  input,select{width:100%;padding:8px 10px;border-radius:8px;border:1px solid #cbd5e1;font-size:14px}
  input:focus,select:focus{border-color:var(--accent);outline:none}
  button{cursor:pointer;border:none;font-weight:600;border-radius:8px}
  .primary{background:var(--primary);color:#fff;padding:10px 14px}
  .ghost{background:#f1f5f9;color:var(--text);padding:8px 12px}
  .results{margin-top:16px;display:none}
  .big-num{font-size:28px;font-weight:700}
  .sub{font-size:13px;color:var(--muted)}
  .tip{background:#f1f5f9;padding:10px;border-radius:8px}
  .visual{height:300px;display:flex;flex-direction:column;align-items:center;justify-content:center;background:#f9fafb;border-radius:12px;border:1px solid #e2e8f0}
  .balloon{margin-top:12px;padding:10px 16px;border-radius:50%;background:var(--accent);color:#fff;font-weight:700;box-shadow:0 6px 16px rgba(0,0,0,0.2)}
  .score{background:#f1f5f9;border:1px solid #e2e8f0;padding:6px 10px;border-radius:8px;font-size:14px;display:inline-flex;gap:6px;align-items:center}
  @media(max-width:900px){.app{grid-template-columns:1fr}}
</style>
</head>
<body>
<main class="app">
  <section class="panel">
    <h1>🌍 Carbon Footprint Knower</h1>
    <p>Interactive • Fast • Actionable</p>

    <div class="form-grid">
      <div class="card">
        <label>Transport</label>
        <select id="transportType">
          <option value="car">🚗 Car</option>
          <option value="motorbike">🛵 Motorbike</option>
          <option value="bus">🚌 Bus</option>
          <option value="train">🚆 Train</option>
          <option value="cycling">🚴 Bicycle/Walk</option>
          <option value="flight">✈️ Flight</option>
        </select>
        <label>Distance per trip (km)</label>
        <input type="number" id="transportKm" placeholder="e.g. 12">
        <label>Trips per week</label>
        <input type="number" id="transportTrips" value="10">
      </div>
      <div class="card">
        <label>Electricity (kWh/month)</label>
        <input type="number" id="electricityKwh" placeholder="200">
        <label>Cooking fuel</label>
        <select id="cookingFuel">
          <option value="lpg">LPG</option>
          <option value="electric">Electric</option>
          <option value="biogas">Biogas</option>
          <option value="wood">Wood</option>
        </select>
        <label>AC usage (hours/day)</label>
        <input type="number" id="acHours" value="0">
      </div>
      <div class="card">
        <label>Diet type</label>
        <select id="dietType">
          <option value="omnivore">Omnivore</option>
          <option value="pescatarian">Pescatarian</option>
          <option value="vegetarian">Vegetarian</option>
          <option value="vegan">Vegan</option>
        </select>
        <label>Meals/day</label>
        <input type="number" id="mealsPerDay" value="3">
      </div>
      <div class="card">
        <label>Water use (litres/day)</label>
        <input type="number" id="waterLitres" placeholder="150">
        <label>Waste reduction</label>
        <select id="wasteReduce">
          <option value="none">None</option>
          <option value="some">Some</option>
          <option value="good">Good</option>
          <option value="excellent">Excellent</option>
        </select>
      </div>
    </div>

    <div style="margin-top:14px;display:flex;gap:10px;flex-wrap:wrap">
      <button class="primary" id="calculateBtn">Calculate</button>
      <button class="ghost" id="resetBtn">Reset</button>
      <div class="score" id="greenScore"><span>🌱</span> <span id="greenScoreText">Score 0</span></div>
    </div>

    <div class="results" id="results">
      <div class="big-num" id="co2Total">0 kg CO₂/month</div>
      <div class="sub" id="breakdown">Breakdown</div>
      <div style="margin-top:10px;display:grid;gap:8px">
        <div class="tip" id="tip1"></div>
        <div class="tip" id="tip2"></div>
        <div class="tip" id="tip3"></div>
      </div>
    </div>
  </section>

  <aside class="panel visual">
    <div id="status">Status: —</div>
    <div class="balloon" id="balloon">0 kg</div>
  </aside>
</main>
<script>
const FACTORS={transport:{car:0.192,motorbike:0.09,bus:0.05,train:0.041,cycling:0,flight:0.255},electricity:0.82,ac:0.9,cooking:{lpg:0.185,electric:0.82,biogas:0.04,wood:0.5},diet:{omnivore:2.5,pescatarian:1.8,vegetarian:1.2,vegan:0.9},water:0.0003,waste:{none:1,some:0.92,good:0.8,excellent:0.6}};
const transportType=document.getElementById("transportType"),transportKm=document.getElementById("transportKm"),transportTrips=document.getElementById("transportTrips"),electricityKwh=document.getElementById("electricityKwh"),cookingFuel=document.getElementById("cookingFuel"),acHours=document.getElementById("acHours"),dietType=document.getElementById("dietType"),mealsPerDay=document.getElementById("mealsPerDay"),waterLitres=document.getElementById("waterLitres"),wasteReduce=document.getElementById("wasteReduce"),calculateBtn=document.getElementById("calculateBtn"),resetBtn=document.getElementById("resetBtn"),results=document.getElementById("results"),co2Total=document.getElementById("co2Total"),breakdown=document.getElementById("breakdown"),tip1=document.getElementById("tip1"),tip2=document.getElementById("tip2"),tip3=document.getElementById("tip3"),balloon=document.getElementById("balloon"),greenScoreText=document.getElementById("greenScoreText"),status=document.getElementById("status");
function calc(){const km=(+transportKm.value||0)*(+transportTrips.value||0)*52/12;const transport=km*(FACTORS.transport[transportType.value]||0);const electr=(+electricityKwh.value||0)*FACTORS.electricity;const ac=(+acHours.value||0)*30*FACTORS.ac;const cooking=(FACTORS.cooking[cookingFuel.value]||0)*30;const food=(FACTORS.diet[dietType.value]||1.5)*30;const water=(+waterLitres.value||0)*30*FACTORS.water;let total=(transport+electr+ac+cooking+food+water)*(FACTORS.waste[wasteReduce.value]||1);show(total,{transport,electr,ac,cooking,food,water});}
function show(total,em){results.style.display="block";co2Total.textContent=`${Math.round(total)} kg CO₂/month`;breakdown.textContent=`Transport ${Math.round(em.transport)}kg, Electric ${Math.round(em.electr)}kg, Food ${Math.round(em.food)}kg`;balloon.textContent=`${Math.round(total)} kg`;status.textContent=total<500?"Status: ✅ Low":"Status: ⚠️ High";let score=total<400?5:total<700?4:total<1000?3:2;greenScoreText.textContent="Score "+score;const tips=["Try carpooling or public transport","Save energy: LED, unplug devices","Shift diet to more veggies"];
tip1.textContent=tips[0];tip2.textContent=tips[1];tip3.textContent=tips[2];}
calculateBtn.onclick=calc;resetBtn.onclick=()=>{document.querySelectorAll("input").forEach(i=>i.value="");transportType.value="car";cookingFuel.value="lpg";dietType.value="omnivore";wasteReduce.value="none";results.style.display="none"};
</script>
</body>
</html>
