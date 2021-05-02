<template>
  <div class="container">
    <Navbar />
    <Header />

    <section class="home-jobs">
      <div class="container">
        <div class="jobs-list" id="jobs">
          <template v-for="job in jobs" :key="job">
            <JobCard
              v-bind:logo="job.logo"
              v-bind:company="job.company"
              v-bind:name="job.name"
              v-bind:tags="job.tags"
            />
          </template>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
//  logo: String,
//     company: String,
//     name: String,
//     tags: Array,
import Navbar from './components/Navbar.vue';
import Header from './components/Header.vue';
import JobCard from './components/JobCard.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    JobCard,
  },
  data() {
    return {
      jobs: [
        {
          logo: '../assets/img/manage.png',
          company: 'Manage',
          name: 'Senior Frontend Developer',
          tags: ['Frontend', 'React', 'Sass'],
        },
        {
          logo: '../assets/img/air.png',
          company: 'Air',
          name: 'Fullstack Developer',
          tags: ['Frontend', 'Backend'],
        },
        {
          logo: '../assets/img/insure.png',
          company: 'Insure',
          name: 'Junior Frontend Developer',
          tags: ['Html', 'css', 'js'],
        },
      ],
    };
  },
};
</script>

<style>
:root {
  --bg-gradient: linear-gradient(
    158.86deg,
    #1c2a34 10.36%,
    #111a20 49.58%,
    #111a20 49.58%
  );
  --green-light: #b0fbbc;
  --green-primary: #82fa91;
  --white-text: #ecf8ff;
  --white-text-dark: #c9e2f0;
  --blue-dark: #111a20;
  --blue-dark-primary: #1c2c35;
  --blue-dark-secondary: #243b4a;
  --blue-light-primary: #416883;
  --blue-light-secondary: #5e8ca7;
}

body {
  background: var(--bg-gradient);
  background-repeat: no-repeat;
  font-size: 16px;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
    Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  padding: 0;
  margin: 0;
  min-height: 100vh;
}
h1,
h2,
h3,
p {
  margin: 0;
  padding: 0;
}
a {
  color: var(--white-text);
  text-decoration: none;
}

.container {
  width: 90%;
  max-width: 990px;
  margin: 0 auto;
}

.btn {
  background-color: transparent;
  color: var(--white-text);
  border: 1px solid var(--blue-light-secondary);
  padding: 0.7rem;
  min-width: 7rem;
  border-radius: 7px;
  cursor: pointer;
  font-weight: 700;
  transition: all 0.1s ease-in;
}
.btn:hover {
  color: var(--green-primary);
  background-color: var(--blue-light-secondary);
}
</style>
