<template>
  <q-page>
    <div class="row flex justify-between q-mt-lg q-px-sm">
      <div>
        <q-btn color="primary" icon="control_point" label="Добавить сотрудника" />
        <q-btn flat class="q-ml-sm" color="primary" icon="edit" label="Редактировать" />
        <q-btn flat class="q-ml-sm" color="primary" icon="military_tech" label="Добавить дело" />
      </div>
      <div>
        <q-btn flat class="q-ml-lg" round color="primary" icon="visibility" />
        <q-btn flat round color="primary" icon="info" />
        <q-btn flat round color="primary" icon="filter_alt" />
        <q-btn flat round color="primary" icon="account_tree" />
        <q-btn flat round color="primary" icon="widgets" />
        <q-btn flat round color="primary" icon="settings" />
      </div>
    </div>
    <div class="cards_grid q-mt-md">
      <UserCard />
      <UserCard />
      <UserCard />
      <UserCard />
      <UserCard />
    </div>
  </q-page>
</template>

<script>
import UserCard from 'components/UserCard'

export default {
  name: 'PageIndex',
  components: { UserCard }
}
</script>

<style lang="sass" scoped>
.cards_grid
  display: flex
  flex-wrap: wrap
</style>
