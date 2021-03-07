<template>
  <q-card class="user_card">
    <img src="../../public/user.jpg" alt="">
    <div style="font-size: 12px;">Киреев Анатолий Сергеевич</div>
    <div style="font-size: 12px;">Kira@mail.ru</div>
    <div style="font-size: 12px;">Тел. +7 (985) 431-07-39</div>
    <q-separator />
    <div class="row flex justify-end">
      <q-checkbox v-model="checkbox" value="false" />
    </div>
  </q-card>
</template>

<script>
export default {
  name: 'UserCard'
}
</script>

<style lang="sass" scoped>
.user_card
  padding: 5px
  margin: 10px
  width: 227px
  height: 233px
</style>
