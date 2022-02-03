<template>

  <ScrollTopComponent>
      <a class="btn btn-light">
        <i class="fas fa-angle-double-up fa-lg"></i>
       <!-- <font-awesome-icon :icon="['fas', 'angle-double-up']" size="3x" />-->
      </a>
  </ScrollTopComponent>
</template>

<script>
import ScrollTopComponent from './ScrollTopComponent'
export default {
  components: {
    ScrollTopComponent
  }
}
</script>

<style>
.btn {
    border-radius: 8px;
    background-color: rgba(0, 0, 0, 0.55);
    padding-top: 27px;
    padding-left: 10px;
    padding-right: 10px;
    padding-bottom: 5px;
}

.btn:hover,
.btn:focus{
  background-color: silver !important;
      



}
</style>