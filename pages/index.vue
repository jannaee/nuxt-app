<template>
  <div>
    <h1>Events</h1>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: 'Event Listing'
    }
  },
  asyncData(context) {
    return context.$axios
      .get('http://localhost:3000/events')
      .then((response) => {
        return {
          events: response.data
        }
      })
  }
}
</script>
