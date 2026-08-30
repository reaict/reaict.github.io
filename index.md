---
layout: home
---

Bienvenue !


<style>
  .aicr-wrap {
    max-width: 680px;
    margin: 0 auto;
  }
  @keyframes aicr-draw { to { stroke-dashoffset: 0; } }
  @keyframes aicr-fadeIn { 0%,4% { opacity: 0; } 8%,100% { opacity: 1; } }
  @keyframes aicr-flankShow { 0%,60% { opacity: 0; } 68%,100% { opacity: 1; } }
  @keyframes aicr-ctReveal { 0%,86% { opacity: 0; } 94%,100% { opacity: 1; } }
  @keyframes aicr-glow { 0%,100% { opacity: 0.75; } 50% { opacity: 1; } }
  @keyframes aicr-ring { 0%,100% { stroke-opacity: 0.3; } 50% { stroke-opacity: 0.8; } }
 
  .aicr-edge-ac { stroke-dasharray: 262; stroke-dashoffset: 262; opacity: 0; animation: aicr-fadeIn 0.01s linear 1s forwards, aicr-draw 0.9s ease-out 1s forwards; }
  .aicr-edge-ct { stroke-dasharray: 262; stroke-dashoffset: 262; opacity: 0; animation: aicr-fadeIn 0.01s linear 2s forwards, aicr-draw 0.9s ease-out 2s forwards; }
 
  .aicr-node-c { opacity: 0; animation: aicr-fadeIn 0.4s ease-out 0.85s forwards; }
  .aicr-node-a { opacity: 0; animation: aicr-fadeIn 0.4s ease-out 1.7s forwards; }
  .aicr-node-t { opacity: 0; animation: aicr-fadeIn 0.4s ease-out 2.7s forwards; }
 
  /* AI : apparait des le debut (0.05s) et pulse en continu ensuite */
  .aicr-ai { opacity: 0; animation: aicr-fadeIn 0.6s ease-out 0.05s forwards, aicr-glow 2.2s ease-in-out 0.65s infinite; }
  /* CT : apparait pendant le tracage du triangle -> forme AICT */
  .aicr-ct { opacity: 0; animation: aicr-ctReveal 8s ease-out 0.05s forwards; }
  /* RE : apparait en dernier -> forme REAICT */
  .aicr-re { opacity: 0; animation: aicr-flankShow 8s ease-out 0.05s forwards; }
 
  .aicr-ring-loop { animation: aicr-ring 3.4s ease-in-out infinite; animation-delay: 7.5s; }
 
  @media (prefers-reduced-motion: reduce) {
    .aicr-edge-ac, .aicr-edge-ct { animation: none; stroke-dashoffset: 0; opacity: 1; }
    .aicr-node-c, .aicr-node-a, .aicr-node-t { animation: none; opacity: 1; }
    .aicr-ai, .aicr-ct, .aicr-re { animation: none; opacity: 1; }
    .aicr-ring-loop { animation: none; }
  }
</style>
 
<div class="aicr-wrap">
  <svg width="100%" viewBox="0 0 680 460" role="img" xmlns="http://www.w3.org/2000/svg">
    <title>REAICT</title>
    <defs>
      <linearGradient id="aicr-edgeGrad" x1="0" y1="0" x2="1" y2="1">
        <stop offset="0%" stop-color="#5DCAA5"/>
        <stop offset="100%" stop-color="#1D9E75"/>
      </linearGradient>
    </defs>
 
    <line class="aicr-edge-ac" x1="169.9" y1="347.6" x2="320.1" y2="102.4" stroke="url(#aicr-edgeGrad)" stroke-width="1.5" opacity="0.85"/>
    <line class="aicr-edge-ct" x1="359.9" y1="102.4" x2="510.1" y2="347.6" stroke="url(#aicr-edgeGrad)" stroke-width="1.5" opacity="0.85"/>
 
    <g class="aicr-node-c">
      <circle class="aicr-ring-loop" cx="340" cy="70" r="38" fill="none" stroke="#1D9E75" stroke-width="1"/>
      <circle cx="340" cy="70" r="30" fill="none" stroke="#1D9E75" stroke-width="1.25"/>
      <text x="340" y="70" text-anchor="middle" dominant-baseline="central" font-size="20" font-weight="500" fill="#0F6E56" font-family="sans-serif">C</text>
    </g>
    <g class="aicr-node-a">
      <circle class="aicr-ring-loop" cx="150" cy="380" r="38" fill="none" stroke="#1D9E75" stroke-width="1"/>
      <circle cx="150" cy="380" r="30" fill="none" stroke="#1D9E75" stroke-width="1.25"/>
      <text x="150" y="380" text-anchor="middle" dominant-baseline="central" font-size="20" font-weight="500" fill="#0F6E56" font-family="sans-serif">A</text>
    </g>
    <g class="aicr-node-t">
      <circle class="aicr-ring-loop" cx="530" cy="380" r="38" fill="none" stroke="#1D9E75" stroke-width="1"/>
      <circle cx="530" cy="380" r="30" fill="none" stroke="#1D9E75" stroke-width="1.25"/>
      <text x="530" y="380" text-anchor="middle" dominant-baseline="central" font-size="20" font-weight="500" fill="#0F6E56" font-family="sans-serif">T</text>
    </g>
 
    <text x="340" y="230" text-anchor="middle" dominant-baseline="central" font-size="32" font-weight="500" letter-spacing="2" font-family="sans-serif">
      <tspan class="aicr-re" fill="currentColor">RE</tspan><tspan class="aicr-ai" fill="#1D9E75">AI</tspan><tspan class="aicr-ct" fill="currentColor">CT</tspan>
    </text>
  </svg>
</div>
 
    <text x="340" y="230" text-anchor="middle" dominant-baseline="central" font-size="32" font-weight="500" letter-spacing="2" font-family="sans-serif">
      <tspan class="aicr-flank" fill="currentColor">RE</tspan><tspan class="aicr-ai" fill="#1D9E75">AI</tspan><tspan class="aicr-flank" fill="currentColor">CT</tspan>
    </text>
  </svg>
</div>
