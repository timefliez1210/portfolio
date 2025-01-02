<script>
    let isOpen = false;
  
    const toggleMenu = () => {
      isOpen = !isOpen;
    };
  </script>
  
  <style>
    /* Base styles */
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      background-color: rgba(26, 26, 26, 0.9); /* Dark background with reduced opacity */
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
      position: sticky;
      top: 0;
      z-index: 1000;
    }
  
    .logo {
      font-size: 1.5rem;
      font-weight: bold;
      color: #ffffff; /* White text */
      text-decoration: none; /* Remove underline from link */
    }
  
    .logo:hover {
      opacity: 0.8; /* Slight hover effect */
    }
  
    .nav-links {
      display: flex;
      gap: 2rem;
      align-items: center;
    }
  
    .nav-links a {
      text-decoration: none;
      color: #ffffff; /* White text */
      font-size: 1rem;
      transition: color 0.3s ease;
    }
  
    .nav-links a:hover {
      color: #007bff; /* Blue hover effect */
    }
  
    /* Mobile styles */
    .hamburger {
      display: none;
      flex-direction: column;
      cursor: pointer;
      background: none;
      border: none;
      padding: 0;
    }
  
    .hamburger div {
      width: 25px;
      height: 3px;
      background-color: #ffffff; /* White bars */
      margin: 4px 0;
      transition: all 0.3s ease;
    }
  
    /* Responsive styles */
    @media (max-width: 768px) {
      .nav-links {
        position: absolute;
        top: 60px;
        right: 0;
        flex-direction: column;
        background-color: rgba(26, 26, 26, 0.9); /* Dark background with reduced opacity */
        width: 100%;
        align-items: center;
        gap: 1rem;
        padding: 1rem 0;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        transform: translateX(100%);
        transition: transform 0.3s ease-in-out;
      }
  
      .nav-links.open {
        transform: translateX(0);
      }
  
      .hamburger {
        display: flex;
      }
  
      .hamburger div {
        transition: transform 0.3s ease;
      }
  
      .hamburger div:nth-child(2) {
        transition: opacity 0.3s ease;
      }
    }
  </style>
  
  <nav>
    <a href="/" class="logo"> <!-- Logo as a link to the homepage -->
      My Portfolio
    </a>
  
    <div class="nav-links {isOpen ? 'open' : ''}">
      <a href="/">Home</a>
      <a href="/#projects">Projects</a>
      <a href="/blog">Blog</a>
      <a href="/contact">Contact</a>
    </div>
  
    <button class="hamburger" on:click={toggleMenu} aria-expanded={isOpen} aria-label="Toggle navigation menu">
      <div style="transform: {isOpen ? 'rotate(45deg)' : 'rotate(0)'};"></div>
      <div style="opacity: {isOpen ? '0' : '1'};"></div>
      <div style="transform: {isOpen ? 'rotate(-45deg)' : 'rotate(0)'};"></div>
    </button>
  </nav>