<template>

  <footer>
    <div class="ms_shorter-container">
      <Informations />

      <DesignedByAndPayments />
    </div>

  </footer>

</template>

<script>
import Informations from './footer-components/Informations.vue';
import DesignedByAndPayments from './footer-components/DesignedByAndPayments.vue';

export default {
  name: 'Footer',
  components: {
    Informations,
    DesignedByAndPayments
  }
}
</script>

<style scoped lang="scss">

footer{
  background-color: #202942;
  color: white;
}

</style>