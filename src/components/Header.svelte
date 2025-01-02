<script>
    import '../styles/styles.css'; // Import global styles
  </script>
  
  <style>
    /* Hero Container */
    .hero {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: var(--spacing-lg) var(--spacing-md);
      background-color: transparent;
      color: var(--text-light);
      min-height: 70vh; /* Adjusted to 70vh */
      position: relative;
    }
  
    /* Heading and Skills Container */
    .hero-content {
      display: flex;
      align-items: center;
      gap: var(--spacing-lg);
      max-width: 1200px;
      margin: 0 auto;
    }
  
    /* Heading Section */
    .hero-heading {
      flex: 1;
      text-align: left;
    }
  
    .hero-heading h1 {
      font-size: 3rem;
      font-weight: bold;
      margin: 0 0 var(--spacing-md) 0;
      line-height: 1.2;
      color: var(--text-light);
    }
  
    .hero-heading p {
      font-size: var(--font-size-lg);
      color: var(--text-muted);
      max-width: 500px;
      margin: 0 0 var(--spacing-lg) 0;
    }
  
    /* Skills Boxes */
    .skills-boxes {
      display: flex;
      gap: var(--spacing-md);
    }
  
    .skill-box {
      background-color: rgba(255, 255, 255, 0.1); /* Transparent background */
      border: 1px solid var(--border-color);
      padding: var(--spacing-md);
      border-radius: 8px;
      text-align: left;
      width: 200px;
    }
  
    .skill-box h3 {
      font-size: var(--font-size-lg);
      font-weight: bold;
      margin: 0 0 var(--spacing-sm) 0;
      color: var(--text-light);
      display: flex;
      align-items: center;
      gap: var(--spacing-sm);
    }
  
    .skill-box p {
      font-size: var(--font-size-base);
      color: var(--text-muted);
      margin: 0;
    }
  
    /* Call-to-Action Button */
    .hero .cta-button {
      background-color: var(--primary-color);
      color: var(--text-light);
      border: none;
      padding: var(--spacing-sm) var(--spacing-md);
      font-size: var(--font-size-base);
      font-weight: bold;
      cursor: pointer;
      transition: background-color var(--transition-speed) ease;
      border-radius: 4px;
    }
  
    .hero .cta-button:hover {
      background-color: darken(var(--primary-color), 10%);
    }
  
    /* Responsive Styles */
    @media (max-width: 768px) {
      .hero-content {
        flex-direction: column;
        text-align: center;
      }
  
      .hero-heading {
        text-align: center;
      }
  
      .skills-boxes {
        flex-direction: column;
        align-items: center;
      }
  
      .skill-box {
        width: 100%;
        max-width: 300px;
      }
    }
  </style>
  
  <section class="hero">
    <div class="hero-content">
      <!-- Heading Section -->
      <div class="hero-heading">
        <h1>Building the Future</h1>
        <p>I design and develop innovative solutions that transform ideas into reality. Let’s create something extraordinary together.</p>
        <button class="cta-button">Get Started</button>
      </div>
  
      <!-- Skills Boxes -->
      <div class="skills-boxes">
        <div class="skill-box">
          <h3>
            <svg xmlns="http://www.w3.org/2000/svg" width="3rem" height="3rem" viewBox="0 0 48 48">
              <g fill="none">
                <path fill="url(#fluentColorCodeBlock480)" d="M12 6a6 6 0 0 0-6 6v24a6 6 0 0 0 6 6h24a6 6 0 0 0 6-6V12a6 6 0 0 0-6-6z"/>
                <path fill="url(#fluentColorCodeBlock481)" d="M20.884 15.366a1.25 1.25 0 0 1 0 1.768L14.018 24l6.866 6.866a1.25 1.25 0 0 1-1.768 1.768l-7.75-7.75a1.25 1.25 0 0 1 0-1.768l7.75-7.75a1.25 1.25 0 0 1 1.768 0m8 0l7.75 7.75a1.25 1.25 0 0 1 0 1.768l-7.75 7.75a1.25 1.25 0 0 1-1.768-1.768L33.982 24l-6.866-6.866a1.25 1.25 0 0 1 1.768-1.768"/>
                <defs>
                  <linearGradient id="fluentColorCodeBlock480" x1="14.778" x2="34.52" y1="6" y2="42" gradientUnits="userSpaceOnUse">
                    <stop offset=".028" stop-color="#e67eea"/>
                    <stop offset=".438" stop-color="#ad64d7"/>
                    <stop offset="1" stop-color="#794dc5"/>
                  </linearGradient>
                  <linearGradient id="fluentColorCodeBlock481" x1="17.165" x2="28.034" y1="15.692" y2="42.785" gradientUnits="userSpaceOnUse">
                    <stop stop-color="#fdfdfd"/>
                    <stop offset="1" stop-color="#f9dcfa"/>
                  </linearGradient>
                </defs>
              </g>
            </svg>
            Web2
          </h3>
          <p>Building modern, responsive, and scalable web and mobile applications.</p>
        </div>
        <div class="skill-box">
          <h3>
            <svg xmlns="http://www.w3.org/2000/svg" width="3rem" height="3rem" viewBox="0 0 24 24"><path fill="none" stroke="#a4259b" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M5.5 10.5c.122 0 .236-.056.463-.17l1.825-.908C8.596 9.019 9 8.818 9 8.5v-4m-3.5 6c-.122 0-.236-.056-.463-.17l-1.825-.908C2.404 9.019 2 8.818 2 8.5v-4m3.5 6v-4m3.5-2c0-.318-.404-.52-1.212-.922L5.963 2.67c-.227-.113-.34-.17-.463-.17c-.122 0-.236.057-.463.17l-1.825.908C2.404 3.981 2 4.182 2 4.5m7 0c0 .318-.404.52-1.212.922l-1.825.908c-.227.113-.34.17-.463.17M2 4.5c0 .318.404.52 1.212.922l1.825.908c.227.113.34.17.463.17m13 4c.122 0 .236-.056.463-.17l1.825-.908C21.596 9.019 22 8.818 22 8.5v-4m-3.5 6c-.122 0-.236-.056-.463-.17l-1.825-.908C15.404 9.019 15 8.818 15 8.5v-4m3.5 6v-4m3.5-2c0-.318-.404-.52-1.212-.922l-1.825-.908c-.227-.113-.34-.17-.463-.17c-.122 0-.236.057-.463.17l-1.825.908C15.404 3.981 15 4.182 15 4.5m7 0c0 .318-.404.52-1.212.922l-1.825.908c-.227.113-.34.17-.463.17m-3.5-2c0 .318.404.52 1.212.922l1.825.908c.227.113.34.17.463.17m-7 0h1M2 12.5V16c0 1.404 0 2.107.337 2.611a2 2 0 0 0 .552.552c.504.337 1.207.337 2.611.337m16.5-7V16c0 1.404 0 2.107-.337 2.611a2 2 0 0 1-.552.552c-.504.337-1.207.337-2.611.337m-8.25-2.569q.262-.003.583-.002h2.334q.32 0 .583.002m-3.5 0c-.723.01-1.133.063-1.408.332c-.342.335-.342.874-.342 1.951c0 1.078 0 1.617.342 1.951c.341.335.891.335 1.991.335h2.334c1.1 0 1.65 0 1.991-.335c.342-.334.342-.873.342-1.95c0-1.078 0-1.617-.342-1.952c-.275-.27-.685-.322-1.408-.332m-3.5 0v-1.717c0-.947.784-1.714 1.75-1.714s1.75.768 1.75 1.714v1.717" color="#a4259b"/></svg>Web3</h3>
          <p>Building Smart Contracts for EVM chains and independant security reviews.</p>
        </div>
      </div>
    </div>
  </section>