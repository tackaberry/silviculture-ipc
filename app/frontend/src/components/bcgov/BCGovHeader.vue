<template>
  <header class="gov-header">
    <v-toolbar color="#003366" flat>
      <!-- Navbar content -->
      <a class="hidden-xs-only" href="https://www2.gov.bc.ca">
        <v-img
          alt="B.C. Government Logo"
          contain
          height="3.5rem"
          src="@/assets/images/17_gov3_bc_logo.svg"
          width="10rem"
        />
      </a>
      <v-toolbar-title class="title">{{ appTitle }}</v-toolbar-title>
      <v-spacer />
      <BaseAuthButton />
    </v-toolbar>
  </header>
</template>

<script>
export default {
  name: 'BCGovHeader',
  computed: {
    appTitle() {
      return process.env.VUE_APP_TITLE;
    }
  }
};
</script>

<style scoped>
.gov-header {
  border-bottom: 2px solid #fcba19;
}

.title {
  color: #ffffff;
  padding: 1rem;
}
</style>
