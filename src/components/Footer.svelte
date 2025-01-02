<script>
    // Social media links
    const socials = [
      {
        name: "GitHub",
        url: "https://github.com/timefliez1210",
        icon: "https://cdn.jsdelivr.net/npm/simple-icons@v11/icons/github.svg",
      },
      {
        name: "X (Twitter)",
        url: "https://x.com/0xTimefliez",
        icon: "https://cdn.jsdelivr.net/npm/simple-icons@v11/icons/x.svg",
      },
    ];
  
  </script>
  
  <style>
    .footer {
      background-color: var(--background-light);
      color: var(--text-light);
      padding: var(--spacing-lg) var(--spacing-md);
      text-align: center;
      border-top: 1px solid var(--border-color);
    }
  
    .footer-content {
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: var(--spacing-lg);
    }
  
    .socials {
      display: flex;
      justify-content: center;
      gap: var(--spacing-md);
    }
  
    .social-link {
      display: flex;
      align-items: center;
      gap: var(--spacing-sm);
      text-decoration: none;
      color: var(--text-light);
      transition: opacity 0.3s ease;
    }
  
    .social-link:hover {
      opacity: 0.8;
    }
  
    .social-icon {
      width: 24px;
      height: 24px;
    }

  
    .copyright {
      font-size: var(--font-size-base);
      color: var(--text-muted);
      margin-top: var(--spacing-md);
    }
  
    /* Responsive Styles */
    @media (max-width: 768px) {
      .socials {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
  
  <footer class="footer">
    <div class="footer-content">
      <!-- Social Links -->
      <div class="socials">
        {#each socials as social}
          <a href={social.url} target="_blank" rel="noopener noreferrer" class="social-link">
            <img src={social.icon} alt={social.name} class="social-icon" />
            <span>{social.name}</span>
          </a>
        {/each}
      </div>
  
      <!-- Copyright Notice -->
      <div class="copyright">
        &copy; 2025 Clemens Fabig. All rights reserved.
      </div>
    </div>
  </footer>