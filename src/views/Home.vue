<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <input type="text" id="datepicker" />
  </div>
</template>

<style></style>

<script>
/* global Pikaday */
// import axios from "axios";
// import moment from "moment";
export default {
  data: function () {
    return {
      message: "Welcome to Vue.js!",
    };
  },
  created: function () {},
  mounted: function () {
    var picker = new Pikaday({
      field: document.getElementById("datepicker"),
      format: "D MMM YYYY",
      onSelect: function () {
        console.log(this.getMoment().format("Do MMMM YYYY"));
      },
    });
    console.log(picker);
  },
  methods: {},
};
</script>
