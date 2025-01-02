<script>
    export let heading = "Project Heading";
    export let picture = "https://via.placeholder.com/300";
    export let description = "This is a description of the project.";
    export let projectLink = "#";
  </script>
  
  <style>
    .card {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 1rem;
      border: 1px solid #e0e0e0;
      border-radius: 8px;
      width: 100%;
      max-width: 300px;
      margin: 1rem;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }
  
    .card img {
      width: 100%;
      height: auto;
      border-radius: 8px;
    }
  
    .card h2 {
      margin: 1rem 0 0.5rem 0;
      font-size: 1.5rem;
      text-align: center;
    }
  
    .card p {
      margin: 0.5rem 0;
      text-align: center;
      color: #666;
    }
  
    .card a {
      margin-top: 1rem;
      padding: 0.5rem 1rem;
      background-color: #007bff;
      color: white;
      text-decoration: none;
      border-radius: 4px;
      transition: background-color 0.3s ease;
    }
  
    .card a:hover {
      background-color: #0056b3;
    }
  </style>
  
  <div class="card">
    <img src={picture} alt={heading} />
    <h2>{heading}</h2>
    <p>{description}</p>
    <a href={projectLink} target="_blank">View Project</a>
  </div>