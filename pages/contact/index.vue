<template>
  <div>
    <h1 class="lg-heading">Contact <span class="text-secondary">Me</span></h1>
    <b-form @submit="handleSubmit" @reset="onReset" v-if="show">
      <b-form-group
        id="input-group-1"
        label="Email address:"
        label-for="input-1"
        description="We'll never share your email with anyone else!"
      >
        <b-form-input
          id="input-1"
          v-model="contactForm.email"
          type="email"
          placeholder="Enter email"
          required
        ></b-form-input
      ></b-form-group>
      <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="contactForm.name"
          placeholder="Enter name"
          required
        ></b-form-input>
      </b-form-group>
      <b-form-group
        id="input-group-3"
        label="Please tell us about your project and how I can help."
        label-for="project-description"
      >
        <b-form-textarea
          id="message"
          v-model="contactForm.message"
          placeholder="Enter something..."
          rows="3"
          max-rows="6"
        ></b-form-textarea
      ></b-form-group>
      <b-button type="submit" variant="primary" @click="handleSubmit"
        >Submit</b-button
      >
      <b-button type="reset" variant="danger">Reset</b-button>
    </b-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      contactForm: {
        name: '',
        email: '',
        message: '',
      },
      show: true,
    }
  },
  head() {
    return {
      title: 'Contact IMTS',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'We would love to talk with you',
        },
      ],
    }
  },
  methods: {
    submitToServer() {
      return new Promise((resolve, reject) => {
        fetch(`${process.env.functions}/mail`, {
          method: 'POST',
          body: JSON.stringify(this.contactForm),
        })
          .then((response) => {
            resolve(response)
          })
          .catch((err) => {
            reject(err)
          })
      })
    },
    handleSubmit() {
      this.submitToServer().then((response) => {
        const body = response.json()
        if (Number(response.status) !== 200) {
          console.log('Error submitting the form.')
        } else {
          console.log('Form was submitted!')
          this.$router.push('/contact/thank-you')
        }
      })
    },
    onReset(event) {
      event.preventDefault()
      this.form.email = ''
      this.form.name = ''
      this.form.project = ''
    },
  },
}
</script>

<style></style>
