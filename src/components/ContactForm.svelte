<script>
    let name = "";
    let email = "";
    let message = "";
  
    function handleSubmit() {
      // Construct the mailto link
      const subject = `Contact Form Submission from ${name}`;
      const body = `Name: ${name}%0D%0AEmail: ${email}%0D%0AMessage: ${message}`;
      const mailtoLink = `mailto:crfabig@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
  
      // Open the default email client
      window.location.href = mailtoLink;
  
      // Reset the form
      name = "";
      email = "";
      message = "";
    }
  </script>
  
  <style>
    .contact-form {
      display: flex;
      flex-direction: column;
      max-width: 400px;
      margin: 0 auto;
      padding: 1rem;
      border: 1px solid #ccc;
      border-radius: 8px;
      background-color: transparent;
      margin-bottom: 200px;
    }
  
    .contact-form label {
      margin-bottom: 0.5rem;
      font-weight: bold;
    }
  
    .contact-form input,
    .contact-form textarea {
      margin-bottom: 1rem;
      padding: 0.5rem;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 1rem;
    }
  
    .contact-form textarea {
      resize: vertical;
      min-height: 100px;
    }
  
    .contact-form button {
      padding: 0.75rem;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 4px;
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
  
    .contact-form button:hover {
      background-color: #0056b3;
    }
  </style>
  
  <div class="contact-form">
    <label for="name">Name:</label>
    <input id="name" type="text" bind:value={name} required />
  
    <label for="email">Email:</label>
    <input id="email" type="email" bind:value={email} required />
  
    <label for="message">Message:</label>
    <textarea id="message" bind:value={message} required></textarea>
  
    <button on:click={handleSubmit}>Send Message</button>
  </div>