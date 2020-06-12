<template>
  <div  class="event-cards">
    <div class="container">
    <EventCard :event="event" />
    </div>
  </div>
</template>

<script>
import EventCard from '@/components/EventCard'
import EventService from '@/services/EventService'
export default {
  head() {
    return {
      title: this.event.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: `This is ${this.event.title}`
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content: 'tit page, tit, view main'
        }
      ]
    }
  },
  async asyncData({ params, error }) {
    try {
      const { data } = await EventService.getEvent(params.title)
      return {
        event: data
      }
    } catch (e) {
      error({
        stautsCode: 503,
        message: 'Unable to fetch events ' + params.title
      })
    }
  },
  components: {
    EventCard
  }
}
</script>

<style></style>
