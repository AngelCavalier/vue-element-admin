<template>
  <div>
    <Detail :is-edit="true" />
  </div>
</template>

<script>
import Detail from './components/Detail'
export default {
  name: 'EditBook',
  components: {
    Detail
  }

}
</script>

<style>

</style>
