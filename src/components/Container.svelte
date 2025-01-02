<script>
    export let imageSrc; // Path to the image
    export let imageAlt; // Alt text for the image
    export let title;    // Title for the text section
    export let text;     // Paragraph text
  </script>
  
  <style>
    .container {
      display: flex;
      align-items: center;
      gap: var(--spacing-lg);
      padding: var(--spacing-lg) 0;
      max-width: 1200px; /* Limit the maximum width */
      margin: 0 auto;    /* Center the container */
    }
  
    .image {
      flex: 1;
      max-width: 50%;
      border-radius: 8px;
      overflow: hidden;
    }
  
    .image img {
      width: 100%;
      height: auto;
      display: block;
    }
  
    .content {
      flex: 1;
      max-width: 50%;
    }
  
    .content h2 {
      font-size: 2rem;
      font-weight: bold;
      margin: 0 0 var(--spacing-md) 0;
      color: var(--text-light);
    }
  
    .content p {
      font-size: var(--font-size-lg);
      color: var(--text-muted);
      margin: 0;
    }
  
    /* Responsive Styles */
    @media (max-width: 768px) {
      .container {
        flex-direction: column;
        text-align: center;
        padding: var(--spacing-md);
      }
  
      .image,
      .content {
        max-width: 100%;
      }
    }
  </style>
  
  <div class="container">
    <div class="image">
      <img src={imageSrc} alt={imageAlt} />
    </div>
    <div class="content">
      <h2>{title}</h2>
      <p>{text}</p>
    </div>
  </div>