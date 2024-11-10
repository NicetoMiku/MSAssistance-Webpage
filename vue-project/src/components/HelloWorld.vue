<template>
  <div class="container my-5">
    <!-- Hero Section -->
    <section class="jumbotron text-center bg-primary text-white p-4 mb-4 rounded shadow">
      <h1 class="display-4">Group 31 - MS Assistance</h1>
      <p class="lead">A collaborative project developed by a dedicated team in Group 31 to assist in various tasks and enhance productivity through an Android app, web interface, and more.</p>
      <p>
        <a :href="courseProjectLink" class="btn btn-light btn-lg mt-3" target="_blank">View CMPT362 Course Project Teams Info</a>
      </p>
    </section>
    
    <!-- Project Details Section -->
    <section class="project-details mb-5">
      <h2>Project Overview</h2>
      <p class="text-muted">
        MS Assistance is a comprehensive project that includes Android app development, server management, database schema design, and a web interface. The project aims to streamline workflows and improve user experience through carefully structured MVVM architecture, responsive design, and efficient backend management.
      </p>
    </section>

    <!-- Team Members Section -->
    <section class="team-members mb-5">
      <h2>Meet the Team</h2>
      <div class="row">
        <div class="col-md-6" v-for="member in members" :key="member.name">
          <div class="card mb-3 shadow-sm">
            <div class="card-body">
              <h5 class="card-title">{{ member.displayName }}</h5>
              <p class="card-text">{{ member.roles }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Links Section -->
    <section class="links-section">
      <h2>Project Repositories</h2>
      <ul class="list-group list-group-flush">
        <li class="list-group-item" v-for="(link, index) in repoLinks" :key="index">
          <a :href="link.url" target="_blank">{{ link.title }}</a>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      members: [
        { name: "Abdi", displayName: "Abdinajib Idle", roles: "Video, Server/Android App Dev, MVVM Diagram" },
        { name: "Horo", displayName: "Hongrui Fan", roles: "Server, Database Schema, MVVM Diagram, Webpage" },
        { name: "Hermit", displayName: "Boyu Zhang", roles: "2nd Android App Dev, Video Editing, MVVM Diagram" },
        { name: "Steven", displayName: "Kwong Hoi Chan", roles: "1st Android App Dev, MVVM Diagram" }
      ],
      repoLinks: [
        { title: "Android App Repository", url: "https://github.com/CMPT-362-Group-31/Project-show_and_tell-2/tree/master" },
        { title: "Database Repository", url: "https://github.com/NicetoMiku/MSAssistance-Database" },
        { title: "Server Repository", url: "https://github.com/NicetoMiku/MSAssistance-Server" },
        { title: "Webpage Repository", url: "https://github.com/NicetoMiku/MSAssistance-Webpage" },
        { title: "Show and tell 1 - video", url: "https://youtu.be/RGbPORWIEhk" }
      ],
      courseProjectLink: "https://docs.google.com/document/d/13MzOHc_98ELQbvu46aHTUSTMu7n2vfERZPpxdBBS16E/edit?tab=t.0#heading=h.yb19j48c8ofs"
    };
  }
};
</script>

<style scoped>
.jumbotron {
  background-color: #007bff;
}
.display-4 {
  font-weight: 300;
}
.project-details,
.team-members,
.links-section {
  margin-top: 2rem;
}
.card-title {
  font-size: 1.25rem;
  font-weight: 500;
}
.btn-lg {
  font-size: 1.125rem;
}
</style>
