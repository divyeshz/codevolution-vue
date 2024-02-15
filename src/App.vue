<template>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <div class="container">
    <div class="row">
      <form @submit.prevent="submitForm()">
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

        <div class="mb-3">

          <div class="form-check">
            <input class="form-check-input" type="checkbox" value="" id="remote-work" v-model="formValues.remoteWork"
              true-value="yes" false-value="no">
            <label class="form-check-label" for="remote-work">
              Remote Work
            </label>
          </div>
        </div>

        <div class="mb-3">
          <label class="form-label" for="">
            Skill Set
          </label>
          <div class="mb-3">
            <div class="form-check form-check-inline">
              <input class="form-check-input" type="checkbox" value="html" id="html" v-model="formValues.skillSet">
              <label class="form-check-label" for="html">
                HTML
              </label>
            </div>

            <div class="form-check form-check-inline">
              <input class="form-check-input" type="checkbox" value="javascript" id="javascript"
                v-model="formValues.skillSet">
              <label class="form-check-label" for="javascript">
                JavasCript
              </label>
            </div>

            <div class="form-check form-check-inline">
              <input class="form-check-input" type="checkbox" value="css" id="css" v-model="formValues.skillSet">
              <label class="form-check-label" for="css">
                CSS
              </label>
            </div>
          </div>
        </div>

        <div class="mb-3">
          <label for="form-label">Years of Experiences</label>
          <div class="mb-3">
            <div class="form-check form-check-inline">
              <input class="form-check-input" type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience">
              <label class="form-check-label" for="0-2">0-2</label>
            </div>
            <div class="form-check form-check-inline">
              <input class="form-check-input" type="radio" id="3-5" value="3-5" v-model="formValues.yearsOfExperience">
              <label class="form-check-label" for="3-5">3-5</label>
            </div>
            <div class="form-check form-check-inline">
              <input class="form-check-input" type="radio" id="6-10" value="6-10" v-model="formValues.yearsOfExperience">
              <label class="form-check-label" for="6-10">6-10</label>
            </div>
          </div>
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
        remoteWork: 'no',
        skillSet: [],
        yearsOfExperience: '',
      }
    }
  },
  methods: {
    submitForm(){
      console.log("Form values" , this.formValues);
    }
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
