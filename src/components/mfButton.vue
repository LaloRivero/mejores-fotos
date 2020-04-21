<template>
  <div class="mf-button">
    <a href>{{ message.name }}</a>
  </div>
</template>

<script>
export default {
  name: 'mf-button',
  props: {
    message: {}
  }
}
</script>

<style scoped>
.mf-button {
  height: 30px;
  margin: 20px;
  padding: 10px 20px;
  background: #212d47;
  color: white;
  text-decoration: none;
  border-radius: 5px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 2px 10px 0 gray;
}
.mf-button:active {
  background: #3e5381;
}
a {
  color: white;
  text-decoration: none;
}
</style>
