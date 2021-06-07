<template>
<!-- submit prevent default with modifier-->
  <form @submit.prevent="sumbitForm">
    <p>kia form with vue ---- {{ JSON.stringify(valueForm, null, 2) }}</p>
    <div>
      <label for="name">Name</label>
	  <!-- add modifier to name trim input -->
      <input
        type="text"
        id="name"
        v-model.trim.lazy="valueForm.name"
        autocomplete="off"
      />
    </div>
    <div>
      <label for="profile">Profile</label>
      <textarea
        name="profile"
        id="profile"
        cols="30"
        rows="10"
        v-model="valueForm.profileSummery"
      ></textarea>
    </div>
    <div>
      <label for="select">Select a Country</label>
      <select id="selectCountry" v-model="valueForm.country">
        <option value="">select A country</option>
        <option value="india">india</option>
        <option value="china">china</option>
        <option value="bangal">bangal</option>
      </select>
    </div>
    <div>
      <label for="jobLocation">Select a Country</label>
      <select id="jobLocation" multiple v-model="valueForm.jobLocation">
        <option value="india">india</option>
        <option value="china">china</option>
        <option value="bangal">bangal</option>
      </select>
    </div>
	<div>
		<!-- modifier enter is used here -->
		<label for="age">Age </label>
		<input @keyup.enter="sumbitForm" type="text"  name="age" v-model="valueForm.age">
	</div>
	<!-- <button>Submit</button> -->
  </form>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      valueForm: {
        name: "",
        profileSummery: "",
        country: "",
        jobLocation: [],
		age : null
      },
    };
  },
  methods: {
    sumbitForm(e) {
		// e.preventDefault()
      console.log(e);
    },
	handleEvent(e){
		console.log(e)

	}
  },
};
</script>
<style scoped>
form {
  width: 80%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
}
form div {
  padding: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>