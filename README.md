
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Enterprise Employment Verification ERP</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
/* ================= GLOBAL THEME ================= */
:root{
 --bg1:#0b1220;--bg2:#020617;
 --glass:rgba(255,255,255,.08);
 --border:rgba(255,255,255,.18);
 --primary:#38bdf8;
 --text:#e5e7eb;--muted:#9ca3af;
 --ok:#22c55e;--warn:#f59e0b;--bad:#ef4444;
}
*{box-sizing:border-box;font-family:Segoe UI,Arial}
body{
 margin:0;min-height:100vh;
 background:
 linear-gradient(rgba(2,6,23,.9),rgba(2,6,23,.9)),
 url("https://images.unsplash.com/photo-1521737604893-d14cc237f11d");
 background-size:cover;background-attachment:fixed;
 color:var(--text);
}

/* ================= COMMON ================= */
.header{
 padding:18px 32px;
 background:linear-gradient(90deg,#020617,#0b1220);
 border-bottom:1px solid var(--border);
 display:flex;justify-content:space-between;align-items:center;
}
.layout{display:flex}
.sidebar{
 width:300px;padding:24px;border-right:1px solid var(--border)
}
.sidebar h3{margin-top:0}
.sidebar a{
 display:block;padding:12px 14px;
 margin-bottom:6px;border-radius:10px;
 cursor:pointer
}
.sidebar a:hover{background:var(--glass)}
.content{flex:1;padding:32px}
.section{display:none}

/* ================= LOGIN ================= */
.login{
 width:440px;margin:80px auto;
 background:var(--glass);
 border:1px solid var(--border);
 backdrop-filter:blur(16px);
 padding:40px;border-radius:20px
}
.login h2{text-align:center}
.login p{text-align:center;color:var(--muted)}
.login input{
 width:100%;padding:12px;margin:12px 0;
 border:none;border-radius:8px;
 background:#020617;color:#fff
}
.login button{
 width:100%;padding:14px;
 border:none;border-radius:8px;
 background:var(--primary);color:#020617;
 font-size:16px;font-weight:600
}

/* ================= UI ================= */
.card{
 background:var(--glass);
 border:1px solid var(--border);
 border-radius:18px;padding:24px;
 margin-bottom:24px
}
.grid{
 display:grid;
 grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
 gap:24px
}
.value{font-size:30px;font-weight:600}

/* ================= IMAGES ================= */
.logo{height:40px}
.hero{
 background:
 linear-gradient(rgba(2,6,23,.75),rgba(2,6,23,.75)),
 url("https://images.unsplash.com/photo-1497366216548-37526070297c");
 background-size:cover;border-radius:20px;
 padding:44px;margin-bottom:26px
}
.profile{
 width:100px;height:100px;
 border-radius:50%;border:3px solid var(--primary)
}
.avatar{
 width:60px;height:60px;border-radius:50%;
 border:2px solid var(--primary);margin-right:10px
}

/* ================= TABLE ================= */
table{width:100%;border-collapse:collapse}
th,td{padding:14px;border-bottom:1px solid var(--border)}
th{color:var(--muted);text-align:left}

/* ================= BADGE & BUTTON ================= */
.badge{padding:4px 10px;border-radius:14px;font-size:12px}
.ok{background:rgba(34,197,94,.15);color:var(--ok)}
.warn{background:rgba(245,158,11,.15);color:var(--warn)}
.bad{background:rgba(239,68,68,.15);color:var(--bad)}

.btn{
 padding:6px 10px;border:none;border-radius:8px;
 font-size:12px;cursor:pointer
}
.accept{background:rgba(34,197,94,.2);color:var(--ok)}
.reject{background:rgba(239,68,68,.2);color:var(--bad)}
.remove{background:rgba(255,255,255,.15);color:#fff}

small{color:var(--muted)}
</style>
</head>

<body>

<!-- ================= LOGIN ================= -->
<div id="loginBox" class="login">
<h2>Employment Verification ERP</h2>
<p>MNC-grade Digital Employee Credential System</p>
<input id="username" placeholder="Username">
<input id="password" type="password" placeholder="Password">
<button onclick="login()">Login</button>
<p id="err" style="color:#f87171;text-align:center"></p>
</div>

<!-- ================= COMPANY DASHBOARD ================= -->
<div id="companyDash" style="display:none">

<div class="header">
<div>
<img class="logo" src="https://upload.wikimedia.org/wikipedia/commons/0/08/Accenture.svg">
 <b>TechNova Solutions Pvt. Ltd.</b>
</div>
<div>CEO: Amit Kulkarni · Employees: 4,532</div>
</div>

<div class="layout">

<div class="sidebar">
<h3>Company ERP</h3>
<a onclick="show('c_exec')">Executive Dashboard</a>
<a onclick="show('c_profile')">Company Profile</a>
<a onclick="show('c_dept')">Departments</a>
<a onclick="show('c_emp')">Employee Directory</a>
<a onclick="show('c_verify')">Verification Queue</a>
<a onclick="show('c_docs')">Document Management</a>
<a onclick="show('c_policy')">Company Policies</a>
<a onclick="show('c_reports')">Reports & Analytics</a>
<a onclick="show('c_audit')">Audit Logs</a>
<a onclick="show('c_roles')">Access & Roles</a>
<a onclick="show('c_loc')">Locations</a>
</div>

<div class="content">

<div id="c_exec" class="section">
<div class="hero">
<h2>Enterprise Overview</h2>
<small>Global IT · Secure Employment Verification</small>
</div>
<div class="grid">
<div class="card"><small>Total Employees</small><div class="value">4,532</div></div>
<div class="card"><small>Countries</small><div class="value">6</div></div>
<div class="card"><small>Pending Checks</small><div class="value">34</div></div>
<div class="card"><small>Compliance Score</small><div class="value">98%</div></div>
</div>
</div>

<div id="c_profile" class="section">
<div class="card">
<h3>Leadership</h3>
<img src="https://randomuser.me/api/portraits/men/75.jpg" class="avatar">
<b>Amit Kulkarni</b> – CEO<br><br>
<img src="https://randomuser.me/api/portraits/women/68.jpg" class="avatar">
<b>Neha Malhotra</b> – VP HR
</div>
</div>

<div id="c_dept" class="section">
<div class="card">
<h3>Departments</h3>
<table>
<tr><th>Department</th><th>Employees</th></tr>
<tr><td>Engineering</td><td>1820</td></tr>
<tr><td>Cloud & DevOps</td><td>640</td></tr>
<tr><td>Data & AI</td><td>520</td></tr>
<tr><td>HR & Ops</td><td>310</td></tr>
</table>
</div>
</div>

<div id="c_emp" class="section">
<div class="card">
<h3>Employee Directory</h3>
<table>
<tr><th>Employee</th><th>Role</th><th>Status</th></tr>
<tr>
<td><img src="https://randomuser.me/api/portraits/men/32.jpg" class="avatar"> Rahul Sharma</td>
<td>Backend Engineer</td>
<td><span class="badge ok">Active</span></td>
</tr>
<tr>
<td><img src="https://randomuser.me/api/portraits/women/45.jpg" class="avatar"> Neha Patel</td>
<td>Data Analyst</td>
<td><span class="badge ok">Active</span></td>
</tr>
</table>
</div>
</div>

<div id="c_verify" class="section">
<div class="card">
<h3>Verification Queue</h3>
<table>
<tr><th>Employee</th><th>Document</th><th>Status</th><th>Action</th></tr>
<tr id="v1">
<td>Rahul Sharma</td>
<td>Experience Letter</td>
<td id="vs1"><span class="badge warn">Pending</span></td>
<td>
<button class="btn accept" onclick="setStatus('vs1','ok')">Accept</button>
<button class="btn reject" onclick="setStatus('vs1','bad')">Reject</button>
<button class="btn remove" onclick="removeRow('v1')">Remove</button>
</td>
</tr>
</table>
</div>
</div>

<div id="c_docs" class="section">
<div class="card">
<h3>Document Inventory</h3>
<ul>
<li>Salary Slips – 82,000+</li>
<li>Experience Letters – 4,200</li>
<li>ID Proofs – 4,532</li>
<li>Offer Letters – 5,000+</li>
</ul>
</div>
</div>

<div id="c_policy" class="section">
<div class="card">
<h3>Company Policies</h3>
<ul>
<li>Data Retention: 5–6 years</li>
<li>Employee consent mandatory</li>
<li>Role-based access control</li>
<li>All actions audited</li>
</ul>
</div>
</div>

<div id="c_reports" class="section">
<div class="card">
<h3>Analytics</h3>
<ul>
<li>Hiring time reduced by 22%</li>
<li>Verification fraud reduced by 41%</li>
<li>HR productivity increased</li>
</ul>
</div>
</div>

<div id="c_audit" class="section">
<div class="card">
<h3>Audit Logs</h3>
<table>
<tr><th>User</th><th>Action</th><th>Date</th></tr>
<tr><td>HR Admin</td><td>Verified Salary Slip</td><td>12 Feb</td></tr>
<tr><td>System</td><td>Profile Access</td><td>11 Feb</td></tr>
</table>
</div>
</div>

<div id="c_roles" class="section">
<div class="card">
<h3>Access Roles</h3>
<ul>
<li>HR Admin – Full Access</li>
<li>HR Executive – Verification</li>
<li>Auditor – Read Only</li>
</ul>
</div>
</div>

<div id="c_loc" class="section">
<div class="card">
<h3>HQ – Pune</h3>
<iframe width="100%" height="320"
src="https://maps.google.com/maps?q=Hinjewadi%20Pune&t=&z=13&ie=UTF8&iwloc=&output=embed">
</iframe>
</div>
</div>

</div>
</div>
</div>

<!-- ================= EMPLOYEE DASHBOARD ================= -->
<div id="employeeDash" style="display:none">

<div class="header">
<div>👤 Rahul Sharma · Backend Engineer</div>
<div><span class="badge ok">Verified Employee</span></div>
</div>

<div class="layout">

<div class="sidebar">
<h3>Employee Portal</h3>
<a onclick="show('e_overview')">Profile Overview</a>
<a onclick="show('e_history')">Employment History</a>
<a onclick="show('e_skills')">Skills & Certifications</a>
<a onclick="show('e_team')">Team & Reporting</a>
<a onclick="show('e_docs')">Documents</a>
<a onclick="show('e_timeline')">Verification Timeline</a>
<a onclick="show('e_company')">Company Info</a>
<a onclick="show('e_privacy')">Privacy & Rights</a>
</div>

<div class="content">

<div id="e_overview" class="section">
<div class="hero">
<h2>Rahul Sharma</h2>
<small>Backend Engineer · TechNova</small>
</div>
<div class="card">
<img src="https://randomuser.me/api/portraits/men/32.jpg" class="profile">
<p><b>Employee ID:</b> EMP-45982</p>
<p><b>Experience:</b> 2.4 Years</p>
<p><b>Location:</b> Pune</p>
</div>
</div>

<div id="e_history" class="section">
<div class="card">
<h3>Employment History</h3>
<ul>
<li>2022–Present · TechNova · Backend Engineer</li>
<li>2021–2022 · Software Intern</li>
</ul>
</div>
</div>

<div id="e_skills" class="section">
<div class="card">
<h3>Skills</h3>
<ul>
<li>Python, SQL, REST APIs</li>
<li>Docker, Git, Linux</li>
<li>AWS Cloud Practitioner</li>
</ul>
</div>
</div>

<div id="e_team" class="section">
<div class="card">
<h3>Manager</h3>
<img src="https://randomuser.me/api/portraits/men/75.jpg" class="avatar">
Rohit Deshpande – Engineering Manager
</div>
<div class="card">
<h3>Team</h3>
<img src="https://randomuser.me/api/portraits/women/45.jpg" class="avatar">
<img src="https://randomuser.me/api/portraits/men/65.jpg" class="avatar">
<img src="https://randomuser.me/api/portraits/men/72.jpg" class="avatar">
</div>
</div>

<div id="e_docs" class="section">
<div class="card">
<h3>Documents</h3>
<table>
<tr><th>Document</th><th>Status</th></tr>
<tr><td>Experience Letter</td><td><span class="badge warn">Pending</span></td></tr>
<tr><td>Salary Slips</td><td><span class="badge ok">Verified</span></td></tr>
</table>
</div>
</div>

<div id="e_timeline" class="section">
<div class="card">
<h3>Verification Timeline</h3>
<ul>
<li>Salary slips verified – Jan 2026</li>
<li>Profile created – Aug 2022</li>
</ul>
</div>
</div>

<div id="e_company" class="section">
<div class="card">
<h3>About Company</h3>
<img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c" style="width:100%;border-radius:16px">
<p>Global IT company with teams across India, US & EU.</p>
</div>
</div>

<div id="e_privacy" class="section">
<div class="card">
<h3>Privacy & Rights</h3>
<ul>
<li>Control data sharing</li>
<li>Raise correction requests</li>
<li>View access history</li>
</ul>
</div>
</div>

</div>
</div>
</div>

<script>
function login(){
 const u=username.value,p=password.value;
 if(u==="company@erp" && p==="company_123"){
  loginBox.style.display="none";
  companyDash.style.display="block";
  show("c_exec");
 }
 else if(u==="employee@erp" && p==="employee_123"){
  loginBox.style.display="none";
  employeeDash.style.display="block";
  show("e_overview");
 }
 else err.innerText="Invalid credentials";
}
function show(id){
 document.querySelectorAll(".section").forEach(s=>s.style.display="none");
 document.getElementById(id).style.display="block";
}
function setStatus(id,t){
 document.getElementById(id).innerHTML=
  t==="ok"?'<span class="badge ok">Verified</span>':'<span class="badge bad">Rejected</span>';
}
function removeRow(id){document.getElementById(id).remove();}
</script>

</body>
</html>
Reduced operational load for companies

The current version is a frontend proof-of-concept, designed to validate usability, logic, and enterprise adoption before building backend, security, and integrations.
