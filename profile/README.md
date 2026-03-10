<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 400 400" width="400" height="400">
  <defs>
    <filter id="glow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="6" result="blur"/>
      <feComposite in="SourceGraphic" in2="blur" operator="over"/>
    </filter>
    <filter id="outerGlow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="12" result="blur"/>
      <feFlood flood-color="#a855f7" flood-opacity="0.6" result="color"/>
      <feComposite in="color" in2="blur" operator="in" result="glow"/>
      <feMerge>
        <feMergeNode in="glow"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    <pattern id="scanlines" patternUnits="userSpaceOnUse" width="400" height="4">
      <rect width="400" height="2" fill="rgba(0,0,0,0.3)"/>
    </pattern>
    <clipPath id="ghostClip">
      <use href="#ghostShape"/>
    </clipPath>
  </defs>
  <style>
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-8px); }
    }
    @keyframes pulseGlow {
      0%, 100% { opacity: 0.4; }
      50% { opacity: 0.8; }
    }
    @keyframes eyeFlicker {
      0%, 90%, 100% { opacity: 1; }
      92%, 98% { opacity: 0.3; }
    }
    @keyframes scanMove {
      0% { transform: translateY(0); }
      100% { transform: translateY(4px); }
    }
    @keyframes glitchShift {
      0%, 94%, 100% { transform: translate(0,0); }
      95% { transform: translate(2px, 0); }
      96% { transform: translate(-2px, 1px); }
      97% { transform: translate(1px, -1px); }
    }
    .ghost-group {
      animation: float 3s ease-in-out infinite, glitchShift 8s steps(1) infinite;
      transform-origin: 200px 200px;
    }
    .glow-aura {
      animation: pulseGlow 3s ease-in-out infinite;
    }
    .eyes {
      animation: eyeFlicker 4s steps(1) infinite;
    }
    .scanline-overlay {
      animation: scanMove 0.15s linear infinite;
    }
  </style>
  <g class="ghost-group">
    <defs>
      <path id="ghostShape" d="
        M 132,84 h 136 v 12 h 12 v 12 h 12 v 12 h 12 v 12 h 12 v 168
        h -24 v -24 h -24 v 24 h -24 v -24 h -24 v 24 h -24 v -24 h -24 v 24 h -24 v -24 h -24 v 24
        h -24 v -168 h 12 v -12 h 12 v -12 h 12 v -12 z
      "/>
    </defs>
    <g filter="url(#glow)">
      <rect x="132" y="84" width="136" height="12" fill="#7c3aed" opacity="0.9"/>
      <rect x="120" y="96" width="160" height="12" fill="#7c3aed" opacity="0.9"/>
      <rect x="108" y="108" width="184" height="12" fill="#7c3aed" opacity="0.85"/>
      <rect x="96" y="120" width="208" height="12" fill="#6d28d9" opacity="0.9"/>
      <rect x="96" y="132" width="208" height="12" fill="#6d28d9" opacity="0.85"/>
      <rect x="96" y="144" width="208" height="12" fill="#7c3aed" opacity="0.8"/>
      <rect x="96" y="156" width="208" height="12" fill="#6d28d9" opacity="0.85"/>
      <rect x="96" y="168" width="208" height="12" fill="#7c3aed" opacity="0.8"/>
      <rect x="96" y="180" width="208" height="12" fill="#6d28d9" opacity="0.85"/>
      <rect x="96" y="192" width="208" height="12" fill="#7c3aed" opacity="0.8"/>
      <rect x="96" y="204" width="208" height="12" fill="#6d28d9" opacity="0.85"/>
      <rect x="96" y="216" width="208" height="12" fill="#7c3aed" opacity="0.8"/>
      <rect x="96" y="228" width="208" height="12" fill="#6d28d9" opacity="0.85"/>
      <rect x="96" y="240" width="208" height="12" fill="#7c3aed" opacity="0.8"/>
      <rect x="96" y="252" width="208" height="12" fill="#6d28d9" opacity="0.85"/>
      <rect x="96" y="264" width="208" height="12" fill="#7c3aed" opacity="0.8"/>
      <rect x="96" y="276" width="24" height="12" fill="#6d28d9" opacity="0.8"/>
      <rect x="144" y="276" width="24" height="12" fill="#6d28d9" opacity="0.8"/>
      <rect x="192" y="276" width="24" height="12" fill="#6d28d9" opacity="0.8"/>
      <rect x="240" y="276" width="24" height="12" fill="#6d28d9" opacity="0.8"/>
      <rect x="280" y="276" width="24" height="12" fill="#6d28d9" opacity="0.8"/>
      <rect x="96" y="288" width="24" height="12" fill="#6d28d9" opacity="0.75"/>
      <rect x="144" y="288" width="24" height="12" fill="#6d28d9" opacity="0.75"/>
      <rect x="192" y="288" width="24" height="12" fill="#6d28d9" opacity="0.75"/>
      <rect x="240" y="288" width="24" height="12" fill="#6d28d9" opacity="0.75"/>
      <rect x="280" y="288" width="24" height="12" fill="#6d28d9" opacity="0.75"/>
      <g class="eyes">
        <rect x="144" y="156" width="36" height="36" fill="#c4b5fd" opacity="0.95"/>
        <rect x="156" y="168" width="12" height="12" fill="#1e1b4b" opacity="0.9"/>
        <rect x="228" y="156" width="36" height="36" fill="#c4b5fd" opacity="0.95"/>
        <rect x="240" y="168" width="12" height="12" fill="#1e1b4b" opacity="0.9"/>
      </g>
      <rect x="168" y="228" width="12" height="12" fill="#c4b5fd" opacity="0.5"/>
      <rect x="180" y="240" width="48" height="12" fill="#c4b5fd" opacity="0.4"/>
      <rect x="228" y="228" width="12" height="12" fill="#c4b5fd" opacity="0.5"/>
    </g>
    <g clip-path="url(#ghostClip)">
      <rect class="scanline-overlay" x="0" y="0" width="400" height="400" fill="url(#scanlines)"/>
    </g>
    <g opacity="0.3">
      <rect x="132" y="84" width="136" height="2" fill="#e9d5ff"/>
      <rect x="120" y="96" width="2" height="12" fill="#e9d5ff"/>
      <rect x="96" y="120" width="2" height="168" fill="#e9d5ff"/>
    </g>
    <g opacity="0.15" fill="#c4b5fd">
      <rect x="108" y="132" width="4" height="4"/>
      <rect x="180" y="108" width="4" height="4"/>
      <rect x="252" y="144" width="4" height="4"/>
      <rect x="132" y="204" width="4" height="4"/>
      <rect x="264" y="228" width="4" height="4"/>
      <rect x="156" y="252" width="4" height="4"/>
      <rect x="216" y="192" width="4" height="4"/>
      <rect x="120" y="168" width="4" height="4"/>
      <rect x="276" y="204" width="4" height="4"/>
      <rect x="192" y="132" width="4" height="4"/>
    </g>
  </g>
  <g opacity="0.4">
    <circle cx="60" cy="100" r="1.5" fill="#a855f7">
      <animate attributeName="opacity" values="0;0.6;0" dur="4s" repeatCount="indefinite"/>
      <animate attributeName="cy" values="100;80;100" dur="4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="340" cy="150" r="1" fill="#c084fc">
      <animate attributeName="opacity" values="0;0.5;0" dur="3s" begin="1s" repeatCount="indefinite"/>
      <animate attributeName="cy" values="150;130;150" dur="3s" begin="1s" repeatCount="indefinite"/>
    </circle>
    <circle cx="80" cy="300" r="1.5" fill="#a855f7">
      <animate attributeName="opacity" values="0;0.4;0" dur="5s" begin="2s" repeatCount="indefinite"/>
      <animate attributeName="cy" values="300;280;300" dur="5s" begin="2s" repeatCount="indefinite"/>
    </circle>
    <circle cx="320" cy="320" r="1" fill="#c084fc">
      <animate attributeName="opacity" values="0;0.5;0" dur="3.5s" begin="0.5s" repeatCount="indefinite"/>
      <animate attributeName="cy" values="320;300;320" dur="3.5s" begin="0.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="50" cy="200" r="1" fill="#7c3aed">
      <animate attributeName="opacity" values="0;0.6;0" dur="4.5s" begin="1.5s" repeatCount="indefinite"/>
      <animate attributeName="cy" values="200;185;200" dur="4.5s" begin="1.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="350" cy="250" r="1.5" fill="#7c3aed">
      <animate attributeName="opacity" values="0;0.5;0" dur="3.8s" begin="0.8s" repeatCount="indefinite"/>
      <animate attributeName="cy" values="250;235;250" dur="3.8s" begin="0.8s" repeatCount="indefinite"/>
    </circle>
  </g>
</svg>
