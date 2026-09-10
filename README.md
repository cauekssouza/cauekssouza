<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1180 610" width="100%" height="100%">
  <defs>
    <!-- Background & Noise -->
    <radialGradient id="bg-glow1" cx="20%" cy="20%" r="50%">
      <stop offset="0%" stop-color="#DBEAFE" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#FFFFFF" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="bg-glow2" cx="80%" cy="80%" r="50%">
      <stop offset="0%" stop-color="#D1FAE5" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#FFFFFF" stop-opacity="0"/>
    </radialGradient>
    <filter id="noise">
      <feTurbulence type="fractalNoise" baseFrequency="0.65" numOctaves="3" stitchTiles="stitch"/>
    </filter>
    
    <!-- Glassmorphism Filter -->
    <filter id="glass">
      <feGaussianBlur stdDeviation="12" result="blur"/>
      <feColorMatrix type="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 18 -7" result="glow"/>
      <feBlend in="SourceGraphic" in2="blur" mode="normal"/>
    </filter>

    <!-- Glowing Text Gradient (Light Mode) -->
    <linearGradient id="accent-grad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#2563EB">
        <animate attributeName="stop-color" values="#2563EB;#06B6D4;#10B981;#2563EB" dur="6s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#06B6D4">
        <animate attributeName="stop-color" values="#06B6D4;#10B981;#2563EB;#06B6D4" dur="6s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>

    <!-- Typing Animation Clip Paths -->
    <clipPath id="typing-clip">
      <rect x="0" y="0" width="0" height="40">
        <animate attributeName="width" values="0; 450; 450; 0; 0" keyTimes="0; 0.3; 0.8; 0.9; 1" dur="8s" repeatCount="indefinite"/>
      </rect>
    </clipPath>
  </defs>

  <!-- Background Layer -->
  <rect width="1180" height="610" fill="#FFFFFF"/>
  <circle cx="200" cy="150" r="400" fill="url(#bg-glow1)"/>
  <circle cx="980" cy="460" r="400" fill="url(#bg-glow2)"/>
  <rect width="1180" height="610" filter="url(#noise)" opacity="0.03"/>

  <!-- Left Side: ASCII Art & Cyber Terminal (38%) -->
  <g transform="translate(40, 40)">
    <!-- Glass Panel -->
    <rect width="420" height="530" rx="20" fill="rgba(248, 250, 252, 0.7)" stroke="rgba(15, 23, 42, 0.08)" stroke-width="1.5" filter="url(#glass)"/>
    
    <!-- Floating ASCII Container -->
    <g font-family="monospace" font-size="12" font-weight="bold" fill="url(#accent-grad)" transform="translate(30, 60)">
      <animateTransform attributeName="transform" type="translate" values="30,60; 30,50; 30,60" dur="4s" repeatCount="indefinite"/>
      
      <text y="20">      .::---::.      </text>
      <text y="35">   -+#%@@@@@@@%#+-   </text>
      <text y="50"> .+#@@@@@@@@@@@@@#+. </text>
      <text y="65"> =%@@@@@@@@@@@@@@@%= </text>
      <text y="80"> #@@@@@@#***#@@@@@@# </text>
      <text y="95"> #@@@@@* =::= *@@@@@ </text>
      <text y="110"> *@@@@@+ +##+ +@@@@* </text>
      <text y="125"> -%@@@@%=====%@@@@%- </text>
      <text y="140">  :*%@@@@@@@@@@@%*:  </text>
      <text y="155">    .=+*#####*+=.    </text>
      
      <text y="185" font-size="14" fill="#64748B">>_ SYSTEM READY.</text>
      <text y="215" font-size="14" fill="#64748B">>_ INITIALIZING DATA...</text>
      <text y="245" font-size="14" fill="#64748B">>_ USER: CAUÊ SOUZA</text>
      <text y="275" font-size="14" fill="#64748B">>_ STATUS: ONLINE</text>
      
      <!-- Scanline -->
      <rect x="-10" y="0" width="380" height="4" fill="#06B6D4" opacity="0.3">
        <animate attributeName="y" values="0; 400; 0" dur="5s" repeatCount="indefinite"/>
      </rect>
    </g>
  </g>

  <!-- Right Side: Professional Info Window (62%) -->
  <g transform="translate(490, 40)">
    <!-- Glass Panel -->
    <rect width="650" height="530" rx="20" fill="rgba(248, 250, 252, 0.7)" stroke="rgba(15, 23, 42, 0.08)" stroke-width="1.5" filter="url(#glass)"/>
    
    <!-- Mac Window Controls -->
    <g transform="translate(25, 25)">
      <circle cx="0" cy="0" r="6" fill="#EF4444"/>
      <circle cx="20" cy="0" r="6" fill="#F59E0B"/>
      <circle cx="40" cy="0" r="6" fill="#10B981"/>
    </g>

    <!-- Content -->
    <g font-family="system-ui, -apple-system, sans-serif" transform="translate(40, 85)">
      
      <!-- Greeting -->
      <text font-size="36" font-weight="800" fill="#0F172A">
        Hi 👋 I'm Cauê Souza
      </text>

      <!-- Animated Roles (Simulated Typing) -->
      <g transform="translate(0, 45)" font-size="24" font-weight="600" fill="url(#accent-grad)">
        <text clip-path="url(#typing-clip)">
          <tspan opacity="1">
            Engenheiro de Software 
            <animate attributeName="opacity" values="1;1;0;0;0;0;1" keyTimes="0;0.3;0.31;0.6;0.61;0.9;1" dur="8s" repeatCount="indefinite"/>
          </tspan>
          <tspan opacity="0" x="0">
            Desenvolvedor Fullstack
            <animate attributeName="opacity" values="0;0;1;1;0;0;0" keyTimes="0;0.3;0.31;0.6;0.61;0.9;1" dur="8s" repeatCount="indefinite"/>
          </tspan>
          <tspan opacity="0" x="0">
            Estagiário de IA &amp; Automação
            <animate attributeName="opacity" values="0;0;0;0;1;1;0" keyTimes="0;0.3;0.31;0.6;0.61;0.9;1" dur="8s" repeatCount="indefinite"/>
          </tspan>
        </text>
        <rect x="0" y="-22" width="12" height="26" fill="#06B6D4">
          <animate attributeName="opacity" values="1; 0; 1" dur="0.8s" repeatCount="indefinite"/>
          <animate attributeName="x" values="0; 280; 280; 0; 0" keyTimes="0; 0.3; 0.8; 0.9; 1" dur="8s" repeatCount="indefinite"/>
        </rect>
      </g>

      <!-- Info Details -->
      <g font-size="16" fill="#475569" transform="translate(0, 110)">
        <text y="0">📍  Curitiba, PR, Brasil</text>
        <text y="35">🎓  Engenharia de Software (PUCPR - 2026)</text>
        <text y="70">💼  IA e Automação de Processos @ Chaves na Mão</text>
        <text y="105">✉️  cauekssouza@gmail.com</text>
      </g>

      <!-- Skills Section -->
      <g transform="translate(0, 260)">
        <text font-size="14" font-weight="bold" fill="#0F172A" letter-spacing="1" opacity="0.9">Habilidades Técnicas</text>
        
        <g transform="translate(0, 25)" font-size="14" font-weight="600" fill="#2563EB">
          <!-- Skill Pills -->
          <g transform="translate(0, 0)">
            <rect width="70" height="30" rx="15" fill="rgba(37, 99, 235, 0.1)" stroke="#2563EB" stroke-width="1"/>
            <text x="35" y="20" text-anchor="middle">React</text>
          </g>
          <g transform="translate(85, 0)">
            <rect width="105" height="30" rx="15" fill="rgba(37, 99, 235, 0.1)" stroke="#2563EB" stroke-width="1"/>
            <text x="52.5" y="20" text-anchor="middle">TypeScript</text>
          </g>
          <g transform="translate(205, 0)">
            <rect width="85" height="30" rx="15" fill="rgba(37, 99, 235, 0.1)" stroke="#2563EB" stroke-width="1"/>
            <text x="42.5" y="20" text-anchor="middle">Node.js</text>
          </g>
          <g transform="translate(305, 0)">
            <rect width="115" height="30" rx="15" fill="rgba(37, 99, 235, 0.1)" stroke="#2563EB" stroke-width="1"/>
            <text x="57.5" y="20" text-anchor="middle">Tailwind CSS</text>
          </g>
          
          <g transform="translate(0, 45)">
            <rect width="90" height="30" rx="15" fill="rgba(16, 185, 129, 0.1)" stroke="#10B981" stroke-width="1"/>
            <text x="45" y="20" text-anchor="middle" fill="#10B981">MongoDB</text>
          </g>
          <g transform="translate(105, 45)">
            <rect width="60" height="30" rx="15" fill="rgba(16, 185, 129, 0.1)" stroke="#10B981" stroke-width="1"/>
            <text x="30" y="20" text-anchor="middle" fill="#10B981">SQL</text>
          </g>
          <g transform="translate(180, 45)">
            <rect width="120" height="30" rx="15" fill="rgba(16, 185, 129, 0.1)" stroke="#10B981" stroke-width="1"/>
            <text x="60" y="20" text-anchor="middle" fill="#10B981">APIs RESTful</text>
          </g>
        </g>
      </g>
    </g>
  </g>
</svg>
