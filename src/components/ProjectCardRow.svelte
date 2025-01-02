<script>
    import ProjectCard from './ProjectCard.svelte';
  
    // Example data for multiple projects
    const projects = [
      {
        heading: "DeFi Stablecoin",
        picture: "https://via.placeholder.com/300",
        description: "An exorgenously backed stablecoin on the Ethereum blockchain, featuring multi-collerateralization and a robust liquidation logic.",
        projectLink: "https://github.com/timefliez1210/StableProtocol",
      },
      {
        heading: "Christmas Dinner",
        picture: "https://via.placeholder.com/300",
        description: "A learning project for aspiring security researches. This code contains bugs and vulnerabilities. It was used as a First Flight Contest on Cyfrin Codehawks",
        projectLink: "https://github.com/timefliez1210/ChristmasDinner",
      },
      {
        heading: "A Shop in React",
        picture: "https://via.placeholder.com/300",
        description: "An abstraction of an old project for a client, sanitized to make it reusable for other projects.",
        projectLink: "https://github.com/timefliez1210/ShopTemplateReact",
      },
    ];
  </script>
  
  <style>
    .projects-container {
      padding: 1rem;
      text-align: center;
    }
  
    .projects-heading {
      font-size: 2rem;
      margin-bottom: 1.5rem;
      color: rgb(236, 234, 234)4d4;
    }
  
    .card-row {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
    }
  </style>
  
  <div class="projects-container" id="projects">
    <h2 class="projects-heading">some projects I have finished:</h2>
    <div class="card-row">
      {#each projects as project}
        <ProjectCard
          heading={project.heading}
          picture={project.picture}
          description={project.description}
          projectLink={project.projectLink}
        />
      {/each}
    </div>
  </div>