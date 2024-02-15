<template>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <div class="container">
    <div class="row">
      <form>
        <div class="mb-3">
          <label for="name" class="form-label">Name</label>
          <input type="name" v-model="formValues.name" class="form-control" id="name">
        </div>
        <div class="mb-3">
          <label for="profile" class="form-label">Profile Summary</label>
          <textarea id="profile" v-model="formValues.profileSummary" class="form-control"></textarea>
        </div>
        <div class="mb-3">
          <label for="country" class="form-label">Country</label>
          <select id="country" class="form-select" v-model="formValues.country">
            <option value="">Select Country</option>
            <option value="IND">India</option>
            <option value="PAK">Pakistan</option>
            <option value="CHINA">China</option>
          </select>
        </div>

        <div class="mb-3">
          <label for="job-location" class="form-label">Job Location</label>
          <select id="job-location" multiple class="form-select" v-model="formValues.jobLocation">
            <option value="IND">India</option>
            <option value="PAK">Pakistan</option>
            <option value="CHINA">China</option>
          </select>
        </div>


        <button type="submit" class="btn btn-primary">Submit</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      formValues: {
        name: '',
        profileSummary: '',
        country: '',
        jobLocation: [],
      }
    }
  },
  methods: {

  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
