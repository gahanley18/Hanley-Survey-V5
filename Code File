<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Hanley Adoption Law Group — Practice Discovery</title>
  <link href="https://fonts.googleapis.com/css2?family=Lora:wght@400;500;600&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --green: #2e7d5e;
      --green-light: #e8f4ef;
      --green-mid: #3a9970;
      --text: #1a1a1a;
      --muted: #6b7280;
      --border: #d1d5db;
      --bg: #f9f8f6;
      --card: #ffffff;
      --radius: 12px;
    }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 40px 20px 80px;
    }

    header { text-align: center; margin-bottom: 36px; }

    header h1 {
      font-family: 'Lora', serif;
      font-size: 1.5rem;
      font-weight: 600;
      color: var(--green);
      letter-spacing: -0.02em;
    }

    header p {
      font-size: 0.85rem;
      color: var(--muted);
      margin-top: 6px;
      font-weight: 300;
      letter-spacing: 0.04em;
      text-transform: uppercase;
    }

    .progress-wrap { width: 100%; max-width: 620px; margin-bottom: 28px; }

    .progress-label {
      display: flex;
      justify-content: space-between;
      font-size: 0.78rem;
      color: var(--muted);
      margin-bottom: 8px;
      font-weight: 400;
    }

    .progress-bar { height: 4px; background: var(--border); border-radius: 99px; overflow: hidden; }

    .progress-fill {
      height: 100%;
      background: var(--green);
      border-radius: 99px;
      transition: width 0.4s ease;
    }

    .card {
      background: var(--card);
      border-radius: var(--radius);
      padding: 40px 44px;
      width: 100%;
      max-width: 620px;
      box-shadow: 0 2px 16px rgba(0,0,0,0.06);
      display: none;
      animation: fadeIn 0.3s ease;
    }

    .card.active { display: block; }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(8px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    .step-tag {
      font-size: 0.72rem;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      color: var(--green);
      margin-bottom: 14px;
    }

    .card h2 {
      font-family: 'Lora', serif;
      font-size: 1.35rem;
      font-weight: 500;
      line-height: 1.45;
      color: var(--text);
      margin-bottom: 28px;
    }

    .question-block { margin-bottom: 28px; }
    .question-block:last-of-type { margin-bottom: 0; }

    .question-label {
      font-size: 0.9rem;
      font-weight: 500;
      color: var(--text);
      margin-bottom: 12px;
      display: block;
    }

    .question-hint {
      font-size: 0.82rem;
      color: var(--muted);
      margin-bottom: 12px;
      font-style: italic;
      font-weight: 300;
    }

    .options { display: flex; flex-direction: column; gap: 10px; }

    .option {
      display: flex;
      align-items: flex-start;
      gap: 12px;
      padding: 13px 16px;
      border: 1.5px solid var(--border);
      border-radius: 8px;
      cursor: pointer;
      transition: border-color 0.2s, background 0.2s;
      font-size: 0.88rem;
      line-height: 1.45;
    }

    .option:hover { border-color: var(--green-mid); background: var(--green-light); }
    .option.selected { border-color: var(--green); background: var(--green-light); }
    .option input { display: none; }

    .option-check {
      width: 18px;
      height: 18px;
      min-width: 18px;
      border: 2px solid var(--border);
      border-radius: 4px;
      margin-top: 1px;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: border-color 0.2s, background 0.2s;
    }

    .option.radio .option-check { border-radius: 50%; }

    .option.selected .option-check {
      border-color: var(--green);
      background: var(--green);
    }

    .option.selected .option-check::after { content: ''; display: block; }

    .option:not(.radio).selected .option-check::after {
      width: 10px; height: 10px;
      background: url("data:image/svg+xml,%3Csvg viewBox='0 0 10 8' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1 4l3 3 5-6' stroke='white' stroke-width='1.8' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E") no-repeat center;
      background-size: contain;
    }

    .option.radio.selected .option-check::after {
      width: 8px; height: 8px;
      background: white;
      border-radius: 50%;
    }

    .option-text { flex: 1; }
    .option-title { font-weight: 500; color: var(--text); }
    .option-sub { font-size: 0.8rem; color: var(--muted); margin-top: 2px; font-weight: 300; }

    textarea {
      width: 100%;
      border: 1.5px solid var(--border);
      border-radius: 8px;
      padding: 14px 16px;
      font-family: 'DM Sans', sans-serif;
      font-size: 0.88rem;
      color: var(--text);
      resize: vertical;
      min-height: 100px;
      outline: none;
      transition: border-color 0.2s;
      background: white;
    }

    textarea:focus { border-color: var(--green); }
    textarea::placeholder { color: #b0b7c0; }

    /* Text input */
    .text-input {
      width: 100%;
      border: 1.5px solid var(--border);
      border-radius: 8px;
      padding: 13px 16px;
      font-family: 'DM Sans', sans-serif;
      font-size: 0.88rem;
      color: var(--text);
      outline: none;
      transition: border-color 0.2s;
      background: white;
    }

    .text-input:focus { border-color: var(--green); }
    .text-input::placeholder { color: #b0b7c0; }

    .slider-wrap { padding: 8px 0; }

    .slider-labels {
      display: flex;
      justify-content: space-between;
      font-size: 0.78rem;
      color: var(--muted);
      margin-top: 10px;
    }

    input[type="range"] {
      width: 100%;
      accent-color: var(--green);
      height: 4px;
      cursor: pointer;
    }

    .divider { border: none; border-top: 1px solid var(--border); margin: 28px 0; }

    .btn-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 36px;
    }

    .btn {
      padding: 12px 28px;
      border-radius: 8px;
      font-family: 'DM Sans', sans-serif;
      font-size: 0.88rem;
      font-weight: 500;
      cursor: pointer;
      border: none;
      transition: background 0.2s, color 0.2s, opacity 0.2s;
    }

    .btn-primary { background: var(--green); color: white; }
    .btn-primary:hover { background: var(--green-mid); }
    .btn-primary:disabled { opacity: 0.6; cursor: not-allowed; }

    .btn-ghost {
      background: transparent;
      color: var(--muted);
      border: 1.5px solid var(--border);
    }

    .btn-ghost:hover { border-color: var(--green); color: var(--green); }

    /* Error message */
    .error-msg {
      font-size: 0.8rem;
      color: #c0392b;
      margin-top: 8px;
      display: none;
    }

    /* Submitting state */
    .submitting-note {
      font-size: 0.82rem;
      color: var(--muted);
      text-align: center;
      margin-top: 12px;
      display: none;
    }

    /* Thank you */
    .thankyou { text-align: center; padding: 20px 0; }

    .thankyou .check-icon {
      width: 56px;
      height: 56px;
      background: var(--green-light);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 24px;
    }

    .thankyou .check-icon svg { width: 26px; height: 26px; }

    .thankyou h2 {
      font-family: 'Lora', serif;
      font-size: 1.5rem;
      font-weight: 500;
      margin-bottom: 14px;
    }

    .thankyou p {
      font-size: 0.9rem;
      color: var(--muted);
      line-height: 1.7;
      max-width: 420px;
      margin: 0 auto;
    }

    .thankyou .response-note {
      margin-top: 28px;
      padding: 16px 20px;
      background: var(--green-light);
      border-radius: 8px;
      font-size: 0.84rem;
      color: var(--green);
      font-weight: 500;
    }

    @media (max-width: 600px) {
      .card { padding: 28px 24px; }
    }
  </style>
</head>
<body>

  <header>
    <h1>Hanley Adoption Law Group</h1>
    <p>Practice Discovery — Confidential</p>
  </header>

  <div class="progress-wrap">
    <div class="progress-label">
      <span id="progress-text">Step 1 of 6 — Day-to-day</span>
      <span id="progress-pct">17%</span>
    </div>
    <div class="progress-bar">
      <div class="progress-fill" id="progress-fill" style="width: 17%"></div>
    </div>
  </div>

  <!-- Step 1 -->
  <div class="card active" id="step-1">
    <div class="step-tag">Step 1 of 6 — Day-to-day</div>
    <h2>Walk me through what a typical week looks like for your team.</h2>

    <div class="question-block">
      <span class="question-label">What's the name of your firm?</span>
      <input type="text" id="q-firm-name" class="text-input" placeholder="e.g. Hanley Adoption Law Group" />
      <div class="error-msg" id="err-firm">Please enter your firm name before continuing.</div>
    </div>

    <hr class="divider" />

    <div class="question-block">
      <span class="question-label">Select everything that's typically on your plate.</span>
      <div class="options" id="q1-tasks">
        <label class="option">
          <input type="checkbox" value="Client intake and onboarding" />
          <span class="option-check"></span>
          <span class="option-text">
            <span class="option-title">Client intake and onboarding</span>
            <span class="option-sub">Collecting documents, answering initial questions, explaining the process</span>
          </span>
        </label>
        <label class="option">
          <input type="checkbox" value="Document preparation and filing" />
          <span class="option-check"></span>
          <span class="option-text">
            <span class="option-title">Document preparation and filing</span>
            <span class="option-sub">Drafting petitions, consent forms, home studies, court filings</span>
          </span>
        </label>
        <label class="option">
          <input type="checkbox" value="Client communication" />
          <span class="option-check"></span>
          <span class="option-text">
            <span class="option-title">Client communication</span>
            <span class="option-sub">Answering emails, status updates, explaining what's next</span>
          </span>
        </label>
        <label class="option">
          <input type="checkbox" value="Court and agency coordination" />
          <span class="option-check"></span>
          <span class="option-text">
            <span class="option-title">Court and agency coordination</span>
            <span class="option-sub">Scheduling, following up with DCS, tracking case timelines</span>
          </span>
        </label>
        <label class="option">
          <input type="checkbox" value="Research and case prep" />
          <span class="option-check"></span>
          <span class="option-text">
            <span class="option-title">Research and case prep</span>
            <span class="option-sub">ICWA determinations, interstate matters, county-specific requirements</span>
          </span>
        </label>
        <label class="option">
          <input type="checkbox" value="General admin" />
          <span class="option-check"></span>
          <span class="option-text">
            <span class="option-title">General admin</span>
            <span class="option-sub">Billing, scheduling, file management</span>
          </span>
        </label>
      </div>
    </div>

    <div class="btn-row">
      <span></span>
      <button class="btn btn-primary" onclick="goTo(2)">Continue</button>
    </div>
  </div>

  <!-- Step 2 -->
  <div class="card" id="step-2">
    <div class="step-tag">Step 2 of 6 — Client intake</div>
    <h2>How do new clients typically find you, and what happens next?</h2>

    <div class="question-block">
      <span class="question-label">How do most new clients first reach out?</span>
      <div class="options" id="q2-reach">
        <label class="option radio">
          <input type="radio" name="reach" value="Most reach out by phone first" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">Most reach out by phone first</span></span>
        </label>
        <label class="option radio">
          <input type="radio" name="reach" value="Most reach out by email or the website form" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">Most reach out by email or the website form</span></span>
        </label>
        <label class="option radio">
          <input type="radio" name="reach" value="Most come through referrals from agencies or past clients" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">Most come through referrals from agencies or past clients</span></span>
        </label>
        <label class="option radio">
          <input type="radio" name="reach" value="A real mix of all of the above" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">A real mix of all of the above</span></span>
        </label>
      </div>
    </div>

    <hr class="divider" />

    <div class="question-block">
      <span class="question-label">Where does the process tend to slow down once someone reaches out?</span>
      <span class="question-hint">For example: collecting documents, explaining eligibility, getting signatures...</span>
      <textarea id="q2-slowdown" placeholder="Share whatever comes to mind..."></textarea>
    </div>

    <div class="btn-row">
      <button class="btn btn-ghost" onclick="goTo(1)">Back</button>
      <button class="btn btn-primary" onclick="goTo(3)">Continue</button>
    </div>
  </div>

  <!-- Step 3 -->
  <div class="card" id="step-3">
    <div class="step-tag">Step 3 of 6 — Document work</div>
    <h2>Let's talk about the document side of your practice.</h2>

    <div class="question-block">
      <span class="question-label">How would you describe your current document process?</span>
      <div class="options" id="q3-process">
        <label class="option radio">
          <input type="radio" name="docprocess" value="We start mostly from scratch each time" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">We start mostly from scratch each time</span></span>
        </label>
        <label class="option radio">
          <input type="radio" name="docprocess" value="We have some templates but they need a lot of customization" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">We have some templates but they need a lot of customization</span></span>
        </label>
        <label class="option radio">
          <input type="radio" name="docprocess" value="We have solid templates but customization still takes real time" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">We have solid templates but customization still takes real time</span></span>
        </label>
        <label class="option radio">
          <input type="radio" name="docprocess" value="Our document process is pretty streamlined already" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">Our document process is pretty streamlined already</span></span>
        </label>
      </div>
    </div>

    <hr class="divider" />

    <div class="question-block">
      <span class="question-label">Which adoption types generate the most document-heavy work?</span>
      <span class="question-hint">Select all that apply.</span>
      <div class="options" id="q3-types">
        <label class="option"><input type="checkbox" value="Foster care adoptions" /><span class="option-check"></span><span class="option-text"><span class="option-title">Foster care adoptions</span></span></label>
        <label class="option"><input type="checkbox" value="Newborn / infant adoptions" /><span class="option-check"></span><span class="option-text"><span class="option-title">Newborn / infant adoptions</span></span></label>
        <label class="option"><input type="checkbox" value="Contested adoptions" /><span class="option-check"></span><span class="option-text"><span class="option-title">Contested adoptions</span></span></label>
        <label class="option"><input type="checkbox" value="ICWA matters" /><span class="option-check"></span><span class="option-text"><span class="option-title">ICWA matters</span></span></label>
        <label class="option"><input type="checkbox" value="International re-adoptions" /><span class="option-check"></span><span class="option-text"><span class="option-title">International re-adoptions</span></span></label>
        <label class="option"><input type="checkbox" value="Guardianships" /><span class="option-check"></span><span class="option-text"><span class="option-title">Guardianships</span></span></label>
      </div>
    </div>

    <div class="btn-row">
      <button class="btn btn-ghost" onclick="goTo(2)">Back</button>
      <button class="btn btn-primary" onclick="goTo(4)">Continue</button>
    </div>
  </div>

  <!-- Step 4 -->
  <div class="card" id="step-4">
    <div class="step-tag">Step 4 of 6 — Client communication</div>
    <h2>How much time goes into keeping clients in the loop?</h2>

    <div class="question-block">
      <span class="question-label">How often do clients reach out asking for a status update?</span>
      <div class="options" id="q4-updates">
        <label class="option radio">
          <input type="radio" name="updates" value="Constantly — it's one of the biggest time drains" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">Constantly — it's one of the biggest time drains</span></span>
        </label>
        <label class="option radio">
          <input type="radio" name="updates" value="Regularly but we manage it" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">Regularly but we manage it</span></span>
        </label>
        <label class="option radio">
          <input type="radio" name="updates" value="Occasionally — clients generally wait for us to reach out" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">Occasionally — clients generally wait for us to reach out</span></span>
        </label>
        <label class="option radio">
          <input type="radio" name="updates" value="Rarely — our process keeps them well informed" />
          <span class="option-check"></span>
          <span class="option-text"><span class="option-title">Rarely — our process keeps them well informed</span></span>
        </label>
      </div>
    </div>

    <hr class="divider" />

    <div class="question-block">
      <span class="question-label">What do you find yourself explaining most often?</span>
      <span class="question-hint">Things like timelines, required documents, what to expect at a hearing...</span>
      <textarea id="q4-explaining" placeholder="Share whatever comes to mind..."></textarea>
    </div>

    <div class="btn-row">
      <button class="btn btn-ghost" onclick="goTo(3)">Back</button>
      <button class="btn btn-primary" onclick="goTo(5)">Continue</button>
    </div>
  </div>

  <!-- Step 5 -->
  <div class="card" id="step-5">
    <div class="step-tag">Step 5 of 6 — Research and counties</div>
    <h2>You finalize adoptions all over Indiana. How much does county variation affect your workload?</h2>

    <div class="question-block">
      <span class="question-label">How much time goes into navigating county-specific requirements or how different courts operate?</span>
      <div class="slider-wrap">
        <input type="range" id="q5-county" min="1" max="5" value="3" />
        <div class="slider-labels">
          <span>Not much — fairly consistent</span>
          <span>A significant part of our work</span>
        </div>
      </div>
    </div>

    <hr class="divider" />

    <div class="question-block">
      <span class="question-label">When ICWA applies, where does the most time go?</span>
      <span class="question-hint">For example: determining tribal affiliation, noticing requirements, coordinating with tribes...</span>
      <textarea id="q5-icwa" placeholder="Share whatever comes to mind..."></textarea>
    </div>

    <div class="btn-row">
      <button class="btn btn-ghost" onclick="goTo(4)">Back</button>
      <button class="btn btn-primary" onclick="goTo(6)">Continue</button>
    </div>
  </div>

  <!-- Step 6 -->
  <div class="card" id="step-6">
    <div class="step-tag">Step 6 of 6 — Priorities</div>
    <h2>If you had extra time back each week, what would you do with it?</h2>

    <div class="question-block">
      <span class="question-label">If you had an extra 5 hours a week, you'd spend them on:</span>
      <span class="question-hint">Select all that apply.</span>
      <div class="options" id="q6-time">
        <label class="option"><input type="checkbox" value="Taking on more clients or cases" /><span class="option-check"></span><span class="option-text"><span class="option-title">Taking on more clients or cases</span></span></label>
        <label class="option"><input type="checkbox" value="Spending more time on complex or contested matters" /><span class="option-check"></span><span class="option-text"><span class="option-title">Spending more time on complex or contested matters</span></span></label>
        <label class="option"><input type="checkbox" value="Improving the client experience" /><span class="option-check"></span><span class="option-text"><span class="option-title">Improving the client experience</span></span></label>
        <label class="option"><input type="checkbox" value="Marketing and growing the practice" /><span class="option-check"></span><span class="option-text"><span class="option-title">Marketing and growing the practice</span></span></label>
        <label class="option"><input type="checkbox" value="Training or developing staff" /><span class="option-check"></span><span class="option-text"><span class="option-title">Training or developing staff</span></span></label>
        <label class="option"><input type="checkbox" value="Personal time — work-life balance could be better" /><span class="option-check"></span><span class="option-text"><span class="option-title">Personal time — work-life balance could be better</span></span></label>
      </div>
    </div>

    <hr class="divider" />

    <div class="question-block">
      <span class="question-label">What's one thing you wish were just simpler?</span>
      <span class="question-hint">No wrong answers — even small frustrations are worth mentioning.</span>
      <textarea id="q6-simpler" placeholder="Share whatever comes to mind..."></textarea>
    </div>

    <div class="btn-row">
      <button class="btn btn-ghost" onclick="goTo(5)">Back</button>
      <button class="btn btn-primary" id="finish-btn" onclick="finish()">Finish</button>
    </div>
    <p class="submitting-note" id="submitting-note">Submitting your responses...</p>
  </div>

  <!-- Thank you -->
  <div class="card" id="step-thanks">
    <div class="thankyou">
      <div class="check-icon">
        <svg viewBox="0 0 26 26" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M5 13l5.5 5.5L21 7.5" stroke="#2e7d5e" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <h2>Thank you so much.</h2>
      <p>That's everything we needed. These answers give a clear picture of where the real friction is in your practice. The next step is a short conversation to walk through what we found and what could realistically help.</p>
      <div class="response-note">A follow-up conversation will be scheduled shortly.</div>
    </div>
  </div>

  <script>
    // ── Airtable config ──────────────────────────────────────────
    const AIRTABLE_TOKEN = 'patOcclumgTNUJJo4.f15bc5ac1a86ae550428cf7b7f156c5a3b7cd6228c3fd8cab98070da00fb7967';
    const AIRTABLE_BASE  = 'appSpLPhgQUhzhdns';
    const AIRTABLE_TABLE = 'Law Firm AI Discovery';
    // ─────────────────────────────────────────────────────────────

    const steps = 6;
    const stepLabels = ['Day-to-day', 'Client intake', 'Document work', 'Client communication', 'Research and counties', 'Priorities'];

    function goTo(n) {
      // Validate firm name before leaving step 1
      if (n === 2) {
        const firmName = document.getElementById('q-firm-name').value.trim();
        const err = document.getElementById('err-firm');
        if (!firmName) {
          err.style.display = 'block';
          return;
        }
        err.style.display = 'none';
      }

      document.querySelectorAll('.card').forEach(c => c.classList.remove('active'));
      document.getElementById('step-' + n).classList.add('active');

      const pct = Math.round((n / steps) * 100);
      document.getElementById('progress-fill').style.width = pct + '%';
      document.getElementById('progress-text').textContent = 'Step ' + n + ' of ' + steps + ' — ' + stepLabels[n - 1];
      document.getElementById('progress-pct').textContent = pct + '%';

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    function getChecked(containerId) {
      const checked = document.querySelectorAll('#' + containerId + ' input[type="checkbox"]:checked');
      return Array.from(checked).map(i => i.value).join(', ');
    }

    function getRadio(name) {
      const el = document.querySelector('input[name="' + name + '"]:checked');
      return el ? el.value : '';
    }

    async function finish() {
      const btn = document.getElementById('finish-btn');
      const note = document.getElementById('submitting-note');

      btn.disabled = true;
      note.style.display = 'block';

      const fields = {
        'Firm Name':                    document.getElementById('q-firm-name').value.trim(),
        'Submitted At':                 new Date().toISOString(),
        'Typical Week Tasks':           getChecked('q1-tasks'),
        'How Clients Reach Out':        getRadio('reach'),
        'Intake Slowdowns':             document.getElementById('q2-slowdown').value.trim(),
        'Document Process':             getRadio('docprocess'),
        'Doc-Heavy Adoption Types':     getChecked('q3-types'),
        'Status Update Frequency':      getRadio('updates'),
        'Most Repeated Explanations':   document.getElementById('q4-explaining').value.trim(),
        'County Variation Score':       parseInt(document.getElementById('q5-county').value),
        'ICWA Time Spent':              document.getElementById('q5-icwa').value.trim(),
        'Extra Time Priorities':        getChecked('q6-time'),
        'One Thing Simpler':            document.getElementById('q6-simpler').value.trim()
      };

      try {
        const url = 'https://api.airtable.com/v0/' + AIRTABLE_BASE + '/' + encodeURIComponent(AIRTABLE_TABLE);
        console.log('Submitting to:', url);
        console.log('Fields:', JSON.stringify(fields));

        const res = await fetch(url, {
          method: 'POST',
          headers: {
            'Authorization': 'Bearer ' + AIRTABLE_TOKEN,
            'Content-Type': 'application/json'
          },
          body: JSON.stringify({ fields })
        });

        const data = await res.json();
        if (!res.ok) {
          console.error('Airtable error:', JSON.stringify(data));
          alert('Submission error: ' + JSON.stringify(data));
        } else {
          console.log('Success:', JSON.stringify(data));
        }
      } catch (e) {
        console.error('Submission error:', e);
        alert('Network error: ' + e.message);
      }

      // Always show thank you regardless of API result
      document.querySelectorAll('.card').forEach(c => c.classList.remove('active'));
      document.getElementById('step-thanks').classList.add('active');
      document.querySelector('.progress-wrap').style.display = 'none';
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    // Checkbox / radio toggle styling
    document.addEventListener('change', function(e) {
      const input = e.target;
      if (input.type === 'checkbox') {
        input.closest('.option').classList.toggle('selected', input.checked);
      } else if (input.type === 'radio') {
        const name = input.name;
        document.querySelectorAll('input[name="' + name + '"]').forEach(r => {
          r.closest('.option').classList.toggle('selected', r.checked);
        });
      }
    });

    // Hide firm name error on input
    document.addEventListener('DOMContentLoaded', function() {
      document.getElementById('q-firm-name').addEventListener('input', function() {
        document.getElementById('err-firm').style.display = 'none';
      });
    });
  </script>
</body>
</html>
