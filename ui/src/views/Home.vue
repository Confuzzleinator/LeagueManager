<template>
  <div class="home">
    <v-btn color="primary" @click="OnClick">{{btnText}}</v-btn>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data: () => {
    return {
          btnText: 'Sim'
    }
  },
  methods: {
    OnClick() {
      this.btnText = Click()
    }
  }
}
</script>
