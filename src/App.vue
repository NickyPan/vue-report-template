<template>
  <div>
    <md-autocomplete v-model="selectedCountry" :md-options="countries">
      <label>Country</label>
    </md-autocomplete>

    <md-autocomplete v-model="selectedEmployee" :md-options="employees" md-dense>
      <label>Employees</label>
    </md-autocomplete>

    <div>
      <small>Raised</small>
      <md-button class="md-raised">Default</md-button>
      <md-button class="md-raised" :md-ripple="false">Ripple Off</md-button>
      <md-button class="md-raised md-primary">Primary</md-button>
      <md-button class="md-raised md-accent">Accent</md-button>
      <md-button class="md-raised" disabled>Disabled</md-button>
    </div>
  </div>
</template>

<script>

export default {
  name: 'app',
  data () {
    return {
      selectedCountry: null,
      selectedEmployee: null,
      countries: [
        'Algeria',
        'Argentina',
        'Brazil',
        'Canada',
        'Italy',
        'Japan',
        'United Kingdom',
        'United States'
      ],
      employees: [
        'Jim Halpert',
        'Dwight Schrute',
        'Michael Scott',
        'Pam Beesly',
        'Angela Martin',
        'Kelly Kapoor',
        'Ryan Howard',
        'Kevin Malone',
        'Creed Bratton',
        'Oscar Nunez',
        'Toby Flenderson',
        'Stanley Hudson',
        'Meredith Palmer',
        'Phyllis Lapin-Vance'
        ]
    }
  }
}
</script>

<style lang="scss">
</style>
