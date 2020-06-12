<template>
  <nuxt-link :to="{ name: 'event-title', params: { title: event.id } }">
    <div class="event-card">
      <div style="display:flex;justify-content: space-between;">
        <span class="date">@{{ event.time }}</span>
        <span class="location">{{ event.location }}</span>
      </div>
      <h3 class="title">{{ event.title }}</h3>
      <p class="lead">{{ event.desc }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    event: Object
  }
}
</script>

<style scoped>
a {
  color: #000;
  text-decoration: none;
}
.event-card {
  padding: 1rem;
  margin-top: 1rem;
  width: 400px;
  background: #f7f7f7;
  transition: all 0.3s ease;
  border-radius: 5px;
  text-align: left;
}
.date {
  font-size: 0.9rem;
  font-style: italic;
  color: rgb(41, 189, 209);
}

.title {
  padding: 0.5rem;
  margin: 0;
}
</style>
