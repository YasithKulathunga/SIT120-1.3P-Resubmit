<template>
    <form @submit.prevent="submitForm">
        <label>
        <span>Email</span>
        <input type="email" name="email" v-model="email" />
        </label>
        <label>
        <span>Message</span>
        <textarea name="message" v-model="message"></textarea>
        </label>
        <button type="submit">Submit</button>
    </form>
</template>

<script>
  export default {
    data() {
      return {
        email: '',
        message: '',
        endpoint: 'https://formcarry.com/s/{Your Form ID}',
      }
    },
    methods: {
      async submitForm() {
        const data = {
          email: this.email,
          message: this.message,
        }
        const response = await this.$axios.post(this.endpoint, data)
      },
    },
  }
</script>