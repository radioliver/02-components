
<script>
import CardComp from './components/CardComp.vue'

export default {
  components: {
    CardComp
  }
}
</script>

<template>
  <div id="wrapper">
    <CardComp>
      <template v-slot:headerSlot>
        <h3>Level Devil</h3>
      </template>

      <template v-slot:default>
        <p>Egy idegesítő játék amit nem lehet letenni...</p>
      </template>

      <template v-slot:footerSlot>
        Értékelés: 9/10
      </template>
    </CardComp>

    <CardComp>
      <template #headerSlot>
        <h3>Rádi Olivér</h3>
      </template>

      <template #default>
        <p>Hobbi: néptánc</p>
      </template>
    </CardComp>
  </div>
</template>

<style>
#wrapper {
  display: flex;
  flex-wrap: wrap;
  padding: 20px;
}

h3 {
  margin: 0;
}

p {
  margin: 0;
}
</style>
