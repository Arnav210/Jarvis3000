---
layout: opencs
title: Jarvis3000 - Vision Intelligence Dashboard
hide: true
show_reading_time: false
---

<link rel="stylesheet" href="{{ '/assets/css/jarvis-dashboard.css' | relative_url }}">

<div class="jarvis-app-container">
  <!-- Outer Modern App Board matching Figma Frame -->
  <div class="jarvis-frame" id="jarvisApp">
    
    <!-- Header: Logo / Navigation to Repository / Log In & Sign Up -->
    <header class="jarvis-header">
      <div class="jarvis-header-left">
        <a href="https://github.com/arnavmittal/Jarvis3000" target="_blank" rel="noopener noreferrer" class="jarvis-brand-link" title="Jarvis3000 Repository">
          <div class="jarvis-logo-icon">
            <img src="{{ site.baseurl }}/images/jarvis-logo.svg" alt="Jarvis3000 Logo" style="width: 100%; height: 100%;">
          </div>
          <div class="jarvis-brand-title">
            <span class="jarvis-brand-name">Jarvis3000</span>
            <div class="jarvis-brand-underline"></div>
            <span class="jarvis-repo-tag">
              <svg width="12" height="12" viewBox="0 0 16 16" fill="currentColor">
                <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
              </svg>
              GitHub Repository ↗
            </span>
          </div>
        </a>
      </div>

      <div class="jarvis-header-actions">
        <a href="https://github.com/arnavmittal/Jarvis3000" target="_blank" rel="noopener noreferrer" class="jarvis-repo-btn">
          <svg width="14" height="14" viewBox="0 0 16 16" fill="currentColor">
            <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
          </svg>
          Repo
        </a>
        <div class="jarvis-auth-btn-group">
          <a href="{{ site.baseurl }}/login" class="jarvis-auth-link" id="dashboardLoginBtn">Log In</a>
          <a href="{{ site.baseurl }}/signup" class="jarvis-auth-link jarvis-auth-primary" id="dashboardSignupBtn">Sign Up</a>
        </div>
      </div>
    </header>

    <!-- 3-Column Main Dashboard Content Matching Figma Wireframe -->
    <main class="jarvis-dashboard-grid">
      
      <!-- LEFT COLUMN: List of Significant Scene Change Images -->
      <section class="jarvis-left-col" aria-label="Scene Change History">
        <div class="jarvis-col-header">
          <div class="jarvis-col-title">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <rect x="3" y="3" width="18" height="18" rx="2"/>
              <circle cx="8.5" cy="8.5" r="1.5"/>
              <path d="M20.4 14.5L16 10 4 20"/>
            </svg>
            Scene Changes
          </div>
          <span class="jarvis-badge-cyan" id="sceneCountBadge">3 Snaps</span>
        </div>

        <div class="jarvis-scene-list" id="sceneThumbnailsList">
          
          <!-- Scene 1: Mouse Missing (12/05/25 17:24) -->
          <div class="jarvis-scene-card active-scene" data-scene-id="mouse" onclick="selectScene('mouse')">
            <div class="jarvis-card-img-wrapper">
              <img src="{{ site.baseurl }}/images/scene_change_mouse.svg" alt="Scene change: Mouse missing">
            </div>
            <div class="jarvis-card-info">
              <span class="jarvis-card-time">12/05/25 17:24</span>
              <span class="jarvis-card-label danger">Mouse missing</span>
            </div>
          </div>

          <!-- Scene 2: Keyboard Missing (12/05/25 17:20) -->
          <div class="jarvis-scene-card" data-scene-id="keyboard" onclick="selectScene('keyboard')">
            <div class="jarvis-card-img-wrapper">
              <img src="{{ site.baseurl }}/images/scene_change_keyboard.svg" alt="Scene change: Keyboard missing">
            </div>
            <div class="jarvis-card-info">
              <span class="jarvis-card-time">12/05/25 17:20</span>
              <span class="jarvis-card-label warning">Keyboard missing</span>
            </div>
          </div>

          <!-- Scene 3: Monitor Moved (12/05/25 16:48) -->
          <div class="jarvis-scene-card" data-scene-id="monitor" onclick="selectScene('monitor')">
            <div class="jarvis-card-img-wrapper">
              <img src="{{ site.baseurl }}/images/scene_change_monitor.svg" alt="Scene change: Monitor moved">
            </div>
            <div class="jarvis-card-info">
              <span class="jarvis-card-time">12/05/25 16:48</span>
              <span class="jarvis-card-label info">Monitor moved</span>
            </div>
          </div>

        </div>
      </section>

      <!-- CENTER COLUMN: Current View (Top) & Current Date/Time (Bottom) -->
      <section class="jarvis-center-col" aria-label="Live Camera Viewport">
        
        <!-- Top: Current View (Teal/Cyan Border) -->
        <div class="jarvis-current-view-container" id="currentViewContainer">
          
          <!-- Live Feed Status Overlay -->
          <div class="jarvis-feed-topbar">
            <div class="jarvis-live-pill">
              <span class="jarvis-pulse-dot"></span>
              <span id="liveFeedStatusText">LIVE FEED</span>
            </div>
            <div class="jarvis-feed-cam-info" id="cameraMetaText">
              CAM-01 • STATION 4 • 1080P
            </div>
          </div>

          <!-- AI Holographic Scanline -->
          <div class="jarvis-scanline" id="aiScanline"></div>

          <!-- Main Feed Image/Video -->
          <div class="jarvis-feed-media" id="mainFeedMedia">
            <img id="activeFeedImg" src="{{ site.baseurl }}/images/scene_current.svg" alt="Current Camera View">
            <video id="webcamVideo" autoplay playsinline muted style="display:none; width:100%; height:100%; object-fit:cover;"></video>
          </div>

          <!-- Bottom Floating Controls -->
          <div class="jarvis-feed-controls">
            <div class="jarvis-ctrl-btn-group">
              <button type="button" class="jarvis-ctrl-btn active" id="btnToggleBBox" onclick="toggleBoundingBoxes()" title="Toggle AI Bounding Boxes">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2"/></svg>
                AI Bounding Boxes
              </button>
              <button type="button" class="jarvis-ctrl-btn active" id="btnToggleScan" onclick="toggleScanline()" title="Toggle AI Scanner">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="2" y1="12" x2="22" y2="12"/></svg>
                Scanner
              </button>
            </div>
            
            <div class="jarvis-ctrl-btn-group">
              <button type="button" class="jarvis-ctrl-btn" onclick="captureSnapshot()" title="Capture Snapshot">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="3"/><path d="M3 7h3l2-3h8l2 3h3v14H3z"/></svg>
                Snapshot
              </button>
              <button type="button" class="jarvis-ctrl-btn" onclick="toggleWebcam()" id="btnWebcam" title="Toggle Webcam">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M23 7l-7 5 7 5V7z"/><rect x="1" y="5" width="15" height="14" rx="2"/></svg>
                Webcam
              </button>
              <button type="button" class="jarvis-ctrl-btn" onclick="openFullscreenModal()" title="Inspect Fullscreen">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M15 3h6v6M9 21H3v-6M21 3l-7 7M3 21l7-7"/></svg>
                Enlarge
              </button>
            </div>
          </div>

        </div>

        <!-- Bottom: Current Date and Time (Gray Slate Card matching Figma) -->
        <div class="jarvis-time-container" id="dateTimeCard">
          <div class="jarvis-time-display" id="liveClockDisplay">
            12/05/2025, 17:30
          </div>
          <div class="jarvis-telemetry-row">
            <span class="jarvis-telemetry-pill">
              <span style="color:#10b981;">●</span> AI Vision: Active
            </span>
            <span class="jarvis-telemetry-pill">
              Model: YOLOv8-SceneDelta
            </span>
            <span class="jarvis-telemetry-pill">
              Confidence: 98.4%
            </span>
            <span class="jarvis-telemetry-pill">
              Latency: 18ms
            </span>
          </div>
        </div>

      </section>

      <!-- RIGHT COLUMN: Change Log (Vibrant Amber / Gold Panel) -->
      <section class="jarvis-right-col" aria-label="Change Log History">
        <div class="jarvis-changelog-card">
          
          <div class="jarvis-changelog-header">
            <h2 class="jarvis-changelog-title">Change Log</h2>
            <span class="jarvis-changelog-count" id="logCount">3 Changes</span>
          </div>

          <div class="jarvis-changelog-divider">
            ---------------------------------
          </div>

          <!-- Quick Action Buttons -->
          <div class="jarvis-changelog-actions">
            <button type="button" class="jarvis-amber-btn" onclick="simulateNewChange()" title="Trigger a simulated detection">
              + Simulate Event
            </button>
            <button type="button" class="jarvis-amber-btn" onclick="filterLogs('all')" id="btnFilterAll">
              All
            </button>
            <button type="button" class="jarvis-amber-btn" onclick="filterLogs('missing')">
              Missing
            </button>
            <button type="button" class="jarvis-amber-btn" onclick="filterLogs('moved')">
              Moved
            </button>
          </div>

          <!-- Chronological List (Latest on top) -->
          <div class="jarvis-changelog-list" id="changeLogList">
            
            <!-- Item 1 -->
            <div class="jarvis-log-item active-log" data-type="missing" data-scene="mouse" onclick="selectScene('mouse')">
              <div class="jarvis-log-timestamp">12/05/25 17:24</div>
              <div class="jarvis-log-description">
                <span>- Mouse missing</span>
              </div>
              <div>
                <span class="jarvis-log-tag">Object Missing</span>
              </div>
            </div>

            <!-- Item 2 -->
            <div class="jarvis-log-item" data-type="missing" data-scene="keyboard" onclick="selectScene('keyboard')">
              <div class="jarvis-log-timestamp">12/05/25 17:20</div>
              <div class="jarvis-log-description">
                <span>- Keyboard missing</span>
              </div>
              <div>
                <span class="jarvis-log-tag">Object Missing</span>
              </div>
            </div>

            <!-- Item 3 -->
            <div class="jarvis-log-item" data-type="moved" data-scene="monitor" onclick="selectScene('monitor')">
              <div class="jarvis-log-timestamp">12/05/25 16:48</div>
              <div class="jarvis-log-description">
                <span>- Monitor moved</span>
              </div>
              <div>
                <span class="jarvis-log-tag" style="background:rgba(217,119,6,0.2); color:#78350f;">Position Shift</span>
              </div>
            </div>

          </div>

        </div>
      </section>

    </main>

  </div>
</div>

<!-- Enlarge / Inspect Modal -->
<div class="jarvis-modal-overlay" id="inspectModal" onclick="closeFullscreenModal(event)">
  <div class="jarvis-modal-dialog" onclick="event.stopPropagation()">
    <div class="jarvis-modal-header">
      <h3 id="modalTitle" style="color:#ffffff; margin:0; font-size:1.1rem; font-weight:700;">Scene Snapshot Inspector</h3>
      <button type="button" onclick="closeFullscreenModal()" style="background:none; border:none; color:#94a3b8; font-size:1.5rem; cursor:pointer;">&times;</button>
    </div>
    <div class="jarvis-modal-body">
      <img id="modalImg" class="jarvis-modal-img" src="{{ site.baseurl }}/images/scene_current.svg" alt="Enlarged view">
      <div style="display:flex; justify-content:space-between; align-items:center; color:#94a3b8; font-size:0.85rem; font-family:var(--font-mono);">
        <span id="modalMeta">Station 4 • Vision Resolution 1920x1080</span>
        <span style="color:#38bdf8;">Status: AI Delta Verified</span>
      </div>
    </div>
  </div>
</div>

<!-- Dashboard Interactive Script -->
<script>
(function() {
  const baseUrl = "{{ site.baseurl }}";
  
  // Scene definitions matching Figma design
  const scenes = {
    mouse: {
      id: 'mouse',
      title: 'Mouse Missing',
      time: '12/05/25 17:24',
      isoTime: '12/05/2025, 17:24',
      img: baseUrl + '/images/scene_change_mouse.svg',
      tag: 'Mouse missing',
      type: 'missing',
      desc: 'Mouse disconnected or removed from Station 4 mouse pad area.'
    },
    keyboard: {
      id: 'keyboard',
      title: 'Keyboard Missing',
      time: '12/05/25 17:20',
      isoTime: '12/05/2025, 17:20',
      img: baseUrl + '/images/scene_change_keyboard.svg',
      tag: 'Keyboard missing',
      type: 'missing',
      desc: 'Dell USB keyboard displaced from primary typing zone.'
    },
    monitor: {
      id: 'monitor',
      title: 'Monitor Moved',
      time: '12/05/25 16:48',
      isoTime: '12/05/2025, 16:48',
      img: baseUrl + '/images/scene_change_monitor.svg',
      tag: 'Monitor moved',
      type: 'moved',
      desc: 'Left 24-inch monitor angled -8 degrees from calibrated orientation.'
    },
    current: {
      id: 'current',
      title: 'Current Live Station View',
      time: 'LIVE',
      isoTime: '12/05/2025, 17:30',
      img: baseUrl + '/images/scene_current.svg',
      tag: 'Live Monitoring',
      type: 'live',
      desc: 'Active camera stream showing real-time scene delta state.'
    }
  };

  let activeSceneKey = 'mouse';
  let isWebcamActive = false;
  let webcamStream = null;
  let showBBoxes = true;
  let showScanline = true;
  let liveClockMode = 'dynamic'; // 'dynamic' or 'fixed'

  // Clock Formatter: matching Figma wireframe e.g. "12/05/2025, 17:30"
  function updateClock() {
    const clockEl = document.getElementById('liveClockDisplay');
    if (!clockEl) return;
    
    if (liveClockMode === 'dynamic') {
      const now = new Date();
      const month = String(now.getMonth() + 1).padStart(2, '0');
      const day = String(now.getDate()).padStart(2, '0');
      const year = now.getFullYear();
      const hours = String(now.getHours()).padStart(2, '0');
      const minutes = String(now.getMinutes()).padStart(2, '0');
      const seconds = String(now.getSeconds()).padStart(2, '0');
      clockEl.textContent = `${month}/${day}/${year}, ${hours}:${minutes}:${seconds}`;
    } else {
      clockEl.textContent = '12/05/2025, 17:30';
    }
  }

  setInterval(updateClock, 1000);
  updateClock();

  // Allow clicking on date/time card to toggle between live clock and recorded timestamp
  const dateCard = document.getElementById('dateTimeCard');
  if (dateCard) {
    dateCard.style.cursor = 'pointer';
    dateCard.title = 'Click to toggle Live Clock / Scene Timestamp (12/05/2025, 17:30)';
    dateCard.addEventListener('click', function() {
      liveClockMode = (liveClockMode === 'dynamic' ? 'fixed' : 'dynamic');
      updateClock();
    });
  }

  // Select a scene snapshot
  window.selectScene = function(sceneKey) {
    activeSceneKey = sceneKey;
    const scene = scenes[sceneKey];
    if (!scene) return;

    // Update active thumbnail card highlight
    document.querySelectorAll('.jarvis-scene-card').forEach(card => {
      card.classList.toggle('active-scene', card.dataset.sceneId === sceneKey);
    });

    // Update active change log item highlight
    document.querySelectorAll('.jarvis-log-item').forEach(item => {
      item.classList.toggle('active-log', item.dataset.scene === sceneKey);
    });

    // Update main feed image
    const imgEl = document.getElementById('activeFeedImg');
    const vidEl = document.getElementById('webcamVideo');
    if (imgEl) {
      imgEl.src = scene.img;
      imgEl.style.display = 'block';
    }
    if (vidEl && isWebcamActive) {
      stopWebcam();
    }

    // Update meta text
    const metaEl = document.getElementById('cameraMetaText');
    if (metaEl) {
      metaEl.textContent = `CAM-01 • ${scene.title.toUpperCase()} • ${scene.time}`;
    }

    // Flash animation on feed
    const container = document.getElementById('currentViewContainer');
    if (container) {
      container.style.transition = 'box-shadow 0.2s ease';
      container.style.boxShadow = '0 0 40px rgba(56, 189, 248, 0.8)';
      setTimeout(() => {
        container.style.boxShadow = '';
      }, 300);
    }
  };

  // Toggle AI Bounding Boxes
  window.toggleBoundingBoxes = function() {
    showBBoxes = !showBBoxes;
    const btn = document.getElementById('btnToggleBBox');
    if (btn) btn.classList.toggle('active', showBBoxes);
    
    // In our SVG images, when bounding boxes are disabled, we can switch to clean baseline or toggle
    const imgEl = document.getElementById('activeFeedImg');
    if (imgEl && !showBBoxes) {
      imgEl.src = baseUrl + '/images/scene_current.svg';
    } else if (imgEl && scenes[activeSceneKey]) {
      imgEl.src = scenes[activeSceneKey].img;
    }
  };

  // Toggle AI Holographic Scanner
  window.toggleScanline = function() {
    showScanline = !showScanline;
    const scanline = document.getElementById('aiScanline');
    const btn = document.getElementById('btnToggleScan');
    if (scanline) scanline.style.display = showScanline ? 'block' : 'none';
    if (btn) btn.classList.toggle('active', showScanline);
  };

  // Camera Flash Snapshot Animation
  window.captureSnapshot = function() {
    const container = document.getElementById('currentViewContainer');
    if (!container) return;
    
    const flash = document.createElement('div');
    flash.style.position = 'absolute';
    flash.style.inset = '0';
    flash.style.backgroundColor = '#ffffff';
    flash.style.zIndex = '50';
    flash.style.opacity = '0.9';
    flash.style.transition = 'opacity 0.5s ease-out';
    container.appendChild(flash);
    
    setTimeout(() => {
      flash.style.opacity = '0';
      setTimeout(() => flash.remove(), 500);
    }, 50);
  };

  // Toggle Webcam Stream
  window.toggleWebcam = async function() {
    const vidEl = document.getElementById('webcamVideo');
    const imgEl = document.getElementById('activeFeedImg');
    const btn = document.getElementById('btnWebcam');
    const statusText = document.getElementById('liveFeedStatusText');

    if (isWebcamActive) {
      stopWebcam();
      return;
    }

    try {
      if (navigator.mediaDevices && navigator.mediaDevices.getUserMedia) {
        webcamStream = await navigator.mediaDevices.getUserMedia({ video: { width: 1280, height: 720 } });
        if (vidEl) {
          vidEl.srcObject = webcamStream;
          vidEl.style.display = 'block';
        }
        if (imgEl) imgEl.style.display = 'none';
        if (btn) btn.classList.add('active');
        if (statusText) statusText.textContent = 'WEBCAM ACTIVE';
        isWebcamActive = true;
      } else {
        alert('Webcam API is not available in this browser.');
      }
    } catch (err) {
      console.warn('Webcam permission denied or unavailable:', err);
      alert('Could not start webcam. Please grant camera permission.');
    }
  };

  function stopWebcam() {
    const vidEl = document.getElementById('webcamVideo');
    const imgEl = document.getElementById('activeFeedImg');
    const btn = document.getElementById('btnWebcam');
    const statusText = document.getElementById('liveFeedStatusText');

    if (webcamStream) {
      webcamStream.getTracks().forEach(track => track.stop());
      webcamStream = null;
    }
    if (vidEl) {
      vidEl.style.display = 'none';
      vidEl.srcObject = null;
    }
    if (imgEl) imgEl.style.display = 'block';
    if (btn) btn.classList.remove('active');
    if (statusText) statusText.textContent = 'LIVE FEED';
    isWebcamActive = false;
  }

  // Fullscreen Inspector Modal
  window.openFullscreenModal = function() {
    const modal = document.getElementById('inspectModal');
    const modalImg = document.getElementById('modalImg');
    const modalTitle = document.getElementById('modalTitle');
    const scene = scenes[activeSceneKey] || scenes.current;

    if (modal && modalImg && scene) {
      modalImg.src = scene.img;
      if (modalTitle) modalTitle.textContent = `${scene.title} (${scene.time}) - Deep Inspector`;
      modal.classList.add('open');
    }
  };

  window.closeFullscreenModal = function(e) {
    const modal = document.getElementById('inspectModal');
    if (modal) modal.classList.remove('open');
  };

  // Simulate new scene change dynamically
  const simulationEvents = [
    { title: 'Water bottle detected', tag: 'Object Added', type: 'added', icon: 'Bottle' },
    { title: 'Backpack left at station', tag: 'Unattended Item', type: 'added', icon: 'Bag' },
    { title: 'Chair angled away from desk', tag: 'Position Shift', type: 'moved', icon: 'Chair' },
    { title: 'Headphones removed', tag: 'Object Missing', type: 'missing', icon: 'Audio' }
  ];
  let simIndex = 0;

  window.simulateNewChange = function() {
    const sim = simulationEvents[simIndex % simulationEvents.length];
    simIndex++;

    const now = new Date();
    const mm = String(now.getMonth() + 1).padStart(2, '0');
    const dd = String(now.getDate()).padStart(2, '0');
    const yy = String(now.getFullYear()).slice(-2);
    const hh = String(now.getHours()).padStart(2, '0');
    const min = String(now.getMinutes()).padStart(2, '0');
    const timeStr = `${mm}/${dd}/${yy} ${hh}:${min}`;

    const list = document.getElementById('changeLogList');
    if (!list) return;

    const item = document.createElement('div');
    item.className = 'jarvis-log-item';
    item.dataset.type = sim.type;
    item.innerHTML = `
      <div class="jarvis-log-timestamp">${timeStr}</div>
      <div class="jarvis-log-description">
        <span>- ${sim.title}</span>
      </div>
      <div>
        <span class="jarvis-log-tag" style="${sim.type === 'added' ? 'background:rgba(16,185,129,0.2); color:#065f46;' : ''}">${sim.tag}</span>
      </div>
    `;

    list.insertBefore(item, list.firstChild);

    // Update count badge
    const countEl = document.getElementById('logCount');
    if (countEl) {
      const count = list.querySelectorAll('.jarvis-log-item').length;
      countEl.textContent = `${count} Changes`;
    }

    // Flash effect on dashboard
    captureSnapshot();
  };

  // Filter logs
  window.filterLogs = function(type) {
    const items = document.querySelectorAll('.jarvis-log-item');
    items.forEach(item => {
      if (type === 'all' || item.dataset.type === type) {
        item.style.display = 'flex';
      } else {
        item.style.display = 'none';
      }
    });
  };

})();
</script>
