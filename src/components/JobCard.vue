<template>
  <div class="job-card">
    <div class="job-logo">
      <img :src="logo" alt="Manage" />
    </div>
    <div class="job-text">
      <h3 class="job-company">{{ company }}</h3>
      <h2 class="job-title">{{ name }}</h2>
      <div class="job-tags">
        <div class="tag" v-for="tag in tags" :key="tag">
          {{ tag }}
        </div>
        <div class="tag">React</div>
        <div class="tag">Sass</div>
      </div>
    </div>
    <div class="job-cta">
      <button class="btn">Aplicar</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'JobCard',
  props: {
    logo: String,
    company: String,
    name: String,
    tags: Array,
  },
};
</script>

<style>
.job-card {
  background-color: rgb(201 226 240 / 7%);
  display: grid;
  border-radius: 7px;
  border-left: 6px solid var(--green-primary);
  grid-template-columns: 70px 1fr 140px;
  align-items: center;
  margin: 2rem 0;
  padding: 2rem 1rem;
}
.job-card .job-logo img {
  width: 68px;
  height: 68px;
}

.job-card .job-text {
  color: var(--white-text-dark);
  margin-left: 1rem;
}

.job-card .job-text .job-company {
  font-size: 1rem;
  font-weight: 200;
}
.job-card .job-text .job-title {
  font-size: 1.2rem;
  font-weight: 600;
  letter-spacing: 2px;
  margin: 0.5rem 0;
}
.job-card .job-text .job-tags {
  display: flex;
  align-items: center;
}
.job-card .job-text .job-tags .tag {
  background-color: rgb(130 250 145 / 13%);
  padding: 0.2rem 0.5rem;
  border: 1px solid var(--green-primary);
  border-radius: 7px;
  font-size: 0.7rem;
  margin-right: 0.5rem;
  margin-top: 0.5rem;
}
</style>
