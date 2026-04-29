<template>
  <div class="wrapper">
    <div class="header">
      <Header />
    </div>
    <div class="contacts">
      <Contacts />
    </div>
    <div class="skills">
      <Education />
      <div class="skills-section">
        <br>
        <Skills />
        <div class="certifications">
          <Certifications />
        </div>
        <div class="profile">
          <Profile />
        </div>
      </div>
    </div>
    <div class="projects">
      <Projects />
      <div class="experience">
        <Experience />
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  display: grid;
  row-gap: 30px;
  grid-template-columns: 1fr 3fr;
  grid-template-rows: 190px 175px auto auto;
  grid-template-areas:
    "header header"
    "contacts experience"
    "skills experience"
    "skills experience";
}
.contacts,
.skills {
  padding: 0 22.5px 0 45px;
}

.skills-section {
  margin-top: 20px;
}

.certifications {
  margin-top: 45px;
}

.profile {
  margin-top: 45px;
}
.projects {
  margin-bottom: 30px
}

.projects {
  padding: 0 45px 0 0;
}

.experience {
  padding: 0 45px 0 0;
}

@media (min-width: 25cm) {
  @media not print {
    .wrapper {
      padding: 0 0 45px 0;
    }
  }
}

.projects {
  padding: 0 !important;
}

.header {
  display: flex;
  grid-area: header;
  background-image: url("../assets/wave.svg");
  background-repeat: no-repeat;
}
.contacts {
  grid-area: contacts;
}
.skills {
  grid-area: skills;
}
.experience {
  grid-area: experience;
}

@media (max-width: 25cm) {
  .wrapper {
    grid-template-columns: 1fr;
    grid-template-rows: auto auto auto auto auto auto;
    grid-template-areas:
      "header"
      "contacts"
      "experience"
      "skills";
  }
  .header {
    background-image: url("../assets/wave-mobile.svg") !important;
  }
  .contacts,
  .skills,
  .experience {
    padding: 0 20px 0 20px !important;
  }
}
@media print {
  .wrapper {
    grid-template-rows: auto 200px auto auto;
    grid-template-areas:
      "header header"
      "contacts experience"
      "skills experience"
      "skills experience"
  }
}
</style>
