<template>
  <main class="main">
    <div class="container">
      <div class="event-cards">
        <EventCard
          v-for="(event, index) in events"
          :key="index"
          :event="event"
        />
      </div>
    </div>
  </main>
</template>

<script>
import EventCard from '@/components/EventCard'
import EventService from '@/services/EventService'
export default {
  head() {
    return {
      title: 'Home'
    }
  },
  components: {
    EventCard
  },
  async asyncData({ error }) {
    try {
      const { data } = await EventService.getEvents()
      return {
        events: data
      }
    } catch (e) {
      error({
        stautsCode: 503,
        message: 'Unable to fetch events.'
      })
    }
  }
}
</script>

<style>
.main {
  display: flex;
  justify-content: center;
}
.event-cards {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>
